.. _hicolor-icon-theme:
**hicolor-icon-theme**
======================

hicolor-icon-theme, Linux ve Unix tabanlı sistemlerde, masaüstü ortamları ve uygulamalar için simge seti sağlayan bir temadır. Bu tema, "hicolor" adıyla bilinir ve genellikle uygulamaların simgelerini bir standarda oturtmak amacıyla kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="hicolor-icon-theme"
	version="0.17"
	description="Freedesktop.org Hicolor icon theme"
	source="http://icon-theme.freedesktop.org/releases/hicolor-icon-theme-$version.tar.xz"
	depends=""
	group="x11.themes"


	setup(){
		cd $SOURCEDIR
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
