# provisionamento-servidor-web


#!/bin/bash

# Atualizar pacotes
sudo apt update -y

# Instalar o Apache2
sudo apt install apache2 -y

# Iniciar o serviço do Apache
sudo systemctl start apache2

# Habilitar o Apache para iniciar no boot
sudo systemctl enable apache2

# Criar uma página HTML de teste
echo "<html><body><h1>Servidor Apache Provisionado com Sucesso!</h1></body></html>" | sudo tee /var/www/html/index.html

# Verificar o status do Apache
sudo systemctl status apache2
