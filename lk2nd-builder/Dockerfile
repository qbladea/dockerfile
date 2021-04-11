FROM archlinux:latest

RUN echo 'Server = https://mirrors.sjtug.sjtu.edu.cn/archlinux/$repo/os/$arch' > /etc/pacman.d/mirrorlist
RUN pacman -Syy --noconfirm && pacman -Syu --noconfirm && pacman -S arm-none-eabi-gcc make dtc python3 tmux vim --noconfirm

CMD groupadd -g ${GID} lk2nd-builder && useradd -g lk2nd-builder -u ${UID} lk2nd-builder && su - lk2nd-builder
