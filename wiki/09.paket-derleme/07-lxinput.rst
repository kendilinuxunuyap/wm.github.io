.. _lxinput:
**lxinput**
===========

Fare ve klavye ayarlarının yapılandırılması için gerekli bileşendir.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxinput"
	version="0.3.5"
	description="LXDE keyboard and mouse configuration tool"
	source="https://downloads.sourceforge.net/lxde/lxinput-$version.tar.xz"
	depends="gtk3"
	builddepend="intltool"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
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
