.. _hsakmt:
**hsakmt**
==========

AMD ROCm (Radeon Open Compute) platformunun parçası olan bir kütüphanedir. Kullanıcı modundan AMD HSA (Heterogeneous System Architecture) çekirdek sürücüsüyle (AMDKFD) iletişim kurmak için bir ara katman sağlar. GPU ve CPU arasındaki heterojen bilgi işlem işlemlerini destekler, özellikle Kaveri ve Carrizo APU'lar için optimize edilmiştir. Hafif ve açık kaynaklıdır.

**Paketi Derleme :**
--------------------

.. code-block:: bash

    #!/usr/bin/env bash
    name="hsakmt"
    version="1.0.0"
    description="Package hsakt"
    source="https://www.x.org/archive/individual/lib/hsakmt-$version.tar.gz"
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

**Not:** Burada verilen derleme talimatı(script) **kly Paket Sistemi**'ni kullanarak paketi derler ve oluştur. Oluşan paket(**.kly uzantılı dosya**)  **kly Paket Sistemi** kullanılarak siteme yüklenebilir. **kly Paket Sistemiyle Paket Yapma** konusunu okumak için `tıklayınız. <#klypaketyap>`_


.. raw:: pdf

   PageBreak
