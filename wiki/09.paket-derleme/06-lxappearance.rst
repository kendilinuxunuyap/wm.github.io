.. _lxappearance:
**lxappearance**
================

GTK temalarını ve simge setlerini yönetmek için kullanılan tema yapılandırma aracıdır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxappearance"
	version="0.6.3"
	description="Feature-rich GTK+ theme switcher of the LXDE Desktop"
	source="https://downloads.sourceforge.net/lxde/$name-$version.tar.xz"
	depends="gtk3,dbus-glib"
	builddepend=""
	group="lxde.base"

	setup(){
		cp -prvf $PACKAGEDIR/00-gtk3-fix.patch /tmp/bps/build/
		cd $SOURCEDIR
		patch -Np1 -i ../00-gtk3-fix.patch
		./configure --prefix=/usr --enable-gtk3 \
		    --libdir=/usr/lib64/ \
		    --enable-dbus
		    
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}


 
.. raw:: pdf

   PageBreak
