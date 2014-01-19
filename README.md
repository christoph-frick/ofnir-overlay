Gentoo overlay
==============

Content
-------

 - SFML 2.1

Add locally to layman
---------------------

Create local source config ``/var/lib/layman/ofnir-overlay.xml``:

	<?xml version="1.0" ?>
	<layman>
		<overlay
			name="ofnir"
			contact="cf@ofnir.net"
			src  = "git://github.com/christoph-frick/ofnir-overlay.git"
			type = "git">
			<link>
				https://github.com/christoph-frick/ofnir-overlay
			</link>
			<description>
				Ofnirs private Gentoo Overlay
			</description>
		</overlay>
	</layman>

Add to layman ``/etc/layman/layman.cfg``:

    overlays  : http://www.gentoo.org/proj/en/overlays/repositories.xml 
                file:///var/lib/layman/ofnir-overlay.xml
	

