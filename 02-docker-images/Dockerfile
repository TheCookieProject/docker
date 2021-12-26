FROM rockylinux:8.5

# Actualizar el OS e instalar paquetes necesarios
RUN yum update -y
RUN yum install -y epel-release
RUN yum install -y bash-completion htop neovim net-tools python39 screen strace telnet unzip vim-enhanced wget yum-utils

# Enchular la terminal
RUN cd /tmp/ && wget -c https://github.com/ogham/exa/releases/download/v0.10.0/exa-linux-x86_64-v0.10.0.zip
RUN cd /tmp/ && unzip exa-linux-x86_64-v0.10.0.zip
RUN cd /tmp/ && cp bin/exa /usr/bin/
RUN echo "alias ll='exa -al --color=always --group-directories-first'" >> /root/.bashrc
RUN echo "alias up='source /opt/venv/bin/activate'" >> /root/.bashrc
RUN echo "alias v='nvim'" >> /root/.bashrc

# Instalar las librerías necesarias de Python
RUN python3.9 -m venv /opt/venv
RUN /opt/venv/bin/python -m pip install --upgrade pip

# Limpiar el contenedor
RUN yum clean all