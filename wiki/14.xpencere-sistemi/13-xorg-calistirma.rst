**LXDE'yi xinit veya startx'le Çalıştırma**
--------------------------------------------

**xinit ve startx** X Pencere Sistemi'ni başlatmak için kullanılan komutlardır. ``xinit`` ve ``startx``, X sunucusunu kullanıcı girişinden sonra manuel olarak başlatmak için kullanılır.

**xinit** X sunucusunu başlatır ve ardından belirtilen tek bir uygulamayı çalıştırır. **startx** ``xinit`` için bir kabuk (wrapper) komutudur. ``~/.xinitrc`` betiğini çalıştırır, yoksa sistem varsayılanını kullanır.

Eğer belirli bir pencere yöneticisi veya masaüstü ortamı ile başlatmak istiyorsanız, ~/.xinitrc dosyasını düzenlemeniz gerekebilir. Dosyanın içeriği şöyle olmalıdır:

**openbox Masaüstü Ortamını Kullanma**
--------------------------------------

.. code-block:: shell

	exec openbox-session

**lxde Masaüstü Ortamını Kullanma**
--------------------------------------

.. code-block:: shell

	exec lxsession



.. code-block:: shell
	
		#startx
		# veya
		xinit
		
**Xorg'u Durdurma**
-------------------

Xorg'u durdurmak için, terminalde Ctrl + Alt + Backspace tuş kombinasyonunu kullanabilirsiniz. Bu, X sunucusunu kapatacaktır.



