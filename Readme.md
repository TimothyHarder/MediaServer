Installation notes:

For Rocky 8:

$ sudo dnf install -y tar bzip2 make automake gcc gcc-c++ pciutils elfutils-libelf-devel libglvnd-devel

$ sudo dnf config-manager --set-enabled crb

$ sudo dnf install -y epel-release
$ distribution=rhel8

$ sudo dnf config-manager --add-repo http://developer.download.nvidia.com/compute/cuda/repos/$distribution/x86_64/cuda-$distribution.repo
$ sudo dnf install -y kernel-devel-$(uname -r) kernel-headers-$(uname -r)
$ sudo dnf module install nvidia-driver:latest-dkms
$ sudo dnf clean all
$ sudo dnf -y module install nvidia-driver:latest-dkms