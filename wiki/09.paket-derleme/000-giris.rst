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

**Linux Masaüstü Ortamları ve Pencere Yöneticileri**
====================================================

Bu belgede, yaygın olarak kullanılan bazı Linux masaüstü ortamları ve pencere yöneticileri tanıtılmaktadır.

***Openbox**
------------

``Openbox``, hafif ve son derece özelleştirilebilir bir *pencere yöneticisidir*. Kendi başına bir masaüstü ortamı değildir, ancak diğer bileşenlerle birlikte kullanılarak işlevsel bir masaüstü ortamı haline getirilebilir.

- Hafif yapısı ile düşük sistem kaynaklarında bile çalışır.
- Menü ve kısayol tuşları tamamen kullanıcı tarafından yapılandırılabilir.
- LXDE gibi hafif masaüstü ortamlarının bir parçası olarak da kullanılır.

**Lumia**
---------

``Lumia``, geleneksel masaüstü düzenine sahip olmayı amaçlayan minimalist ve modern bir *masaüstü ortamıdır*. LXQt çatallanması değildir ancak benzer bir hafifliği hedefler.

- Daha az bilinen bir projedir.
- GTK veya Qt yerine bağımsız araçlarla geliştirilmiş olabilir.
- Hedefi hafiflik ve basitliktir.

(Not: Lumia ismi bazı kaynaklarda farklı anlamlarda kullanılabilir. Eğer belirli bir proje veya bağlantıdan söz ediliyorsa, detayları güncellenmelidir.)

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
   * - Lumia
     - ?
     - Çok Hafif
     - Az
     - ?
     - ?
     - Var
     - Az
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




.. _giris:
**Ön Hazırlık**
---------------

Paket derleme işlemi öncesi aşağıdaki konuları bilmemiz gerekmektedir. Bunlar; 

1. Derleme(Dinamik/Static) 
2. chroot Kullanımı 
3. İso Oluşturma
4. ssh Kullanımı
5. sftp Kullanımı
6. scp Kullanımı
7. VirtualBox Kullanmı
8. cfdisk Kullanımı

Burada liste halinde verilen konu başlıkları bu dokümanın **Yardımcı Konular** bölümünde anlatılmaktadır. 

Bundan sonraki adımlarda kendi dağıtımımızın **xorg ve x11** pencere sistemini derleyerek **Temel Sistem** üzerinde çalıştıracağız!


GNU Araçlarıyla **xorg ve x11** derleme işlemini **kly Paket Sistemi** kullanılarak derleyeceğiz. Derleme işlemini **kly -c** komutuyla yapacağız. Derlenen paketleri **scp** ve **sftp** kullanarak **Temel Sistem** üzerine kopyalayacağız. **kly -i** komutumuzla
kopyaladığımız paketi **Temel Sistem** üzerine kuracağız. Oluşturduğumuz paketleri istersek github'a yükleyip. github üzerinden kururabiliriz.

.. raw:: pdf

   PageBreak


**xorg ve x11'in Çalışması için Gerekli Paketler**
-----------------------------------------------

.. list-table::
   :widths: 33 33 33

   * - 0- :ref:`giris`
     - 25- :ref:`libX11`
     - 50- :ref:`libinput`
   * - 1- :ref:`xorg-server`
     - 26- :ref:`libICE`
     - 51- :ref:`mtdev`
   * - 2- :ref:`pixman`
     - 27- :ref:`libXrender`
     - 52- :ref:`libevdev`
   * - 3- :ref:`libpciaccess`
     - 28- :ref:`libxcb`
     - 53- :ref:`libwacom`
   * - 4- :ref:`libXau`
     - 29- :ref:`libSM`
     - 54- :ref:`libgudev`
   * - 5- :ref:`libXdmcp`
     - 30- :ref:`xf86-input-libinput`
     - 55- :ref:`libffi`
   * - 6- :ref:`libXfont2`
     - 31- :ref:`xf86-input-vmmouse`
     - 56- :ref:`xinit`
   * - 7- :ref:`libxshmfence`
     - 32- :ref:`xf86-video-amdgpu`
     - 57- :ref:`xcalc`
   * - 8- :ref:`libdrm`
     - 33- :ref:`xf86-video-ast`
     - 58- :ref:`libXi`
   * - 9-  :ref:`libxcvt`
     - 34- :ref:`xf86-video-ati`
     - 59- :ref:`openbox`
   * - 10- :ref:`libfontenc`
     - 35- :ref:`xf86-video-dummy`
     - 60- :ref:`libXcursor`
   * - 11- :ref:`freetype`
     - 36- :ref:`xf86-video-fbdev`
     - 61- :ref:`libXfixes`
   * - 12- :ref:`libpng`
     - 37- :ref:`xf86-video-intel`
     - 62- :ref:`pango`
   * - 13- :ref:`harfbuzz`
     - 38- :ref:`xf86-video-mga`
     - 63- :ref:`libXrandr`
   * - 14- :ref:`glib`
     - 39- :ref:`xf86-video-nouveau`
     - 64- :ref:`fribidi`
   * - 15- :ref:`xterm`
     - 40- :ref:`xf86-video-r128`
     - 65- :ref:`xcb-util`
   * - 16- :ref:`libXft`
     - 41- :ref:`xf86-video-siliconmotion`
     - 66- :ref:`libthai`
   * - 17- :ref:`fontconfig`
     - 42- :ref:`xf86-video-vboxvideo`
     - 67- :ref:`libdatrie`
   * - 18- :ref:`dejavu`
     - 43- :ref:`xf86-video-vesa`
     - 68- 
   * - 19- :ref:`libXext`
     - 44- :ref:`xf86-video-vmware`
     - 69- 
   * - 20- :ref:`libXaw`
     - 45- :ref:`xkbcomp`
     - 70- 
   * - 21- :ref:`libXmu`
     - 46- :ref:`libxkbfile`
     - 71- 
   * - 22- :ref:`libXinerama`
     - 47- :ref:`libglvnd`
     - 72- 
   * - 23- :ref:`libXpm`
     - 48- :ref:`startup-notification`
     - 73-    
   * - 24- :ref:`libXt`
     - 49- :ref:`xkeyboard-config`
     - 74-

1.  lxmenu-data
2.  lxde-common
3.  lxappearance
4.  lxinput
5.  lxrandr
6.  lxsession
7.  lxpanel
8.  lxtask
9.  lxterminal
10. pcmanfm
11. lxlauncher
12. lxhotkey
13. lxde-base (meta)

Ek Notlar

    libfm ve menu-cache gibi alt bağımlılıkları da pcmanfm, lxpanel gibi bileşenlerden önce kurulmalıdır.
    
Kaynaklar
---------

- https://wiki.lxde.org/en/Main_Page
- https://github.com/lxde
- https://wiki.archlinux.org/title/LXDE



**Bağımlılık Zinciri**
----------------------

Linux paketinin sorunsuz çalışabilmesi için bağımlı olduğu tüm paketlerin önceden derlenmiş olması gerekir. 
**x11**'in en temel paketleri **xorg-server, mesa, llvm, cairo** paketleridir.  Tüm paketleri derlesek bile **xorg-server, mesa, llvm, cairo** paketleri düzgün ve uyumlu versiyonları olmadığı zaman x penceremiz açılmayacaktır. Buradaki tüm paketler ve bağımlılıkları derlendikten sonra **Xorg:0** şeklinde x pencere sistemimiz çalışacaktır.

**Derleme Öncesi Hazırlık!**
----------------------------

Paket derleme işlemine başlamadan önce, aşağıdaki temel araçları sisteminize kurmalısınız.

.. code-block:: bash

	sudo apt update
	sudo apt-get install debootstrap xorriso mtools make squashfs-tools gcc wget unzip xz-utils tar zstd fakeroot \
	autoconf automake autotools-dev make meson cmake ninja-build pkgconf patch libtool grub-pc grub-pc-bin
	
.. raw:: pdf

   PageBreak

