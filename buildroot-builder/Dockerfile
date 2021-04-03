FROM centos:8

RUN dnf install -y epel-release dnf-plugins-core && dnf update -y && dnf config-manager --set-enabled powertools -y && dnf makecache -y && dnf install gzip bzip2 xz zstd patch findutils diffutils libtool which file cpp gcc gcc-c++ glibc-devel make bc cmake cpio cvs git mercurial python3 python3-flake8 python3-nose2 python3-pexpect rsync subversion unzip wget ncurses-devel perl-ExtUtils-MakeMaker -y && dnf clean packages

CMD groupadd -g ${GID} buildroot-builder && adduser -g buildroot-builder -u ${UID} buildroot-builder && su - buildroot-builder
