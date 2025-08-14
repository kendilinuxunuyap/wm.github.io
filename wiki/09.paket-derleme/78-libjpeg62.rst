.. _libjpeg62:
**libjpeg62**
=============

libjpeg62, JPEG formatındaki resimlerin sıkıştırılması, çözülmesi ve işlenmesi için kullanılan bir kütüphanedir. Genellikle görüntü işleme uygulamalarında, web servislerinde ve fotoğraf düzenleme yazılımlarında kullanılır. Daha yeni sürümler olsa da, libjpeg62 eski sistemler ve uygulamalar için hala önemli bir kütüphanedir.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libjpeg62"
	version="0"
	description="MMX, SSE, and SSE2 SIMD accelerated JPEG library"
	source="http://ftp.de.debian.org/debian/pool/main/libj/libjpeg6b/libjpeg6b_6b2.orig.tar.gz"
	depends=""
	group="media.libs"

	setup(){
		cd $SOURCEDIR 
		autoreconf -fvi    
		./configure --prefix=/lib64/libjpeg62
	}

	build(){
		make
	}

	package(){
		make install DESTDIR=$DESTDIR
		mkdir -p $DESTDIR/lib64
		cd $DESTDIR/lib64
		ln -s libjpeg62/lib/libjpeg.so.62 libjpeg.so.62
	}


 
.. raw:: pdf

   PageBreak
