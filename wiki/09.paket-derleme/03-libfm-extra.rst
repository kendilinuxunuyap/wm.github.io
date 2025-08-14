.. _libfm-extra:
**libfm-extra**
===============

Menü tanımları ve veri dosyalarını içerir. Diğer bileşenlerin menü bilgilerini kullanabilmesi için öncelikle derlenmelidir.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libfm-extra"
	version="1.3.2"
	description="Library for file management"
	source="https://github.com/lxde/libfm/archive/refs/tags/${version}.tar.gz"
	depends="gtk3,pango,intltool,menu-cache"
	group="x11.libs"


	setup(){
		mkdir -p /tmp/bps/build/patches
		cp ${dizin}/${paket}/patches/* /tmp/bps/build/patches/
		cd $SOURCEDIR
		patch -Np1 -i ../patches/libfm-fixes.patch
		autoreconf -fvi
		 ./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
			  --with-gtk=3   \
			 --with-extra-only
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}

.. raw:: pdf

   PageBreak
