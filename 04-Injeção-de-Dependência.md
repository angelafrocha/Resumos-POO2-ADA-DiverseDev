# Injeção de Dependência

![injeção](https://dkrn4sk0rn31v.cloudfront.net/uploads/2021/05/inje--o.jpg)

**Dependência:** Uma dependência é simplesmente um objeto que a sua classe precisa para funcionar.

Injeção de dependências (ou “Dependency Injection”, em inglês) é um padrão de design de software que se refere à técnica de fornecer objetos ou componentes externamente a um objeto que depende deles. Em outras palavras, em vez de criar ou instanciar objetos dentro de uma classe ou componente, esses objetos são passados para ele por meio de um construtor ou método.

A injeção de dependências ajuda a melhorar a modularidade, flexibilidade e testabilidade do software, pois torna os objetos dependentes mais independentes e mais fáceis de serem testados e modificados. Além disso, ela permite que diferentes implementações de uma mesma interface possam ser usadas em diferentes contextos, sem que o código que depende dessa interface precise ser alterado.

## Interface IServiceCollection

Em projetos desenvolvidos em .NET, a injeção de dependências é uma funcionalidade nativa e suportada pelo framework. Ela é implementada por meio da interface IServiceCollection, que permite registrar e configurar os serviços e dependências do aplicativo.

Para registrar os serviços no .NET, nós devemos utilizar as classes AddSingleton, AddScoped e AddTransient para especificar como os objetos devem ser criados e gerenciados. A seguir, você tem um resumo de cada uma dessas classes:

- **AddSingleton:** é usado quando nós precisamos registrar um objeto que deve ser criado apenas uma vez durante a vida útil do aplicativo.
- **AddScoped:** é usado para registrar um objeto que deve ser criado uma vez por solicitação. Isso significa que o objeto é criado quando a solicitação é recebida e descartado quando a solicitação é concluída. Ele é muito útil quando precisamos trabalhar com escopos.
- **AddTransient:** esse eu vejo como um dos mais utilizados pelos desenvolvedores .NET. Nós registramos um objeto como AddTransient quando precisamos que o objeto seja criado sempre que um componente o solicita e descartado assim que a operação é concluída.

## Conclusão
A injeção de dependências ajuda a melhorar a modularidade, flexibilidade e testabilidade do software, pois torna os objetos dependentes mais independentes e mais fáceis de serem testados e modificados. Dito isso, no .Net, nós devemos utilizar as classes AddSingleton, AddScoped e AddTransient para especificar como os objetos devem ser criados e gerenciados.
Ao escolher entre AddSingleton, AddScoped e AddTransient, deve-se considerar o ciclo de vida do objeto e como ele será usado em seu aplicativo.


# Fontes
https://www.youtube.com/watch?v=uyOJ2jjBtBs
https://learn.microsoft.com/pt-br/dotnet/core/extensions/dependency-injection
https://programadriano.medium.com/net-inje%C3%A7%C3%A3o-de-depend%C3%AAncia-c7475a93b5cb
https://www.treinaweb.com.br/blog/entendendo-injecao-de-dependencia

