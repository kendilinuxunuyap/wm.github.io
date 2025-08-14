.. _lxde-icon-theme:
**lxde-icon-theme**
===================

Lxde ikon ve tema paketidir.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxde-icon-theme"
	version="0.5.1"
	description="LXDE default icon theme based on nuoveXT2"
	source="https://downloads.sourceforge.net/lxde/lxde-icon-theme-$version.tar.xz"
	depends=""
	builddepend=""
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
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
