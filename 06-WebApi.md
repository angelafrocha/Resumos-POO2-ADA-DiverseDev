# Web API
API é um agente de software intermediário que permite que duas ou mais aplicações interajam entre si; uma API web é uma interface de programação de aplicativos para um aplicativo web ou servidor web.  Ele usa o protocolo HTTP para comunicação entre clientes e sites para ter acesso aos dados. 

Trata-se de uma forma de integrar sistemas, permitindo de forma segura que aplicações Desktop, Web, Aplicativos Mobile e IOT interajam com sua aplicação sem que seja necessário expor acesso direto à bancos de dados, numa linguagem que possui limitações de sistema operacional ou tecnologia.

Ao desenvolver uma API, os programadores precisam considerar vários fatores além de apenas implementar funcionalidades básicas. Eles devem abordar questões como controle de versão, segurança, desempenho, tratamento de erros e documentação. 

## Práticas recomendados para desenvolver APIs
### Versionar API
O versionamento de API é uma técnica usada para gerenciar alterações em uma API enquanto mantém a compatibilidade com versões anteriores para clientes existentes. Ele permite que os desenvolvedores introduzam novos recursos, corrijam bugs ou façam outras modificações na API sem afetar a funcionalidade das integrações existentes.

**Vantagens:**
- Compatibilidade com versões anteriores: garante que os clientes possam continuar usando a versão mais antiga enquanto novos clientes podem aproveitar as vantagens dos recursos atualizados.
- Evolução da API: à medida que sua API evolui ao longo do tempo, o controle de versão permite introduzir novos recursos, descontinuar funcionalidades desatualizadas e fazer melhorias sem interromper os clientes existentes.
- Flexibilidade do cliente: Clientes diferentes podem ter requisitos diferentes ou precisar de recursos específicos disponíveis em uma versão específica da API.

### Usar métodos HTTP adequados
O uso de métodos HTTP adequados é importante porque garante a adesão aos princípios do estilo arquitetural REST, melhora o design e a capacidade de manutenção da API, aumenta a segurança ao impor controles de acesso apropriados, promove escalabilidade e mecanismos de cache e permite interoperabilidade e compatibilidade com vários clientes e servidores em todo o mundo. 

**Pincipais:**
- **GET:** Use GET para recuperar dados de um recurso. Não deve ter efeitos colaterais no servidor.
- **POST:** Use POST para criar um novo recurso. A carga útil da solicitação normalmente contém os dados do novo recurso e o servidor atribui um identificador exclusivo a ele.
- **PUT:** Use PUT para atualizar um recurso existente ou criar um novo recurso se ele não existir. A carga útil da solicitação contém a representação completa do recurso que está sendo atualizado.
- **PATCH:** Use PATCH para realizar uma atualização parcial em um recurso existente. A carga útil da solicitação inclui apenas as alterações que precisam ser aplicadas ao recurso.
- **DELETE:** Use DELETE para excluir um recurso identificado por seu identificador exclusivo

### Proteger a API
Refere-se ao processo de implementação de medidas e práticas para proteger uma Interface de Programação de Aplicativo (API) contra acesso não autorizado, violações de dados e outros riscos de segurança. Envolve a implementação de autenticação, autorização, criptografia e outros mecanismos de segurança para garantir a confidencialidade, integridade e disponibilidade da API e dos dados que ela trata.

**Principais aspectos a serem considerados**: Autenticação, autorização e limpeza de taxa

### Armazenar respostas em cache
O cache de resposta envolve armazenar a resposta de uma solicitação de API e atendê-la diretamente do cache quando a mesma solicitação for feita novamente. Ao armazenar respostas em cache, reduzimos a necessidade de reprocessar a mesma solicitação diversas vezes, resultando em tempos de resposta mais rápidos e maior escalabilidade. 

**Vantaagens:**
- Desempenho aprimorado : em vez de executar repetidamente os mesmos cálculos caros ou consultas de banco de dados, a resposta armazenada em cache é servida rapidamente a partir da memória ou de um armazenamento de cache. O armazenamento em cache das respostas reduz o tempo de resposta e melhora o desempenho geral da sua API.
- Economia de largura de banda : em vez de transmitir toda a resposta a cada vez, as solicitações subsequentes podem buscar a resposta armazenada em cache, economizando largura de banda. O armazenamento em cache das respostas reduz a quantidade de dados enviados pela rede.
- Reduz a carga do servidor: ao fornecer respostas em cache, seu servidor lida com menos solicitações, resultando em carga reduzida do servidor e maior escalabilidade. Isso é especialmente benéfico ao lidar com APIs de alto tráfego ou uso intensivo de recursos

### Validação de entrada do usuário
A validação de entrada do usuário é o processo de verificação e validação dos dados inseridos pelos usuários antes de aceitá-los e processá-los na API. Envolve a verificação do formato, tipo e integridade da entrada para evitar vulnerabilidades de segurança comuns.

**Vantagens:**
- Integridade de dados : ao validar a entrada do usuário, você pode impor regras de negócios, restrições de dados e requisitos específicos de formatação. Isso ajuda a manter a integridade e a consistência dos seus dados.
- Prevenção de vulnerabilidades de segurança : a validação de entrada do usuário ajuda a proteger sua API contra riscos de segurança comuns, detectando e rejeitando entradas maliciosas ou malformadas. Ele garante que os dados processados ​​pela sua API sejam confiáveis ​​e seguros de manusear.
- Tratamento de erros : a validação da entrada do usuário permite fornecer mensagens de erro e respostas significativas quando uma entrada inválida é detectada. Isso ajuda os usuários a compreender e corrigir suas entradas, levando a uma melhor experiência do usuário

### Tratamento de exceção
O tratamento adequado de exceções permite tratar erros, recuperar-se de falhas e fornecer respostas aos clientes. O tratamento de exceções é o processo de gerenciar e responder a situações inesperadas.

**Vantagens:**
- Evitar exceções não tratadas : você pode capturar e tratar exceções antes que elas se propaguem na pilha de chamadas e causem exceções não tratadas, resultando em comportamento imprevisível ou travamentos.
- Tratamento de erros “elegante” : ajuda a fornecer respostas de erro significativas aos clientes, melhorando a experiência do usuário.
- Depuração e registro em log : exceções registradas corretamente fornecem informações valiosas sobre as causas dos erros e auxiliam na solução de problemas.

### Documentando sua API
"Documentar uma API" refere-se ao processo de criação de documentação abrangente e informativa que descreve a funcionalidade, o uso e as especificações de uma Interface de Programação de Aplicativo (API). 

**Vantagens:**
- Integração de terceiros : a documentação é crucial quando você deseja que outros desenvolvedores ou organizações integrem seus aplicativos ou serviços à sua API. Serve como base para a compreensão dos requisitos de integração, formatos de dados e mecanismos de autenticação.
- Usabilidade aprimorada: APIs bem documentadas fornecem instruções claras e exemplos sobre como fazer solicitações, lidar com respostas e utilizar os recursos disponíveis. Isso leva a um uso mais eficaz da API e reduz a chance de erros ou mal-entendidos

## Conclusão

API é um agente de software intermediário que permite que duas ou mais aplicações interajam entre si; uma API web é uma interface de programação de aplicativos para um aplicativo web ou servidor web.  Ele usa o protocolo HTTP para comunicação entre clientes e sites para ter acesso aos dados. 
As boas práticas para a construção de APIs são:
- Versionar a API
- Usar métodos HTTP adequados
- Proteger a API
- Armazenar respostas em cache
- Validar entrada do usuário
- Tratar Exceções
- Documentar a API


# Fontes
https://www.c-sharpcorner.com/article/asp-net-core-5-0-web-api/
https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-8.0&tabs=visual-studio
https://marcionizzola.medium.com/criando-a-primeira-api-com-net-core-54181b1f5f59
https://blog.treblle.com/mastering-net-web-api-best-practices-for-building-powerful-apis/
