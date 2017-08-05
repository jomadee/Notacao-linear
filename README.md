# Notação linear
Uma forma de escrever melodias musicais no computador com textos simples ou até mesmo a mão, sem a necessidade de uma pauta

## Notas musicais
É necessário que você já tenha um conhecimento musical mínino a fim de utilizar essa notação, usaremos a notação de Cifras como base de escrita, ou seja, as notas serão representadas pelas letras: A B C D E F G

## Compasso
O simbolo de divisão de compasso será **|**, para representar o inicio da música utilizamos uma marcação dupla de compasso **||**, todo elemento de configuração da notação deve ser colocado antes dessa referência 

```
ex: || C D E F | G A B C |
```
Obs: a marcação de início da música pode ser utilizado no meio de uma notação para mudar as configurações

## Gráus
Grau musical é uma nomenclatura criada para ajudar o músico na localização dos intervalos. 

Gráus na escala maior de **C** e **D**

|Tom | 1º | 2º | 3º  | 4º | 5º | 6º | 7º  |
|----|----|----|-----|----|----|----|-----|
| C  | C  | D  | E   | F  | G  | A  | B   |
| D  | D  | E  | F#  | G  | A  | B  | C#  |


### Representação do tom da música 
Utilize o simbolo (letra) correspondente ao tom desejado no início da escrita seguido de uma barra de compasso

Exemplo:
```
Para tom em C = C|| 1 2 3 4 | 5 6 7 8 |
Trascrição      C|| C D E F | G A B C |
Para tom em E = E|| E F# G# A | B C# D# E |
```

### Khz ou intervalos de 8ª

| C3	| D3	| E3	| F3	| G3	| A3	| B3    | A4  | A5   |
|-------|-------|-------|-------|-------|-------|-------|-----|------|
| 261.6	| 293.6	| 329.6	| 349.2	| 391.9	| 440	| 493.8 | 880 | 1760 |
	
O intervalo de uma nota pode ser definido com o número correspondente exatamente após a nota ou no inicio do compasso, nesse caso todas as notas desse compasso e dos próximos estarão na mesma oitava até que seja alterado em um novo compasso ou em casos em que o intervalo esteja especificado na nota,

Exemplo:
```
Forma extensa:   C||  C3 D3 E3 F3 | G3 A3 B3 C4 |
Forma abreviada: C||3 C  D  E  F  | G  A  B  C4 |
		 C||3 1  2  3  4  | 5  6  7  14 |
		 D||3 D  E  F# G  | A  B  C# D4 |				 
                 D||3 1  2  3  4  | 5  6  7  14 |
```

    
## Sinais de dinâmica

|    |     |
|----|-----|
|ppp | >>> |
|pp  | >>  |
|p   | >   |
|mp  | <>  |
|mf  | ><  |
|f   | <   |
|ff  | <<  |
|fff | <<< |

Exemplo:
```
Forma extensa:   | C< D< E< F< | G> A> B> C> |
Forma abreviada: |< C D E F |> G A B C |
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
Na referência pontual podemos indicamos qual o ponto de inicio de execução referenciada irá ser repetido, isso se deve utilizando o simbolo de incio de referencia juntamente com um número da seguinte forma **|1:**, e na chamada irá ser utilizado o numéro referente a referência desejada, **:1|**

Exemplo:
```
| C G |1: G - A | F E F D |: G C4 | G F E D | C - :1|
```

O exemplo acima seria o mesmo que escrever 

```
| C G | G - A | F E F D | G C4 | G F E D | C - | G - A | F E F D | G C4 | G F E D | C - |
```

Um exemplo com dois pontos de referência
```
 1     2        3           4        5           6
| C G |1: G - A | F E F D |2: G C4 | G F E D :1| C - :2|
```

Nesse exemplo foi numerado os compassos afim de ver o momento em que serão repetidos
Escrevendo o exemplo por extenso ficaria dessa forma:

```
 1      2      3         4      5         2       3           
| C G | G - A | F E F D | G C4 | G F E D | G - A | F E F D | 
  4      5         6     4      5         6
| G C4 | G F E D | C - | G C4 | G F E D | C - |
```

Explicando esse caso: Tocamos do compasso 1 até 5 onde encontramos a chamada para referência **:1|** (toque da referencia 1 até aqui) então tocamos 2 à 5, após isso seguimos no compasso 6, onde temos uma nova chamda de referência, **:2|** (toque da referencia 2 até aqui) então tocamos os compassos 4, 5 e 6 novamente

### Referência pontual avançada
Também é possível indicar o término de uma repetição, para isso basta que em sua chamada sejá indicado a referencia de inicio e fim separados por um **-** (hífen), **:1-2|**

Exemplo:
```
 1       2         3            4         5              6
|1: C G |2: G - A | F E F D |3: G C4 |4: G F E D :|2-3| C - :|1-4|
```

Por extenso teremos a seguinte melodia:
```
 1      2       3         4      5        2       3         6     1     2       3         4
| C G | G - A | F E F D | G C4 | G F E D | G - A | F E F D | C - | C G | G - A | F E F D | G C4 |
```

## Ligadura
Para indicar ligadura entre as notas utiliza-se o símbolo **~** na nota anterior a que será ligada

Exemplo:

```
| C D E F~ | F G A B |
```

## Acordes
Para indicar que mais de uma nota sera tocada ao mesmo tempo utilizamos o simbolo **^** entre as notas desejadas, uma observação é que a duração da nota pode ser descrita apenas na última nota do conjunto, sendo assim todas as anteriores terão a mesma duração

Exemplo
```
| C4^G3^C3+1 A D |
```

## Comentários

Utilize um texto entre o simbolo de * para um comentario

```
C||3) *com pedal* G.5 G.5| A G D | C4+3 |
```
