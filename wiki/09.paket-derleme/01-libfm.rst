.. _libfm:
**libfm**
===============

Menü tanımları ve veri dosyalarını içerir. Diğer bileşenlerin menü bilgilerini kullanabilmesi için öncelikle derlenmelidir.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libfm"
	version="1.4.0"
	description="Library for file management"
	source="https://github.com/lxde/libfm/archive/${version}.tar.gz"
	depends="gtk3,pango,intltool,menu-cache"
	group="x11.libs"

	setup(){
		cd $SOURCEDIR

		autoreconf -fvi
		 ./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --sysconfdir=/etc \
			--with-gtk=3 \
			--with-gnu-ld
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
