#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 14/07/2021<br>
#Data de atualização: 30/07/2021<br>
#Versão: 0.01<br>
#Testado e homologado no Proxmox-VE v7.x x64 Bit

06/07/2021 - Proxmox Virtual Environment 7.0 released: https://www.proxmox.com/en/news<br>
Link de Download do Proxmox-VE v7.x: https://www.proxmox.com/en/downloads/category/proxmox-virtual-environment<br>
Documentação Oficial do Projeto: https://www.proxmox.com/en/downloads/category/documentation-pve

OBSERVAÇÃO IMPORTANTE 01: O Proxmox-VE é um Bare Metal (Servidor Físico Dedicado) que utiliza
a Distribuição Debian 11 com suporte ao KVM (Kernel-based Virtual Machine) nativo no Kernel para 
suportar o Hypervisor (Monitor de Máquina Virtual) e com suporte a Containers utilizando a 
tecnologia de LXC (Linux Containers - Obs: antigamente o Proxmox-VE utiliza o OpenVZ para containers)

#Instalação do Proxmox-VE v7.x no Desktop Huananzhi X99-F8 Xeon E5-2678 V3

#01_ Software para criação de Pen Drive Bootável<br>

	_ Rufus: https://rufus.ie/pt_BR/
	_ YUMI: https://www.pendrivelinux.com/yumi-multiboot-usb-creator/
	_ Etcher: https://www.balena.io/etcher/
	_ UNetbootin: https://unetbootin.github.io/
	_ Ventoy: https://www.ventoy.net/en/index.html
	_ Linux Live USC Creator: https://www.linuxliveusb.com/

#02_ Configurações do Hardware do Desktop Huananzhi X99-F8 Xeon E5-2678 V3<br>

	_ CPU Intel Xeon E5-2678 V3 2.5Ghz 12/24, 32.0GB DDR-4 3000Mhz, SSD Adata SU630 - 240GB, SSD NVMe 
	_ Lexar NM700 - 512GB, Monitor 17", Ethernet Realtek RTL-8168, Intel UHD Graphics 630, Asus Strix 
	_ AMD Radeon RX Vega64, Power Supply Silver Stone ET750, Water Cooler Lian Li Galahad AIO 360mm RGB, 
	_ Kit Fan Resi Mode Fan Galaxy, Gabinete Lian Li Lancool 215

#03_ Configuração da BIOS (versão 5.11)<br>

	_ Bios já atualizada pelo Professorramos (Leandro Ramos) possibilitando trabalhar com Turbo Unlock 
	_ X99, mais informações acesse o vídeo de Upgrade da Bios: https://www.youtube.com/watch?v=d_KtZfNG4RY
	_ Hyper-Threading [All] habilitado, VMX habilitado, AES-NI habilitado, Intel TXT e SMX desabilitados

#04_ Acessando a BIOS da Placa Mãe Huananzhi X99

	_ Delete (Dell)
	_ Advanced
		NVMe Configuration
			Lexar 512GB SSD
	_ IntelRCSetup
		Processor Configuration
			Hyper-Threading [All] Enable;
			Enable Intel TXT Support Disable;
			VMX Enabled;
			Enable SMX Disable;
			AES-NI Enable.
		IIO Configuration
			Intel VT for Directed I/O (VT-d)
				Intel Vt for Directed I/O (VT-d) Enable
		PCH Configuration
			PCH sSATA Configuration
				Configure sSATA as AHCI
				sSATA Port 3
					Port 3 ADATA SU630 - 240GB
			
#04_ Inicialização da Instalação<br>

	_01 Install Proxmox-VE <Enter>
	_02 End User License Agreement (EULA): <I agree>
	_03 Proxmox Virtual Environment (PVE)
		Target Hard Disk: /dev/nvme0n1 (476GiB, Lexar 512GB SSD): <Next>
	_04 Location and Time Zone selection
		Country: Brazil
		Time zone: America/Sao_Paulo
		Keyboard Layout: Brazil-Portuguese <Next>
	_05 Administrator Password and Email Address
		Password: pti@2018
		Confirm: pti@2018
		Email: vaamonde@pti.intra <Next>
	_06 Management Network Configuration
		Management Interface: enp8s0 - 00:e0:4c:af:00:0a (r8169)
		Hostname (FQDN): ptispo01vm01.pti.intra
		IP Address (CIDR): 192.168.0.200/24
		Gateway: 192.168.0.1
		DNS Server: 192.168.0.1 <Next>
	_07 Summary
		[Disable] Automatically reboot after successful installation <Install>
		(Retirar o Pen Drive no final da instalação do Proxmox-VE)

#05_ Pós-Instalação do Proxmox-VE v7.x

	_01 *Proxmox VE GNU/Linux (Boot padrão do GRUB)
	_02 Usuário padrão: root - senha: pti@2018
	_03 Acesso remoto do Proxmox-VE: https://192.168.0.200:8006
	_04 Atualizando o Proxmox-VE
		apt update
		apt upgrade
		apt dist-upgrade
		apt full-upgrade
		apt autoremove
		apt autoclean
		reboot

#06_ Acessando o GUI do Proxmox-VE v7.x

	_01 Recomendado utilizado o Navegador Firefox: https://192.168.0.200:8006
		Avançado
			Aceitar o Risco e continuar
	_02 Login Proxmox-VE
		Nome do usuário: root
		Senha: pti@2018
		Domínio: Linux PAM standard authentication
		Idioma: Portuguese (Brazil) <Logar>