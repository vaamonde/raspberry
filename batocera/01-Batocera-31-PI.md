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
#Data de atualização: 10/10/2021<br>
#Versão: 0.6<br>
#Testado e homologado no Raspberry Pi 3 B e Batocera v31

#Site Oficial do Batocera: https://batocera.org/<br>
#Changelog do Batocera: https://batocera.org/changelog<br>
#Manual de configuração do Batocera: https://wiki.batocera.org/<br>
#Controles/Joystick Suportados: https://wiki.batocera.org/supported_controllers<br>
#Screen Scraper (informações das ROMS): https://www.screenscraper.fr/<br>
#Download Full-Pack BIOS Batocera v31: http://theminicaketv.free.fr/PACK-BIOS-BATOCERA.htm<br>
#Download BIOS Batocera v30: https://archive.org/details/complete-bios-collection-batocera-30<br>
#Download BIOS Batocera v31: https://archive.org/details/bios-batocera-v-31<br>
#Download RetroPie Image: https://www.arcadepunks.com/pi-images-downloads-page/<br>
#Mirror Batocera Old Version: https://mirrors.o2switch.fr/batocera/rpi3/stable/last/archives/

#Alternativas de Distribuições Retrô Games<br>
#RetroPie: https://retropie.org.uk/<br>
#Recalbox: https://www.recalbox.com/pt-br/<br>
#RetroArch: https://www.retroarch.com/<br>
#Lakka: https://www.lakka.tv/<br>
#RetroBat: https://www.retrobat.ovh/

#Indicação de Joystick com Review do Professor Ramos (https://www.youtube.com/professorramos)<br>
#Joystick GameSir G4s PT-BR 🎮 Gamepad Bluetooth - 2.4G Wi-Fi - USB 🌟Análise - Review: https://www.youtube.com/watch?v=NejpVhA45xQ<br>
#Joystick para celular Android e PC Windows e Linux !!! Gamepad iPega 9099 Wolverine: https://www.youtube.com/watch?v=MIf5Q_R1vEI<br>
#Agora eu vou dar Hadouken !!! Joystick Arcade iPega PG-9059 Fight | PC | Nintendo Switch | PS3 e 4: https://www.youtube.com/watch?v=OnaDImXmWz8

#Instalação do Batocera v31 (18/06/2021) Raspberry Pi 3 B

#01_ Software para a gravação das Imagem do Batocera no microSD Card<br>

	_ RPI-Manager: https://www.raspberrypi.org/software/

#02_ Download da Imagem do Batocera v31 Raspberry Pi 3 B/B+
		
	_ Site oficial do Batocera: https://batocera.org/download
	_ Suporte para as versões do Raspberry: Pi 3 B/B+

#03_ Limpando as Partições microSD Card

	_ Recomendado utilizar o Gerenciador de Unidade de Disco do Linux Mint (Menu, Discos)
	_ Limpar todas as partições antes de gravar a imagem do Batocera v31 no microSD Card
	_ OBS1: utilizar sempre microSD Card >= 32GB Classe 10 (recomendado microSD >=64GB)

#04_ Gravando a imagem do Batocera v31 no microSD Card

	_ Botão direito do mouse na imagem compactada: batocera-rpi3-31-20210615.img.gz
	_ Selecionar: Extrair aqui
	_ Botão direito do mouse na imagem descompactada: batocera-rpi3-31-20210615.img
	_ Selecionar: Abrir com, Gravador de Imagem de Disco
	_ Destino: Driver de 16GB/32GB - Generic SD/MMC/MS PRO (/dev/sdb) <Iniciar restauração>

#05_ Ligando o Raspberry Pi 3 B com o microSD Card do Batocera v31
	
	_ OBS2: é recomendado ligar o Batocera v31 conectado com o Joystick ou Teclado e Rede Cabeada
	_ OBS3: no primeiro boot o sistema irá executar o redimensionamento das partições
	_ OBS4: no Batocera v31 os controles/joystick são reconhecidos automaticamente

#06_ Configurações básicas do Batocera v31

	_ OBS5: por padrão o Batocera v31 vem configurado na linguagem Americano/Inglês
	_ Alterar a linguagem: Start (Menu), System Settings, Language: Portugues Brasileiro
	_ OBS6: na versão v32 do Batocera não é necessário reinicializar o sistema
	_ Atualizando a lista de jogos: Start (Menu), Opções de Jogos, Atualizar Lista de Jogos, Sim
	_ Para sair de um jogo pressiona: Start + Select

#07_ Partições do Batocera v31

	_ Partição BATOCERA: sistema de boot e arquivos de inicialização/binários do Batocera
	_ Partição SHARE: localização das ROMS (jogos), BIOS (PS2/PS3, etc...), Músicas, Temas, etc...
	_ Na partição SHARE no diretório: roms e onde fica localizado todos os diretórios dos
	_ consoles que o Batocera tem suporte, cada diretório tem um nome correspondente ao
	_ seu console, exemplo: snes = Super Nintendo, psx = Playstation, n64 = Nintendo 64, etc...
	_ OBS8: para copiar arquivos para a partição SHARE no Linux Mint é necessário acessar
	_ como Root a partição (Botão direito do mouse na partição/diretório Abrir como root)

#08_ Dicas de configurações dos emuladores

	_ Nintendo 64: emulador que funciona perfeitamente os jogos: LIBRETRO / PARALLEL N64
	_	Acessar Nintendo 64, Opções (Select), Opções Avançadas do Sistema, Emulador: LIBRETRO / PARALLEL N64
	_ Playstation 2: configuração do recurso de Speedhacks do PCX2-CONFIG
	_	Acessar o Menu de Jogos, F1 (Arquivos), Aplicativos, pcsx2-config
	_	Config, Video (GS), Core GS Settings, Speedhacks
	_		Enable speedhacks: ON
	_		EE Cyclerate [Not Recommended]: 3
	_		EE Cycle Skipping [Not Recommended]: 3
	_		Enable INTC Spin Detection: ON
	_		Enable Wait Loop Detection: ON
	_		Enable fast CDVD: ON
	_		mVU Flag Hack: ON
	_		MTUV (Multi-Threaded microVU1): ON
	_	System, Exit
	_ Atualização das informações das ROMS (Screen Scraper): fazer o cadastro no site: https://www.screenscraper.fr/
	_	Acessar o Menu de Jogos, Menu (Start), Scrape
	_		Banco de Dados: Screenscraper
	_		Fonte da Imagem: Screenshot
	_		Fonte da Caixa: Caixa 2D
	_		Fonte do Logotipo: Logotipo
	_		Obter Avaliações: ON
	_		Obter Vídeos: ON
	_		Obter Fanart: ON
	_		Obter parte de trás da Caixa: ON
	_		Obter Mapa: ON
	_		Obter Manual: ON
	_		Obter Configuração do Controle e Teclado: ON
	_		Usuário: usuário_screenscraper
	_		Senha: senha_screenscraper
	_	Iniciar Procura
	_		Filtro: Apenas Mídias Ausentes
	_		Sistema: Número de Intens Selecionados
	_	Iniciar (Aguardar esse processo demora dependendo da quantidade de jogos para obter as informações)
	_	Voltar, Opções de Jogos, Atualizar Listas de Jogos, Sim 