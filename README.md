# Notação linear
Uma forma de escrever melodias musicais no computador com textos simples ou até mesmo a mão, sem a necessidade de uma pauta

## Notas musicais
É necessário que você já tenha um conhecimento musical mínino a fim de utilizar essa notação, usaremos a notação de Cifras como base de escrita, ou seja, as notas serão representadas pelas letras: A B C D E F G

## Compasso
O simbolo de divisão de compasse será **|**

```
ex: | C D E F | G A B C |
```

## Gráus
|Tom | 1 | 2 | 3  | 4 | 5 | 6 | 7  |
|----|---|---|----|---|---|---|----|
|  C | C | D | E  | F | G | A | B  |
|  D | D | E | F# | G | A | B | C# |

### Khz ou intervalos de 8ª

| C3	| D3	| E3	| F3	| G3	| A3	| B3    | A4  | A5   |
|-------|-------|-------|-------|-------|-------|-------|-----|------|
| 261.6	| 293.6	| 329.6	| 349.2	| 391.9	| 440	| 493.8 | 880 | 1760 |
	
O intervalo de uma nota pode ser definido com o número correspondente exatamente após a nota ou no inicio do compasso, nesse caso todas as notas desse compasso e dos próximos estarão na mesma oitava até que seja alterado em um novo compasso ou em casos em que o intervalo esteja especificado na nota,

Exemplo:
```
Forma extensa:   C||  C3 D3 E3 F3 | G3 A3 B3 C4 |
Forma abreviada: C||3 C  D  E  F  | G  A  B  C4 |
                 C||3 C  D  E  F  | G  A  B  C/ |
                 C||3 1  2  3  4  | 5  6  7  1/ |
```

### Representação do da música 
Utilize o simbolo correspondente ao tom desejado no incio da escrita
Exemplo:
```
Para tom em C = C|| 1 2 3 4 | 5 6 7 8 |
Trascrição      C|| C D E F | G A B C |
Para tom em E = E|| E F# G# A | B C# D# E |
```
   
## Sinais de dinâmica

|    |   |
|----|---|
|ppp | { |
|pp  | [ |
|p   | ( |
|mp  | < |
|mf  | > |
|f   | ) |
|ff  | ] |
|fff | } |

Exemplo:
```
Forma extensa:   | C( D( E( F( | G> A> B> C> |
Forma abreviada: | C( D E F | G> A B C |
```

## Tempo das notas
Imaginaremos o seguinte cenario, uma música que está a 60BPM logo teremos uma *batida* por segundo, assim então compreendemos que o tempo inteiro corresponde a **1s**, para demonstrar isso na notação vamos utilizar a seguinte tabela:

|np*	| s	| Transcrição |
|-------|-------|-------------|
|	| 6	| +5          |
|1	| 4	| +3          |
|1/2	| 2	| +1          |
|1/4	| 1	|             |
|1/8.	| 0,75	|             |
|1/8	| 0,5	| .5          |
|1/16.	| 0,37	|             |
|1/16	| 0,25	| .25         |
|1/32.	| 0,18	|             |
|1/32	| 0,12	| .12         |

*Notação em pauta musical convencional

Logo para escrever uma nota *Mi* que ira durar 2 tempos inteiros deve se escrever **E+1**, ou seja, uma nota Mi inteira mais um; para dizer que irar durar meio tempo deve se escrever **E.5**, ou seja, 50% da duração de um tempo inteiro.

Exemplo:
```
| C D E+1 | F.5 G.5 A+1 B |
```
## Formas de escrita

### Exemplo de escrita da nota C (Dó) de meio tempo na 3ª oitava com o tom da música em C

Em graús (Forma completa)
*C|| 13.5*
Em graús com intervalo abreviado
*C||3 1.5*
Em cifra (Forma inteligível)
*C|| C3.5*
Em cifra com intervalo abreviado (Forma inteligível simplificada)
*C||3 C.5*

## Pausa
As pausas são simbolizadas por **-**, e a definicão de sua duração é igual de uma nota.

Exemplo
```
| C D E - | G A -+1|
```

Esse exemplo seria lido da seguinte forma: dó, ré, mi, pausa de um tempo, sol, la, pausa de dois tempos.

## Exemplos

### Música Parabéns a você

#### Com notas de forma abreviada
```
Forma 1: C||3) G.5 G.5 | A G D | C4+3 |
Forma 2: C||3) G.5 G.5 | A G D |4 C+3 |
```

#### Com notas por extenso
```
C||) G3.5  G3.5 | A G D | C4+3 |
```

#### Em Gráus de forma abreviada
```
Forma 1: C||3) 5.5 5.5 | 6 5 2 | 14+3 |
Forma 1: C||3) 5.5 5.5 | 6 5 2 |4 1+3 |
```

#### Em gráus por extenso
```
C||) 53.5 53.5 | 63 53 23 | 14+3 |
```

## Retornos
Em nossa notação não utilizamos o conceito de retornos, mas sim de marcações de partes da música e de chamadas a essas marcações.

### Chamadas simples
Para dizer que iremos tocar o mesmo compaço novamente deve se utizar o simbolo **%** no compaço subsequente.
Exemplo:

```
| C D E F | % |
```

Isso seria o mesmo que escrever

```
| C D E F | C D E F |
```

Após o sinal de **%** podemos colocar o número, referente a quantidade de compassos anteriores que iremos repetir, ou seja, para repetir os ultimos três compassos deve se escrever **%3**

Exemplo:

```
| C D E F | G A B C | %2 |
```

Seria o mesmo que escrever 


```
| C D E F | G A B C |  C D E F | G A B C  |
```

### Referência simples
Para fazer uma referencia simples de execução de compaços anteriores utilizaremos o simbolo **|:** para representar o inicio de uma referência e o símbolo **:|** para realizar uma chamada a referência.

Exemplo:

```
|: C D E F | F F | C D C D | D D | C G F E | E E | C D E F | F F :|

```

Dessa forma dizemos que quando chegarmos a **:|** iremos tocar novamente tudo que estiver depois de **|:**, isso seria o mesmo que tocar:

```
| C D E F | F F | C D C D | D D | C G F E | E E | C D E F | F F | 
| C D E F | F F | C D C D | D D | C G F E | E E | C D E F | F F |
```
### Referência pontual
Uma referencia pontual é quando é especificado um ponto de termino da execução para isso deve-se usar o simbolo **|:|**
Exemplo:

```
|: C D E F | F F |:| C D C D | D D | C G F E | E E :|
```

Conforme o exemplo, iremos tocar toda a música até **:|** ao chegar nesse ponto tocamos de **|:** até **|:|**, seria o mesmo que escrever assim:

```
| C D E F | F F | C D C D | D D | C G F E | E E | C D E F | F F |
```

### Referência pontual avançada
Na referência pontual avançada podemos indicamos o ponto de inicio e de fim da execução referenciada, isso se deve utilizando o simbolo de termino de referencia juntamente com um número, ou seja, utilizamos **|:1|**

Exemplo:
```
| C G |: G - A | F E F D |:1| G C4 :|1| G F E D | C - |
```

O exemplo acima seria o mesmo que escrever 

```
| C G | G - A | F E F D | G C4 | G - A | F E F D | G F E D | C - |
```

Um exemplo com dois terminos de referência
```
 1     2        3            4         5            6
| C G |: G - A | F E F D |:1| G C4 |:2| G F E D :|1| C - :|2|
```

Nesse exemplo foi numerado os compassos afim de ver o momento em que serão repetidos
Escrevendo o exemplo por extenso ficaria dessa forma:

```
 1      2      3         4      5         2       3         6     2       3         4            
| C G | G - A | F E F D | G C4 | G F E D | G - A | F E F D | C - | G - A | F E F D | G C4 |
```

Explicando esse caso: Tocamos do compasso 1 até 5 onde encontramos a chamada para referência **:|1|** (toque da referencia até 1) então tocamos 2 e 3, após isso seguimos no compasso 6, onde temos uma nova chamda de referência, **:|2|** (toque da referencia até 2) então tocamos os compassos 2, 3 e 4

### Referência pontual avançada 2
Outra forma de criar referências é de nomearmos o inicio das referencias utilizando o simbolo de incio de referencia juntamente com um número, da seguinte forma: **|1:** ; Para utilizar ao realizar uma chamada indicaremos o numero do inicio e o número do termino separados por um **-** (hífen), **:|1-1|**

Exemplo:
```
 1       2         3            4         5              6
|1: C G |2: G - A | F E F D |:1| G C4 |:2| G F E D :|2-1| C - :|1-2|
```

Por extenso teremos a seguinte melodia:
```
 1      2       3         4      5        2       3         6     1     2       3         4
| C G | G - A | F E F D | G C4 | G F E D | G - A | F E F D | C - | C G | G - A | F E F D | G C4 |
```


## Comentários

Utilize um texto entre o simbolo de * para um comentario

```
C||3) *com pedal* G.5 G.5| A G D | C4+3 |
```
