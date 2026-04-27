.. _gdbm:

**gdbm**
========

Anahtar-değer çifti olarak depolayan bir veritabanı yönetim sistemidir.

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


**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


 
.. raw:: pdf

   PageBreak
