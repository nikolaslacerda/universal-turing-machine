# Universal Turing Machine
A universal turing machine in JFLAP

$0^k+1 * <M> $ ^ x
  
<M> = 0001011 onde 00(estado) 0(lê) 10(próximo estado) 1(escreve) 1(direita (1), esquerda(0))
x = entrada
  
0 <-> Z

1 <-> U

B <-> W

## 1: Get :heavy_check_mark:

- Vai até o ^ e pega o simbolo a direita
- Trás esse simbolo até uma casa antes do primeiro *
- Volta para o primeiro $

##### Começa: No primeiro $
##### Termina: No primeiro $

## 2: Find :heavy_check_mark:

- Se só tem letras até o primeiro *
  - Vai até o primeiro número
  - Vai para a maquina fetch
- Lê o primeiro simbolo não letra e substitui por letra (na memoria)
- Vai até a primeira não letra depois de um *
- Se o simbolo não bater, substitui por letras até o próximo *
  - Volta até o primeiro $
  - Substitui (na memoria) as letras por números até o primeiro *
  - Volta até o primeiro $
  - Recomeça
- Se bater substitui esse simbolo por letra
  - Volta até o primeiro $
  - Recomeça
  
##### Começa: No primeiro $
##### Termina: No primeiro simbolo depois de letras

## 3: Fetch :heavy_check_mark:

- Pega o simbolo e substitui ele por letra
- Vai até o primeiro $
- Escreve na próxima letra o simbolo que pegou
- Vai até o próximo simbolo não letra
- Se só tem simbolos não letras até o primeiro * termina
- Se não recomeça

##### Começa: No primeiro simbolo depois de letras (nas transições)
##### Termina: No primeiro *

## 4: Execute :heavy_check_mark:

- Volta uma casa
- Pega o simbolo
- Vai até a direita do ^
- Escreve o simbolo
- Volta até o primeiro $

##### Começa: No primeiro *
##### Termina: No primeiro $

## 5: Movehead :heavy_check_mark:

- Vai até o primeiro 0 ou 1
- Pega o numero
- Vai até o ^
- Lê o simbolo do lado referente ao numero
- Troca o simbolo com o ^

##### Começa: No primeiro $
##### Termina: A direita do segundo $

## 6: Clean :heavy_check_mark:

- Vai até o primeiro $ trocando as letras por seus respectivos simbolos

##### Começa: A direita do segundo $
##### Termina: No primeiro $
