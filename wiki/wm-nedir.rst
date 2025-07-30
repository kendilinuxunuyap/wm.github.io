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
   - Bazı pencere yöneticileri bağımsız çalışırken (örneğin Fluxbox),
     bazıları masaüstü ortamlarının bir parçasıdır (örneğin GNOME → Mutter, KDE → KWin).

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
