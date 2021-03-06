# :penguin: :penguin: Curso GRÁTIS de Hypervisor (Virtualização) utilizando o Proxmox-VE, XCP-NG e VMware ESXi

## 💰 Ajude o projeto Bora para Prática a continuar fazendo vídeos e materiais gratuitos para o Canal
## 💰 Chave PIX do projeto: robsonvaamonde@gmail.com
## 💰 Link de doação do PagSeguro: https://pag.ae/bjlSJcH

Robson Vaamonde<br>
Procedimentos em TI: http://procedimentosemti.com.br<br>
Bora para Prática: http://boraparapratica.com.br<br>
Robson Vaamonde: http://vaamonde.com.br<br>
Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
Facebook Bora para Prática: https://www.facebook.com/boraparapratica<br>
Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
LinkedIn Robson Vaamonde: https://www.linkedin.com/in/robson-vaamonde-0b029028/<br>

## **Links Oficiais dos Hypervisor:**
Site do Proxmox: https://www.proxmox.com/en/​<br>
Site do KVM: https://www.linux-kvm.org/page/Main_Page<br>
Site do XCP-NG: https://xcp-ng.org/​<br>
Site do XenProject: https://xenproject.org/<br>
Site do VMware: https://www.vmware.com/br.html<br>

## **Playlist do YouTUBE com todos os Vídeos dos Hypervisor:**
Link da Playlist: https://www.youtube.com/playlist?list=PLozhsZB1lLUOF7ibs1q3jkRX4i5scv3XZ

## **🖥😍 Apresentação do Hardware utilizado no Curso de Hypervisor (Virtualização) Open Source 😍🖥**

Vídeo mostrando o Hardware utilizado nas aulas do Curso GRÁTIS de Hypervisor Open Source (Free Software) utilizando os Appliances: Proxmox-VE, XCP-NG e o VMware ESXi.

Agradecimento especial para o Prof. Leandro Ramos do Site http://professorramos.com/ e do Canal do YouTUBE: ProfessorRamos https://www.youtube.com/professorramos que forneceu o Hardware de Desktop para a preparação desse curso, sem esse equipamento eu não teria a possibilidade de montar o conteúdo para esse curso e nem gravar as aulas, novamente: MUITO OBRIGADO.

O Proxmox Virtual Environment é uma plataforma de gerenciamento de virtualização de servidor de código aberto. É uma distribuição Linux baseada em Debian com um Kernel Ubuntu LTS modificado que permite a implantação e gerenciamento de máquinas virtuais e contêineres.

O XCP-ng significa Xen Cloud Platform - New Generation. É uma distribuição turnkey do Xen Project Hypervisor, contando principalmente com o Xen Hypervisor e o projeto Xen API (XAPI). O projeto nasceu em 2018, seguindo a bifurcação do projeto open source Xen Server (agora Citrix Hypervisor).

VMware ESXi é um Hypervisor de nível empresarial tipo 1 desenvolvido pela VMware para implantar e prover maquinas virtuais. Como hypervisor tipo 1, o ESXi não é um software aplicativo instalado em um sistema operacional; em vez disso, inclui e integra componentes vitais do sistema operacional e um único núcleo.

![Hardware Hypervisor](00-Projeto-Hypervisor-Hardware.png "Hardware Hypervisor")

Informações detalhes do Review do Hardware utilizado no Curso:

🐲 COMO MONTAR UM PC XEON 2678 V3 + Gabinete Gamer Lian Li Lancool 215 + Water Cooler Lian Li Galahad<br>
https://www.youtube.com/watch?v=VSI9VsKOhWo

🐲 Como Fazer o Turbo Unlock Fácil no seu XEON V3 X99 e Undervoltage PT-BR + Testes Antes e depois<br>
https://www.youtube.com/watch?v=d_KtZfNG4RY

💥 SSD NVME LEXAR NM700 Professional M.2 2280 PCIE - Instalação e Testes<br>
https://www.youtube.com/watch?v=68F5zm6c7Qg

Quer Fluxo de AR ??? Então TOMA !!! Gabinete Gamer Lian Li Lancool 215 Mesh ARGB com 2 FAN de 200 mm<br>
https://www.youtube.com/watch?v=7UgIm3kDXAQ

🥇 Fonte 80 Plus Gold com Precinho de Bronze ou White - Fonte SilverStone ET750-G 750W 80 Plus Gold<br>
https://www.youtube.com/watch?v=F1xOp8dRS_0

⚡ SSD Muito Bom e Barato 💥 Review e Testes do SSD ADATA SU630 com 3 anos de Garantia no Brasil<br>
https://www.youtube.com/watch?v=1WmyQGr9MDg

Memoria GLOWAY DDR4 é BOA ??? Review + Testes + Overclock da Memória RAM mais Barata do Mundo !!!<br>
https://www.youtube.com/watch?v=EaQwTN3l0nU&t

👉 Memória OLOy é boa ??? 🔥 RAM DDR4 OLOy WarHawk Alta Frequência com Preço Justo !!!<br>
https://www.youtube.com/watch?v=J3Or0bcr1PM

[![Apresentação do Hardware](http://img.youtube.com/vi/vS3SVAzp3QU/0.jpg)](https://www.youtube.com/watch?v=vS3SVAzp3QU "Apresentação do Hardware")

Link da vídeo aula: https://www.youtube.com/watch?v=vS3SVAzp3QU

Link da apresentação utilizada nesse vídeo: https://github.com/vaamonde/hypervisor/blob/main/00-Projeto-Hypervisor-Hardware.pdf

## **🛡 #001_ COMO instalar o PROXMOX-VE versão v7.0 no Desktop Xeon E5-2678 V3 MB-X99 🛡**

Vídeo mostrando os procedimentos básicos para baixar, criar o pen driver e instalar o Hypervisor Open Source Proxmox-VE versão v7.0.1 no Desktop Xeon E5-2678 V3 utilizando uma Placa Mãe MB-x99.

O Ambiente Virtual Proxmox (Proxmox VE; abreviação PVE) é uma plataforma de gerenciamento de virtualização de servidor de código aberto. É uma distribuição Linux baseada em Debian com um Kernel Ubuntu LTS modificado que permite a implantação e gerenciamento de máquinas virtuais e contêineres. O Proxmox-VE inclui um console da web e ferramentas de linha de comando e fornece uma API REST para ferramentas de terceiros. Dois tipos de virtualização são suportados: baseada em contêiner com LXC (a partir da versão 4.0 substituindo o OpenVZ usado na versão até 3.4) e virtualização completa com KVM. Ele vem com um instalador bare-metal e inclui uma interface de gerenciamento baseada na web. Proxmox-VE é licenciado sob a GNU Affero General Public License versão 3.

Mais informações acesse o site Oficial: https://proxmox.com/en/

[![Instalação do Proxmox-VE](http://img.youtube.com/vi/829fLZWJ-Bo/0.jpg)](https://www.youtube.com/watch?v=829fLZWJ-Bo "Instalação do Proxmox-VE")

Link da vídeo aula: https://www.youtube.com/watch?v=829fLZWJ-Bo

Link dos procedimentos utilizados nesse vídeo: https://github.com/vaamonde/hypervisor/blob/main/etapas/proxmox-ve/001-InstalacaoDoProxmox-VE.md