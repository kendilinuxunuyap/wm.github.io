.. _lxhotkey:
**lxhotkey**
============

Klavye kısayollarının yönetimi ve atanması için kullanılır.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxhotkey"
	version="0.1.1"
	description="LXDE hotkey"
	source="https://github.com/lxde/lxhotkey/archive/refs/tags/$version.tar.gz"
	depends="libfm"
	builddepend="libexif"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --with-gtk=3
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}

	 
.. raw:: pdf

   PageBreak
