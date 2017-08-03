# Notacao-de-Frachen
Uma forma de escrever melodias musicas no computador com textos simples

## Notas musicais
É necessário que você já tenha um conhecimento musical mínino a fim de utilizar essa notação, usaremos a  a notação de Cifras como base de escrita, ou seja, as notas serão representadas pelas letras: A B C D E F G

## Compasso
simbolo: |

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
Entendodo o basico do tempo das notas
a 60BPM 1 = 1s

|np*	| s		| Transcrição |
|-------|-------|-------------|
|		| 6		| +5          |
|1		| 4		| +3          |
|1/2	| 2		| +1          |
|1/4	| 1		|             |
|1/8.	| 0,75	|             |
|1/8	| 	0,5	| .5          |
|1/16.	| 0,37	|             |
|1/16	| 0,25	| .25         |
|1/32.	| 0,18	|             |
|1/32	| 0,12	| .12         |

*Notação em pauta musical convencional

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

## Comentários

Utilize um texto entre o simbolo de * para um comentario

```
C||3) *com pedal* G.5 G.5| A G D | C4+3 |
```
