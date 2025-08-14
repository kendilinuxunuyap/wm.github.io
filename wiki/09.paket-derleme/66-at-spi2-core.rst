.. _at-spi2-core:
**at-spi2-core**
================

at-spi2-core, GNOME masaüstü ortamında kullanılan AT-SPI2 (Assistive Technology Service Provider Interface 2) framework'ünün çekirdek bileşenidir. Bu framework, erişilebilirlik (accessibility) araçları ve yazılımları ile masaüstü uygulamaları arasındaki iletişimi sağlar. AT-SPI2, özellikle görme engelli kullanıcılar için ekran okuyucuları ve diğer yardımcı teknolojilerle etkileşimde bulunabilmesini sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="at-spi2-core"

	version="2.50.1"
	url="https://gitlab.gnome.org/GNOME/at-spi2-core"
	description="GTK+ & GNOME Accessibility Toolkit"

	source="https://gitlab.gnome.org/GNOME/at-spi2-core/-/archive/AT_SPI2_CORE_${version//./_}/at-spi2-core-AT_SPI2_CORE_${version//./_}.tar.gz"
	depends="glib,libffi,libpcre2,libXtst"

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
