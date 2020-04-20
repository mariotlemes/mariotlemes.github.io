---
layout: page
title: CCNA1v6 - Introdução às redes
#tags: [, Jekyll, theme, moon]
date: 2020-04-20
comments: true
---

__Modos de execução no ios da Cisco__
{: .notice}

1) Execução de usuário -> Switch>

2) Execução de usuário privilegiado -> Switch#

3) Configuração global -> Switch#(conf t)

4) Submódulo de configuração de console -> Switch#(conf-line)

5) Submódulo de configuração de interface -> Switch#(conf-if)

6) ...

__Modos de navegação no ios da Cisco__
{: .notice}

Switch> -> __enable__ -> Switch# -> __configure terminal__ -> Switch#(conf t) -> __interface fastethernet 0/1__ -> Switch#(conf-if) -> __line console 0__ -> Switch#(conf-line) -> __exit__ -> Switch#(conf t) -> __exit/end__ -> Switch# -> __disable__ -> Switch>

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
__Inserir um banner__
{: .notice}

```
en
conf t
banner motd #Mensagem Personalizada#
```

__Alterar hostname__
{: .notice}

```
en
conf t
hostname novoNome
```
__Salvar configurações locais (running-config) para o arquivo de configuração inicial (startup-config)__
{: .notice}

```
en
copy running-config startup-config
```

__Reiniciar um dispositivo__
{: .notice}

```
en
reload
```
__Apagar o arquivo de configuração inicial__
{: .notice}

```
en
erase startup-config
```

__Configurar a SVI de um Switch__
{: .notice}

```
en
conf t
interface vlan 1
ip address 192.168.1.1 255.255.255.0
no shutdown
```
