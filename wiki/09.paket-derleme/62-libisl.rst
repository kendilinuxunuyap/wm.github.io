.. _libisl:
**libisl**
==========

libisl, Integer Set Library'nin kısaltmasıdır ve tam sayı kümeleri üzerinde işlem yapmak için kullanılan bir kütüphanedir. Genellikle doğrusal optimizasyon ve matematiksel modelleme problemleri çözmek için kullanılır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libisl"
	version="0.26"
	description="An Integer Set Library for the Polyhedral Model"
	source="https://libisl.sourceforge.io/isl-${version}.tar.bz2"
	depends="gmp"
	builddepend=""
	group="dev.libs"

	setup(){
		cd $SOURCEDIR

		./configure --prefix=/usr \
			--mandir=/usr/share/man \
			--infodir=/usr/share/info \
			--localstatedir=/var
	}

	build(){
		make
	}

	package(){
		make DESTDIR=$DESTDIR install
		install -dm755 "${DESTDIR}"/usr/share/gdb/python/auto-load/usr/lib
		mv "$DESTDIR"/usr/lib/*-gdb.py "$DESTDIR"/usr/share/gdb/python/auto-load/usr/lib/
	}

 
.. raw:: pdf

   PageBreak
