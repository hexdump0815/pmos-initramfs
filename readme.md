# pmos-initramfs

this imports the initramfs and initramfs-extra files built from the pmos
pmaports to use them as a base for building own bootable kernels
    
special initramfs files are required for older android devices which do not
have enough space in the boot partition for a kernel plus a regular
debian/ubuntu initrd - postmarketos solved that problem very nicely by building
a small enough initramfs for the boot.img which then loads an initramfs-extra
from the boot partition
    
the proper way to deal with this here would be to make use of
https://gitlab.com/postmarketOS/postmarketos-mkinitfs to build them natively on
debian, but as an easier starting point for now some build initramfs images
from pmos are used and adjusted for an own kernel build (i.e. the kernel
modules in the pmos initramfs images will be replaced with the self built ones)

