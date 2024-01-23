# Solid
![Solid](https://miro.medium.com/v2/resize:fit:1191/1*OzwARbvHUg1RlZ7LYyLCrg.png)

Os princípios SOLID são os princípios de design que nos permitem gerenciar vários problemas de design de software. Robert C. Martin compilou esses princípios na década de 1990. Esses princípios nos fornecem maneiras de passar de código fortemente acoplado e pouco encapsulamento para os resultados desejados de necessidades reais de negócios fracamente acoplados e encapsulados de maneira adequada. SOLID é um acrônimo para o seguinte.

- **S:** Princípio de Responsabilidade Única (SRP)
- **O:** Princípio Aberto-Fechado (OCP)
- **L:** Princípio de substituição de Liskov (LSP)
- **I:** Princípio de Segregação de Interface (ISP)
- **D:** Princípio de Inversão de Dependência (DIP)


## Princípio de Responsabilidade Única (SRP)
![Pesponsabilidade Única](https://miro.medium.com/v2/resize:fit:1400/1*KPWLpdpYemtLxaNH5MvT_A.png)

O princípio de responsabilidade única é geralmente definido como: Um objeto deve ter apenas um motivo para mudar; quanto maior o arquivo ou a classe, mais difícil será para ele atingir isto. 

Isso significa que cada classe ou estrutura semelhante em seu código deve ter apenas um trabalho. Tudo nessa aula deve estar relacionado a um único propósito. Nossa aula não deve ser como um canivete suíço onde se um deles precisar ser trocado, toda a ferramenta precisará ser alterada. Isso não significa que suas classes devam conter apenas um método ou propriedade. Pode haver muitos membros, desde que se relacionem com uma única responsabilidade.

## Princípio Aberto-Fechado (OCP)
Aberto à extensão, mas fechado à modificação

Devemos projetar nosso módulo/classe para que a nova funcionalidade possa ser adicionada somente quando novos requisitos forem gerados. "Fechado para modificação" significa que já desenvolvemos uma classe e ela passou por testes unitários. Não devemos então alterá-lo até encontrarmos bugs.


## Princípio de substituição de Liskov (LSP)
![LSP](https://miro.medium.com/v2/resize:fit:1400/1*iV_TeHoEDE0TwhQEFj2fxA.png)

Você deve ser capaz de usar qualquer classe derivada em vez de uma classe pai e fazer com que ela se comporte da mesma maneira sem modificaçãoocê deve ser capaz de usar qualquer classe derivada em vez de uma classe pai e fazer com que ela se comporte da mesma maneira sem modificação
O princípio de substituição de Liskov define algumas instruções para manter a substituição do herdeiro. Transferir um herdeiro de objetos em lugar da classe base não deve quebrar nenhuma funcionalidade existente no método chamado. Você deve ser capaz de substituir todas as implementações de uma determinada interface entre si.

Este princípio é apenas uma extensão do Princípio Aberto e Fechado, e devemos garantir que as classes recém-derivadas estendam as classes base sem alterar seu comportamento. Explicarei isso com um exemplo do mundo real que viola o LSP.

## Princípio de Segregação de Interface (ISP)
![](https://miro.medium.com/v2/resize:fit:1400/1*XexgJFeS88wcllcxFFqklQ.png)

Os clientes não devem ser forçados a implementar interfaces que não usam. Em vez de uma interface gorda, muitas interfaces pequenas são preferidas com base em grupos de métodos, cada um servindo um submódulo

Cada interface deve ter um fim específico. Você não deve ser forçado a implementar uma interface quando seu objeto não compartilha aquele fim. Por extrapolação, quanto maior a interface, mais provável que ela inclua métodos que nem todos os implementadores possam alcançar. Esta é a essência do princípio de Segregação de interface.

Os métodos na interface são definidos por quais métodos o código do cliente precisa, em vez de quais métodos a classe implementa. Portanto, os clientes não devem ser forçados a depender de interfaces que não utilizam.

## Princípio de Inversão de Dependência (DIP)

Módulos/classes de alto nível não devem depender de módulos/classes de baixo nível

Isso significa que quando precisarmos incluir uma classe como uma dependência, devemos tentar evitar nos referir a classes concretas (a implementação real), mas em vez disso, nos referir a abstrações, como as interfaces ou classes abstratas que as classes concretas implementam ou subclasse .

- Não se refira a classes concretas. Consulte interfaces abstratas. Isso impõe uma restrição na criação de objetos e geralmente impõe o uso de Abstract Factories.
- Não derive de classes concretas voláteis.
- Não substitua funções concretas. Eles exigem dependências de código-fonte
- Nunca mencione o nome de nada concreto.

## Conclusão

SOLID é um acrônimo para cinco princípios de design de código orientado a objetos que foram definidos por Robert C. Martin, mais conhecido como Uncle Bob. Esses princípios são projetados para tornar o código mais flexível, modular e escalável.
Os cinco princípios SOLID são:

- Single Responsibility Principle (SRP): Cada classe ou módulo deve ter apenas uma responsabilidade.
- Open-Closed Principle (OCP): Classes ou módulos devem ser abertos para extensão, mas fechados para modificação.
- Liskov Substitution Principle (LSP): Subclasses devem poder ser substituídas por suas superclasses sem afetar o comportamento do sistema.
- Interface Segregation Principle (ISP): Classes não devem ser forçadas a depender de métodos que não usam.
- Dependency Inversion Principle (DIP): Classes de alto nível não devem depender de classes de baixo nível, mas sim de abstrações.

# Fontes
https://www.c-sharpcorner.com/UploadFile/damubetha/solid-principles-in-C-Sharp/
https://learn.microsoft.com/pt-br/archive/msdn-magazine/2014/may/csharp-best-practices-dangers-of-violating-solid-principles-in-csharp
https://khalilstemmler.com/wiki/dependency-inversion/
