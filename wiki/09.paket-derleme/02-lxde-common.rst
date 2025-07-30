**lxde-common**
===============

Ortak konfigürasyon dosyaları, tema ve temel altyapı öğelerini sağlar. LXDE'nin diğer bileşenleri için temel oluşturur.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxde-common"
	version="0.99.2"
	description="LXDE Session default configuration files and nuoveXT2 iconset "
	source="https://github.com/lxde/lxde-common/archive/refs/tags/$version.tar.gz"
	depends=""
	builddepend=""
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
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


.. raw:: pdf

   PageBreak
