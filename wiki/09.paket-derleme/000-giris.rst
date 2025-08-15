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

Bundan sonraki adımlarda kendi dağıtımımızın **LXDE masaüstü ortmaını** derleyerek **X Pencere Sistemi** üzerinde çalıştıracağız!


GNU Araçlarıyla **LXDE Masaüstü Ortamının** derleme işlemini **kly Paket Sistemi** kullanılarak derleyeceğiz. Derleme işlemini **kly -c** komutuyla yapacağız. Derlenen paketleri **scp** ve **sftp** kullanarak **Temel Sistem** üzerine kopyalayacağız. **kly -pi** komutumuzla kopyaladığımız paketi **X Pencere Sistemi** üzerine kuracağız. Oluşturduğumuz paketleri istersek github'a yükleyip. github üzerinden kururabiliriz.

.. raw:: pdf

   PageBreak


**LXDE Masaüstü Ortamı için Gerekli Paketler**
----------------------------------------------

.. list-table::
   :widths: 33 33 33

   * - 0- :ref:`giris`
     - 27- :ref:`libXcomposite`
     - 54- :ref:`shared-mime-info`
   * - 1- :ref:`libfm`
     - 28- :ref:`libXdamage`
     - 55- :ref:`lz4`
   * - 2- :ref:`menu-cache`
     - 29- :ref:`libXfont`
     - 56- :ref:`gnutls`
   * - 3- :ref:`libfm-extra`
     - 30- :ref:`libxkbcommon`
     - 57- :ref:`lcms2`
   * - 4- :ref:`lxmenu-data`
     - 31- :ref:`libxkbui`
     - 58- :ref:`cups`
   * - 5- :ref:`lxde-common`
     - 32- :ref:`libxklavier`
     - 59- :ref:`gdbm`
   * - 6- :ref:`lxappearance`
     - 33- :ref:`libXpresent`
     - 60- :ref:`mpdecimal`
   * - 7- :ref:`lxinput`
     - 34- :ref:`libXres`
     - 61- :ref:`libgusb`
   * - 8- :ref:`lxrandr`
     - 35- :ref:`libxss`
     - 62- :ref:`libisl`
   * - 9-  :ref:`lxsession`
     - 36- :ref:`libXtst`
     - 63- :ref:`libmpc`
   * - 10- :ref:`lxpanel`
     - 37- :ref:`libXv`
     - 64- :ref:`duktape`
   * - 11- :ref:`lxtask`
     - 38- :ref:`libXvMC`
     - 65- :ref:`atkmm`
   * - 12- :ref:`lxterminal`
     - 39- :ref:`libXxf86dga`
     - 66- :ref:`at-spi2-core`
   * - 13- :ref:`pcmanfm`
     - 40- :ref:`libXxf86vm`
     - 67- :ref:`libtiff`
   * - 14- :ref:`lxlauncher`
     - 41- :ref:`tslib`
     - 68- :ref:`libepoxy`
   * - 15- :ref:`lxhotkey`
     - 42- :ref:`vte3`
     - 69- :ref:`gobject-introspection`
   * - 16- :ref:`lxde-icon-theme`
     - 43- :ref:`xapp`
     - 70- :ref:`p11-kit`
   * - 17- :ref:`libjpeg-turbo`
     - 44- :ref:`xcb-util-cursor`
     - 71- :ref:`nettle`
   * - 18- :ref:`cairo`
     - 45- :ref:`xcb-util-errors`
     - 72- :ref:`desktop-file-utils`
   * - 19- :ref:`gdk-pixbuf`
     - 46- :ref:`xcb-util-image`
     - 73- :ref:`libidn2` 
   * - 20- :ref:`gtksourceview4`
     - 47- :ref:`xcb-util-keysyms`
     - 74- :ref:`locale-tr`
   * - 21- :ref:`hsakmt`
     - 48- :ref:`xcb-util-renderutil`
     - 75- :ref:`hicolor-icon-theme`
   * - 22- :ref:`libFS`
     - 49- :ref:`xcb-util-wm`
     - 76- :ref:`polkit`
   * - 23- :ref:`libnotify`
     - 50- :ref:`xtrans`
     - 77- :ref:`libjpeg62`
   * - 24- :ref:`libvdpau`
     - 51- :ref:`libkeybinder3`
     - 78- :ref:`gpicview`
   * - 25- :ref:`libwnck3`
     - 52- :ref:`libexif`
     - 79- :ref:`libdmx`
   * - 26- :ref:`libXaw3d`
     - 53- :ref:`gtk3`
     - 80- 


**Bağımlılık Zinciri**
----------------------

**LXDE** paketleri **gtk3** ile derlenecek. Bunun için **libfm** paketinin **gtk3** ile derlenmeli ve sonra mevcut sistemimize kurmalıyız. Sistemimize kurulduktan sonra **LXDE** paketlerini **gtk3** ile  derlenmeli. Önemli detaylardan biriside **libfm**  ve menu-cache gibi alt bağımlılıkları da pcmanfm, lxpanel gibi bileşenlerden önce kurulmalıdır.


**Derleme Öncesi Hazırlık:** Paket derleme işlemine başlamadan önce, aşağıdaki temel araçları sisteminize kurmalısınız.

.. code-block:: bash

	sudo apt update
	sudo apt-get install debootstrap xorriso mtools make squashfs-tools gcc wget unzip xz-utils tar zstd fakeroot \
	autoconf automake autotools-dev make meson cmake ninja-build pkgconf patch libtool grub-pc grub-pc-bin
	
.. raw:: pdf

   PageBreak

