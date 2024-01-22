# Aggregate na modelagem de domínios

Um padrão muito utilizado no DDD é o padrão agreggate, que auxiliar no agrupamento de funcionalidades de um objeto de domínio partindo sempre de uma raiz de agregação (aggregate root), que é responsável por gerenciar os objetos de domínio filhos e garantir que os dados serão sempre salvos em conjunto, sendo assim, o repositório terá acesso somente a raiz de agregação e não aos objetos filhos.

# Fontes
https://medium.com/@edin.sahbaz/exploring-the-power-of-aggregates-in-domain-driven-design-and-clean-architecture-6408d6128d3b
https://learn.microsoft.com/pt-br/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/net-core-microservice-domain-model
https://renatogontijo.medium.com/aggregate-root-na-modelagem-de-dom%C3%ADnios-ricos-7317238e6d97
