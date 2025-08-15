**Pencere Yöneticisi Nedir?**
=============================

Bir ``pencere yöneticisi`` (window manager), bir masaüstü sisteminde **kullanıcı ve uygulama pencereleri arasındaki etkileşimi yöneten** temel yazılımlardır. Kimi bağımsız çalışırken, kimileri tam masaüstü ortamlarının bir parçasıdır. Sistem kaynakları, kullanıcı deneyimi ve özelleştirme gereksinimlerine göre farklı türleri tercih edilebilir.

Temel Görevleri
---------------

1. **Pencere Oluşturma ve Kontrolü**
   - Uygulama pencerelerini oluşturur, kapatır, yeniden boyutlandırır ve taşır.
   - Pencerelerin hangi sırada ve hangi pencerenin önde olduğunu belirler (odak yönetimi).

2. **Çerçeve ve Dekorasyon Sağlama**
   - Pencerelere başlık çubuğu, kenarlık, simge durumuna küçültme, büyütme ve kapatma gibi kontroller ekler.
   - Bazı yöneticiler tema desteği ile görsel özelleştirme sunar.

3. **Düzenleme (Layout) Yönetimi**
   - Pencerelerin nasıl yerleşeceğini belirler:
   - **Stacking (Yığınlama):** Pencereler üst üste gelir (örnek: Openbox, XFWM).
   - **Tiling (Döşeme):** Pencereler ekranı böler, üst üste gelmez (örnek: i3, bspwm).
   - **Dynamic:** Hem stacking hem tiling yöntemlerini karıştırabilir (örnek: awesomewm).

4. **Fare ve Klavye Etkileşimi**
   - Pencereleri sürükleme, yeniden boyutlandırma gibi işlemleri fareyle yapmaya olanak tanır.
   - Kısayol tuşları ile pencere geçişi, kapatma, taşıma gibi işlemleri sağlar.

5. **Masaüstü Ortamı Entegrasyonu (isteğe bağlı)**
   - Bazı pencere yöneticileri bağımsız çalışırken (örneğin Fluxbox),bazıları masaüstü ortamlarının bir parçasıdır (örneğin GNOME → Mutter, KDE → KWin).

.. list-table:: Popüler Pencere Yöneticileri
   :header-rows: 1
   :widths: 15 15 40

   * - Adı
     - Türü
     - Açıklama
   * - Openbox
     - Stacking
     - Hafif ve özelleştirilebilir
   * - i3
     - Tiling
     - Klavye odaklı, minimal
   * - KWin
     - Stacking + efekt
     - KDE Plasma bileşeni
   * - Mutter
     - GNOME bileşeni
     - Modern kompozit WM
   * - XFWM4
     - XFCE bileşeni
     - Hafif ve geleneksel
   * - Fluxbox
     - Stacking
     - Minimalist, bağımsız


Kaynaklar
---------

- ArchWiki – Window Manager: https://wiki.archlinux.org/title/Window_manager
- Debian Wiki – WindowManagers: https://wiki.debian.org/WindowManager
- Gentoo Wiki – Window Managers: https://wiki.gentoo.org/wiki/Window_managers
- https://en.wikipedia.org/wiki/Window_manager

.. raw:: pdf

   PageBreak

**Linux Masaüstü Ortamları ve Pencere Yöneticileri**
====================================================

Bu belgede, yaygın olarak kullanılan bazı Linux masaüstü ortamları ve pencere yöneticileri tanıtılmaktadır.

***Openbox**
------------

``Openbox``, hafif ve son derece özelleştirilebilir bir *pencere yöneticisidir*. Kendi başına bir masaüstü ortamı değildir, ancak diğer bileşenlerle birlikte kullanılarak işlevsel bir masaüstü ortamı haline getirilebilir.

- Hafif yapısı ile düşük sistem kaynaklarında bile çalışır.
- Menü ve kısayol tuşları tamamen kullanıcı tarafından yapılandırılabilir.
- LXDE gibi hafif masaüstü ortamlarının bir parçası olarak da kullanılır.

**LXDE (Lightweight X11 Desktop Environment)**
----------------------------------------------

``LXDE``, düşük donanım kaynaklarına sahip sistemler için tasarlanmış hafif bir masaüstü ortamıdır.

- Ana pencere yöneticisi: ``Openbox``
- Hızlı ve düşük bellek kullanımı
- GTK2 üzerine inşa edilmiştir
- Geliştiricileri, daha modern bir yapı olan ``LXQt`` projesine yönelmiştir.

**XFCE**
--------

``XFCE``, hafifliği ve kullanıcı dostu arayüzüyle bilinen bir masaüstü ortamıdır.

- GTK tabanlıdır (GTK3)
- Panel, dosya yöneticisi (Thunar), ayarlar ve eklenti sistemi gibi bileşenlere sahiptir.
- Hem hafif hem de modern bir masaüstü deneyimi sunar.

**KDE Plasma**
--------------

``KDE``, tam özellikli ve görsel olarak zengin bir masaüstü ortamıdır. Günümüzde ``KDE Plasma`` olarak anılır.

- Qt kütüphanesi kullanılarak geliştirilmiştir.
- Geniş özelleştirme seçenekleri ve güçlü yerleşik uygulamalar (Dolphin, Konsole, KWin)
- Sistem kaynaklarını daha fazla kullanır, ancak son sürümler büyük ölçüde optimize edilmiştir.

**Cinnamon**
------------

``Cinnamon``, geleneksel masaüstü deneyimini korumayı hedefleyen modern bir ortamdır. ``Linux Mint`` tarafından geliştirilmiştir.

- GNOME 3'ün bir çatallanmasıdır, ancak klasik masaüstü düzenine sahiptir.
- GTK üzerine inşa edilmiştir.
- Windows benzeri menü ve panel yapısı sunar.

**GNOME**
---------

``GNOME``, modern ve basit bir masaüstü ortamıdır. Özellikle dokunmatik destekli ve geniş ekran cihazlar için optimize edilmiştir.

- GTK+ tabanlıdır.
- Minimalist tasarımıyla dikkat çeker (örneğin varsayılan olarak masaüstü simgeleri yoktur).
- Özellikle Ubuntu’nun varsayılan masaüstüdür.

Karşılaştırma Özeti
-------------------

.. list-table:: Popüler Linux Masaüstü Ortamları Karşılaştırması
   :header-rows: 1
   :widths: 15 15 15 15 10 10 10 10

   * - Ortam
     - Teknoloji
     - Hafiflik
     - Özellik
     - Panel
     - Menü
     - Tema
     - Uygulama
   * - Openbox
     - WM (X11)
     - Çok Hafif
     - Az
     - Hayır
     - Evet
     - Var
     - Yok
   * - LXDE
     - GTK2
     - Hafif
     - Orta
     - Evet
     - Evet
     - Var
     - Orta
   * - XFCE
     - GTK3
     - Orta
     - Orta
     - Evet
     - Evet
     - Var
     - Orta
   * - KDE Plasma
     - Qt
     - Ağır
     - Geniş
     - Evet
     - Evet
     - Çok
     - Geniş
   * - Cinnamon
     - GTK3
     - Orta-Ağır
     - Geniş
     - Evet
     - Evet
     - Çok
     - Geniş
   * - GNOME
     - GTK4
     - Ağır
     - Geniş
     - Hayır
     - Hayır
     - Az
     - Geniş

Kaynaklar
---------

- https://wiki.archlinux.org/title/Desktop_environment
- https://wiki.debian.org/DesktopEnvironment
- https://www.gnome.org/
- https://www.kde.org/
- https://www.linuxmint.com/

.. raw:: pdf

   PageBreak

