**lxmenu-data**
===============

Menü tanımları ve veri dosyalarını içerir. Diğer bileşenlerin menü bilgilerini kullanabilmesi için öncelikle derlenmelidir.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="menu-cache"
	version="1.1.0"
	description="Caching mechanism for freedesktop.org compliant menus"
	source="https://github.com/lxde/menu-cache/archive/refs/tags/$version.tar.gz"
	depends="libfm-extra"
	group="lxde.base"


	prepare(){
		patch -Np1 -i ../
	}

	setup(){
		mkdir -p /tmp/bps/build/patches
		cp ${dizin}/${paket}/patches/* /tmp/bps/build/patches/
		cd $SOURCEDIR
		patch -Np1 < ../patches/menu-cache-1.1.0-0001-Support-gcc10-compilation.patch
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ 
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}

.. raw:: pdf

   PageBreak
