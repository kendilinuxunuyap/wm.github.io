.. _libdmx:
**libdmx**
==========

libdmx, DMX (Distributed Multihead X) protokolünü destekleyen bir kütüphanedir. DMX, X Window System üzerinde birden fazla ekranı (multihead) birleştirerek dağıtık bir masaüstü ortamı oluşturmanıza olanak tanır. DMX, temel olarak, birden fazla X sunucusunun birleşik bir şekilde çalışmasını sağlar, böylece birden fazla monitörü tek bir büyük masaüstü ortamı olarak kullanabilirsiniz.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libdmx"
	version="1.1.4"
	description="X.Org dmx library"
	source="https://www.x.org/archive/individual/lib/libdmx-$version.tar.gz"
	depends=""
	group="x11.libs"


	setup(){
		$SOURCEDIR/configure --prefix=/usr \
		    --libdir=/usr/lib64/
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
	}


 
.. raw:: pdf

   PageBreak
