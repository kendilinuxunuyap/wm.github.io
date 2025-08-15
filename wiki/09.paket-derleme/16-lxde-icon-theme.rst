.. _lxde-icon-theme:
**lxde-icon-theme**
===================

Lxde ikon ve tema paketidir.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxde-icon-theme"
	version="0.5.1"
	description="LXDE default icon theme based on nuoveXT2"
	source="https://downloads.sourceforge.net/lxde/lxde-icon-theme-$version.tar.xz"
	depends=""
	builddepend=""
	group="lxde.base"


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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


	 
.. raw:: pdf

   PageBreak
