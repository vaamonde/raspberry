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
#Data de atualização: 27/09/2021<br>
#Versão: 0.2<br>
#Testado e homologado no Linux Mint 20.2 Uma e Batocera v31

#Site Oficial do Linux Mint: https://www.linuxmint.com/<br>
#Site Oficial do Batocera: https://batocera.org/<br>
#Changelog do Batocera: https://batocera.org/changelog<br>
#Site Oficial do Linux Mint: https://www.linuxmint.com/<br>
#Changelog do Linux Mint 20.2 Uma: https://linuxmint.com/rel_uma_cinnamon.php<br>
#Manual de configuração do Batocera: https://wiki.batocera.org/<br>
#Controles/Joystick Suportados: https://wiki.batocera.org/supported_controllers<br>
#Screen Scraper (informações das ROMS): https://www.screenscraper.fr/<br>
#Download Full-Pack BIOS Batocera V31: http://theminicaketv.free.fr/PACK-BIOS-BATOCERA.htm<br>
#Download BIOS Batocera V310: https://archive.org/details/complete-bios-collection-batocera-30<br>
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

	_ Bootar o sistema com o Pen Driver do Linux Mint 20.2 Uma
	_ Executar o aplicativo Gparted: Menu, Share, Gparted
	_ Nesse exemplo estou utilizando um Hard Disk NVMe de 512GB em: /dev/nvme0 (476,94GB)
	_ Botão direito na partição: /dev/nvme0n1p5, selecionar: Resize/Mode
	_ Diminuir a partição para: 256GB (256621MB) - <Resize/Move>
	_ No espaço não alocado (unallocated), clicar com o botão direito na partição e selecionar: New
	_ Criar uma partição de: 10GB (10825MB), File system: Fat32, Label: BATOCERA <Add>
	_ No espaço não alocado (unallocated), clicar com o botão direito na partição e selecionar: New
	_ Criar uma partição de: Total do Disco (130424), File system: Ext4, Label: SHARE <Add>
	_ Clicar na opção: Apply All Operations, <Apply> (esse processo demora um pouco) <Close>

#03_ Instalação do Batocera Linux na partição Batocera

	_ Verificando as partições criadas: Menu, Pesquisa, Disco
	_ Download do arquivo: boot.tar.xz, descompactá-lo e mover todo os arquivo para a partição BATOCERA
	_ Link do download: http://batocera.org/upgrades/x86_64/stable/last/boot.tar.xz
	_ Botão direito no arquivo: boot.tar.xz, selecionar: Extrair Aqui
	_ Acessar o diretório boot, copiar/colar todos os arquivos na raiz da partição BATOCERA
	_ OBS1: não é necessário configurar a partição SHARE, ela será configurada automaticamente
	_ no primeiro Boot do Batocera

#04_ Configuração do Grub para suportar o Dual Boot do Batocera Linux

	_ Fazer o download do projeto do Github: https://github.com/vaamonde/raspberry
	_ Descompactar a pasta do download do projeto do Github
	_ Abrir a pasta: raspberry-man/batocera como Root: Botão direito do Mouse, Abrir como Root
	_ Copiar o arquivo: 15_batocera para: /​etc/​grub.d/​15_batocera
	_ Acessar o Terminal e digitar os comandos:
	_	sudo chmod a+x /​etc/​grub.d/​15_batocera <Enter>
	_	sudo vim /etc/default/grub
	_		GRUB_TIMEOUT_STYLE=menu
	_		GRUB_TIMEOUT=10
	_	sudo update-grub <Enter>

#05_ Ligando o Linux Mint 20.2 com o Batocera Linux v31 em Dual Boot
	
	_ OBS2: é recomendado ligar o Batocera 31 conectado com Teclado, Joystick e Rede Cabeada
	_ OBS3: no primeiro boot o sistema irá executar a configuração das partições
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