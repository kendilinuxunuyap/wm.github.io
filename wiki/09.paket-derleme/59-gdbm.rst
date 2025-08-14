.. _gdbm:
**gdbm**
========

GDBM, GNU Database Manager'ın kısaltmasıdır ve verileri anahtar-değer çiftleri (key-value pairs) olarak depolayan bir veritabanı yönetim sistemidir. C dilinde yazılmıştır ve düşük seviyeli, hızlı ve taşınabilir bir veritabanı çözümü sunar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="gdbm"
	version="1.23"
	description="GNU dbm is a set of database routines that use extensible hashing"
	source="https://ftp.gnu.org/gnu/gdbm/gdbm-$version.tar.gz"
	depends=""
	builddepend=""
	group="dev.libs"

	setup(){
		cd $SOURCEDIR
		./configure --prefix=/usr \
			--libdir=/usr/lib64 \
			--enable-libgdbm-compat \
			--disable-largefile \
			--disable-dependency-tracking \
			--enable-fast-install
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}


 
.. raw:: pdf

   PageBreak
