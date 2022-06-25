# thinkpad-t23-gentoo-s3-savage-x11
This is my personal portage layer from may 2020, where i tried to run X11 with gpu acceleration on my super old Thinkpad which has odd S3 SuperSavage gpu. Spoiler: it works (glxgears shows about 200 fps on small (around 200px\*300px) window), but it looks more like Jenga, then real working pc.

S3 SuperSavage is a super old gpu, so it requers specific versions of soft and other setups:
- X11 - 1.12.4
- Mesa - 7.11.2
- xf86-video-savage - any probably...
- gentoo2011 layer
- gentoo-x86 layer
- stage3-i686-20140826 (not this specific version, but i used this one)
- linux 4.0.5 (kernel config `CONFIG_DRM_SAVAGE=y`. Also you can find my kernel config in this repo)

This layer **DONT** really work out of the box. It contains some patches and updated EBUILDs, but you have to manualy find all missing ebuilds and sources that needed for X11 and Mesa dependencies.
