.. _mpdecimal:

**mpdecimal**
=============

MPDecimal, çok hassas sayısal hesaplamalar yapmak için kullanılan bir kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="mpdecimal"
	version="4.0.0"
	url="https://www.bytereef.org/mpdecimal/index.html"
	description="Package for correctly-rounded arbitrary precision decimal floating point arithmetic"
	source="https://www.bytereef.org/software/$name/releases/$name-$version.tar.gz"
	depends=""
	builddepend=""
	group="net.db"

	setup(){
		cd $SOURCEDIR
		./configure --prefix=/usr \
		    --libdir=/usr/lib64
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}


**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
