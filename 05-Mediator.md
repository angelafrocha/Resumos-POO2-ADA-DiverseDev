# Mediator

O Mediator Pattern cuida das interações entre diferentes objetos, fornecendo uma classe mediadora que coordena todas as interações entre os objetos, visando diminuir o acoplamento e a dependência entre eles e facilitando as manutenções. Portanto, nenhum objeto conversa diretamente com outro, sempre um objeto utilizará a classe mediadora para conversar indiretamente com outros objetos.

![](https://miro.medium.com/v2/resize:fit:640/format:webp/1*JJOGVux0MWZUGW9Ro-cULw.png)

**Vantagens**
- Desacoplamento entre os objetos, pois nenhum objeto se conhece na
comunicação;
- O fluxo de comunicação está centralizado, com isso, alterações no
mediador não afetam seus ouvintes;
- Mudanças podem ser aplicadas facilmente nos objetos, pois são
independentes;

**Desvantagens**
- Dependendo da quantidade de informações a ser processada, o mediador
pode se tornar o gargalo da aplicação
- Maior complexidade de código

No contexto de microsserviços em .NET, o Mediator Pattern é frequentemente utilizado para gerenciar a comunicação entre diferentes serviços de maneira eficiente e organizada e possui uma biblioteca C#, o mediatR, que simplifica e facilita sua implementação: mediatR

## Biblioteca MediatR
A biblioteca MediatR pode ser usada em uma variedade de aplicações .NET, incluindo aplicativos web, aplicativos de desktop e aplicativos móveis. Ela pode ser
usada para melhorar a modularidade, a testabilidade e a reusabilidade de aplicações.

![](https://alinabo.com/assets/blog/posts/imgs/mediatR.png)

**Funcionalidades**
- **Objeto Mediator:** O objeto Mediator é responsável por encapsular a comunicação entre os objetos.
- **Interfaces para mensagens:** A biblioteca MediatR fornece interfaces para diferentes tipos de mensagens, como comandos, consultas e notificações.
- M**ecanismo de despacho de mensagens:** A biblioteca MediatR fornece um mecanismo de despacho de mensagens que permite enviar mensagens para objetos específicos ou para todos os objetos que implementam uma determinada interface.

A MediatR promove uma abordagem centralizada para manipulação de mensagens em seu aplicativo usando a classe pública. Em vez de espalhar lógica de comando ou consulta em vários controladores ou serviços, o MediatR permite definir manipuladores para cada tipo de mensagem em um local centrale. Essa abordagem simplifica a ordem de tratamento das mensagens e facilita o gerenciamento e a manutenção do aplicativo.

**Interfaces:**
- IResponse: A interface IResponse representa o resultado de uma solicitação.
- INotification: A interface INotification representa uma notificação que pode ser
enviada para outros componentes do sistema.
- IPipelineBehavior: A interface IPipelineBehavior permite que você personalize
- comportamento do pipeline de MediatR.
- IRequestHandler: A interface IRequestHandler representa um manipulador de
solicitações que pode ser usado para processar uma solicitação.
- IRequestReciever: A interface IRequestReciever representa um receptor de
solicitações que pode receber solicitações do pipeline de MediatR.

## Conclusão

Em síntese, Mediator é um padrão de projeto comportamental que define um objeto que encapsula a forma como um conjunto de objetos interage. O Mediator promove o acoplamento fraco ao evitar que os objetos se refiram uns aos outros de forma explícita e permite variar suas interações independentemente.

MediatR é uma biblioteca .NET que implementa o padrão Mediator.



# Fontes
https://medium.com/jundevelopers/mediator-pattern-com-mediatr-asp-net-core-2-2-6d8d2e3dc3c5
https://learn.microsoft.com/pt-br/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/microservice-application-layer-implementation-web-api
