#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Linkedin Robson Vaamonde: https://www.linkedin.com/in/robson-vaamonde-0b029028/<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 23/09/2021<br>
#Data de atualização: 23/09/2021<br>
#Versão: 0.1<br>
#Testado e homologado no Raspberry Pi 3 B e LineageOS 17.1

#Instalação do LineageOS 17.1 no Raspberry Pi 3 B

#01_ Software para a gravação das Imagem do LineageOS no microSD Card<br>

	_ RPI-Manager: https://www.raspberrypi.org/software/
	_ Etcher: https://www.balena.io/etcher/

#02_ Download da Imagem do LineageOS 17.1 Raspberry Pi 3 B/B+
		
	_ Site (NÃO) oficial do LineageOS: https://konstakang.com/devices/rpi3/
	_ Suporte para as versões do Raspberry: Pi 3 B/B+
	_ Site (NÃO) oficial do LineageOS Recovery 2 Boot: https://androidfilehost.com/?fid=8889791610682901035
	_ Site do Open Google Apps: https://opengapps.org/

	_ Link para Hardware diferentes: https://konstakang.com/devices/

#03_ Limpando as Partições microSD Card

	_ Recomendado utilizar o Gerenciador de Unidade de Disco do Linux Mint (Menu, Discos)
	_ Limpar todas as partições antes de gravar a imagem do LineageOS 17.1 no microSD Card
	_ OBS1: utilizar sempre microSD Card >= 16GB Classe 10 (recomendado microSD >=64GB)

#04_ Gravando a imagem do LineageOS 17.1 no microSD Card

	_ Botão direito do mouse na imagem compactada: lineage-17.1-20201108-UNOFFICIAL-KonstaKANG-rpi3.zip
	_ Selecionar: Extrair aqui
	_ Botão direito do mouse na imagem descompactada: lineage-17.1-20201108-UNOFFICIAL-KonstaKANG-rpi3.img
	_ Selecionar: Abrir com, Gravador de Imagem de Disco
	_ Destino: Driver de 16GB/32GB - Generic SD/MMC/MS PRO (/dev/sdb) <Iniciar restauração>

#05_ Formatar um Pen Driver em FAT32 para copiar os arquivos do Google Apps

	_ OBSERVAÇÃO IMPORTANTE: Conforme documentado no site, o desenvolvedor não "RECOMENDA" fazer a instalação
	_ do Google Apps (gapps) no Raspberry Pi 3 devido a pouca memória que o mesmo possui, nesse cenário ele
	_ recomenda utilizar a versão Pi 4 com no mínimo 4GB de memória RAM
	_ Formatar um Pen Driver em FAT32 e copiar os arquivos:
	_ Primeiro: lineage-17.1-rpi-recovery2boot.zip (não precisa descompactar)
	_ Segundo: open_gapps-arm-10.0-tvstock-20200918.zip (não precisa descompactar)

#06_ Ligando o Raspberry Pi 3 B com o microSD Card do LineageOS 17.1
	
	_ OBS2: é recomendado ligar o LineageOS 17.1 conectado na e Rede Cabeada e com acesso a Internet
	_ OBS3: o primeiro boot do LineageOS 17.1 demora bastante pois será feito o reparticionamento do microSD
	_ OBS4: ligar o Raspberry Pi com o microSD Card do LineageOS e também o Pen Driver com o Google Apps

#07_ Configuração inicial do LineageOS 17.1

	_ Tela inicial do LineageOS: Next
	_ End User License Agreement (EULA): Accept
	_ Language: Português do Brasil: Próximo
	_ Data e hora: Brasília: Próximo
	_ Serviço de localização: Permitir: Próximo
	_ Recurso LineageOS: Ajude a melhorar o LineageOS: Próximo
	_ Projeta o seu tablet: Proteger este dispositivo (Configurar): Pular
	_ OBS5: o sistema será finalizado, algumas falhas de tela apareceu na versão do Pi3, depois que você clicar
	_ no botão: Iniciar o sistema funciona perfeitamente sem falhas.

#08_ Habilitando o modo Desenvolvedor do LineageOS

	_ Acessar: Configurações, na Barra de: Pesquisar em Configurações digite: Sobre o Tablet (About)
	_ Descer até a opção: Número da versão (Build), Clicar várias vezes para habilitar o Modo Desenvolvedor
	_ Voltar em: Configurações, Sistema, Avançado, Opções do Desenvolvedor
	_ Habilitar: Root Access <OK>
	_ Habilitar: Depuração Android <OK>
	_ Habilitar: Terminal Local <OK>
	_ Voltar em: Configurações, Apps e Notificações, Ver todos os 15 apps, Terminal <Abrir> <Permitir>
	_ Digite: su <Enter>, depois: rpi3-recevory.sh <Enter> depois: reboot <Enter>

#07_ Instalação do Google Apps TVStock no LineageOS 17.1

	_ Na tela do TWRP (Team Win Recovery Project) clique em: Swipe to Allow Modifications
	_ Na tela do Modifications clique em: Install
	_ Na tela do Install clique em: Select Storage
	_ Na tela do Select Storage selecione em: USB (16GB) <OK>