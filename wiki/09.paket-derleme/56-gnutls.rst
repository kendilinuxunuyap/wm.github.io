.. _gnutls:
**gnutls**
==========

GnuTLS, SSL/TLS (Secure Sockets Layer / Transport Layer Security) protokollerini ve kripto işlemleri uygulamak için kullanılan açık kaynaklı bir kütüphanedir. Güvenli internet iletişimini sağlamak için yaygın olarak kullanılır.

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
		make $jobs
	}

	package(){
		make install DESTDIR=$DESTDIR
	}


 
.. raw:: pdf

   PageBreak
