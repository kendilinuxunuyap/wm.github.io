**lxrandr**
===========


Ekran çözünürlüğü ve monitör yapılandırması için grafiksel arayüz sağlar. `xrandr` aracı üzerine kuruludur.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxrandr"
	version="0.3.2"
	description="Monitor configuration tool (part of LXDE)"
	source="https://downloads.sourceforge.net/lxde/lxrandr-$version.tar.xz"
	depends="gtk3,xrandr"
	builddepend="intltool"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
			--enable-gtk3 \
			--enable-man \
		    --libdir=/usr/lib64/
	}

	build(){
		make DESTDIR=$DESTDIR
	}

	package(){
		make DESTDIR=$DESTDIR install
	}

 
.. raw:: pdf

   PageBreak
