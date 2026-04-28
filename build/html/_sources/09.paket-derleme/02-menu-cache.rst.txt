.. _menu-cache:

**menu-cache**
==============

LXDE için gerekli temel kütüphanedir.


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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_

.. raw:: pdf

   PageBreak
