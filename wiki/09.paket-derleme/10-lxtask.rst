**lxtask**
==========

Basit bir görev yöneticisidir. Sistem kaynaklarını ve çalışan işlemleri gösterir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxtask"
	version="0.1.10"
	description="LXDE Task manager"
	source="https://github.com/lxde/lxtask/archive/refs/tags/$version.tar.gz"
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
