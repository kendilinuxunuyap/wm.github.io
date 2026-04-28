.. _locale-tr:

**locale-tr**
=============

locale-tr, Türkçe dil ve yerel ayarları sistemde uygun şekilde sağlamak için kullanılan bir yerelleştirme dosyası ya da paketi olup, sistemdeki tarih, saat, dil, para birimi gibi birçok yerel ayarın Türkçe’ye uyumlu olmasını sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="locale-tr"
	version="1.0"
	description="loacale türkçeleştirme ayarı"
	source=""
	depends="glibc,tzdata"
	group="sys.apps"


	setup(){
		echo ""
	}

	build(){
		echo ""
	}

	package(){
	umask 022
	mkdir -p ${DESTDIR}/lib64
	mkdir -p ${DESTDIR}/lib64/locale

	mkdir -p ${DESTDIR}/etc
	mkdir -p ${DESTDIR}/etc/profile.d
	cp -prfv $PACKAGEDIR/files/locale.sh  ${DESTDIR}/etc/profile.d/locale.sh
	cp -prfv $PACKAGEDIR/files/keyboard.sh  ${DESTDIR}/etc/profile.d/keyboard.sh
	cp -prfv $PACKAGEDIR/files/locale.gen  ${DESTDIR}/etc/locale.gen
	cp -prfv $PACKAGEDIR/files/profile  ${DESTDIR}/etc/profile
	}

Ek dosyaları indirmek için `tıklayınız.. <https://kendilinuxunuyap.github.io/_static/files/locale-tr/files.tar>`_

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
