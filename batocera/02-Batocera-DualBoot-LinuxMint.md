#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Linkedin Robson Vaamonde: https://www.linkedin.com/in/robson-vaamonde-0b029028/<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 26/09/2021<br>
#Data de atualização: 26/09/2021<br>
#Versão: 0.1<br>
#Testado e homologado no Linux Mint 20.2 Uma e Batocera v31

#Site Oficial do Batocera: https://batocera.org/<br>
#Changelog do Batocera: https://batocera.org/changelog<br>
#Site Oficial do Linux Mint: https://www.linuxmint.com/<br>
#Changelog do Linux Mint 20.2 Uma: https://linuxmint.com/rel_uma_cinnamon.php<br>
#Manual de configuração do Batocera: https://wiki.batocera.org/<br>
#Controles/Joystick Suportados: https://wiki.batocera.org/supported_controllers<br>
#Screen Scraper (informações das ROMS): https://www.screenscraper.fr/<br>
#Download Full-Pack BIOS Batocera V31: http://theminicaketv.free.fr/PACK-BIOS-BATOCERA.htm<br>
#Download RetroPie Image: https://www.arcadepunks.com/pi-images-downloads-page/

#Alternativas de Distribuições Retrô Games<br>
#RetroPie: https://retropie.org.uk/<br>
#Recalbox: https://www.recalbox.com/pt-br/<br>
#RetroArch: https://www.retroarch.com/<br>
#Lakka: https://www.lakka.tv/<br>
RetroBat: https://www.retrobat.ovh/

#Indicação de Joystick com Review do Professor Ramos (https://www.youtube.com/professorramos)<br>
#Joystick GameSir G4s PT-BR 🎮 Gamepad Bluetooth - 2.4G Wi-Fi - USB 🌟Análise - Review: https://www.youtube.com/watch?v=NejpVhA45xQ<br>
#Joystick para celular Android e PC Windows e Linux !!! Gamepad iPega 9099 Wolverine: https://www.youtube.com/watch?v=MIf5Q_R1vEI<br>
#Agora eu vou dar Hadouken !!! Joystick Arcade iPega PG-9059 Fight | PC | Nintendo Switch | PS3 e 4: https://www.youtube.com/watch?v=OnaDImXmWz8

#Instalação do Batocera v31 (18/06/2021) em Dual Boot com o Linux Mint 20.2 Uma (Desktop ou Notebook)

#01_ Reparticionamento do Linux Mint utilizando o Gparted

	_ Para reparticionar o Linux Mint é necessário utilizar um Pen Driver do Mint com o sistema desmontado
	_ Utilizar o software Gparted do Live do Mint para reparticionar o HD e criar as partições do Batocera
	_ Partição 1: Tipo (type) = fat32, Nome (name) = BATOCERA, Tamanho mínimo de 5GB (recomendado 10GB)
	_ Partição 2: Tipo (type) = ext4, Nome (name) = SHARE, deve ser criada logo após a partição BATOCERA.

#02_ Criação das Partições do Batocera Linux

#03_ Instalação do Batocera Linux na partição Batocera

#04_ Configuração do Grub para suportar o Dual Boot do Batocera Linux

#05_ Ligando o Linux Mint 20.2 com o Batocera Linux v31 em Dual Boot
	
	_ OBS1: 
	_ OBS2: é recomendado ligar o Batocera 31 conectado com o Joystick ou Teclado e Rede Cabeada
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
	_ seu console, exemplo: snes = Super Nintendo, psx = Playstation, n64 = Nintendo 64, etc...
	_ OBS6: para copiar arquivos para a partição SHARE no Linux Mint e necessário acessar
	_ como Root a partição (Botão direito do mouse na partição/diretório Abrir como root)