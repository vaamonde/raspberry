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
#Data de atualização: 23/09/2021<br>
#Versão: 0.3<br>
#Testado e homologado no Raspberry Pi 3 B e Batocera 31

#Changelog do Batocera: https://batocera.org/changelog

#Instalação do Batocera 31 (18/06/2021) Raspberry Pi 3 B

#01_ Software para a gravação das Imagem do Batocera no microSD Card<br>

	_ RPI-Manager: https://www.raspberrypi.org/software/

#02_ Download da Imagem do Batocera 31 Raspberry Pi 3 B/B+
		
	_ https://batocera.org/download
	_ Suporte para as versões do Raspberry: Pi 3 B/B+
	_ Manual de configuração do Batocera: https://wiki.batocera.org/
	_ Screen Scraper (informações das ROMS): https://www.screenscraper.fr/

	_ Download Full-Pack BIOS Batocera V31: http://theminicaketv.free.fr/PACK-BIOS-BATOCERA.htm
	_ Download RetroPie Image: https://www.arcadepunks.com/pi-images-downloads-page/

	_ Alternativas de Distribuições Retrô Games
	_ RetroPie: https://retropie.org.uk/
	_ Recalbox: https://www.recalbox.com/pt-br/
	_ RetroArch: https://www.retroarch.com/
	_ Lakka: https://www.lakka.tv/
	_ RetroBat: https://www.retrobat.ovh/

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
	
	_ OBS2: é recomendado ligar o Batocera 31 conectado com o Joystick ou Teclado e Rede
	_ OBS3: no primeiro boot o sistema irá executar o redimensionamento das partições
	_ OBS4: no Batocera 31 os controles/joystick são reconhecidos automaticamente

#06_ Configurações básicas do Batocera 31

	_ OBS5: por padrão do Batocera vem configurado na linguagem Americano/Inglês
	_ Alterar a linguagem: Start (Menu), System Settings, Language: Portugues Brasileiro
	_ Reinicialização necessária para aplicar as mudanças: Start (Menu), Quit, Reboot System: Yes
	_ Atualizando a lista de jogos: Start (Menu), Opções de Jogos, Atualizar Lista de Jogos, Sim
	_ Para sair de um jogo pressiona: Start + Select

#07_ Partições do Batocera 31

	_ Partição BATOCERA: sistema de boot e arquivos de inicialização/binários do Batocera
	_ Partição SHARE: localização das ROMS (jogos), BIOS (PS2/PS3, etc...), Musicas, Temas, etc...
	_ Na partição SHARE no diretório: roms e onde fica localizado todos os diretórios dos
	_ consoles que o Batocera tem suporte, cada diretório tem um nome correspondente ao
	_ seu console, exemplo: snes = Super Nintendo, psx = Playstation, n64 = Nintendo 64
	_ OBS6: para copiar arquivos para a partição SHARE no Linux Mint e necessário acessar
	_ como Root a partição (Botão direito do mouse na partição/diretório Abrir como root)