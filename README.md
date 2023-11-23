## A3 | SISTEMAS COMPUTACIONAIS E SEGURANÇA




> *INTRO*

Você é um engenheiro de segurança da informação recém-contratado em uma empresa de desenvolvimento de software. A empresa está preocupada com a segurança de suas aplicações e sistemas, especialmente em relação às vulnerabilidades que envolvem operações aritméticas binárias. Sua tarefa é realizar uma análise abrangente de segurança em uma fonte de código fornecida e propor melhorias para proteção contra ataques de injeção de código e estouro de buffer relacionados a operações binárias.




> PROPOSTA

- *Analisar o Código Recebido*
- *identificar as Vulnerabilidades do Código*
- *Propor Melhoriaas*
- *Implementar um  Código*


___

## PROJETO



>**ANÁLISE DO CÓDIGO**

Este relatório aborda uma análise de segurança em um trecho de código Java responsável pela realização de operações binárias. A análise concentra-se na identificação de ameaças potenciais, como injeção de código e erros relacionados com a segurança das aplicações e sistemas, especialmente em relação às vulnerabilidades associadas às operações aritméticas binárias. 
O código original foi submetido a uma avaliação, levando em consideração a qualidade do código, a identificação de vulnerabilidades e propostas de melhorias. A entrega final inclui um novo código com as melhorias descobertas, garantindo que as operações binárias sejam realizadas de maneira segura e eficaz.

> **IDENTIFICAÇÃO DAS  VULNERABILIDADS**

1. *Validação de Entrada:*
• Vulnerabilidade: O código não valida se os valores inseridos (valor1 e valor2) representam números binários válidos (compostos apenas por '0' e '1'). Isso deixa a aplicação vulnerável a ataques de injeção de código, onde um usuário mal-intencionado pode fornecer valores que não são binários, explorando a lógica do programa.
Isso pode resultar em resultados inesperados, cálculos incorretos e até mesmo em comportamento inseguro, dependendo da manipulação do código fornecido pelo usuário.

2. *Operação de Divisão por Zero:*
• Vulnerabilidade: Não há verificação para garantir que valor2 não seja zero antes de realizar uma operação de divisão. Isso pode levar a erros de tempo de execução, como a exceção de divisão por zero.
Além de falhas no programa, essa vulnerabilidade pode ser explorada para negação de serviço (DoS) se um ataque intencional for fornecido valor2 como zero, causando uma interrupção do programa.

3. *Erros de Digitação:*
• Vulnerabilidade: Corrija os erros de digitação, pois isso resultará em um erro de compilação.
O programa não será compilado corretamente, ou será uma vulnerabilidade em si, pois a aplicação ficará inutilizável devido a um erro de sintaxe.


> **PROPOSTAS DE MELHORIAS**

1. *Validação de entrada:*
Adicione uma função de validação para verificar se os valores fornecidos contêm apenas '0' e '1'. Se a validação falhar, exiba uma mensagem de erro e execute a execução ou solicite uma nova entrada.
Isso reduzirá o risco de injeção de código, garantindo que apenas valores binários válidos sejam processados.

2. *Verificação de Divisão por Zero:*
Antes de realizar a operação de divisão, verifique se valor2 é diferente de zero. Se valor2 for zero, exiba uma mensagem de erro e encerre a execução ou solicite uma nova entrada.
Isso evitará erros de tempo de execução e prevenirá possíveis ataques de negação de serviço.

3. *Limitação de Tamanho:*
 Para evitar estouro de buffer, você pode impor limites no tamanho dos valores binários que podem ser fornecidos, garantindo que não excedam um certo número de bits.

4. *Tratamento de Exceções:*
 Utilize tratamento de exceções para lidar com casos inesperados e erros de validação, garantindo que o programa não quebre inesperadamente.

Essas melhorias corrigirão as vulnerabilidades identificadas, e tornarão o código mais robusto e resistente a falhas, promovendo boas práticas de segurança e desenvolvimento de software.
Além disso, recomendo revisar e validar cada linha do código em busca de vulnerabilidades específicas.
___


## IMPLEMENTAÇÃO DO CÓDIGO COM AS MELHORIAS


Essas melhorias corrigirão as vulnerabilidades identificadas, e tornarão o código mais robusto e resistente a falhas, promovendo boas práticas de segurança e desenvolvimento de software.


___
## 🔗 Link

[CÓDIGO](https://github.com/amandaevans19/Analise-de-Codigo/blob/main/.gitignore)
