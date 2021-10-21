## Arquitetura Software (Software Architecture)

`Link`: [Fullcycle](https://portal.fullcycle.com.br/)

- **Course:** Fullcycle - Imersão Full Stack & Full Cycle 
- **Education:** Code Education & School of Net 
- **Instructor:** Wesley Willians

# ⚙️ 🏛  Arquitetura Software 🏛 ⚙️ 
<!--Arquitetura--> 
<img src="https://miro.medium.com/max/1838/0*XQFsUIreMxdgMxWI.png" raw="true" alt="imagem" width="900px" />

<hr />
<img src="https://i.imgur.com/uld4nrX.png" raw="true" alt="imagem" width="900px" />


## Fundamentos da arquitetura de software
* Pilares
* Momentos no mundo da arquitetura
* Guias sobre Arquitetura
* Sistemas monolíticos
* Tipos de escalonamentos
* BFF

## CONTEÚDO

### FUNDAMENTOS
- [x] 1. Introdução a arquitetura de software

* **1.1 O que é Arquitetura?**
    * "Organização de um sistema, contemplando seus componentes, os relacionamentos entre estes e com o ambiente, e os princípios que governam seu projeto e evolução". (ISO 42010:2011)

* **1.2 Pilares**
    * Organização de um sistema
    * Componentização
    * Relacionamento entre sistemas
    * Governança (Infra, Time e Arquitetura)
    * Ambiente (padronização)
    * Projeto
    * Projeção
    * Cultura

* **1.3 Frameworks**
    * **Frameworks** são ferramentas e métodos que nos ajudam a focar essencialmente no objetivo final.
    * Frameworks nos ajudam a definir um padrão de trabalho.

    * 1.3.1 **TOGAF** (The TOGAF Standard - Version 9.2)
        * **Framework conceitual:**
            * Definição dos processos de arquitetura
            * +900 páginas
            * Conceitos e nomenclaturas

        * **Visão geral de tipos de arquiteturas:**
            * Negócio
            * Sistemas de Informação
            * Tecnologia
            * Planos de migração

    * 1.3.2 **ISO/IEC/IEEE 42010** - Systems and software engineering — Architecture description
        * **Architecture description**
            * Lançado em 2001 pela ISO
            * Mais simplificado em relação as 900 páginas do TOGAF
            * Formalizada os fundamentos da área de arquitetura de software.
        
- [x] 2. Momentos da arquitetura na História

* **Modelo Tradicional**
    * **Metodologias:** Waterfall - Modelo Cascata
    * **Tipos de aplicação:** Aplicações Monolíticas
    * **Infraestrutura:** Infraestrutura on-premise (Infra dentro da própria empresa)

* **Modelo Atual**
    * **Metodologias:** Agile
    * **Tipos de aplicação:** Multi-tier architecture (softwares distribuidos que se comunicam entre si)
    * **Infraestrutura:** Virtualização

* **Modelo Emergente**
    * **Metodologias:** DevOps / Full Cycle 
        * Desenvolvedor Full Cycle, ele consegue fazer uma tarefa até o final. 
        * Resumindo, um profissional Full Cycle deve entender e realizar a operação de um fluxo completo de desenvolvimento. Dos commits iniciais até a produção e monitoramento.
        * `Link:` https://fullcycle.com.br/tudo-que-voce-precisa-saber-sobre-full-cycle-development/
    * **Tipos de aplicação:** Aplicações em Microserviços
    * **Infraestrutura:** Containers [Docker / Kubernetes]

* **Modelo Futuro**
    * **Metodologias:** NoOps
    * **Tipos de aplicação:** Serverless Applications
        * Conjuntos de funções que as empresas pagam pelo acesso
        * Ex: Amazon Web Services; Google Cloud
    * **Infraestrutura:** Public Cloud

- [x] 3. Introdução a escalabilidade e sistemas monolíticos

## Sistemas Monolíticos

<img src="https://i.imgur.com/ZiER4mV.png" width="800px" />

### Sistemas Monolíticos
* Não é crime usar um sistema monolítico
* Na maioria dos casos vai atender
* Menos complexidade na maioria dos casos
* Sistema monolítico é Vida!
* Não é crime usar um sistema monolítico

## Escalabilidade

### Escalando o software - Escala Vertical X Escala Horizontal

* **Escala Vertical** - + recursos computacionais (uma única maquina)
* **Escala Horizontal** - + App (várias maquinas pequenas - Balancer)

<img src="https://i.imgur.com/4xvZbvz.png" width="670px" />

### Detalhe sobre a Arquitetura da Aplicação

<img src="https://i.imgur.com/NIWGqJ0.png" width="700px" />

## Material Complementar (Pesquisas na Internet)
Segue abaixo as minhas pesquisas sobre os Sistemas Monolíticos.

## Sistemas Monolíticos

<img src="https://fullcycle.com.br/wp-content/uploads/2019/08/image-41-768x675.png" raw="true" alt="imagem" width="600px" />

É um sistema onde regras de negócio, APIs, autenticação, banco de dados estão normalmente juntos. Vamos dizer que é o famoso sistema tradicional que normalmente você e eu fazemos por padrão. Possui alto acoplamento. Se tivermos que escalar esse sistema, teremos que duplicá-lo por inteiro.

Um **exemplo** desses tipos sistema é quando desenvolvemos um projeto usando algum framework como DJango, Ruby on Rails, não importa. Criamos o projeto e colocamos o sistema de autenticação, cadastro de produtos, o cadastro de categorias, estoque, vendas, ordem de serviço. Desenvolvemos os testes, todos se comunicam e subimos para um servidor qualquer. Pronto, o sistema está em funcionamento.

**Agora pergunta: O que há de errado em desenvolver assim?** 
Não há nada de errado. Na maioria das vezes, usaremos esse sistema e raramente teremos que utilizar outra abordagem.

Os **sistemas monolíticos** possuem algumas características que não são, necessariamente ruins, porém, dependendo do contexto em que você estiver, sem dúvidas você poderá ter diversos tipos de desafios. Por esse motivo que muitas pessoas estão optando em utilizar outras abordagens, incluindo a abordagem baseada na arquitetura de microsserviços.

## Características de Sistemas Monolíticos

### Escalabilidade 
**Escalabilidade** – no sistema monolítico sempre que houver a necessidade de escalar determinada funcionalidade, temos que duplicar o sistema inteiro, mesmo que somente uma funcionalidade necessite de mais recursos. Isso acaba gerando um custo muito grande e desnecessário.

**Exemplo:** o sistema está funcionando corretamente, de repente percebemos que ela começa a ter picos de acesso. O primeiro passo é aumentar a capacidade o servidor, porém, mesmo assim ocorrem quedas. Para resolver isso, colocamos um load balancer e atrás dele, colocamos duas máquinas rodando. Conforme as pessoas acessam, há a distribuição nessas máquinas. De acordo com a necessidade, vamos criando mais máquinas. Até aí, tudo bem, não há problemas. Mas veja, cada vez que escalamos o sistema, temos que gerar uma cópia do sistema inteiro.
Dependendo do contexto, isso é muito ruim e muitas pessoas estão tentando outras abordagens.

**Um exemplo é um e-commerce**: Verificamos que o sistema está tendo muitos acessos, mas na verdade 95% dos acessos as pessoas só estão navegando no site e somente 5% efetivamente comprando. Nesse caso, no **sistema monolítico**, duplicando todo o sistema, ficamos com a área de vendas ociosa. Isso é um gasto desnecessário.

### Flexibilidade
**Flexibilidade** – o sistema monolítico **NORMALMENTE** não permite que se desenvolva aplicações em linguagens diferentes. Se desenvolvemos o sistema em Ruby e por algum motivo queremos desenvolver uma aplicação em Go, por exemplo, não é possível. Isso gera uma grande dificuldade. Nesses casos, acabamos desenvolvendo um sistema em paralelo para resolver a questão.
Outro caso é quando o sistema cresce muito, e todas as vezes que criamos novas funcionalidades, para realizar os testes dessa nova funcionalidade, temos que rodar os testes no sistema todo, gerando uma grande complexidade e trabalho.

### Sistema Único
**Sistema Único** – quando um sistema acaba crescendo, normalmente mais desenvolvedores são contratados e quanto mais desenvolvedores, maiores são os desafios para gerenciar pull requests, funcionalidades, conflitos, etc; uma vez que tudo acontece na mesma base do código.

### Tolerância a falhas
**Tolerância a falhas**: Podemos dizer que um sistema monolítico é intolerante a falhas. Qualquer deslize pode ocasionar a queda de todo o sistema.

### Conclusão dos Sistemas Monolíticos
Portanto, de qualquer forma, é importante ressaltar que na maioria das vezes, **sistemas monolíticos** são mais do que suficientes para dar conta do recado. De forma geral são mais simples de administrar, comunicar e integrar. Logo, é importante deixar claro que não há nada de errado trabalhar com sistemas monolíticos.

## Microsserviços

### Conceitos e Vantagens
Antes de iniciarmos o assunto sobre microsserviços, precisamos definir alguns detalhes para não termos qualquer tipo de confusão com termos semelhantes, como **SOA (Arquitetura Orientada a Serviço)**.

### O que é um serviço?
Um **serviço** disponibiliza a informação, realiza transações, resolve problemas de negócio, independe da tecnologia ou protocolo que está sendo utilizado e também pode estabelecer comunicação com diversos clientes.

### SOA (Service Oriented Architecture)
O **SOA** é uma **Arquitetura Orientada a Serviços** que visa a reutilização de sistemas evitando assim o grande retrabalho, uma vez que corporações muitas vezes acabavam repetindo funcionalidades e funções entre seus sistemas. 

Normalmente utiliza uma camada chamada **ESB – Enterprise Service Bus**, que trabalha como interface de conexão entre os serviços. É importante ressaltar que é muito comum nessa arquitetura que os serviços compartilhem o mesmo banco de dados.
Como neste tipo de aplicação todo o sistema depende do ESB, se houver uma falha nessa camada, todo o sistema cai. Ou seja o **ESB** é considerado um **ponto único de falha** (ou **single point of failure**).

<img src="https://fullcycle.com.br/wp-content/uploads/2019/08/image-42.png" raw="true" alt="imagem" width="400px" />


### OBS:
É importante ressaltar que quando falamos em Microsserviços, **não estamos falando em SOA**.

### Conceitos importantes sobre Microsserviços

**Sistemas Independentes** – Tratando-se de microsserviços, os sistemas precisam ser independentes. Esse serviço tem uma função única e compartilha algumas regras de negócios, que poderá ser utilizado em outros sistemas.
Cada serviço trabalha independente para que o sistema, como um todo, possa funcionar corretamente.

**Sistemas totalmente distribuídos** – Os microsserviços conseguem consumir outro microsserviço e assim sucessivamente. Temos serviços com arquiteturas diferentes, tecnologias diferentes e banco de dados independentes. Quando trabalhamos com microsserviços, raramente compartilhamos banco de dados.

Logo, o **principal conceito dos microsserviços é que os sistemas sejam desacoplados e totalmente independentes**.

**Exemplo:** Colocamos um serviço no ar e ele deve funcionar de forma autônoma, sem depender de outro sistema. Ele tem que poder funcionar sozinho. Se houver necessidade, ele poderá se comunicar com outro microsserviço, porém, ele sempre terá que ter um **fallback** caso ele não estabeleça tal comunicação, e nesse caso, provavelmente, ele terá que degradar suas funcionalidades.

Entendendo esses conceitos, fica mais claro como funciona a arquitetura baseada em microsserviços e como se diferencia de SOA. Contudo, vale ressaltar que tudo é serviço e eles acabam se comunicando. Por esse motivo, muitas pessoas falam que os microsserviços são simplesmente um subset do SOA.

Sempre que pensamos em microsserviços, devemos pensar em granularidade. São diversos serviços pequenos, comunicando-se e gerando um resultado maior.

<img src="https://fullcycle.com.br/wp-content/uploads/2019/08/image-43.png" raw="true" alt="imagem" width="400px" />

### Comunicação Assíncrona vs Síncrona
Anteriormente, falamos que os microsserviços são independentes e trabalham com banco de dados diferentes. Entretanto, há situações em que um microsserviço depende de outro microsserviço. Isso significa que muitas vezes um microsserviço precisa estabelecer comunicação para que ele consiga realizar um determinado processamento de dados para retornar o resultado para o cliente dele.

No caso de **comunicação síncronoa**, quando uma solicitação é realizada, espera-se o resultado de forma imediata; por exemplo: se estivermos realizando uma requisição HTTP, esperamos que a resposta (response) já seja o resultado esperado referente a aquela requisição.

No caso de **comunicação assíncrona**, quando uma solicitação é realizada, não é esperado a resposta de forma imediata. Normalmente a request vai para uma fila de processamento e seu resultado pode demorar alguns minutos ou até mesmo dias para ser entregue.

### Fallback
Quando o microsserviço faz a solicitação, ele precisa saber que o outro microsserviço irá demorar para devolver o resultado. Nesse momento é necessário ter uma estratégia de fallback para saber o que fazer se os dados não forem entregues no tempo esperado. 

Quais decisões tomar: tento depois? Quando receber os dados, o que fazer? Ou, consigo fazer algo se não receber os dados?

O nível de complexidade é muito alto. Não há uma regra geral para trabalhar com microsserviços. Cada empresa, cada negócio, tem a sua necessidade e os conceitos se aplicam a todas as necessidades.
Quando falamos que o microsserviço tem que ser independente, é porque se ele não receber o retorno de outro microsserviço, é preciso ter outra solução para saber o que fazer, nem que seja, esperar um dia para aguardar o retorno do outro microsserviço.

### Vantagens dos Microsserviços

#### Tolerância a falhas
Um dos **pontos principais em arquiteturas baseadas em microsserviços** é a *tolerância a falhas*.
Sempre que criamos uma arquitetura baseada em microsserviços, partimos do princípio que todo microsserviço pode apresentar um problema e ficará indisponível naquele momento. Quando trabalhamos com microsserviços dessa forma , temos uma grande vantagem, pois se uma funcionalidade falhar, todas as outras continuam funcionando. O sistema não cai por completo.

**Exemplo:** Acessamos o Facebook e o messenger está com problemas no chat. Se fosse um monolítico, possivelmente todo o Facebook cairia. Trabalhando com microsserviços, simplesmente não exibimos o chat que está com problemas ou informamos que está temporariamente fora e os outros recursos da plataforma continuam funcionando.
Trabalhando dessa forma, temos problemas localizados de falhas, mas raramente, tudo falhará ao mesmo tempo. Temos que diminuir o nível daquela funcionalidade com problema, para garantir que todo o resto continue funcionando.

### Principais Características

**Componentização via serviços** – em cada componente do negócio, cada produto normalmente é um serviço.

<img src="https://fullcycle.com.br/wp-content/uploads/2019/08/image-45-768x294.png" raw="true" alt="imagem" width="900px" />

**Importante:** A estrutura é baseada em produtos e estratégia de negócios não em projetos

**Smart endpoints & Dumb pipes** – é necessário acessar facilmente todos os endpoints de cada microsserviço e ao mesmo tempo os mecanismos de entrega de informação não precisam necessariamente entender a mensagem.

**Governança decentralizada** – é possível ter equipes diferentes, tecnologias diferentes, sistemas de controle de versão diferentes. Ou seja, cada microsserviço pode ter uma governança totalmente adequada a sua necessidade.

**Decentralização no gerenciamento de dados** – Os microsserviços não compartilham um único banco de dados. Nesse ponto, os mesmos tem a flexibilidade de modelar e utilizar seus dados da melhor forma possível.

**Desenhado para falhar** – é necessário prever a falhas e qual os pontos a serem tomados caso isso aconteça. Também é necessário saber quais outros microsserviços ela atingirá.

**Design Evolutivo** – Produtos bem definidos podem evoluir ou serem extintos por razões de negócio .

**Automação de infraestrutura** – o deploy de um microsserviço deve ser rápido e cada um tem sua própria forma de realizá-lo, apesar que a tendência hoje seja uma padronização.

### CI e CD 

Normalmente processos de **CI e CD** são muito comuns no processo de testes e entrega.

* **CI – Integração Contínua** – um processo onde se desenvolve e instala o software para poder testar no servidor. Sempre que fizermos um commit, um pull request, o sistema é instalado no servidor, todo processo de teste roda e se estiver tudo certo, permitimos fazer o merge.

* **CD – Entrega Contínua**– após a aplicação testada temos que colocá-la em produção facilmente. Há diversas técnicas e ferramentas para fazermos isso. Algumas que realizam o processo de forma totalmente automatizada e outras que intervenção humana é necessária por razões de segurança.

### Desvantagens em utilizar Microsserviços
É preciso esclarecer que não devemos aplicar microsserviços em todos os casos. 

Lembre-se dessas características:

**Arquitetura extremamente complexa** – é necessário ter conhecimento profundo do negócio da empresa para poder quebrar o sistema em pequenos serviços para que possam se comunicar

**Alto custo** – será necessário investir em recursos de infraestrutura, pois cada microsserviço será um servidor ou será parte de um container que deverá ser gerenciado por um sistema maior.

**Necessidade de várias equipes para mantê-lo**– para poder gerenciar é necessário ter uma equipe grande para manter os microsserviços funcionando. logo, o sistema deverá ser grande o suficiente para justificar o custo.

**Gera problemas que talvez você não tivesse antes** –
 Um **exemplo** simples é sobre um **microsserviço A** fazendo uma solicitação ao **microsserviço B** e por algum motivo o microsserviço B estava indisponível. 
 Para não perder essa solicitação será necessário tomar algumas medidas para solucionar a questão. Possivelmente, será necessário trabalhar com sistemas de filas, de mensagens, processos de retry ou podemos deixar na fila até que haja um retorno.

**Monitoramento complexo** – quando há diversos serviços, podem haver pontos de falha e é necessário tomar conhecimento, imediatamente, para pode resolvê-los. Normalmente, quando temos um sistema grande rodando, utilizamos diversas ferramentas para monitorar a aplicação, como: New Relic, monitoramento da Amazon, entre outros e ficamos monitorando a aplicação. Se tivermos diversas aplicações para monitorar, comunicando-se entre si e houver um problema, há a necessidade de saber quais estão sendo afetadas pelo problema. Todo esse monitoramento é muito complexo. 

Além disso, é necessário ter um sistema de alerta. Sempre que houver uma falha, o time que cuida do microsserviço com problema tem que ser comunicado, imediatamente, assim como as pessoas que estão em volta daquele microsserviço, para verificarem se os fallbacks criados estão funcionando para que esse problema não seja escalado para os outros microsserviços.

### Quebrar a Aplicação em Microsserviços
Não é recomendado quebrar a aplicação pensando em processos meramente técnicos. Pense em produto. Nesse caso, o **DDD – Domain Driven Design,** se aplica muito bem, pois ele trabalha com um conceito muito importante que são os **escopos muito bem definidos**, os **Bounded Contexts**.

Quando temos os **escopos de domínio, bem definidos**, podemos pegar um desses **escopos** e transformá-lo em **serviços**. Uma vez que transformamos em serviços, será necessário migrar os dados que esse serviço utiliza para um banco de dados próprio.
Uma vez que temos esse serviço, expomos suas APIs para que o sistema monolítico consiga iniciar o processo de consumo.

### Conclusão
Trabalhar com microsserviços é muito útil em um contexto que escalar de forma rápida e precisa seja necessário. Microsserviços nos dão independência, disponibilidade distribuída, controle descentralizado e um risco menor para todo sistema. 

Por outro lado, nem tudo são flores. Processos básicos de comunicação e outros procedimentos que são extremamente simples que realizamos no dia a dia com sistema monolíticos podem ser altamente complexos no mundo dos microsserviços. 

Dessa forma, a adoção dessa arquitetura não deve ser realizada simplesmente por moda, mas sim com muita responsabilidade e sabedoria, entendendo principalmente o negócio como um todo.

* **Fonte:**
* `Link:` https://martinfowler.com/articles/microservices.html



- [ ] 4. Distribuição de responsabilidades
- [ ] 5. Introdução aos microsserviços
- [ ] 6. Orientação a negócios
- [ ] 7. Outras características
- [ ] 8. API Gateway
- [ ] 9. Service Discovery
- [ ] 10. Comunicação entre microsserviços
- [ ] 11. Exemplo do RabbitMQ
- [ ] 12. Dupla latência
- [ ] 13. Backend for Frontend

### DESAFIOS


## Microsserviços
* Principais conceitos
* Vantagens e Desvantagens
* Quebrando aplicações monolíticas
* Principais patterns
* Complexidades

<hr />
<img src="https://i.imgur.com/1AD2lse.png" raw="true" alt="imagem" width="900px" />

## Domain Driven Design
* Entendendo DDD
* Linguagem Ubíqua
* Domínio e subdomínios
* Contextos delimitados
* Mapas de contextos
* Design patterns

## Arquitetura Hexagonal
* Fundamentos
* Motivações
* Evoluções
* Principais camadas
* Direcionamento único
* Dependency Inversion
* Fundamentos da arquitetura de software

<hr />
<img src="https://i.imgur.com/cgx0E0I.png" raw="true" alt="imagem" width="900px" />

## Comunicação entre serviços
* Comunicação síncrona vs assíncrona
* REST
* gRPC
* Filas com RabbitMQ
* Apache Kafka

## Apache Kafka
* Principais conceitos
* Conceitos básicos a prática
* Desenvolvendo aplicação
* Kafka Connect na prática
* Serviços gerenciados

<hr />
<img src="https://i.imgur.com/AMJHrHX.png raw="true" alt="imagem" width="900px" />

## Autenticação entre Microsserviços
* Formatos de autenticação
* Saml2
* OAuth2
* OpenID Connect
* Keycloak na prática
* Fundamentos da arquitetura de software

## Service discovery
* O que é service discovery
* Exemplos diários
* Formatos de descoberta de serviço
* Service discovery na prática com Consul

<hr />



