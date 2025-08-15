.. _nettle:
**nettle**
==========

Nettle, kriptografik algoritmalar için bir açık kaynak kütüphanesidir. Linux sistemlerinde genellikle güvenlik ve şifreleme işlemleri için kullanılır. AES, SHA, RSA gibi yaygın kriptografik algoritmaları sağlar ve bunların hızlı bir şekilde uygulanabilmesini sağlar. Bu paket, birçok kriptografi tabanlı uygulama ve yazılımda temel bir bileşen olarak yer alır. Nettle, C dilinde yazılmıştır ve GNU Genel Kamu Lisansı (GPL) altında dağıtılmaktadır. Kısacası, güvenli veri iletimi ve şifreleme için kritik bir araçtır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="nettle"
	version="3.9"
	url="https://www.lysator.liu.se/~nisse/nettle"
	description="A low-level cryptographic library"
	source="https://ftp.gnu.org/gnu/nettle/nettle-${version}.tar.gz"
	depends="glibc"
	group="dev.libs"


	setup(){
		cd $SOURCEDIR
		./configure --prefix=/usr \
		    --libdir=/usr/lib64
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
