.. _libmpc:
**libmpc**
==========

libmpc, Multiple Precision Complex (Çok Hassas Karmaşık Sayılar) kütüphanesidir. Bu kütüphane, yüksek doğruluklu karmaşık sayılarla çalışmayı sağlayan bir matematiksel araçtır. Özellikle karmaşık sayılar üzerinde yapılan hesaplamaların çok hassas ve yüksek doğruluk gerektirdiği durumlarda kullanılır.

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



 
.. raw:: pdf

   PageBreak
