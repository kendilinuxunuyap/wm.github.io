.. _lxpanel:

**lxpanel**
===========

Lxde görev çubuğu ve panel bileşeni.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxpanel"
	version="0.10.1"
	description="Lightweight X11 desktop panel for LXDE"
	source="https://downloads.sourceforge.net/lxde/lxpanel-$version.tar.xz"
	depends="libwnck3,wireless-tools,curl,alsa-lib,libwnck,"
	builddepend="intltool,docbook-xml,docbook-xsl,wireless_tools"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		# Disable pager plugin as it breaks panel layout with GTK+ 3
		# https://sourceforge.net/p/lxde/bugs/773/
		sed -i "/pager.c/d" plugins/Makefile.am
		sed -i "/STATIC_PAGER/d" src/private.h
		sed -i "s/libwnck-3.0//" configure.ac
		sed -i "s/background=1/background=0/" data/default/panels/panel.in
		
		autoreconf -fvi
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    --enable-gtk3 \
		    --disable-silent-rules \
		    --with-plugins=all,-cpufreq
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
