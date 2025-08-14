.. _shared-mime-info:
**shared-mime-info**
====================

Linux ve Unix sistemlerinde MIME türlerini tanımlamak için kullanılan bir veritabanıdır. MIME (Multipurpose Internet Mail Extensions), internetteki çeşitli dosya türlerini tanımlamak için kullanılan bir standarttır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="shared-mime-info"
	version="2.4"
	description="The Shared MIME-info Database specification"
	source="https://gitlab.freedesktop.org/xdg/shared-mime-info/-/archive/${version}/shared-mime-info-${version}.tar.gz"
	depends="libxml2"
	group="x11.misc"

	setup(){
		
		cd $SOURCEDIR
		meson setup $BUILDDIR --prefix=/usr \
		    --libdir=/usr/lib64/
	}

	build(){
		ninja -C $BUILDDIR
	}

	package(){
		DESTDIR=$DESTDIR ninja -C $BUILDDIR install
	}


	 
.. raw:: pdf

   PageBreak
