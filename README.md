## 📓  Estudos sobre Java
Repositório com anotações que fiz durante estudos e cursos sobre a linguagem Java e o framework Spring Boot, este contéudo está em constante atualização 😜

<br>

## Tabela de conteúdos
- [POO & SOLID](#poo-&-solid)
- [Clean Code](#clean-code)
- [Design Patterns](#design-patterns)
- [Clean Architecture](#clean-architecture)

<br>

## POO & SOLID
### Single Responsibility Principle
- Just because you can, doesn't mean you should
- Uma classe deveria ter apenas um único motivo para mudar
- Focando em manter a coesão do código
###  Open Closed Principle
- Entidades devem estar abertas para extensão, porém fechadas para modificação
### Liskov Substitution Principle
- "Se parece com um pato, se faz 'quack' igual um pato, mas precisa de baterias, então não é um pato, você está usando uma abstração errada"
- Quando há herança é utilizada de maneira errada pode causar comportamentos indesejados no código, e irá ferir o princiopio de Liskov. Não é só porque a entidade é parecida que pode ser herdada
### Interface Segregation Principle
- "Uma interface não deveria ser forçada a depender de métodos que não utilizará"
- Uma classe não deve ser obrigada a implementar um método de determinada interface se ele não for útil
### Dependency Inversion Principle
- "Abstrações não devem depender de implementações. Implementações devem depender de abstrações"
- Ex: caso uma determinada implementação mude, o código não será afetado, pois depende apenas de sua interface

### Princípios de Orientação a Objetos
- Coesão 
	- "União harmônica entre uma coisa e outra"
	- Uma classe tem que ser coesa possui metodos e atributos que façam sentido com o seu propósito
	- Classes com uma única responsabilidade
	- Classes não coesas tendem a crescer indefinidamente, o que as tornam difíceis de manter
- Encapsulamento
	- "Incluir ou proteger alguma coisa em uma cápsula"
	- "Blindar" uma classe contra influencias externas
	- Classes não enacpsuladas permitem violação de regras de negócio, além de aumentarem o acoplamento
- Acoplamento
	- "Ação de acoplar. Agrupamento aos pares"
	- Quando uma classe conhece muitos detalhes de outra
	- Classes acopladas causam fragilidade no código da aplicação (qualquer mudança em um ponto pode impactar muitos lugares no código), o que dificulta sua manutenção

### Pontos de atenção:
-  Interfaces são menos propensas a sofrer mudanças enquanto implementações podem mudar a qualquer momento

<br>

## Clean Code
Considerações na hora de escrever o código:
- Ele está legivel e organizado? Os nomes estão semânticos?
	- Quanto mais fácil for ler o código menos esorço fazemos para entendê-lo
- Está testável?
	- Para você ter segurança na hora de realizar alterações é importante que o código te possibilite escrever testes

<br>

## Design Patterns
Design Pattern: Solução comum para um problema recorrente ao utilizar o paradigma da orientação a objetos

Categorias:
- Criacionais
	- Foco em criação de objetos
- Estruturais
	- Como as classes se relacionam entre si
- Comportamentais
	- Foco em métodos, estados, interação das classes

## Clean Architecture
Design de código vs Arquitetura: a arquitetura é uma visão de alto nivel de como você vai modelar seu sistema, por exemplo como você organiza seus pacotes (clean arch, hexagonal arch ...) já o design é uma visão de nivel mais baixo, do código em si (SOLID, DDD, Design Patterns ...)

Id não é um conceito do dominio da aplicação, o pessoal de negócios não fala sobre o Id, nós assumimos isso por trabalharmos com banco de dados relacionais, adicionando o ID no dominio nós levamos uma questão de infraestrutura para ele e de acordo com o Clean Arch o dominio tem que ser totalmente desacoplado dela.

Entidade: objeto que conseguimos diferenciar por meio de alguma identificação, ex: cpf
Value Object: objeto que não possui identificação 
