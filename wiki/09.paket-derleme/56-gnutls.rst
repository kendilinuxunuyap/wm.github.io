.. _gnutls:
**gnutls**
==========

Kripto işlemleri uygulamak için kullanılan bir kütüphanedir. 

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="gnutls"
	version="3.8.0"
	url="https://www.gnupg.org/ftp/gcrypt/gnutls"
	description="The GnuTLS Transport Layer Security Library"
	source="https://www.gnupg.org/ftp/gcrypt/gnutls/v${version%.*}/gnutls-${version}.tar.xz"
	depends="nettle,p11-kit,unbound"
	group="net.libs"
	uses_extra="zstd brotli libidn2"


	setup(){
	cd $SOURCEDIR
		./configure --prefix=/usr \
		--libdir=/usr/lib64 \
		--disable-guile \
		--enable-ssl3-support \
		--enable-openssl-compatibility \
		--with-included-unistring \
		--with-included-libtasn1\
		--with-zstd \
		--with-brotli \
		--with-libidn2
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
