.. _libfm-extra:
**libfm-extra**
===============

LXDE için gerekli temel kütüphanedir.


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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_

.. raw:: pdf

   PageBreak
