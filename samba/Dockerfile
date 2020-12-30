FROM ubuntu
RUN apt-get update -y
RUN apt install -fy samba
RUN useradd -m -d /mnt/share meu
RUN echo meu:meu | chpasswd
RUN printf 'meu\nmeu\n' | pdbedit -a meu -t
COPY ./smb.conf /etc/samba/smb.conf