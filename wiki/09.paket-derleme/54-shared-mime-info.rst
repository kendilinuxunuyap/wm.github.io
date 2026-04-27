.. _shared-mime-info:

**shared-mime-info**
====================

Dosya türlerini tanımlamak için kullanılan bir standarttır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="shared-mime-info"
	version="2.4"
	description="The Shared MIME-info Database specification"
	source="https://gitlab.freedesktop.org/xdg/shared-mime-info/-/archive/${version}/shared-mime-info-${version}.tar.gz"
	depends="libxml2"
	group="x11.misc"

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

Ek dosyaları indirmek için `tıklayınız.. <https://kendilinuxunuyap.github.io/_static/files/shared-mime-info/files.tar>`_

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


	 
.. raw:: pdf

   PageBreak
