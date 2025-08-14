.. _polkit:
**polkit**
==========

Polkit, Linux ve diğer Unix tabanlı sistemlerde, yönetici yetkisi gerektiren işlemleri güvenli bir şekilde yetkilendirmek için kullanılan bir araçtır. Kullanıcılar, sistemdeki kritik işlemleri gerçekleştirirken Polkit sayesinde yalnızca gerekli izinlere sahip olduklarında işlem yapabilir. Bu, hem güvenliği arttırır hem de sistem yöneticilerine daha ayrıntılı izin yönetimi sunar.

**Paketi Derleme :**
--------------------

.. code-block:: bash

	#!/usr/bin/env bash
	name="polkit"
	version="123"
	url="https://gitlab.freedesktop.org/polkit/polkit"
	description="Application development toolkit for controlling system-wide privileges"
	source="https://gitlab.freedesktop.org/polkit/polkit/-/archive/$version/polkit-$version.tar.gz"
	depends="duktape,expat,glib,pam,elogind"
	builddepend="gobject-introspection,gtk-doc,meson"
	group="sys.auth"

	setup(){
	cp -prfv $PACKAGEDIR/files /tmp/kly/build/
	cd $SOURCEDIR

		meson setup $BUILDDIR --prefix=/usr \
		    --libdir=/usr/lib64/ \
		    -Db_lto=true \
		    -Dsession_tracking="libelogind" \
		    -Dsystemdsystemunitdir=/trash \
			-Dpam_prefix=/etc/pam.d \
			-Dpolkitd_user=polkitd

	}

	build(){
		ninja -C $BUILDDIR $jobs
	}

	package(){
		DESTDIR=$DESTDIR ninja -C $BUILDDIR install $jobs
		DESTDIR="$BUILDDIR/elogind/dest" meson install --no-rebuild -C elogind
		
		chown -R polkitd:polkitd $DESTDIR/etc/polkit-1/rules.d $DESTDIR/usr/share/polkit-1/rules.d
		chmod -R 700 $DESTDIR/etc/polkit-1/rules.d $DESTDIR/usr/share/polkit-1/rules.d
		chmod 4755 $DESTDIR/usr/lib/polkit-1/polkit-agent-helper-1
		chmod 4755 $DESTDIR/usr/bin/pkexec

		rm -rf $DESTDIR/garbage
		install -d $DESTDIR/etc/init.d

		install -Dm755 ../files/polkit.initd $DESTDIR/etc/init.d/polkit
		mkdir -p $DESTDIR/var
		mkdir -p $DESTDIR/var/empty
	}

 
.. raw:: pdf

   PageBreak
