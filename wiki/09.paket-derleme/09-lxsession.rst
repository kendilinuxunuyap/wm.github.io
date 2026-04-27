.. _lxsession:

**lxsession**
=============

LXDE oturum yöneticisi.


**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="lxsession"
	version="0.5.5"
	description="Lightweight X11 session manager"
	#source="https://downloads.sourceforge.net/lxde/lxsession-$version.tar.xz"
	source="https://salsa.debian.org/lxde-team/lxsession/-/archive/debian/$version-2/lxsession-debian-$version-2.tar.gz"
	depends="gtk3,polkit"
	builddepend="intltool,vala,docbook-xsl"
	group="lxde.base"


	setup(){
		cd $SOURCEDIR
		autoreconf -fvi
		./configure --prefix=/usr\
		    --sysconfdir=/etc \
		    --libexecdir=/usr/libexec \
		    --enable-gtk3 \
		    --enable-buildin-clipboard \
		    --libdir=/usr/lib64/ \
		    --enable-buildin-polkit
	}

	build(){
		make
	}

	package(){
		make  DESTDIR="$DESTDIR" install
		# Ignore package by AppStream to avoid duplicated IDs
		echo "X-AppStream-Ignore=true" >> "$DESTDIR/usr/share/applications/lxsession-default-apps.desktop"
		echo "X-AppStream-Ignore=true" >> "$DESTDIR/usr/share/applications/lxsession-edit.desktop"
	}

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
