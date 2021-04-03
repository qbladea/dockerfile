FROM centos:8

RUN dnf install -y epel-release dnf-plugins-core && dnf update -y && dnf config-manager --set-enabled powertools -y && dnf makecache -y && dnf install gawk make wget tar bzip2 gzip python2 python3 unzip perl patch diffutils diffstat git cpp gcc gcc-c++ glibc-devel texinfo chrpath ccache socat perl-Data-Dumper perl-Text-ParseWords perl-Thread-Queue python3-pip python3-GitPython python3-jinja2 python3-pexpect xz which SDL-devel xterm rpcgen mesa-libGL-devel -y && dnf install make python3-pip which -y && pip3 install -i https://pypi.tuna.tsinghua.edu.cn/simple sphinx sphinx_rtd_theme pyyaml && dnf clean packages

CMD groupadd -g ${GID} yocto-builder && adduser -g yocto-builder -u ${UID} yocto-builder && su - yocto-builder
