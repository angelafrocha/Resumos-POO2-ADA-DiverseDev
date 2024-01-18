# Projetar um microsserviço orientado a DDD
O DDD (design orientado a domínio) defende modelagem com base na realidade dos negócios conforme relevante para os seus casos de uso.O objetivo é criar sistemas que sejam fáceis de entender e manter, mesmo para desenvolvedores que não sejam especialistas no domínio.

Se cria e aprimora um modelo de domínio restrito por limites que definem o contexto. Esse modelo é explicitamente representado na forma de um microsserviço. Os componentes dentro desses limites se tornam os próprios microsserviços. Para projetar um microserviço orientado a DDD é necessário manter os Limites de cotexto do Microsserviço relativamente pequeno.

## Limites de contexto do microsserviço

Incicialmente é preciso refletir sobre a natureza de ter que equilibrar entre dois objetivos concorrentes:

- Criar os menores microsserviços possiveis.

- Evitar comunicações verborrágicas entre microsserviços.

OBS: Se dois microsserviços precisarem colaborar muito entre si, eles deverão provavelmente ser o mesmo microsserviço; se um microsserviço precisar confiar em outro serviço para atender diretamente a uma solicitação, ele não será realmente autônomo.

## Camadas de microsserviços em DDD

As camadas são um artefato lógico e não estão relacionadas à implantação do serviço. Elas existem para ajudar os desenvolvedores a gerenciar a complexidade no código. Diferentes camadas (como a camada de modelo de domínio versus a camada de apresentação, etc.) poderão ter tipos diferentes, o que exigirá conversões entre esses tipos.
![MOdelode camadas](https://learn.microsoft.com/pt-br/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/media/ddd-oriented-microservice/domain-driven-design-microservice.png)

Cada camada é um projeto do VS: a camada de aplicativo é Ordering.API, a camada de domínio é Ordering.Domain e a camada de infraestrutura é Ordering.Infrastructure.

### 1. Camada de modelo de domínio

Responsável por representar conceitos de negócios, informações sobre a situação de negócios e as regras de negócio. O estado que reflete a situação de negócios é controlado e usado aqui, embora os detalhes técnicos de armazená-lo sejam delegados à infraestrutura. Essa camada é a essência do software de negócios.

- Essa camada deve ignorar totalmente os detalhes de persistência de dados. Essas tarefas de persistência devem ser executadas pela camada de infraestrutura. Portanto, essa camada não deveria receber dependências diretas da infraestrutura
-  Idealmente, suas entidades de domínio não devem derivar nem implementar nenhum tipo definido em nenhuma estrutura de infraestrutura.

### 2. Camada de Aplicativo

Define os trabalhos que o software deve fazer e direciona os objetos de domínio expressivos para resolver problemas. As tarefas pelas quais esta camada é responsável são significativas para os negócios ou necessárias para a interação com as camadas do aplicativo de outros sistemas.

-  Essa camada é mantida fina.
-  Não contém regras de negócio nem conhecimento, mas apenas coordena o trabalho de tarefas e delegados para colaborações de objetos de domínio na próxima camada abaixo.
-  Não tem um estado refletindo a situação de negócios, mas pode ter um estado que reflita o progresso de uma tarefa para o usuário ou o programa.

A camada de aplicativo de um microsserviço no .NET geralmente é codificada como um projeto ASP.NET Core Web API. Portanto, o projeto implementa a interação do microsserviço, o acesso remoto à rede e as APIs Web externas usadas na interface do usuário ou nos aplicativos cliente.

### 3. Camada de Infraestrutura

A camada de infraestrutura é como os dados inicialmente mantidos em entidades de domínio (em memória) são mantidos em bancos de dados ou outro repositório persistente. 

- A camada de infraestrutura não deverá "contaminar" a camada do modelo de domínio.
- As classes de entidade de modelo de domínio independentes da infraestrutura que você usa para manter os dados (EF ou qualquer outra estrutura) não obtendo dependências rígidas de estruturas.

## Conclusão

A camada de aplicativo depende do domínio e da infraestrutura e a infraestrutura depende do domínio, mas o domínio não depende de nenhuma camada. Esse design de camada deve ser independente de cada microsserviço. Conforme observado anteriormente, você pode implementar os microsserviços mais complexos seguindo padrões DDD ao mesmo tempo em que implementa microsserviços conduzidos por dados mais simples (CRUD simples em uma única camada) de maneira mais simples.

![Dependencia entre camadas](https://learn.microsoft.com/pt-br/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/media/ddd-oriented-microservice/ddd-service-layer-dependencies.png)

## Fonte
https://learn.microsoft.com/pt-br/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/ddd-oriented-microservice

