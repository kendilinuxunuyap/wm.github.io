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

+------------+--------------+-------------+-----------+----------+----------+---------+--------+
| Ortam      | Teknoloji    | Hafiflik    | Özellik   | Panel    | Menü     | TEMA    | Uygulama|
+============+==============+=============+===========+==========+==========+=========+=========+
| Openbox    | WM (X11)     | Çok Hafif   | Az        | Hayır    | Evet     | Var     | Yok     |
| Lumia      | ?            | Çok Hafif   | Az        | ?        | ?        | Var     | Az      |
| LXDE       | GTK2         | Hafif       | Orta      | Evet     | Evet     | Var     | Orta    |
| XFCE       | GTK3         | Orta        | Orta      | Evet     | Evet     | Var     | Orta    |
| KDE Plasma | Qt           | Ağır        | Geniş     | Evet     | Evet     | Çok     | Geniş   |
| Cinnamon   | GTK3         | Orta-Ağır   | Geniş     | Evet     | Evet     | Çok     | Geniş   |
| GNOME      | GTK4         | Ağır        | Geniş     | Hayır    | Hayır    | Az      | Geniş   |
+------------+--------------+-------------+-----------+----------+----------+---------+--------+

Kaynaklar
---------

- https://wiki.archlinux.org/title/Desktop_environment
- https://wiki.debian.org/DesktopEnvironment
- https://www.gnome.org/
- https://www.kde.org/
- https://www.linuxmint.com/

.. raw:: pdf

   PageBreak

