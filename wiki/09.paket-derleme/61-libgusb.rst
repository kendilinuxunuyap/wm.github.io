.. _libgusb:
**libgusb**
===========

libgusb, USB cihazlarıyla etkileşim kurmak için kullanılan bir C kütüphanesidir. GUSB (GNOME USB) olarak da bilinir ve özellikle GNOME masaüstü ortamı ile entegre çalışmak için geliştirilmiştir. USB cihazlarını yönetmek ve onlarla iletişim kurmak için düşük seviyeli API'ler sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libgusb"
	version="0.4.9"
	url="https://github.com/hughsie/libgusb"
	description=" GObject wrapper for libusb "
	source="https://github.com/hughsie/libgusb/archive/refs/tags/$version.tar.gz"
	depends="vala,gi-docgen,mesa,libusb,json-glib"
	group="dev.libs"

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
