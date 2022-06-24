# thinkpad-t23-gentoo-s3-savage-x11
Gentoo layer with custom patches to run x11 with gpu acceleration on S3 SuperSavage (IBM ThinkPad T23).

My layer from may 2020, where i tried to run x11 with gpu acceleration on my super old Thinkpad. Spoiler: it works, but it looks more like Jenga, then real working pc.

S3 SuperSavage is a super old gpu, so it requers specific versions of soft and other setups:
- X11 - 1.12.4
- Mesa - 7.11.2
- xf86-video-savage - any probably...
- gentoo2011 layer
- gentoo-x86 layer
- stage3-i686-20140826 (not this specific version, but i used this one)
- linux 4.0.5 (kernel config `CONFIG_DRM_SAVAGE=y`. Also you can find my kernel config in this repo)

glxgears shows about 200 fps on small (around 200px\*300px) window.

This layer *DONT* really work out of the box. It contains some patches and updated EBUILDs, but you have to manualy find all missing ebuilds and sources that needed for X11 and Mesa dependencies.
