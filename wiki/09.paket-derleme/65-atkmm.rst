.. _atkmm:
**atkmm**
=========

atkmm, C++ için ATK (Accessibility Toolkit) bağlayıcısıdır. ATK, GNOME ve diğer Linux masaüstü ortamlarında erişilebilirlik (accessibility) desteği sağlamak için kullanılan bir araçtır. atkmm, C++ dilinde yazılmış uygulamaların ATK ile etkileşime girmesini sağlayan bir kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="atkmm"
	version="2.28.3"
	url="https://www.gtkmm.org"
	description="Atkmm is the official C++ interface for the ATK accessibility toolkit library."
	source="https://download.gnome.org/sources/atkmm/${version%.*}/atkmm-${version}.tar.xz"
	depends="at-spi2-core,glibmm"
	group="dev.cpp"

	setup () {
	cd $SOURCEDIR
		meson setup $BUILDDIR --prefix=/usr \
		--libdir=/usr/lib64/
	}

	build () {
		ninja -C $BUILDDIR
	}

	package () {
		DESTDIR=${DESTDIR} ninja -C $BUILDDIR install
	}


 
.. raw:: pdf

   PageBreak
