Bir önceki kitabımızda **X Pencere Sistemini** oluşturmayı ve iso halinde kurulumu anlatmıştık.
Şimdi ise bu **X Pencere Sistemini** kurarak bu sistem üzerine **LXDE** araçları ve kütüphanelerini derleyerek **LXDE** masaüstü ortamının nasıl çalışacağı analatılacaktır. **X Pencere Sistemi** https://github.com/kendilinuxunuyap/kly-x11-distro/releases/download/current/kly-x11-distro.iso adresinde bulunmaktadır. İso indirip kurulum yapabilirsiniz.

**X Pencere Sistemi Kurulumu**
------------------------------

Sistemin kurulumu için resimlerde görünen sıraya göre seçimler yapmalıyız.

.. image:: /_static/images/iso-30.png
  :width: 600

.. image:: /_static/images/iso-31.png
  :width: 600

.. raw:: pdf

   PageBreak
   
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

.. image:: /_static/images/x110.png
  :width: 600
  
**xinit** çalışınca **X Pencere Sistemine** geçiş yapılacak.

.. raw:: pdf

   PageBreak
   
**xinit** çalışınca **X Pencere Sistemi** aşağıdaki gibi açılacaktır.

.. image:: /_static/images/x111.png
  :width: 600
  
**X Pencere Sistemi** çalıştırılmış ve pencere yönetimini ve masaüstü ortamı için **openbox** çalıştırılıyor.

.. image:: /_static/images/x112.png
  :width: 600

**xcalc** uygulamasının çalıştırılması aşağıda gösterilmiştir.

.. image:: /_static/images/x113.png
  :width: 600

**X Pencere Sistemi** sistemi görüldüğü üzere çalışmaktadır. Artık **LXDE Masaüstü Ortamı** paketlerini ve bağımlılıklarını **kly Paket Sistemini** kullanarak derlenecek ve **X Pencere Sistemi** üzerine kurularak masaüstü ortamımızı çalışır hale getireceğiz.

.. raw:: pdf

   PageBreak
