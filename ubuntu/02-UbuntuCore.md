#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Linkedin Robson Vaamonde: https://www.linkedin.com/in/robson-vaamonde-0b029028/<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 24/08/2021<br>
#Data de atualização: 24/08/2021<br>
#Versão: 0.1<br>
#Testado e homologado no Raspberry Pi 3 B e Ubuntu Core 20 ARM x64 Bits

#Instalação do Ubuntu Core 20 ARM x64 Bits

#01_ Software para a gravação das imagens no microSD Card<br>

	_ RPI-Manager: https://www.raspberrypi.org/software/

#02_ Download da Imagem do Ubuntu Core 20 ARM x64 Bits
	
	_ Informações sobre o Ubuntu Core: https://ubuntu.com/core
	_ Link para download: https://cdimage.ubuntu.com/ubuntu-core/20/stable/current/
	_ Suporte para as versões do Raspberry: Pi3, Pi4, Pi400 e PiCM4

#03_ Limpando as Partições microSD Card

	_ Recomendado utilizar o Gerenciador de Unidade de Disco do Linux Mint (Menu, Discos)
	_ Limpar todas as partições antes de gravar a imagem do Ubuntu Core no microSD Card
	_ OBS1: utilizar sempre microSD Card >= 16GB Classe 10

#04_ Gravando a imagem do Ubuntu Core 20 ARM x64 Bits no SD Card

	_ Botão direito do mouse na imagem: ubuntu-core-20-arm64+raspi.img.xz
	_ Selecionar: Abrir com o Gravador de imagem de disco
	_ Destino: Driver de 16GB/32GB - Generic SD/MMC/MS PRO (/dev/sdb) <Iniciar restauração>

#05_ Criando sua conta no Ubuntu One

	_ Ubuntu One: https://login.ubuntu.com/

#06_ Criando o Par de Chaves SSH para autenticação no Ubuntu Core 20 ARM x64 Bits

	_ Criando a chave pública: ssh-keygen -t rsa
	_ Visualizando o conteúdo da chave pública: cat ~/.ssh/id_rsa.pub

#07_ Copiando o conteúdo da Chave Pública no Ubuntu One

	_ Ubuntu One SSH Key: https://login.ubuntu.com/ssh-keys
	_ Copiar a colar os valores da chave pública no campo: Import new SSH key <Import SSH Key>

#08_ Ligando o Raspberry Pi 3 B com o microSD Card do Ubuntu Core 20 ARM x64 Bits

	_ Observação: No primeiro boot do Ubuntu Core o processo demora um pouco, devido ao 
	_ reparticionamento do microSD e a instalação e configuração dos serviços base da 
	_ distribuição, após essa configuração o sistema será reinicializado.

#09_ Configurando o Ubuntu Core 20 ARM x64 Bits

	_ Após a inicialização do Ubuntu Core, será solicitado para você fazer as configurações do sistema;
	_	Press enter to configure <Enter>
	_	Configure the network and setup an administrator account on this all-snap Ubuntu Core system. <OK>
	_	Configure at least one interfaces this server can use to talk to other machines, and which
	_	preferably provides sufficient access for updates. <Done>
	_	Enter an email address from your account in the store. <Done>
	_ 	This device is registered to: seuemail@seudominio.com. <Done>

#10_ Acessando remotamente o Ubuntu Core 20 ARM x64 Bits

	_ Terminal: ssh seuusuarioubuntuone@endereço_ipv4_ubuntu_core