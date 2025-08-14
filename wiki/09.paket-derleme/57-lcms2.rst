.. _lcms2:
**lcms2**
=========

lcms2 (Little CMS 2), görüntü işleme ve renk yönetimi için kullanılan açık kaynaklı bir kütüphanedir. Görüntülerin renk profilini yönetmek, dönüştürmek ve renk doğruluğunu sağlamak için kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lcms2"
	version="2.16"
	url="https://netix.dl.sourceforge.net/project/lcms/lcms/2.14/lcms2-2.14.tar.gz"
	description="Small-footprint color management engine, version 2"
	source="https://netix.dl.sourceforge.net/project/lcms/lcms/${version}/lcms2-${version}.tar.gz"
	depends="libtiff"
	group="media.libs"

	setup(){

		$SOURCEDIR/configure --prefix=/usr \
		    --libdir=/usr/lib64/
	}

	build(){
		make $jobs
	}

	package(){
		make install DESTDIR=$DESTDIR
	}


 
.. raw:: pdf

   PageBreak
