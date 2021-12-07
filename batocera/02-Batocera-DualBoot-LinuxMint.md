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
#Data de atualização: 07/12/2021<br>
#Versão: 0.10<br>
#Testado e homologado no Linux Mint 20.2 Uma e Batocera v32

#Site Oficial do Linux Mint: https://www.linuxmint.com/<br>
#Site Oficial do Batocera: https://batocera.org/<br>
#Changelog do Batocera: https://batocera.org/changelog<br>
#Site Oficial do Linux Mint: https://www.linuxmint.com/<br>
#Changelog do Linux Mint 20.2 Uma: https://linuxmint.com/rel_uma_cinnamon.php<br>
#Manual de configuração do Batocera: https://wiki.batocera.org/<br>
#Controles/Joystick Suportados no Batocera: https://wiki.batocera.org/supported_controllers<br>
#Site de Screen Scraper (informações das ROMS): https://www.screenscraper.fr/<br>
#Site de Arcade Database (informações das ROMS): http://adb.arcadeitalia.net/<br>
#Site de The Games Database (informações das ROMS): https://thegamesdb.net/<br>
#Download Full-Pack BIOS Batocera v31: http://theminicaketv.free.fr/PACK-BIOS-BATOCERA.htm<br>
#Download BIOS Batocera v30: https://archive.org/details/complete-bios-collection-batocera-30<br>
#Download BIOS Batocera v31: https://archive.org/details/bios-batocera-v-31<br>
#Download RetroPie Image: https://www.arcadepunks.com/pi-images-downloads-page/<br>
#Mirror Batocera Old Version: https://mirrors.o2switch.fr/batocera/rpi3/stable/last/archives/

#Alternativas de Distribuições Retrô Games Open Source<br>
#RetroPie: https://retropie.org.uk/<br>
#Recalbox: https://www.recalbox.com/pt-br/<br>
#RetroArch: https://www.retroarch.com/<br>
#Lakka: https://www.lakka.tv/<br>
#RetroBat: https://www.retrobat.ovh/<br>
#EmuELEC: https://github.com/EmuELEC/EmuELEC/releases

#Sites para baixar ROMS<br>
#Emulator Games: https://www.emulatorgames.net/<br>
#ROMS Games: https://www.romsgames.net/roms/<br>
#ROMS Mania: https://romsmania.games/<br>
#ROMS Download: https://roms-download.com/<br>
#ROMS Download: https://romsdownload.net/<br>
#ROMS Fun: https://romsfun.com/

#Apresentação do Hardware utilizado no Curso de Hypervisor (Virtualização) Open Source:<br>
https://www.youtube.com/watch?v=vS3SVAzp3QU

#Indicação de Joystick com Review do Professor Ramos (https://www.youtube.com/professorramos)<br>
#Joystick GameSir G4s PT-BR 🎮 Gamepad Bluetooth - 2.4G Wi-Fi - USB 🌟Análise - Review:<br> 
#Link: https://www.youtube.com/watch?v=NejpVhA45xQ<br>
#Joystick para celular Android e PC Windows e Linux !!! Gamepad iPega 9099 Wolverine:<br> 
#Link: https://www.youtube.com/watch?v=MIf5Q_R1vEI<br>
#Agora eu vou dar Hadouken !!! Joystick Arcade iPega PG-9059 Fight | PC | Nintendo Switch | PS3 e 4:<br> 
#https://www.youtube.com/watch?v=OnaDImXmWz8

#Instalação do Batocera v32 (30/09/2021) em Dual Boot com o Linux Mint 20.2 Uma (Desktop ou Notebook)

#01_ Reparticionamento do Linux Mint utilizando o Gparted

	_ Para reparticionar o Linux Mint é necessário utilizar um Pen Driver do Mint com o sistema desmontado;
	_ Utilizar o software Gparted do Live do Mint para reparticionar o HD e criar as partições do Batocera;
	_ Partição 1: Tipo (type) = fat32, Nome (name) = BATOCERA, Tamanho mínimo de 5GB (recomendado 10GB);
	_ Partição 2: Tipo (type) = ext4, Nome (name) = SHARE, deve ser criada logo após a partição BATOCERA.

#02_ Criação das Partições do Batocera Linux

	_ Iniciar o sistema com o Pen Driver do Linux Mint 20.2 Uma;
	_ Executar o aplicativo Gparted: Menu, Search, Gparted;
	_ OBS1: nesse exemplo estou utilizando um Hard Disk NVMe de 512GB em: /dev/nvme0 (476,94GB);
	_ Botão direito do mouse na partição: /dev/nvme0n1p5 (Raiz do Linux), selecionar: Resize/Mode;
	_ Diminuir a partição para: 256GB (+-256621MB) - <Resize/Move>;
	_ No espaço não alocado (unallocated), clicar com o botão direito do mouse na partição e selecionar: New;
	_ Criar uma partição de: 10GB (+-10825MB), File system: Fat32, Label: BATOCERA <Add>;
	_ No espaço não alocado (unallocated), clicar com o botão direito do mouse na partição e selecionar: New;
	_ Criar uma partição de: Total do Disco (+-230424MB), File system: Ext4, Label: SHARE <Add>;
	_ Clicar na opção: Apply All Operations, <Apply> (esse processo demora um pouco) <Close>;
	_ Reiniciar o sistema e voltar para o Linux Mint instalado no Hard Disk para verificar se está tudo OK.

#03_ Instalação do Batocera Linux na partição Batocera

	_ Verificando as partições criadas: Menu, Pesquisar, Discos;
	_ OBS2: verificar se as partições BATOCERA e SHARE foram criadas corretamente; 
	_ Fazer o download do Batocera no Link: http://batocera.org/upgrades/x86_64/stable/last/boot.tar.xz
	_ Após o download do arquivo do Batocera acessar o diretório Download;
	_ Clicar com o botão direito do mouse no arquivo: boot.tar.xz, selecionar: Extrair Aqui;
	_ Após extrair os arquivos, será criado o diretório: boot, acessar o conteúdo do diretório boot;
	_ Selecionar todos os arquivos (Ctrl+A), copiar todo o conteúdo (Ctrl+C) e colar (Ctrl+V) na Raiz da partição BATOCERA;
	_ OBS3: não é necessário configurar a partição SHARE, ela será configurada automaticamente no primeiro boot do Batocera; 
	_ No primeiro boot do Batocera será criado os arquivos e diretórios de configuração do na partição BATOCERA e SHARE.

#04_ Configuração do Grub para suportar o Dual Boot do Batocera e do Linux Mint

	_ Fazer o download do projeto do Github: https://github.com/vaamonde/raspberry opção: Code, Download Zip;
	_ OBS4: você também pode clonar o projeto com o comando: git clone https://github.com/vaamonde/raspberry
	_ Descompactar o arquivo raspberyy-main.zip, botão direito do mouse no arquivo e selecionar: Extrair Aqui;
	_ Acessar a pasta raspberry-man/batocera como Root: Botão direito do Mouse, selecionar: Abrir como Root;
	_ Selecionar e copiar o arquivo: 15_batocera para o diretório: /etc/grub.d/15_batocera;
	_ No diretório /etc/grub.d/, acessar o Terminal como Root: Botão direito do Mouse, selecionar: Abrir no Terminal;
	_ Digitar os seguintes comandos;
	_	#Alterando as permissões do arquivo: 15_batocera para Todos (a=All) Executar (x=Exec) 
	_	chmod a+x 15_batocera <Enter>;
	_	#Instalando o editor de Texto VIM
	_	apt install vim <Enter>;
	_	OBS5: utilizar o editor de Texto VIM para editar o arquivo do Grub;
	_	#Editando o arquivo de configuração do GRUB
	_	vim /etc/default/grub <Enter>;
	_		#Pressione INSERT para entrar no modo de Edição, alterar as linhas abaixo:
	_			GRUB_TIMEOUT_STYLE=menu	<-- mudar de hidden para menu
	_			GRUB_TIMEOUT=10	<-- mudar de 0 para 10
	_		#Pressione ESC para sair do modo de Edição, pressione: Shift :x <Enter> para salvar e sair do VIM
	_	#Atualizando as informações do GRUB
	_	update-grub <Enter>.
	_	#Reinicializando a máquina para testar as configurações do GRUB
	_	reboot <Enter>

#05_ Ligando o Linux Mint 20.2 com o Batocera Linux v32 em Dual Boot
	
	_ OBS6: é recomendado ligar o Batocera v32 conectado com Teclado, Joystick e Rede Cabeada;
	_ OBS7: no primeiro boot o sistema irá executar as configurações das partições BATOCERA e SHARE;
	_ OBS8: no Batocera v32 os controles/joystick são reconhecidos automaticamente.

#06_ Configurações básicas do Batocera v32

	_ OBS9: por padrão o Batocera vem configurado na linguagem Americano/Inglês;
	_ Alterar a linguagem: Start (Menu ou Barra de Espaço), System Settings, Language: Portugues Brasileiro;
	_ OBS10: na versão v32 do Batocera não é necessário reinicializar o sistema;
	_ Atualizando a lista de jogos: Start (Menu ou Barra de Espaço), Opções de Jogos, Atualizar Lista de Jogos, Sim;
	_ Para sair de um jogo você pressiona: Start + Select.

#07_ Partições do Batocera v32

	_ Partição BATOCERA: sistema de boot e arquivos de inicialização/binários do Batocera;
	_ Partição SHARE: localização das ROMS (jogos), BIOS (PS2/PS3, etc...), Músicas, Temas, etc...;
	_ Na partição SHARE no diretório: roms fica localizado todos os diretórios dos consoles que o 
	_ Batocera tem suporte, cada diretório tem um nome correspondente ao seu console;
	_ Exemplo: snes = Super Nintendo, psx = Playstation, n64 = Nintendo 64, etc...;
	_ OBS11: para copiar arquivos para a partição SHARE no Linux Mint é necessário acessar como Root 
	_ a partição (Botão direito do mouse na partição/diretório SHARE, selecionar: Abrir como root).

#08_ Dicas de configurações dos emuladores do Batocera V32

	_ Nintendo 64: emulador que funciona perfeitamente os jogos: LIBRETRO / PARALLEL N64;
	_	Acessar Nintendo 64, Opções (Select ou Backspace), Opções Avançadas do Sistema, Emulador: LIBRETRO/PARALLEL N64.
	_
	_ Playstation 2: configuração do recurso de Speedhacks do PCX2-CONFIG;
	_	Acessar o Menu de Jogos, F1 (Arquivos), Aplicativos, pcsx2-config;
	_	Config, Video (GS), Core GS Settings, Speedhacks;
	_		Enable speedhacks: ON
	_		EE Cyclerate [Not Recommended]: 3
	_		EE Cycle Skipping [Not Recommended]: 3
	_		Enable INTC Spin Detection: ON
	_		Enable Wait Loop Detection: ON
	_		Enable fast CDVD: ON
	_		mVU Flag Hack: ON
	_		MTUV (Multi-Threaded microVU1): ON
	_	System, Exit
	_
	_ Atualização das informações das ROMS (Screen Scraper): fazer o cadastro no site: https://www.screenscraper.fr/;
	_	Acessar o Menu de Jogos, Menu (Start ou Barra de Espaço), Scrape;
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
	_	Iniciar Procura;
	_		Filtro: Apenas Mídias Ausentes
	_		Sistema: Número de Intens Selecionados
	_	Iniciar (Aguardar esse processo demora um pouco dependendo da quantidade de jogos para obter as informações);
	_	Voltar, Opções de Jogos, Atualizar Listas de Jogos, Sim.
	_
	_ Steam: instalação do cliente no Batocera
	_ 	Acessar o Menu de Jogos, F1 (Arquivos), Aplicativos, Flatpak-Config
	_	Em: buscar digite: steam <Enter>
	_	Selecione: Steam e clique em: <Instalar>, depois: <Sim>
	_	Selecione: Steam Link e clique em: <Instalar>, depois: <Sim>
	_	Feche o aplicativo: Flatpak-Config em: <Close>
	_	Saia do gerenciador de Arquivos, clique em: Arquivo e selecione: Fechar Janela
	_	Acessar o Menu de Jogos, Menu (Start ou Barra de Espaço) e selecionar: Opções de Jogos;
	_	Em Ferramentas, selecione: Atualizar Lista de Jogos <Sim>
	_	Acessar as opções de: Ports e clicar em: Steam (Flatpak)
	_	OBS11: na primeira vez que você acessar o Steam ele não irá executar o procedimento de atualizar o cliente,
	_	você precisa sair do Steam, depois voltar novamente, na segunda vez que você acessar o Steam ele vai começcar
	_	a atualizar o sistema e instalar o cliente.
	_	Aguarde a atualização do aplicativo Steam (esse processo demora um pouco)
	_	Após a atualização do Steam, se autenticar com sua conta e senha.
	_
	_ Firefox: instalação do navegador Mozilla Firefox no Batocera
	_ 	Acessar o Menu de Jogos, F1 (Arquivos), Aplicativos, Flatpak-Config
	_	Em: buscar digite: firefox <Enter>
	_	Selecione: Firefox e clique em: <Instalar>, depois: <Sim>
	_	Feche o aplicativo: Flatpak-Config em: <Close>
	_	Saia do gerenciador de Arquivos, clique em: Arquivo e selecione: Fechar Janela
	_	Acessar o Menu de Jogos, Menu (Start ou Barra de Espaço) e selecionar: Opções de Jogos;
	_	Em Ferramentas, selecione: Atualizar Lista de Jogos <Sim>
	_	Acessar as opções de: Ports e clicar em: Steam (Flatpak)
	_	Aguarde a atualização do aplicativo Steam (esse processo demora um pouco)
	_	Após a atualização do Steam, se autenticar com sua conta e senha
	
