.. _atkmm:
**atkmm**
=========

ATK, masaüstü ortamlarında erişilebilirlik desteği için kullanılan araçtır. 

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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
