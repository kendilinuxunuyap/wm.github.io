.. _libepoxy:
**libepoxy**
===========

libepoxy, OpenGL ve OpenGL ES gibi grafik API'leri için platformlar arası uyumluluk sağlamak amacıyla kullanılan bir C kütüphanesidir. Bu kütüphane, özellikle OpenGL sürüm uyuşmazlıklarını çözer ve dinamik sürücü yükleme gibi işlemleri kolaylaştırır. Yani, farklı sistemlerde ve platformlarda OpenGL ile çalışan uygulamalar için bir uyumluluk katmanı sağlar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="libepoxy"
	version="1.5.10"
	description="Library for handling OpenGL function pointer management"
	source="https://github.com/anholt/libepoxy/archive/refs/tags/$version.tar.gz"
	depends="libX11,mesa"
	group="media.libs"


	setup(){
		cd $SOURCEDIR
		meson setup $BUILDDIR --prefix=/usr \
		    --libdir=/usr/lib64/
	}

	build(){
		ninja -C $BUILDDIR 
	}

	package(){
		DESTDIR=$DESTDIR ninja -C $BUILDDIR install
	}


**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
