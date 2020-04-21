---
layout: page
title: CCNA R&S - Introdução às Redes
#tags: [, Jekyll, theme, moon]
date: 2020-04-20
comments: false
---

__Objetivo geral__

* Ensinar ao aluno de forma detalhada o processo de comunicação entre dois computadores ou mais baseando-se no serviço que está sendo executado.

__Objetivos específicos__

* Comparar a comunicação humana com a comunicação em rede e ver as semelhanças entre elas.
* Conhecer os dois modelos principais usados para planejar e implementar redes: OSI/ISO e TCP/IP.
* Compreender a abordagem “em camadas” para redes.
* Examinar as camadas OSI/ISO e TCP/IP com detalhes para entender suas funções e serviços.
* Familiarizar-se com vários dispositivos de rede e esquemas de endereçamento de rede.
* Descobrir os tipos de meios físicos usados para transportar dados pela rede
* Criar LANs simples, executar configurações básicas em roteadores e switches e implementar esquemas de endereçamento IP.

---

__Considerações sobre a Arquitetura TCP/IP__
{: .notice}
![Arquitetura TCP/IP (5 camadas) x Arquitetura TCP/IP considerada na Academia Cisco](https://mariotlemes.github.io/images/tcp-ip.png)


---
__Passo 1: Enviando informação digital por um cabo par trançado__
{: .notice}

A informação entre dois computadores pode ser transmitida por meio de um cabo de rede par trançado. Este cabo possui 4 pares de fios (8 fios no total) que conduzem os pulsos elétricos.

Para que a informação seja gerada, é preciso energizar os fios com voltagens que variam entre 0v e 5v. Portanto, diferentes combinações referentes a energizar ou não energizar um fio, durante um determinado período de tempo, podem ser estabelecidas.

As voltagens de 0v e 5v podem ser representadas por símbolos (0 para 0v e 1 para 5v). Portanto, pode-se representar a combinação de energizar ou não energizar um fio, durante um determinado período de tempo, por uma sequência de 0s e 1s. Veja na Figura abaixo a representação dessa combinação.

![Representação da transmissão de bits](https://mariotlemes.github.io/images/bits.png)

Sendo assim, ao energizar um fio do cabo par trançado por:

* 0v por 1 segundo;
* 5v por 1 segundo;
* 0v por 2 segundos;
* 5v por 2 segundos;
* 0v por 1 segundo;
* 5v por 1 segundo;

Gera-se a sequência de 0s e 1s: 01001101, conforme mostrado na figura abaixo.

![fig2](https://mariotlemes.github.io/images/bin-dec.png)

A sequência binária __01001101__ em decimal equivale ao número __77__. O número __77__ equivale ao caractere __M__, segundo o mapeamento da tabela ASCII.

Portanto, para enviar um texto qualquer deve-se energizar ou não o fio do cabo par trançado, durante período de tempos aleatórios, para gerar a sequência de 0s e 1s e assim transmitir a informação desejada.

---

__Passo 2: Introdução ao cabo de fibra óptica__
{: .notice}













---


__Modos de execução no Cisco IOS__
{: .notice}

![Modos de execução no Cisco IOS](https://mariotlemes.github.io/images/1.png)


__Modos de navegação no Cisco IOS__
{: .notice}

![Resumo esquemático da navegação](https://mariotlemes.github.io/images/2.png)

---

__Proteger o acesso no modo local e no modo privilegiado__
{: .notice}

```
en
conf t
line console 0
password senha
login
exit
enable secret senha
```
---

__Proteger o acesso remoto e criptografar todas as senhas__
{: .notice}

```
en
conf t
line vty 0 15
password senha
login
transport input ssh
login
exit
service password-encryption
```
---
__Inserir um banner__
{: .notice}

```
en
conf t
banner motd #Mensagem Personalizada#
```
---
__Alterar hostname__
{: .notice}

```
en
conf t
hostname novoNome
```
---
__Salvar configurações locais (running-config) para o arquivo de configuração inicial (startup-config)__
{: .notice}

```
en
copy running-config startup-config
```
---

__Reiniciar um dispositivo__
{: .notice}

```
en
reload
```
---
__Apagar o arquivo de configuração inicial__
{: .notice}

```
en
erase startup-config
```
---

__Configurar a SVI de um SW__
{: .notice}

```
en
conf t
interface vlan 1
ip address 192.168.1.1 255.255.255.0
no shutdown
```
---

__Verificar IPs das interfaces de rede de um SW__
{: .notice}

```
en
show ip interface brief
```
---

__Evitar que as mensagens de console atrapalhem o código__
{: .notice}

```
en
conf t
line con 0
logg sync
pass Cisco
login
```
---
__Ver tabela MAC de um SW__
{: .notice}

```
en
show mac address-table
```
---

__Apagar tabela MAC de um SW__
{: .notice}

```
en
clear mac address-table dynamic
```
---

__Limpar a tabela ARP de um PC__
{: .notice}

```
arp -d
```
---

__Listar os vizinhos IPv6 de um Roteador__
{: .notice}

```
en
sh ipv6 neighbors
```
---

__Limpar a lista de vizinhos IPv6 de um Roteador__
{: .notice}

```
en
clear ipv6 neighbors
```
---

__Configurar uma interface com endereços IPV6 unicast global/link local__
{: .notice}

```
en
conf t
int g0/0
ipv6 address 2001:db8:acad:100::1/64
ipv6 address fe80:14 link-local
no sh
```
---

__Habilitar o roteamento IPv6 em um Roteador__
{: .notice}

```
en
conf t
ipv6 unicast-routing
```
---

__Configurar várias interfaces em um SW L3__
{: .notice}

```
en
conf t
hostname SW-L3
ip routing
int range f0/1-5
no switchport
int f0/1
ip address IP Mascara
no sh
int f0/2
ip address IP Mascara
no sh
```
---

__Comandos diversos__
{: .notice}

```
en
conf t
security passwords min-lenght 10
ipv6 unicast-routing
ip domain-name CCNA-lab.com
crypto key generate rsa 1024
username admin privilege 15 secret Cisco
line vty 0 15
login local
exec-timeout 5
transport input ssh
exit
login block-for 180 attemps 4 within 120
line console 0
exec-timeout 300
```
---
