---
layout: page
title: CCNA1v6 - Introdução às redes
#tags: [, Jekyll, theme, moon]
date: 2020-04-20
comments: true
---

__Modos de execução no ios da Cisco__
{: .notice}

1) Execução de usuário -> Switch__>__
2) Execução de usuário privilegiado -> Switch__#__
3) Configuração global -> Switch__#(conf t)__
4) Submódulo de configuração de console -> Switch__#(conf-line)__
5) Submódulo de configuração de interface -> Switch__#(conf-if)__
6) ...

__Modos de navegação no ios da Cisco__
{: .notice}

Switch> -> __enable__ -> Switch# -> __configure terminal__ -> Switch#(conf t) -> interface fastethernet 0/1 -> Switch#(conf-if) -> line console 0 -> Switch#(conf-line) -> exit -> Switch#(conf t) -> exit/end -> Switch# -> disable -> Switch>
