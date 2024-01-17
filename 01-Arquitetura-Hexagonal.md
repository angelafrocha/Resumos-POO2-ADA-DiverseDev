# Arquitetura Hexagonal

Em outras formas de arquitetura, o software pode tornar-se altamente acoplado a detalhes externos, resultando na evolução da aplicação ditada pelos limites dos fornecedores. A **Arquitetura Hexagonal**, também conhecida como *Ports and Adapters*, é uma estratégia que visa desacoplar os casos de uso dos detalhes externos.

O objetivo desta abordagem é organizar o código em camadas, cada uma sendo completamente autocontida e isolada do mundo externo, comunicando-se entre si por meio de "portas e adaptadores".

## Princípios da Arquitetura Hexagonal

A arquitetura Hexagonal é um padrão que busca criar sistemas altamente flexíveis e desacoplados, visando aprimorar a manutenção, testabilidade e evolução do código.

### Camadas Principais

1. **Domínio:** Responsável pelas regras de negócio da aplicação.
2. **Infraestrutura:** Responsável por interagir com o mundo externo, como bancos de dados, APIs e sistemas operacionais.

### Detalhes Externos e Camada de Aplicação

- *Detalhes Externos:* Tudo que oferece suporte a capacidades externas.
- *Camada de Aplicação:* Contém as Regras de Negócio e Casos de Uso, sustentados a longo prazo.

## Vantagens da Arquitetura Hexagonal

Ao adotar a arquitetura hexagonal, os desenvolvedores podem criar aplicações que possuem as seguintes características:

- **Facilmente Testáveis:** As regras de negócio são isoladas da infraestrutura, facilitando os testes sem depender de componentes externos.
- **Evoluíveis:** A infraestrutura pode ser alterada sem afetar o domínio, facilitando a evolução da aplicação.
- **Flexíveis:** A aplicação pode ser facilmente adaptada a diferentes ambientes e necessidades.

## Benefícios Principais

### Testabilidade

A arquitetura hexagonal facilita o teste da aplicação, pois as regras de negócio são isoladas da infraestrutura.

### Evolutividade

A evolução da aplicação é simplificada, pois a infraestrutura pode ser alterada sem impactar o domínio.

### Flexibilidade

A arquitetura hexagonal permite a fácil adaptação da aplicação a diferentes ambientes e necessidades.
