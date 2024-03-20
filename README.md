QEMU SPOOF KVM HANDLER UPDATED
RDTSC
Updated for 6.5 KERNEL

Steps:
git clone https://github.com/torvalds/linux.git
cd linux
git checkout v6.5

download & replace
arch/x86/kvm/vmx/vmx.c
arch/x86/kvm/vmx/vmx.h

compile

sudo apt-get install build-essential libncurses-dev bison flex libssl-dev libelf-dev

cp -v /boot/config-$(uname -r) .config
make -j $(nproc)

sudo make INSTALL_MOD_STRIP=1 modules_install && sudo make install

Check if a new kernel was installed

uname -a

