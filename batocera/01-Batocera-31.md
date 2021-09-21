#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Linkedin Robson Vaamonde: https://www.linkedin.com/in/robson-vaamonde-0b029028/<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 17/09/2021<br>
#Data de atualização: 17/09/2021<br>
#Versão: 0.1<br>
#Testado e homologado no Raspberry Pi 3 B e Batocera 31

#Changelog do Batocera: https://batocera.org/changelog

#Instalação do Batocera 31 (18/06/2021) Raspberry Pi 3 B

#01_ Software para a gravação das imagens no microSD Card<br>

	_ RPI-Manager: https://www.raspberrypi.org/software/

#02_ Download da Imagem do Batocera 31 Raspberry Pi 3 B/B+
		
	_ https://batocera.org/download
	_ Suporte para as versões do Raspberry: Pi 3 B/B+

#03_ Limpando as Partições microSD Card

	_ Recomendado utilizar o Gerenciador de Unidade de Disco do Linux Mint (Menu, Discos)
	_ Limpar todas as partições antes de gravar a imagem do Batocera 31 no microSD Card
	_ OBS1: utilizar sempre microSD Card >= 16GB Classe 10 (recomendado microSD >=64GB)

#04_ Gravando a imagem do Batocera 31 no microSD Card

	_ Botão direito do mouse na imagem compactada: batocera-rpi3-31-20210615.img.gz
	_ Selecionar: Extrair aqui
	_ Botão direito do mouse na imagem descompactada: batocera-rpi3-31-20210615.img
	_ Selecionar: Abrir com, Gravador de Imagem de Disco
	_ Destino: Driver de 16GB/32GB - Generic SD/MMC/MS PRO (/dev/sdb) <Iniciar restauração>

#05_ Ligando o Raspberry Pi 3 B com o microSD Card do Batocera 31
	
	_ OBS1: é recomendado ligar o Batocera 31 conectado com o Joystick ou Teclado e Rede
	_ 