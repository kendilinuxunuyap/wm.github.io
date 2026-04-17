.. _lxinput:
**lxinput**
===========

Giriş aygıtlarını yapılandırma için gerekli bileşendir.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxinput"
	version="0.3.5"
	description="LXDE keyboard and mouse configuration tool"
	source="https://downloads.sourceforge.net/lxde/lxinput-$version.tar.xz"
	depends="gtk3"
	builddepend="intltool"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --enable-gtk3 
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
