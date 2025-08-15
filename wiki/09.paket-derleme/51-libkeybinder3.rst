.. _libkeybinder3:
**libkeybinder3**
=================

Linux masaüstü ortamlarında global klavye kısayollarını yakalamak ve yönetmek için kullanılan bir kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libkeybinder3"
	version="0.3.2"
	description="Musical key detection library for digital audio"
	source="https://github.com/kupferlauncher/keybinder/releases/download/keybinder-3.0-v$version/keybinder-3.0-$version.tar.gz"
	depends="gtk3"
	builddepend="gtk-doc,gobject-introspection"
	group="dev.libs"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --with-gtk=3
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
