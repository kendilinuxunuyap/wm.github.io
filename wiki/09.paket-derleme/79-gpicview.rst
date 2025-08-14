.. _gpicview:
**gpicview**
============

gpicview, GNOME masaüstü ortamı için hafif, hızlı ve basit bir resim görüntüleyicisidir. Kullanıcı dostu arayüzü ve temel görüntüleme özellikleriyle, sistem kaynaklarını verimli kullanırken kullanıcıya hızlı bir şekilde resimlere göz atma imkanı sunar. 

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="gpicview"
	version="0.3.1"
	description="Lightweight image viewer"
	source="https://github.com/lxde/gpicview/archive/refs/tags/$version.tar.gz"
	depends="gtk3"
	builddepend="intltool"
	group="lxde.apps"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
			--enable-gtk3 \
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
