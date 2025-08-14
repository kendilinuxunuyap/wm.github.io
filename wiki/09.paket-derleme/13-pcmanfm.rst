.. _pcmanfm:
**pcmanfm**
===========

Dosya yöneticisi. Dosya gezintisi, masaüstü yönetimi ve simge gösterimi işlevlerini yerine getirir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="pcmanfm"
	version="1.3.2"
	description="LXDE keyboard and mouse configuration tool"
	source="https://github.com/lxde/pcmanfm/archive/refs/tags/$version.tar.gz"
	depends="lxmenu-data,libfm,menu-cache,libkeybinder3"
	builddepend="intltool"
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
