**lxlauncher**
==============

Netbook tarzı uygulama başlatıcı. Menü verilerine dayanır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxlauncher"
	version="0.2.5"
	description="Open source clone of the Asus launcher for EeePC"
	source="https://github.com/lxde/lxlauncher/archive/refs/tags/$version.tar.gz"
	depends="startup-notification,gtk3,menu-cache"
	builddepend="intltool"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --sysconfdir=/etc \
		    --enable-gtk3
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}

 
.. raw:: pdf

   PageBreak
