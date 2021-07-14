#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 14/07/2021<br>
#Data de atualização: 14/07/2021<br>
#Versão: 0.01<br>
#Testado e homologado no Proxmox-VE v7.x x64 Bit

06/07/2021 - Proxmox Virtual Environment 7.0 released: https://www.proxmox.com/en/news
Link de Download do Proxmox-VE v7.x: https://www.proxmox.com/en/downloads/category/proxmox-virtual-environment
Documentação Oficial do Projeto: https://www.proxmox.com/en/downloads/category/documentation-pve

#Instalação do Proxmox-VE v7.x no Desktop Huananzhi X99-F8 Xeon E5-2678 V3

#01_ Software para criação de Pen Drive Bootável<br>

	_ Rufus: https://rufus.ie/pt_BR/
	_ YUMI: https://www.pendrivelinux.com/yumi-multiboot-usb-creator/
	_ Etcher: https://www.balena.io/etcher/
	_ UNetbootin: https://unetbootin.github.io/
	_ Ventoy: https://www.ventoy.net/en/index.html
	_ Linux Live USC Creator: https://www.linuxliveusb.com/

#02_ Configurações do Hardware do Desktop Huananzhi X99-F8 Xeon E5-2678 V3<br>

	_ CPU Intel Xeon E5-2678 V3 2.5Ghz 12/24, 32.0GB DDR-4 3000Mhz, SSD Adata SU630 - 240GB, SSD NVMe Lexar NM700 - 512GB, 
	_ Monitor 17", Ethernet Realtek RTL-8168, Intel UHD Graphics 630, Asus Strix AMD Radeon RX Vega64, Power Supply Silver
	_ Stone ET750, Water Cooler Lian Li Galahad AIO 360mm RGB, Kit Fan Resi Mode Fan Galaxy, Gabinete Lian Li Lancool 215

#03_ Configuração da BIOS (versão 5.11)<br>

	_ Bios já atualizada pelo Professorramos (Leandro Ramos) possibilitando trabalhar com Turbo Unlock X99, mais informações
	_ acesse o vídeo de Upgrade da Bios: https://www.youtube.com/watch?v=d_KtZfNG4RY
	_ Hyper-Threading [All] habilitado, VMX habilitado, AES-NI habilitado, Intel TXT e SMX desabilitados
	
#04_ Inicialização da Instalação<br>

	_01 Install Proxmox-VE <Enter>
	_02 End User License Agreement (EULA): <I agree>
	_03 Target Hard Disk: /dev/nvme0n1 (476GiB, Lexar 512GB SSD): <Next>
	_04