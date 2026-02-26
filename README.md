# Notação Linear
Uma forma de escrever melodias musicais no computador com textos simples ou até mesmo à mão, sem a necessidade de uma pauta

## Notas musicais
É necessário que você já tenha um conhecimento musical mínimo a fim de utilizar essa notação. Usaremos a notação germânica como base de escrita, ou seja, as notas serão representadas pelas letras: A B C D E F G

Acidentes são representados pelo símbolo **#** (sustenido) e **b** (bemol) logo após a letra da nota. Exemplo: **F#** (Fá sustenido), **Bb** (Si bemol).

Entenda mais sobre a notação germânica [clicando aqui](https://pt.wikipedia.org/wiki/ABC_(nota%C3%A7%C3%A3o_musical))

## Compasso
O símbolo de divisão de compasso será **|**, para representar o início da música utilizamos uma marcação dupla de compasso **||**, todo elemento de configuração da notação deve ser colocado após essa referência

```
ex: || C D E F | G A B C |
```

A ordem dos elementos de configuração após `||` é: **Tom**, **Fórmula de compasso** e **Oitava**, todos opcionais.

```
|| [tom] [fórmula] [oitava] notas...
```

Obs: a marcação `||` pode ser utilizada no meio de uma notação para mudar as configurações

## Representação do tom da música
Utilize o símbolo (letra) correspondente ao tom desejado logo após o `||`

Exemplo:
```
Tom em C: || C C D E F | G A B C |
Tom em E: || E E F# G# A | B C# D# E |
```

## Fórmula de compasso
A fórmula de compasso indica quantos tempos cabem em cada compasso e qual figura vale um tempo. Ela é representada no formato tradicional (ex: **4/4**, **3/4**, **6/8**) e posicionada após o tom.

Exemplo:
```
|| C 4/4 C D E F | G A B C |
|| D 3/4 D E F | G A B |
|| C 6/8 C D E F G A | B C D E F G |
```

## Oitavas

| C4    | D4    | E4    | F4    | G4    | A4   | B4    | C5    |
| ----- | ----- | ----- | ----- | ----- | ---- | ----- | ----- |
| 261,6 | 293,7 | 329,6 | 349,2 | 392,0 | 440  | 493,9 | 523,3 |

A oitava padrão da notação é a **4ª oitava** (onde se encontra o dó central do piano, C4 = 261,6 Hz). Quando nenhuma oitava é especificada, todas as notas são interpretadas na 4ª oitava.

A oitava de uma nota pode ser definida com o número correspondente exatamente após a nota ou no início do compasso. Nesse caso, todas as notas desse compasso e dos próximos estarão na mesma oitava até que seja alterado em um novo compasso ou em casos em que a oitava esteja especificada na nota.

Exemplo:
```
Forma extensa:   || C 4/4  C4 D4 E4 F4 | G4 A4 B4 C5 |
Forma abreviada: || C 4/4 4 C  D  E  F | G  A  B  C5 |
                 || D 4/4 4 D  E  F# G | A  B  C# D5 |
```

## Tempo das notas
Imaginaremos o seguinte cenário: uma música que está a **60BPM**, logo teremos uma *batida* por segundo, assim então compreendemos que o tempo inteiro corresponde a **1s**. Para demonstrar isso na notação vamos utilizar a seguinte tabela:

| Notação tradicional* | Duração (tempos) | Transcrição |
| -------------------- | ---------------- | ----------- |
| 1.                   | 6                | +5          |
| 1                    | 4                | +3          |
| 1/2.                 | 3                | +2          |
| 1/2                  | 2                | +1          |
| 1/4.                 | 1,5              | +.5         |
| *1/4*                | *1*              |             |
| 1/8.                 | 0,75             | .75         |
| 1/8                  | 0,5              | .5          |
| 1/16.                | 0,375            | .375        |
| 1/16                 | 0,25             | .25         |
| 1/32.                | 0,1875           | .1875       |
| 1/32                 | 0,125            | .125        |

*Notação em pauta musical convencional

Logo, para escrever uma nota *Mi* que irá durar 2 tempos inteiros deve-se escrever **E+1**, ou seja, uma nota Mi inteira mais um; para dizer que irá durar meio tempo deve-se escrever **E.5**, ou seja, 50% da duração de um tempo inteiro.

Exemplo:
```
| C D E+1 | F.5 G.5 A+1 B |
```

> **Regra de leitura:** A ordem de leitura é: **Nota + Oitava (opcional, 1 dígito) + Duração (opcional, .X ou +X)**. Exemplo: `E4.5` = nota Mi, 4ª oitava, meio tempo.

> **Importante:** Um número isolado após a nota **sempre** indica oitava, **nunca** duração. A duração obrigatoriamente utiliza os prefixos **+** ou **.**. Portanto `E4` = Mi na 4ª oitava, enquanto `E+3` = Mi com duração de 4 tempos (semibreve).

### Exemplo completo

Escrita da nota C (Dó) de meio tempo na 4ª oitava com o tom da música em C:

- Forma completa: `|| C 4/4 C4.5`
- Forma abreviada: `|| C 4/4 4 C.5`

## Pausa
As pausas são simbolizadas por **-**, e a definição de sua duração é igual à de uma nota.

Exemplo
```
| C D E - | G A -+1|
```

Esse exemplo seria lido da seguinte forma: dó, ré, mi, pausa de um tempo, sol, lá, pausa de dois tempos.

## Anacruse
O símbolo **)** após a marcação de início indica que as notas seguintes, antes do primeiro compasso, são uma **anacruse** (notas que antecedem o primeiro tempo forte da música).

Exemplo:
```
|| C 4/4 4) G.5 G.5 | A G D | C5+3 |
```
Neste caso, `G.5 G.5` são as notas da anacruse, tocadas antes do primeiro tempo forte.

## Ligadura
Para indicar ligadura entre as notas utiliza-se o símbolo **~** na nota anterior à que será ligada

Exemplo:

```
| C D E F~ | F G A B |
```

## Acordes
Para indicar que mais de uma nota será tocada ao mesmo tempo basta colocá-las entre **[ ]**. Uma observação é que a duração da nota pode ser descrita apenas após o conjunto, sendo assim todas as notas terão a mesma duração

Exemplo:
```
| [C5 G4 C4]+1 A D |
```

## Comentários

Utilize um texto entre chaves **{ }** para um comentário

```
|| C 4/4 4) {com pedal} G.5 G.5| A G D | C5+3 |
```

## Retornos
Em nossa notação não utilizamos o conceito de retornos, mas sim de marcações de partes da música e de chamadas a essas marcações.

### Chamadas simples
Para dizer que iremos tocar o mesmo compasso novamente deve-se utilizar o símbolo **%** no compasso subsequente.
Exemplo:

```
| C D E F | % |
```

Isso seria o mesmo que escrever

```
| C D E F | C D E F |
```

Após o sinal de **%** podemos colocar o número referente à quantidade de compassos anteriores que iremos repetir, ou seja, para repetir os últimos três compassos deve-se escrever **%3**

Exemplo:

```
| C D E F | G A B C | %2 |
```

Seria o mesmo que escrever


```
| C D E F | G A B C |  C D E F | G A B C  |
```

### Referência simples
Para fazer uma referência simples de execução de compassos anteriores utilizaremos o símbolo **|:** para representar o início de uma referência e o símbolo **:|** para realizar uma chamada à referência.

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
Na referência pontual podemos indicar qual o ponto de início da execução referenciada será repetido, utilizando o símbolo de início de referência juntamente com um número da seguinte forma **|1:**, e na chamada será utilizado o número referente à referência desejada, **:1|**

Exemplo:
```
| C G |1: G - A | F E F D |: G C5 | G F E D | C - :1|
```

O exemplo acima seria o mesmo que escrever

```
| C G | G - A | F E F D | G C5 | G F E D | C - | G - A | F E F D | G C5 | G F E D | C - |
```

Um exemplo com dois pontos de referência
```
 1     2        3           4        5           6
| C G |1: G - A | F E F D |2: G C5 | G F E D :1| C - :2|
```

Nesse exemplo foram numerados os compassos a fim de ver o momento em que serão repetidos.
Escrevendo o exemplo por extenso ficaria dessa forma:

```
 1      2      3         4      5         2       3
| C G | G - A | F E F D | G C5 | G F E D | G - A | F E F D |
  4      5         6     4      5         6
| G C5 | G F E D | C - | G C5 | G F E D | C - |
```

Explicando esse caso: Tocamos do compasso 1 até 5 onde encontramos a chamada para referência **:1|** (toque da referência 1 até aqui) então tocamos 2 a 5, após isso seguimos no compasso 6, onde temos uma nova chamada de referência, **:2|** (toque da referência 2 até aqui) então tocamos os compassos 4, 5 e 6 novamente

### Referência pontual avançada
Também é possível indicar o término de uma repetição, para isso basta que em sua chamada seja indicada a referência de início e fim separados por um **-** (hífen), **:1-2|**

Exemplo:
```
 1       2         3            4         5              6
|1: C G |2: G - A | F E F D |3: G C5 |4: G F E D :|2-3| C - :|1-4|
```

Por extenso teremos a seguinte melodia:
```
 1      2       3         4      5        2       3         6     1     2       3         4
| C G | G - A | F E F D | G C5 | G F E D | G - A | F E F D | C - | C G | G - A | F E F D | G C5 |
```

## Exemplos

### Música Parabéns a Você

#### Com notas de forma abreviada
```
Forma 1: || C 4/4 4) G.5 G.5 | A G D | C5+3 |
Forma 2: || C 4/4 4) G.5 G.5 | A G D |5 C+3 |
```

#### Com notas por extenso
```
|| C 4/4) G4.5 G4.5 | A G D | C5+3 |
```

### Ode à Alegria — 9ª Sinfonia de Beethoven (4º Movimento)

```
|| D 4/4 4 |1: F# F# G A | A G F# E | D D E F# |2: F#+.5 E.5 E+1 :|1-2| E+.5 D.5 D+1 | E E F# D | E F#.5 G.5 F# D | E F#.5 G.5 F# E | D E A3+1 :|1-2| E+.5 D.5 D+1 |
```

Nesse exemplo, `:|1-2|` repete os compassos da referência 1 até a referência 2 (os três primeiros compassos do tema). Isso é utilizado duas vezes: primeiro para a repetição do tema A com um final diferente, e depois para o retorno do tema A após a seção B.

Por extenso a melodia ficaria assim:
```
{Tema A - 1º final}
| F# F# G A | A G F# E | D D E F# | F#+.5 E.5 E+1 |
{Tema A - 2º final}
| F# F# G A | A G F# E | D D E F# | E+.5 D.5 D+1 |
{Seção B}
| E E F# D | E F#.5 G.5 F# D | E F#.5 G.5 F# E | D E A3+1 |
{Tema A - retorno}
| F# F# G A | A G F# E | D D E F# | E+.5 D.5 D+1 |
```
