**lxmenu-data**
===============

Menü tanımları ve veri dosyalarını içerir. Diğer bileşenlerin menü bilgilerini kullanabilmesi için öncelikle derlenmelidir.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxmenu-data"
	version="0.1.5"
	description="Provides files needed for LXDE application menus"
	source="https://github.com/lxde/lxmenu-data/archive/refs/tags/$version.tar.gz"
	depends=""
	builddepend="intltool"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
		    --sysconfdir=/etc
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}


.. raw:: pdf

   PageBreak
