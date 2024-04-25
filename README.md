#


int INDICE = 13, SOMA = 0, K = 0;

enquanto K < INDICE faça

{

K = K + 1;

SOMA = SOMA + K;

}

imprimir(SOMA);

1° questão 
K = 0, SOMA = 0 (antes do loop)
K = 1, SOMA = 1
K = 2, SOMA = 3
K = 3, SOMA = 6
K = 4, SOMA = 10
K = 5, SOMA = 15
K = 6, SOMA = 21
K = 7, SOMA = 28
K = 8, SOMA = 36
K = 9, SOMA = 45
K = 10, SOMA = 55
K = 11, SOMA = 66
K = 12, SOMA = 78
K = 13, SOMA = 91
Portanto, ao final do processamento, o valor da variável SOMA será 91.

2° questão
Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.
package Fibonacci;

public class Fibonacci {

 

      public static boolean isFibonacci(int number) {
        int[] sequence =new int[number];
        if (number == 0 || number == 1){
            return true;
        }
        sequence[0] = 0;
        sequence[1]= 1;
        while (sequence[1] < number) {
            int temp = sequence[0];
            sequence[0] = sequence[1];
            sequence[1] = sequence[1] + temp;
        }
        return sequence[1] == number;
    }
}


3- Descubra a lógica e complete o próximo elemento:



a) 1, 3, 5, 7, ___

b) 2, 4, 8, 16, 32, 64, ____

c) 0, 1, 4, 9, 16, 25, 36, ____

d) 4, 16, 36, 64, ____

e) 1, 1, 2, 3, 5, 8, ____

f) 2,10, 12, 16, 17, 18, 19, ____


1-
n=numero impar
n=1+2=3
n=3+2=5
n=5+2=7
n=7+2=9


2- 2x2=4; 
  4x2=8
  8x2=16
  16x2=32
  32x2=64
  64x2=128


3-(+1, +3, +5, +7, +9, +11, +13)



4-
n=numero par 
n=(n)²
n=(4)²=16

5-
1+1=2, 1+2=3, 2+3=5, 3+5=8, 5+8=13.

6-baseado na seguencia de palavras 
dez, doze...
r=200

seguencia da resposta : 9,128,49,100,13,200

4° Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em uma sala diferente. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada.

Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada



Ligo o interruptor  1 por 3 minutos e o desligo, ligo oo interruptor 2 e na mesma hora vou até uma das 3 salas
- Se a lampada estiver acessa, pertence ao interruptor 2, se estiver desligada e quente pertence ao interruptor 1, se estiver desligada e fria pertence ao interruptor 3.

Na segunda ida:
- Sabendo já a qual pertence um interruptor, apenas deixo um ligado e outro desligado entre o restantes
- Vou até outra sala e descubro os outros dois.

5°  
Escreva um programa que inverta os caracteres de um string.
package InverteString;

public class InverteString {


    public static void inverteString(String str) {
        StringBuilder inversa = new StringBuilder();
        for (int i = str.length() - 1; i >= 0; i--) {
            inversa.append(str.toCharArray()[i]);
        }
        System.out.printf("Palavra invertida: %s\n", inversa);
    }
}


