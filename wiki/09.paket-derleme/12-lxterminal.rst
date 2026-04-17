.. _lxterminal:
**lxterminal**
==============

LXDE için terminal öykünücüsüdür.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxterminal"
	version="0.4.0"
	description="Lightweight vte-based tabbed terminal emulator for LXDE"
	source="https://salsa.debian.org/lxde-team/lxterminal/-/archive/debian/$version-2/lxterminal-debian-$version-2.tar.gz"
	#source="https://downloads.sourceforge.net/lxde/lxterminal-$version.tar.xz"	
	depends="vte3,gtk3,dejavu"
	builddepend="intltool"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure \
			--prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --enable-gtk3 
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
