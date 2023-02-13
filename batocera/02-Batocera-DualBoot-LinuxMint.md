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
#Data de atualização: 13/02/2023<br>
#Versão: 0.13<br>
#Testado e homologado no Linux Mint 20.2 Uma, 20.3 Una, 21 Vanessa e 21.1 Vera<br>
#Testado e homologado no Batocera v34 e v35

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
#Download BIOS Batocera v32: https://archive.org/details/bios-batocera-v-32<br>
#Download BIOS Batocera v33: https://archive.org/details/batocera-33-bios<br>
#Download BIOS Batocera v34: https://archive.org/details/full-pack-bios-batocera-v-34-tmctv<br>
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

#01_ Partições utilizadas pelo Batocera que deve ser criada no Linux Mint

	OBSERVAÇÃO IMPORTANTE: Para reparticionar o Linux Mint é necessário utilizar um Pen Driver 
	do Mint com o sistema desmontado;
	
	Utilizar o software Gparted do Live do Mint para reparticionar o Hard Disk e criar as duas 
	partições utilizadas pelo Batocera;
	
	Partição 1: Tipo (type) = fat32, Nome (name) = BATOCERA, Tamanho mínimo de 5GB (recomendado 10GB);
	Partição 2: Tipo (type) = ext4,  Nome (name) = SHARE, deve ser criada logo após a partição BATOCERA.

#02_ Iniciando o Linux Mint com o Pendrive de Instalação

	OBSERVAÇÃO IMPORTANTE: Cada computador ou notebook possuí uma forma diferente de iniciar o
	Linux Mint pelo Pendrive, podendo ser pelas teclas de atalho: F8, F11 ou F12.

	01_ Plugar o Pendrive do Linux Mint no seu computador;
	02_ Ligar o computador e acessar o sistema de boot com as teclas atalho (F8, F11 ou F12);
	03_ Iniciar o Linux Mint como se fosse fazer uma nova instalação. 

#02_ Diminuir a Partição Raiz do Linux Mint para instalar o Batocera

	01_ Após a inicialização do Linux Mint executar o aplicativo Gparted: 
		Menu, 
			Search, 
				Gparted;

	OBSERVAÇÃO IMPORTANTE: no meu exemplo estou utilizando um Hard Disk NVMe de 512GB que foi 
	montado em: /dev/nvme0 (476,94GB);

	02_ Selecionar a partição Raiz do Linux Mint em: /dev/nvme0n1p5 (Raiz do Linux - alterar a
	localização do Disco conforme a sua necessidade), clicar com o botão direito do mouse na 
	partição e selecionar: Resize/Mode;

	03_ Diminuir a partição para: 256GB (+-256621MB - alterar conforme a sua necessidade e tamanho
	do disco disponível) - <Resize/Move>;

	OBSERVAÇÃO IMPORTANTE: Esse procedimento demora um pouco dependendo do tipo de Hard Disk que 
	você está usando (HD mecânico de 5400rpm por exemplo).

	04_ Clicar na opção: Apply All Operations, <Apply> (esse processo demora um pouco, aguarde)
	<Close>;

#03_ Criando as Partições do Batocera no Espaço não Alocado do Linux Mint

	01_ No espaço não alocado (unallocated), clicar com o botão direito do mouse na partição e 
	selecionar: New;

	02_ Criar uma partição de: 10GB (+-10825MB), File system: Fat32, Label: BATOCERA <Add>;

	03_ No espaço não alocado (unallocated), clicar com o botão direito do mouse na partição e 
	selecionar: New;
	
	04_ Criar uma partição de: Total do Disco (+-230424MB ou quanto sobre no seu disco), File 
	system: Ext4, Label: SHARE <Add>;

	OBSERVAÇÃO IMPORTANTE: Esse procedimento demora um pouco dependendo do tipo de Hard Disk que 
	você está usando (HD mecânico de 5400rpm por exemplo).

	05_ Clicar na opção: Apply All Operations, <Apply> (esse processo demora um pouco) <Close>;

	06_ Reiniciar o Live do Linux Mint e volte para o Linux Mint instalado no Hard Disk para 
	verificar se está tudo OK na inicializando.

	OBSERVAÇÃO IMPORTANTE: CASO VOCÊ ALTERE AO APAGUE A PARTIÇÃO DE BOOT DO LINUX MINT ELE NÃO
	IRÁ MAIS INICIAR CORRETAMENTE, MUITO CUIDADO NOS PROCEDIMENTOS DE REDIMENCIONAMENTO DE DISCO.

#04_ Instalando o Batocera Linux na partição BATOCERA criada no Linux Mint

	01_ Verifique se as partições foram criadas com sucesso: 
	Menu, 
		Pesquisar, 
			Discos;
	
	OBSERVAÇÃO IMPORTANTE: verifique se as partições BATOCERA e SHARE foram criadas corretamente;

	02_ Fazer o download do Batocera no Link: http://batocera.org/upgrades/x86_64/stable/last/boot.tar.xz

	03_ Após o download do arquivo do Batocera acesse o diretório: Download;

	04_ Clicar com o botão direito do mouse no arquivo: boot.tar.xz, selecionar: Extrair Aqui;

	05_ Após extrair os arquivos, será criado o diretório: boot, acessar o diretório: boot 
	clicando duas nele;

	06_ Selecionar todos os arquivos com o atalho: Ctrl + A (selecionar tudo), copiar todo o 
	conteúdo do diretório com o atalho: Ctrl + C (copiar) e colar todo o conteúdo na Raiz da 
	partição: BATOCERA com o atalho: Ctrl + V (colar);

	OBSERVAÇÃO IMPORTANTE: não é necessário configurar a partição SHARE, ela será configurada 
	automaticamente no primeiro boot do Batocera; 
	
	07_ No primeiro boot do Batocera será criado os arquivos e diretórios de configuração do 
	Batocera na partição BATOCERA e SHARE.

#05_ Criando o arquivo do Grub para suportar o Dual Boot do Batocera e do Linux Mint

	01_ Fazer o download do projeto do Github: https://github.com/vaamonde/raspberry 
		Clique na opção: Code, depois: Download Zip;

	Link direto: https://github.com/vaamonde/raspberry/archive/refs/heads/main.zip

	OBSERVAÇÃO IMPORTANTE: você pode clonar o projeto utilizando o comando: git no seu terminal:
		Atalho Terminal: Ctrl + Alt + T
		git clone https://github.com/vaamonde/raspberry
	
	02_ Descompactar o arquivo raspberry-main.zip, botão direito do mouse no arquivo e selecione: 
	Extrair Aqui;

	03_ Acesse o diretório criado: raspberry-man/batocera 
	
	04_ Altera para Root clicando com o Botão direito do Mouse, selecione: Abrir como Root;

	05_ Selecione o arquivo: 15_batocera clique com o botão direito do mouse e selecione: Copiar;
	
	06_ Navegue até o diretório: Sistemas de arquivo, /etc/ e /grub.d/ cole o arquivo: 15_batocera
	nesse diretório com o atalho: Ctrl + V ou com o Botão Direito do mouse e selecione: Colar

#06 Habilitando o arquivo do Grub do Batocera no Linux Mint

	01_ No diretório: /etc/grub.d/, acesse o Terminal como Root, clique com o Botão direito do Mouse
	na área branca e selecione: Abrir no Terminal;

	02_ Digite os seguintes comandos para habilitar o boot do Batocera;

	#Instalando o editor de Texto VIM
	apt update
	apt install vim

	#Alterando as permissões do arquivo: 15_batocera para: Todos (a=All) + (Adicionar) Executar (x=Exec) 
	chmod a+x 15_batocera

	#Editando o arquivo de configuração do GRUB
	vim /etc/default/grub <Enter>;

		#Pressione INSERT para entrar no modo de Edição, alterar as linhas abaixo:
			
			#mudar de hidden para menu
			GRUB_TIMEOUT_STYLE=menu
			
			#mudar de 0 para 10
			GRUB_TIMEOUT=10
		
		#Pressione ESC para sair do modo de Edição, pressione: Shift :x <Enter> para salvar e sair do VIM

	#Atualizando as informações do GRUB
	update-grub

	OBSERVAÇÃO IMPORTANTE: deverá aparecer a seguinte mensagem confirmando que o Batocera
	foi instalado com sucesso: Imagem do Batocera encontrada

	#Reinicializando a máquina para testar as configurações do GRUB
	reboot

#07_ Ligando o Linux Mint com Dual Boot do Batocera Linux
	
	01_ Na instalação do Linux Mint selecione: Batocera Linux Retro Games

	OBSERVAÇÃO IMPORTANTE: é recomendado ligar o Batocera Linux conectado com Teclado, Joystick 
	e Placa de Rede Cabeada (Internet);

	OBSERVAÇÃO IMPORTANTE: no primeiro boot do Batocera ele irá começar a executar as configurações 
	das partições BATOCERA e SHARE, aguarde;

	OBSERVAÇÃO IMPORTANTE: no Batocera Linux os controles/joystick são reconhecidos automaticamente.

#08_ Configurações básicas do Batocera Linux

	OBSERVAÇÃO IMPORTANTE: por padrão o Batocera Linux vem configurado na lingua Americano/Inglês;

	01_ Alterar a linguagem: 
		Start (Menu ou Barra de Espaço), 
			System Settings, 
				Language: Português Brasileiro;
	
	OBSERVAÇÃO IMPORTANTE: a partir da versão v32 do Batocera não é mais necessário reinicializar 
	o sistema para aplicar as mudanças;

	02_ Atualizando as listas de jogos: 
		Start (Menu ou Barra de Espaço), 
			Opções de Jogos, 
				Atualizar Lista de Jogos, Sim;

	OBSERVAÇÃO IMPORTANTE: Para sair de um jogo você pressiona: Start + Select (Simultaneamente).

#09_ Conhecendo as Partições do Batocera Linux

	Partição BATOCERA: sistema de boot e arquivos de inicialização/binários do Batocera;
	
	Partição SHARE: localização das ROMS (jogos), BIOS (PS2/PS3, etc...), Músicas, Temas, etc...;
	
	Na partição SHARE no diretório: roms fica localizado todos os diretórios dos consoles que o 
	Batocera tem suporte, cada diretório tem um nome correspondente ao seu console;
	
	EXEMPLO: snes = Super Nintendo, psx = Playstation, n64 = Nintendo 64, etc...;
	
	OBSERVAÇÃO IMPORTANTE: para copiar arquivos para a partição SHARE no Linux Mint é necessário 
	acessar como Root a partição SHARE (Botão direito do mouse na partição/diretório SHARE, 
	selecionar: Abrir como root).

#10_ Dicas de configurações dos emuladores do Batocera Linux

	NINTENDO 64: emulador que funciona perfeitamente os jogos: LIBRETRO / PARALLEL N64;

	Acessar Nintendo 64, 
		Opções (Select ou Backspace), 
			Opções Avançadas do Sistema, 
				Emulador: LIBRETRO/PARALLEL N64.
	
	PLAYSTATION 2: configuração do recurso de Speedhacks do PCX2-CONFIG;
	
	Acessar o Menu de Jogos, F1 (Arquivos), 
		Aplicativos, 
			pcsx2-config;
				Config, 
					Video (GS), 
						Core GS Settings, 
							Speedhacks;
								Enable speedhacks: ON
								EE Cyclerate [Not Recommended]: 3
								EE Cycle Skipping [Not Recommended]: 3
								Enable INTC Spin Detection: ON
								Enable Wait Loop Detection: ON
								Enable fast CDVD: ON
								mVU Flag Hack: ON
								MTUV (Multi-Threaded microVU1): ON
			System, Exit
	
	SCREEN SCRAPER: Atualização das informações das ROMS (Screen Scraper): 
	
		Primeiro: fazer o cadastro no site: https://www.screenscraper.fr/;
		
		Acessar o Menu de Jogos, 
			Menu (Start ou Barra de Espaço), 
				Scrape;
					Banco de Dados: Screenscraper
					Fonte da Imagem: Screenshot
					Fonte da Caixa: Caixa 2D
					Fonte do Logotipo: Logotipo
					Obter Avaliações: ON
					Obter Vídeos: ON
					Obter Fanart: ON
					Obter parte de trás da Caixa: ON
					Obter Mapa: ON
					Obter Manual: ON
					Obter Configuração do Controle e Teclado: ON
					Usuário: usuário_screenscraper
					Senha: senha_screenscraper
					Iniciar Procura;
					Filtro: Apenas Mídias Ausentes
					Sistema: Número de Intens Selecionados
				Iniciar (Aguardar esse processo demora um pouco dependendo da quantidade de jogos 
				para obter as informações);
		
			Voltar, 
				Opções de Jogos, 
					Atualizar Listas de Jogos, Sim.

	STEAM: instalação do cliente no Batocera
	
		Acessar o Menu de Jogos, F1 (Arquivos), 
			Aplicativos, 
				Flatpak-Config
					Em: buscar digite: steam <Enter>
					Selecione: Steam e clique em: <Instalar>, 
						depois: <Sim>
					Selecione: Steam Link e clique em: <Instalar>, 
						depois: <Sim>
					Feche o aplicativo: Flatpak-Config em: <Close>
		
		Saia do gerenciador de Arquivos, clique em: Arquivo e selecione: Fechar Janela
		
		Acessar o Menu de Jogos, Menu (Start ou Barra de Espaço) e selecionar: Opções de Jogos;

		Em Ferramentas, selecione: Atualizar Lista de Jogos <Sim>

		Acesse as opções de: Ports e clicar em: Steam (Flatpak)

		OBSERVAÇÃO IMPORTANTE: na primeira vez que você acessar o Steam ele não irá executar o 
		procedimento de atualizar o cliente, você precisa sair do Steam, depois voltar novamente, 
		na segunda vez que você acessar o Steam ele vai começar a atualizar o sistema e instalar 
		o cliente.
		
		Aguarde a atualização do aplicativo Steam (esse processo demora um pouco)
		
		Após a atualização do Steam, faça a autenticação com sua conta e senha.

	FIREFOX: instalação do navegador Mozilla Firefox no Batocera
	
		Acessar o Menu de Jogos, F1 (Arquivos), 
			Aplicativos, 
				Flatpak-Config
					Em: buscar digite: firefox <Enter>
					Selecione: Firefox e clique em: <Instalar>, depois: <Sim>
					Feche o aplicativo: Flatpak-Config em: <Close>
					Saia do gerenciador de Arquivos, clique em: Arquivo e selecione: Fechar Janela
		
		Acessar o Menu de Jogos, Menu (Start ou Barra de Espaço) e selecionar: Opções de Jogos;
		
		Em Ferramentas, selecione: Atualizar Lista de Jogos <Sim>
		
		Acessar as opções de: Ports e clicar em: Steam (Flatpak)
		
		Aguarde a atualização do aplicativo Steam (esse processo demora um pouco)
		Após a atualização do Steam, se autenticar com sua conta e senha
	
