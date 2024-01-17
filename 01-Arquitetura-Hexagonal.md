# Arquitetura Hexagonal

Em outras formas de arquitetura, o software pode tornar-se altamente acoplado a detalhes externos, resultando na evolução da aplicação ditada pelos limites dos fornecedores. A **Arquitetura Hexagonal**, também conhecida como *Ports and Adapters*, é uma estratégia que visa desacoplar os casos de uso dos detalhes externos.

O objetivo desta abordagem é organizar o código em camadas, cada uma sendo completamente autocontida e isolada do mundo externo, comunicando-se entre si por meio de "portas e adaptadores", criando sistemas altamente flexíveis e desacoplados, visando aprimorar a manutenção, testabilidade e evolução do código.

![Arquitetura Hexagonal](https://miro.medium.com/v2/resize:fit:1400/0*DA-VUfJf4h2eVPN-)

## Princípios da Arquitetura Hexagonal

### Camadas Principais

**1. Domínio:** Responsável pelas regras de negócio da aplicação.
 (Camada de Aplicação: Contém as Regras de Negócio e Casos de Uso, sustentados a longo prazo.)

Nesta camada é onde fica a declaração das “Portas”/Interfaces (Adapters) de saída para comunicação com o meio externo, além das entidades que representam o  negócio e a “porta de entrada” para a regra de negócio especificamente (Services).:


![Dominio](https://miro.medium.com/v2/resize:fit:640/format:webp/1*4VTNDUGiwp3U_XI0sDm6cw.png)

**2. Aplicação:** Nesta camada é onde ficará as implementações, de fato, das regras de negócio


![CAmadaAplicação](https://miro.medium.com/v2/resize:fit:640/format:webp/1*kfGloqZqic_NPRxLvRQ1aA.png)


**3. Infraestrutura:** Responsável por interagir com o mundo externo, como bancos de dados, APIs e sistemas operacionais.
 (Detalhes Externos: Tudo que oferece suporte a capacidades externas)


![Infra](https://miro.medium.com/v2/resize:fit:640/format:webp/1*2JTF8w6dGlEKMgXaORzUkA.png)



### VIsão geral dos Detalhes Externos e Camada de Aplicação

![geral](https://github.com/angelafrocha/Resumos-POO2-ADA-DiverseDev/assets/127805091/3248e2b0-377a-406d-97d7-b785246b1940)


## Vantagens da Arquitetura Hexagonal

Ao adotar a arquitetura hexagonal, os desenvolvedores podem criar aplicações que possuem as seguintes características:

- **Facilmente Testáveis:** As regras de negócio são isoladas da infraestrutura, facilitando os testes sem depender de componentes externos.
- **Escaláveis:** A infraestrutura pode ser alterada sem afetar o domínio, facilitando a evolução da aplicação.
- **Flexíveis:** A aplicação pode ser facilmente adaptada a diferentes ambientes e necessidades.

## Fontes
https://www.youtube.com/watch?v=7SaA3HCOc4c

https://www.youtube.com/watch?v=YpCy012NhQ0

https://alexalvess.medium.com/organizando-seu-projeto-net-com-arquitetura-hexagonal-parte-02-fe9a8ed6ab02


