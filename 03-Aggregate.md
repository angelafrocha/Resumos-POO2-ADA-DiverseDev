# Aggregate na modelagem de domínios

Um padrão muito utilizado no DDD é o padrão agreggate, que auxiliar no agrupamento de funcionalidades de um objeto de domínio partindo sempre de uma raiz de agregação (aggregate root).

## Raíz agregada

A raiz agregada serve como ponto de entrada para acessar e modificar o estado interno do agregado, protegendo sua integridade e aplicando regras de negócios. Ao focar nos agregados, o DDD incentiva um design granular e centrado no domínio que se alinha ao espaço do problema, em vez de considerações técnicas. Em outras palavras, 

![Order Aggregate](https://learn.microsoft.com/pt-br/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/media/net-core-microservice-domain-model/vs-solution-explorer-order-aggregate.png)

Ter um meio de raiz de agregação significa que a maioria do código relacionado à consistência e às regras de negócio das entidades da agregação deve ser implementada como métodos na classe raiz agregada de Ordem. Portanto, não se deve criar nem atualizar objetos OrderItems de modo independente ou direto; a classe AggregateRoot deve manter o controle e a consistência de qualquer operação de atualização com relação às suas entidades filho.

## Encapsulamento de dados nas entidades de Domínio

![Raizes de agregação](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*PBHIxQ_6i5R0dm3V)

Para seguir padrões DDD, as entidades não devem ter setters públicos em nenhuma propriedade de entidade. Desse modo, alterações em uma entidade devem ser controladas pelos métodos explícitos com linguagem ubíqua explícita sobre a alteração que estão sendo executadas na entidade. Para isso, todos os setters devem ser privados ou, pelo menos, somente leitura externamente, de modo que qualquer operação contra os dados da entidade ou suas entidades filho deve ser executada por meio dos métodos na classe de entidade.

## Diretrizes gerais para projetar aggregate
- **Identifique limites:** identifique os limites dentro do seu domínio onde entidades e objetos de valor se agrupam naturalmente. Defina raízes agregadas claras que encapsulam esses clusters e servem como pontos de acesso aos componentes internos do agregado.
- **Projete agregados coerentes:** certifique-se de que cada agregado se concentre em um conceito de negócio único e coeso. Evite criar grandes agregados com inúmeras responsabilidades, pois isso pode levar à complexidade e à redução da compreensão.
- **Definir regras de consistência:** defina claramente as regras de consistência e invariantes que devem ser mantidas em cada agregação. Aplique essas regras nos métodos agregados, mantendo a integridade e protegendo a lógica de negócios.
- **Definir Interfaces Bem Definidas:** Definir interfaces para comunicação entre agregados, aderindo ao Princípio de Inversão de Dependências. Isto promove um acoplamento fraco, permitindo que alterações em um agregado tenham impacto mínimo em outros.
- **Considerar armazenamento e recuperação de dados:** Ao projetar agregados, considere os mecanismos de persistência e recuperação.

## Benefícios 

- **Consistência e Integridade:** Os agregados garantem que as entidades dentro deles estejam sempre em um estado consistente. Ao encapsular o estado e o comportamento internos, os agregados fornecem um limite claro para o gerenciamento de regras de negócios e a aplicação de invariantes.
- **Limites transacionais:** os agregados permitem atomicidade e integridade transacional. As alterações feitas em um agregado são persistidas como uma única unidade, garantindo que todas as modificações sejam bem-sucedidas ou falhem juntas, mantendo a integridade dos dados.
- **Escalabilidade e desempenho:** os agregados ajudam a otimizar o acesso aos dados e a minimizar conflitos de consistência de dados. Eles fornecem uma unidade natural de trabalho, permitindo a recuperação e modificação eficiente de dados, reduzindo a contenção e melhorando o desempenho.
- **Teste simplificado:** os agregados facilitam os testes unitários encapsulando a lógica de negócios em uma unidade coesa. Os testes podem ser escritos na interface pública do agregado, permitindo testes focados e isolados de comportamentos de domínio.

## Conclusão
Compreender as Raízes Agregadas e seu papel na aplicação de invariantes é fundamental no Design Orientado a Domínio. Os agregados definem limites transacionais, garantem a consistência dos dados e fornecem uma estrutura clara para gerenciar alterações no seu modelo de domínio. Assim, os agregados melhoram a modularidade, a flexibilidade e a capacidade de manutenção dos sistemas de software, alinhando-os mais estreitamente com o domínio e os requisitos de negócio.


# Fontes
https://medium.com/@edin.sahbaz/exploring-the-power-of-aggregates-in-domain-driven-design-and-clean-architecture-6408d6128d3b
https://learn.microsoft.com/pt-br/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/net-core-microservice-domain-model
https://renatogontijo.medium.com/aggregate-root-na-modelagem-de-dom%C3%ADnios-ricos-7317238e6d97
