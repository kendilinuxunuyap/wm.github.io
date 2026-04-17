.. _libmpc:
**libmpc**
==========

Sayı işleme kütüphanesi.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	version="1.3.1"
	name="libmpc"
	depends="glibc,mpfr"
	description="Library for the arithmetic of complex numbers with arbitrarily high precision"
	source="https://ftp.gnu.org/gnu/mpc/mpc-$version.tar.gz"
	groups="dev.libs"

	setup()
	{
		cd $SOURCEDIR
		./configure --prefix=/usr \
		    --libdir=/usr/lib64
	}
	build()
	{
		make
	}
	package()
	{
		make install DESTDIR=${DESTDIR}
	}

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
