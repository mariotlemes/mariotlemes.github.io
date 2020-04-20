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
