Bu dokümanda anlatılan paketlerin **kly Paket Sistemiyle** hazırlanmış **LXDE Masaüstü Ortamı** isosu hazırlandı. İsoyu https://github.com/kendilinuxunuyap/kly-lxde-distro/releases/download/current/kly-lxde-distro.iso adresinden indirebilirsiniz.

Şimdi hazırlanan ISO’yu **QEMU** veya **VirtualBox** kullanarak çalıştıralım. Ekran görüntüleri aşağıda verilmiştir.

**Canlı(live) Sistem Kullanımı**
--------------------------------

.. image:: /_static/images/iso-20.png
  :width: 600
  :height: 200

.. image:: /_static/images/iso-21.png
  :width: 600
  :height: 450

Canlı(live) sistem çalıştırıldığında overlay live bir sistemin açıldığını görmekteyiz. Canlı(live) sistemde kullanıcı adları ve parolaları;

- Kullanıcı: root	Parola: 1
- Kullanıcı: live	Parola: live

.. raw:: pdf

   PageBreak
   
**Sistem Kurulumu**
-------------------

Sistemin kurulumu için resimlerde görünen sıraya göre seçimler yapmalıyız.

.. image:: /_static/images/iso-30.png
  :width: 600

.. image:: /_static/images/iso-31.png
  :width: 600

Kurulum menüsünde kullanıcı adları ve parolaları, klayve varsayılan olarak;

- Kullanıcı: root	Parola: 1
- Kullanıcı: user1	Parola: 1
- Dil   	: tr_TR
- Klavye   	: trq

menüden değişiklik yapabilirsiniz. Değişiklik yapmadan sadece kurulum diskini ve disk bölümünü seçip Install(Yükle) işlemi yapabilirsiniz.


.. image:: /_static/images/iso-32.png
  :width: 600

.. image:: /_static/images/iso-33.png
  :width: 600


.. raw:: pdf

   PageBreak
   
**Sistemin Çalışması**
----------------------

Sistem kurulumu gerçekleştiğinde  sistem resimde görüldüğü gibi açılmalıdır.

.. image:: /_static/images/iso-40.png
  :width: 600

Sisteme **user1** (parola=1) kullanıcısı olarak giriş yapıldığı görülmektedir.

.. image:: /_static/images/lxde0.png
  :width: 600
  
**xinit** çalışınca **X Pencere Sistemine** geçiş yapılacak.

.. raw:: pdf

   PageBreak
   
**xinit** çalışınca **X Pencere Sistemi** aşağıdaki gibi açılacaktır.

.. image:: /_static/images/lxde1.png
  :width: 600
  
**X Pencere Sistemi** çalışınca aşağı ve pencere yönetimini ve masaüstü ortamı için **exec lxsession** çalıştırılıyor.

.. image:: /_static/images/lxde2.png
  :width: 600

Artık LXDE Masaüstü ortamındayız. LXDE araçlarının çalıştırılmış hali aşağıda görülmektedir.

.. image:: /_static/images/lxde3.png
  :width: 600

LXDE, sade sistem isteyen kullanıcılar için mükemmel bir tercihtir. Ancak görsellik, modernlik veya geniş özellik seti beklentiniz varsa daha güncel alternatifler (XFCE, Cinnamon) tercih edilebilir.

.. raw:: pdf

   PageBreak
