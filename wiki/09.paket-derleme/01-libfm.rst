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
		#sed -i -e 's/ -shared / -Wl,-O1,--as-needed\0/g' libtool
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}


.. raw:: pdf

   PageBreak
