---
layout: post
title:  "Blink controlado por botão"
date:   2018-04-21
excerpt: "Este projeto mostra como acender o led através de um botão (push button)."
comments: true
---

## Descrição
Este projeto mostra como acender o led através de um botão (push button). Note que o botão é ligado na porta 2 e o led na porta 7. A variável inteira buttonState é responsável por armazenar a leitura do botão, se a mesma estiver pressionada (HIGH), o led é ligado através da função digitalWrite(). Caso contrário, o led é desligado utilizando, da mesma forma, a função digitalWrite().

## Componentes de hardware utilizados
* 1 Arduino uno.
* 1 led difuso 5 mm.
* 1 resistor de 560 ohms.
* 1 resistor de 10k ohms.
* 1 push button.
* Fios de conexão (jumpers).

## Código

{% highlight c %}
/*
Button
Utiliza um botão de pressão, conectado ao pino 2, para ligar e
desligar um LED conectado ao pino digital 13.
*/

int buttonState = 0; // Variável para leitura do estado do botão

// Executa uma vez ao ligar ou reiniciar a placa
void setup() {

  pinMode(ledPin, OUTPUT); //Inicializa o pino do LED como saída (OUTPUT)
  pinMode(buttonPin, INPUT); // Inicializa o pin do botão como entrada (INPUT)
}

// Executa infinitamente quando liga a placa
void loop() {

// Lê o estado do botão (HIGH -> +5V -> botão press.) (LOW -> 0V)
buttonState = digitalRead(buttonPin);

// Testa se o botão está pressionado
// Se sim, o estado do botão e alto (HIGH)

if (buttonState == HIGH) {
  digitalWrite(ledPin, HIGH); // Liga o LED
}
// Senão (Botão não pressionado)
else {
  digitalWrite(ledPin, LOW); // Desliga o LED
  }
}

{% endhighlight %}
