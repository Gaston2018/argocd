# argocd
Instalación ArgoCD

# Basado en el siguiente tutorial
https://www-fosstechnix-com.translate.goog/how-to-install-argocd-on-minikube/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc

# Instalar minikube

sudo apt update -y

# Instalar los paquetes para Minikube
sudo apt install curl wget apt-transport-https -y

# Instalar docker
sudo apt install docker.io

# Configurar para ejecutar Docker sin permiso de sudo
sudo usermod -aG docker $USER
sudo chmod 666 /var/run/docker.sock

# Para comprobar si el soporte de virtualización está habilitado en su máquina o no
egrep -q 'vmx|svm' /proc/cpuinfo && echo yes || echo no

# Para descargar la última configuración de Minikube, consulte la página de descarga oficial de Minikube.
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

# Instale Minikube en Ubuntu 22.04 LTS
sudo install minikube-linux-amd64 /usr/local/bin/minikube

# Para comprobar la versión de minikube en Ubuntu
minikube version

# Descargue el binario de kubectl con curl en Ubuntu usando el siguiente comando
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

# Hacer que el binario de kubectl sea ejecutable
chmod +x ./kubectl
sudo mv kubectl /usr/local/bin/
versión de kubectl --client --output=yaml
