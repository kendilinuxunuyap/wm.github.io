.. _mpdecimal:
**mpdecimal**
=============

MPDecimal, çok hassas sayısal hesaplamalar yapmak için kullanılan, yüksek hassasiyetli aritmetik sağlayan bir kütüphanedir. Özellikle ondalık sayı işlemlerine odaklanarak, kayıpları minimize eder ve kullanıcıya gelişmiş hassasiyet sunar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="mpdecimal"
	version="4.0.0"
	url="https://www.bytereef.org/mpdecimal/index.html"
	description="Package for correctly-rounded arbitrary precision decimal floating point arithmetic"
	source="https://www.bytereef.org/software/$name/releases/$name-$version.tar.gz"
	depends=""
	builddepend=""
	group="net.db"

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


 
.. raw:: pdf

   PageBreak
