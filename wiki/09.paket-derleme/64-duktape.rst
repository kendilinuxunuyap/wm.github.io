.. _duktape:
**duktape**
===========

Duktape, C dilinde yazılmış ve gömülü sistemler için optimize edilmiş bir JavaScript motorudur. Hafif, taşınabilir ve kolayca entegre edilebilen bir JavaScript çalışma zamanı sağlar. Genellikle, JavaScript'i düşük seviyeli uygulamalara eklemek isteyen geliştiriciler tarafından kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="duktape"
	version="2.7.0"
	url="https://duktape.org"
	description="Embeddable Javascript engine"
	source="https://duktape.org/$name-$version.tar.xz"
	group="dev.lang"


	_make(){
		make -f Makefile.sharedlibrary INSTALL_PREFIX=/usr "$@"
	}
	setup()
	{
	cd $SOURCEDIR
		# tools/configure.py needs Python 2
		sed -i 's/^#undef DUK_USE_FASTINT$/#define DUK_USE_FASTINT/' src/duk_config.h

		# Add missing NEEDED on libm.so
		sed -i 's/duktape\.c/& -lm/' Makefile.sharedlibrary

	}
	build(){
		_make
	}

	package(){
		_make DESTDIR="$DESTDIR" install
		install -Dt "$DESTDIR/usr/share/licenses/$name" -m644 LICENSE.txt
	}


**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
