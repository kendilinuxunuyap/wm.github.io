.. _xtrans:
**xtrans**
==========

xcb-util-wm, XCB tabanlı pencere yöneticileri ve X11 istemcileri için, ICC ve EWMH gibi pencere yöneticisi protokollerini uygulamayı kolaylaştıran bir yardımcı kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="xtrans"
	version="1.5.0"
	description="X.Org xtrans library"
	source="https://www.x.org/archive//individual/lib/xtrans-$version.tar.gz"
	depends=""
	group="x11.libs"


	setup(){

		$SOURCEDIR/configure --prefix=/usr \
		    --libdir=/usr/lib64/
	}

	build(){
		make
	}

	package(){
		make DESTDIR=$DESTDIR install
	}


 
.. raw:: pdf

   PageBreak
