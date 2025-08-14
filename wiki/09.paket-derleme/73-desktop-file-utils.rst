.. _desktop-file-utils:
**desktop-file-utils**
======================

desktop-file-utils, Linux sistemlerinde masaüstü ortamlarıyla ilgili dosya işlemleri yapan bir yazılım paketidir. Bu araç, .desktop dosyalarını işlemek ve doğrulamak için kullanılır. .desktop dosyaları, bir uygulamanın masaüstü ortamında nasıl görüntüleneceği ve çalıştırılacağına dair bilgi içeren metin dosyalarıdır. Bu dosyalar, bir uygulamanın menülerde nasıl görüneceğini, hangi simgeyi kullanacağını, çalıştırılacak komutları ve diğer önemli bilgileri belirler.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="desktop-file-utils"
	version="0.27"
	description="Command line utilities for working with desktop entries"
	source="https://www.freedesktop.org/software/desktop-file-utils/releases/desktop-file-utils-${version}.tar.xz"
	depends="glib"
	builddepend="git,meson"
	group="dev.util"


	setup(){
		cd $SOURCEDIR
		meson setup $BUILDDIR --prefix=/usr \
		    --libdir=/usr/lib64/
	}

	build(){
		ninja -C build
	}

	package(){
		DESTDIR=$DESTDIR ninja -C $BUILDDIR install
	}

 
.. raw:: pdf

   PageBreak
