.. _gobject-introspection:
**gobject-introspection**
=========================

GObject için temel kütüphane.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="gobject-introspection"
	version="1.72.0"
	description="Introspection system for GObject-based libraries"
	source="https://gitlab.gnome.org/GNOME/gobject-introspection/-/archive/${version}/gobject-introspection-${version}.tar.gz"
	depends="cairo,libtool,python,py3-setuptools"
	builddepend="bison,flex,libffi,meson"
	group="dev.libs"

	setup(){
		cd $SOURCEDIR
		meson setup $BUILDDIR --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --wrap-mode=nodownload
	}

	build(){
		ninja -C $BUILDDIR
	}

	package(){
		DESTDIR=$DESTDIR ninja -C $BUILDDIR install
	}


**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
