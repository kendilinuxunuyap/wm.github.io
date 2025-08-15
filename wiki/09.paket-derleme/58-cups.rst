.. _cups:
**cups**
========

CUPS, Unix ve Unix benzeri işletim sistemlerinde (Linux, macOS, BSD gibi) kullanılan, yazıcıların yönetimi ve baskı işlemlerini yöneten açık kaynaklı bir yazıcı sunucu sistemidir. CUPS, yazıcılar arası iletişimi yönetmek için Internet Printing Protocol (IPP) kullanır ve baskı kuyruklarını, yazıcı yönetimini sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="cups"
	version="2.4.7"
	description="The Common Unix Printing System "
	source="https://github.com/OpenPrinting/cups/releases/download/v${version}/cups-${version}-source.tar.gz"
	depends="openssl"
	group="net.print"


	setup(){
		cp -prvf $PACKAGEDIR/files/ /tmp/kly/build/
		cd $SOURCEDIR
		./configure --prefix=/usr \
		    --libdir=/usr/lib64/ \
			--sysconfdir=/etc \
			--localstatedir=/var \
			--with-menudir=/usr/share/applications \
			--with-icondir=/usr/share/icons \
			--with-logdir=/var/log/cups \
			--with-docdir=/usr/share/cups \
			--with-rundir=/run/cups \
			--with-cupsd-file-perm=0755 \
			--with-cups-user=lp \
			--with-cups-group=lp \
			--with-system-groups=lpadmin \
			--with-domainsocket=/run/cups/cups.sock \
			--enable-libusb \
			--without-rcdir \
			--without-php \
			--disable-pam \
			--enable-raw-printing \
			--enable-dbus \
			--with-dbusdir=/usr/share/dbus-1 \
			--enable-libpaper \
			--enable-ssl=yes \
			--enable-gnutls \
			--disable-launchd \
			--disable-systemd
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
		mkdir -p "$DESTDIR"/etc/{passwd,group,init}.d
		install ../files/cups.groups "$DESTDIR"/etc/group.d/cups
		install ../files/cups.users "$DESTDIR"/etc/passwd.d/cups
		install ../files/cupsd.initd "$DESTDIR"/etc/init.d/cupsd
		
		mv $DESTDIR/usr/lib/* $DESTDIR/usr/lib64/
		rm -rf $DESTDIR/usr/lib
	}

Ek dosyaları indirmek için `tıklayınız. <https://kendilinuxunuyap.github.io/_static/files/cups/files.tar>`_

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
