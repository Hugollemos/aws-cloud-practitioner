<div id="topo"></div>

# Certificação AWS Cloud Practitioner

Minhas anotações tiradas do curso da **[Escola da nuvem](https://www.escoladanuvem.org)**  e da **[AWS Skill Builder: AWS Cloud Practitioner Essentials
](https://explore.skillbuilder.aws/learn/signin)** para estudo referente ao exame da **[AWS Certified Cloud Practitioner](https://aws.amazon.com/pt/certification/certified-cloud-practitioner).** 

<div id="assunto"></div>

* [Assuntos](#assunto)
    - [Pesos](#Pesos)
    - [O que é a computação em nuvem ? ](#O_que_é_a_computação_em_nuvem)
    - [vantagens da computação da nuvem](#vantagens)
    - [Computação na nuvem](#nuvem)
    - [Infraestrutura global e Confiabilidade](#infra)
    - [Redes](#redes)
    - [Armazenamento e Bancos de Dados](#banco)
    - [Segurança](#seguranca)
    - [Monitoramento e análise](#Monitoramento)
    - [Definição de preços e suporte](#preco)
    - [Migração e inovação](#migracao)
* [links](#links)

<hr>
<div id="Pesos"></div>

## Pesos 🏋️
Domínio | % do exame
---------|----------|
Domínio 1: Cloud Concepts | 26%  
Domínio 2: security and compliance | 25%  
Domínio 3: Technology | 33%  
Domínio 4: Billing and pricing | 16%  
TOTAL | 100%  

**[REFERENCIA](https://d1.awsstatic.com/pt_BR/training-and-certification/docs-cloud-practitioner/AWS-Certified-Cloud-Practitioner_Exam-Guide.pdf
)** 
<hr>

<div id="O_que_é_a_computação_em_nuvem"></div>

## 1. O que é a computação em nuvem ? ☁️ ☁️ ☁️ 


"É a entrega sob demanda de recursos computacionais, através de uma plataforma de serviços via internet, sem o gerenciamento ativo do usuário".

**[REFERENCIA](https://aws.amazon.com/pt/what-is-cloud-computing/
)** 
<hr> 

<div id="vantagens"></div>

# As 6 vantagens da computação da nuvem na visão da AWS. 🥇

# Save money
"Pare de gastar recursos financeiros na manutenção da infraestrutura e tenha mais foco nos clientes."

# Stopguessing capacity
"Elimina a adivinhação de quanto a infraestrutura precisa, Com a computação em nuvem, você não precisa prever a capacidade de infraestrutura necessária antes de implantar um aplicativo.

# variable expenses
"Ao adotar uma abordagem de computação em nuvem com o benefício de **despesas variáveis**, as empresas podem implementar soluções inovadoras enquanto economizam custos."

# economies of scale
"O uso da computação em nuvem permite obter um custo variável inferior ao que você consegue por conta própria."

# increase speed and agility
"Mais facilidade na hora de usar o serviço em poucos cliques. "

# go global
"Facilidade em disponibilizar o serviço em varias partes no globo."

**[REFERENCIA](https://docs.aws.amazon.com/pt_br/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html
)** 
<hr>

# Tipos de clouds
## Temos 3 tipos de clouds!

* IAAS
Infrastructure as a service (infraestrutura como serviço). Exemplo AWS EC2 a onde usamos o hardware da aws para montar servidores virtuais, utilizando rede, armazenamento e processamento. 

* PAAS
plataform as a service (plataforma como serviço), sua organização não precisa gerenciar a infraestrutura subjacente (geralmente hardware e sistemas operacionais), e você pode focar na implantação e no gerenciamento de suas aplicações.

* SAAS
SaaS – software as a service (software como serviço). Quando utilizamos o software: Amazon CloudFront, Amazon Detective,Amazon DocumentDB etc.

**[REFERENCIA](https://aws.amazon.com/pt/types-of-cloud-computing/
)** 

<p align="center">
  <a><img src="../img/plataforma.png"></a>
</p>

<div id="nuvem"></div>

# 2. COMPUTAÇÃO NA NUVEM 🖥 ☁️

O Amazon EC2 é um serviço que disponibiliza uma capacidade computacional segura, representado por uma instancia redimensionável na Nuvem.

### CARACTERÍSTICAS
* amazon EC2 Elastic Compute Cloud
* Modelo Infraestrutura como Serviço
* Alugar máquinas virtuais (EC2)
* Armazenar dados em volumes virtuais (EBS)
* Distribuir a carga de trabalho (ELB)
* Escalar o serviço de acordo com a demanda (ASG)
* Modelo Computacional Infraestrutura como Serviço
* Ambiente operacional Windows, MacOS e Linux
* Cobrança por hora ou segundo (mínimo de  60 segundos)

# Tipos de instancia

FAMÍLIA | OTIMIZADO | IDEAL PARA
---------|----------|---------|
`A, T, M, MAC`      | Uso geral | Servidores de web, homologação e repositórios de código
`C`      | Computação |Modelagem científica, servidores de jogos, servidor de anúncios, machine learning
`R, X, Z`      | Memória | Cargas de trabalho que processam grandes conjuntos de dados na memória.
`I, D, H`      | Processamento | Executar funçoes, como cálculos de números de ponto flutuante, processamento de gráficos.
`I, D, H`      | Armazenamento | Cargas de trabalho qeu requerem uso intensivo de disco (IOPS)


## ✨ Amazon EC2 Launch Types

Launch | Especifico | Preço | Útil 
---------|----------|---------|---------
SOB DEMANDA | Cobrança o que usar (por hora OU por segundo); Sem compromisso de uso (anos); Sem pagamento adiantado; Pode aumentar ou diminuir a capacidade computacional. | Alto custo se usado por longo prazo | Cargas de trabalho de curtoprazo, validar hipóteses, com picode utilização previsível, testar e experimentar um ambiente.
INSTANCIAS RESERVADAS | Aplicações que exigem capacidade reservadacomprometimento de uso da instancia por um período de 01 ou 03 anos |possui pagamento adiantado; Até 75% desconto comparação instancias por demanda | Ambiente de produção que foi testado e não será modificado, aplicação que precisa ter estado constante; Excelente para banco de dados.
HOST DEDICADO | Hardware dedicado; Servidor físico EC2 exclusivo para você ;Cumprir requisitos de conformidade ;Visibilidade de soquetes, núcleos. IDs de host ;Comprometimento por um período de 03 anos;Pode ser comprado sob demanda de horas | se optar por reserva, até 70% desconto em comparação com instancias por demanda | Vincular licenças de software como Windows Server, AWS Server e SUSE Linux Enterprise Server.
INSTANCIA DEDICADA | Hardware dedicado Pode compartilhar o hardware com outras instancias, na mesma conta. Não tem controle sobre o posicionamento da instancia (você só pode movimentar hardware se interromper e reiniciar); Comprometimento por um período de 03 anos
INSTANCIAS SPOT | são terminadas quando o preço do spot, é maior do que o preço que você estabeleceu para pagar; terminate =(preço spot da AWS > seu preço) | Até 90% desconto comparação instancias por demanda | Quando você tem urgência de grande capacidade computacional, workloads que podem parar e serem iniciados novamente, trabalhos em iote, análise de dados, processamento de imagens.

## Amazon EC2 Auto Scaling

O Amazon EC2 Auto Scaling permite que você adicione ou remova automaticamente instâncias do Amazon EC2 em resposta à alteração da demanda do aplicativo.

- No Amazon EC2 Auto Scaling, há duas abordagens disponíveis: scaling dinâmico e scaling preditivo.

* O scaling dinâmico responde às alterações na demanda. 
* O scaling preditivo programa automaticamente o número correto de instância do Amazon EC2 com base na demanda prevista.

<p align="center">
  <a><img src="../img/scale.png"></a>
</p>

## escalabilidade
almenta os recursos computacionais como: RAM,CPU etc.

## elasticidade 
almenta os números de intancias(máquinas)

obs:
* Definir uma quantidade mínima, desejável e máxima de instancias
* Scale out (aumentar com as demandas) e Scale in (diminuir quando a demanda deixa de ocorrer)
* Auto Scaling Group é gratuito, voce paga apenas pelas instancias que estao sendo executadas

## Elastic Load Balancing
O Elastic Load Balancing é o serviço AWS que distribui automaticamente o tráfego de entrada de aplicativos entre vários recursos, como instâncias do Amazon EC2.

## Amazon Simple Notification Service (Amazon SNS)
O Amazon Simple Notification Service (Amazon SNS) é um serviço de publicação/assinatura.

## Amazon Simple Queue Service (Amazon SQS)
O Amazon Simple Queue Service (Amazon SQS) é um serviço de enfileiramento de mensagens. 

## AWS Lambda
O AWS Lambda é um serviço que permite a execução de códigos sem a necessidade de provisionar ou gerenciar servidores.
Permite que voce execute códigos sem provisionar ou gerenciar servidores, pagando apenas pelo número de solicitações e pelo tempo de computação que voce utilizar.

OBS: 
* serviço serveless e gerenciado pela AWS
* AWS Lambda dimensiona suas aplicações 
* voce pode otimizar o tempo de execuçao e o tamanho de memoria
* cobrança por númeo de solicitacoes de duas funcoes e pela duracao por cada milissegundo que leva para que seu codigo seja executado

## Amazon Elastic Container Service (Amazon ECS)
É um sistema de gerenciamento de contêineres altamente dimensionável e de alto desempenho que permite executar e dimensionar aplicativos em contêineres na AWS.
## Amazon Elastic Kubernetes Service (Amazon EKS)
É um serviço totalmente gerenciado que você pode usar para executar o Kubernetes na AWS.

## AWS Fargate
O AWS Fargate é um mecanismo de computação sem servidor para contêineres. Ele funciona com o Amazon ECS e o Amazon EKS.
Com o AWS Fargate, você não precisa provisionar ou gerenciar servidores. 

<div id="infra"></div>

# 3. INFRAESTRUTURA GLOBAL E CONFIABILIDADE 🛰 🏭

## Uma regiao é a disponibilizacao de uma colecao de recursos AWS em uma localizacao geografica, sendo ele composto por um conjunto de zonas de disponibilidade
região: é um conjunto de data centers em uma localização geográfica.

ZONA DE DISPONIBILIDADE: Uma zona de disponibilidade é um conjunto de datacenters que estão na mesma REGIÃO, porém separados por uma distancia significativa, atuando de forma independente em caso de falha de uma zona.

pontos de presença é uma infraestrutura de servidores, localizado proximno de uma ZD, que armazena os dados mais solicitados no cahce, para entregar com menor latencia uma requisicao de consulta
sao tulizados como cache de dados para distribuicao de conteudo

## AWS Elastic Beanstalk
Você fornece definições de *código* e configuração, e o Elastic Beanstalk implanta os recursos necessários para executar as seguintes tarefas:

* Balancear carga
* Dimensionar de forma automática
* Monitorar a integridade do aplicativo
* Ajustar capacidade
* Auto Scaling Group (ASG)
* Alta disponibilidade (Multi-az)
* Upload código arquivo <512Mb ou Upload via URL Buckeat S3
* Plataforma como Serviço (PaaS)

## AWS CloudFormation
Você pode considerar sua infraestrutura como código. 
crie frequentemente a infraestrutura e os aplicativos sem precisar executar ações manuais ou criar scripts personalizados. 

<div id="redes"></div>

# 4. REDES 📡

## AMAZON VPC
O Amazon VPC é uma sessão isolada logicamente na nuvem AWS, que permite customizar uma rede virtual e executar recursos, em uma ambiente com controle total

## AWS Direct Connect
O AWS Direct Connect é um serviço que permite estabelecer uma conexão privada dedicada entre seu data center e uma VPC.

A conexão privada que o AWS Direct Connect fornece ajuda você a reduzir os custos de rede e a aumentar a quantidade de largura de banda que pode trafegar pela sua rede.

## Gateway da internet X Gateway privado virtual

Para permitir que o tráfego público da internet acesse sua VPC, é preciso anexar um gateway da internet à VPC.

Para acessar recursos privados em uma VPC, você pode usar um gateway privado virtual. 

Uma sub-rede é uma seção de uma VPC na qual você pode agrupar recursos com base em necessidades operacionais ou de segurança. As sub-redes podem ser públicas ou privadas. 

## Lista de controle de acesso (ACL) de rede.
Uma lista de controle de acesso (ACL) de rede é um firewall virtual que controla o tráfego de entrada e saída no nível de sub-rede.

Uma lista de controle de acesso (ACL) de rede permite ou não determinado tráfego de entrada ou de saída no nível da sub-rede.

# Filtragem de pacotes stateless
As ACLs de rede executam a filtragem de pacotes stateless. Elas não se lembram de nada e verificam os pacotes que atravessam a fronteira da sub-rede em todos os sentidos: entrada e saída.

# Filtragem de pacotes stateful
Os grupos de segurança fazem a filtragem de pacotes stateful. Eles se lembram de decisões anteriores tomadas para pacotes recebidos.

## Grupos de segurança

Um grupo de segurança é um firewall virtual que controla o tráfego de entrada e saída de uma instância do Amazon EC2.

Por padrão, um grupo de segurança nega todo o tráfego de entrada e permite todo o tráfego de saída. 

## Amazon Route 53

é um serviço web de DNS. Oferece aos desenvolvedores e empresas uma maneira confiável de rotear os usuários finais para aplicativos da internet hospedados na AWS.

### REGISTROS COMUNS

URL | IP | REGISTRO/RECORD | TIPO
---------|----------|---------|---------
www.google.com | 216.239.38.120 | A | IPv4
www.google.com | 0:0:0:0:0:ffff:d8ef:2678 |AAAA |IPv6
search.google.com | www.google.com | CNAME | Hostname para Hostname
exemplo | Recurso AWS | ALIAS | ELB, CloudFront, S3, DRS...

<div id="banco"></div>

# 5. Armazenamento e Bancos de Dados 📊 🗂 💻

## Amazon Elastic Block Store (Amazon EBS)
é um serviço que fornece volumes de armazenamento a nível de bloco que você pode usar com instâncias do Amazon EC2. Se você interromper ou encerrar uma instância do Amazon EC2, todos os dados no volume do EBS anexo permanecerão disponíveis.

## Snapshots do Amazon EBS
Um snapshot do EBS é um backup incremental. Isso significa que o primeiro backup de um volume copia todos os dados.

## Amazon Simple Storage Service (Amazon S3)
É um serviço gerenciado de armazenamento e recuperação  de objetos, respondendo com escalabilidade, disponibilidade, segurança e performance.
* O Amazon S3 oferece espaço de armazenamento ilimitado. O tamanho máximo de arquivo para um objeto no Amazon S3 é de 5 TB.

## Classes de armazenamento do Amazon S3

* S3 Standar
-Projetado para dados acessados com frequência
-Armazena dados em um mínimo de três Zonas de Disponibilidade
-99.999999999 de durabilidade

O S3 Standard fornece alta disponibilidade para objetos. Isso o torna uma boa escolha para diversos casos de uso, como sites, distribuição de conteúdo e análise de dados. O S3 Standard tem um custo mais alto do que outras categorias de armazenamento para dados acessados com pouca frequência e armazenamento de arquivamento.

* Standard-Infrenquent Access (S3 Standdar-IA)
-Ideal para dados com pouca frequência de acesso
-Semelhante ao S3 Standard, mas com um preço de armazenamento mais baixo e um preço de recuperação mais alto

O S3 Standard-IA é ideal para dados acessados com pouca frequência, mas que precisam ter alta disponibilidade para quando necessário. O S3 Standard e o S3 Standard – IA armazenam dados em um mínimo de três Zonas de Disponibilidade. O S3 Standard – IA fornece o mesmo nível de disponibilidade do S3 Standard, mas com um preço de armazenamento mais baixo e um preço de recuperação mais alto.


* One Zone-Infrequent Access (S3 One Zone - IA)
-Armazena dados em uma única Zona de Disponibilidade
-Tem um preço de armazenamento menor do que o S3 Standard – IA

* Intelligent Tiering
-Ideal para dados com padrões de acesso desconhecidos ou em alteração
-Requer uma pequena taxa mensal de monitoramento e automação por objeto

Na categoria de armazenamento S3 Intelligent-Tiering, o Amazon S3 monitora os padrões de acesso dos objetos. Se você não acessou um objeto por 30 dias consecutivos, o Amazon S3 o move automaticamente para o nível de acesso pouco frequente S3 Standard – IA. Se você acessar um objeto no nível de acesso pouco frequente, o Amazon S3 o move automaticamente para o nível de acesso frequente S3 Standard.

* Glacier
-Armazenamento de baixo custo projetado para arquivamento de dados
-Capaz de recuperar objetos em poucos minutos a horas

O S3 Glacier é uma categoria de armazenamento de baixo custo, ideal para o arquivamento de dados. Por exemplo, você pode usar essa categoria para armazenar registros de clientes arquivados ou arquivos de fotos e vídeos mais antigos.

* S3 Glacier Deep Archive
-Categoria de armazenamento de objetos com menor custo, ideal para arquivamento
-Capaz de recuperar objetos em 12 horas

Ao decidir entre o Amazon S3 Glacier e o Amazon S3 Glacier Deep Archive, considere a prontidão com que você precisa recuperar objetos arquivados. É possível recuperar objetos armazenados na categoria de armazenamento S3 Glacier de alguns minutos a algumas horas. Em comparação, é possível recuperar objetos armazenados na categoria de armazenamento S3 Glacier Deep Archive em até 12 horas.

---
## Amazon Elastic File System (Amazon EFS)

é um sistema de arquivos escalável usado com os serviços de nuvem AWS e recursos locais. À medida que você adiciona e remove arquivos, o Amazon EFS expande e retrai automaticamente. Ele pode dimensionar sob demanda para petabytes sem interromper os aplicativos. 

## Amazon Relational Database Service (Amazon RDS)

O Amazon Relational Database Service (Amazon RDS) é um serviço que permite executar bancos de dados relacionais na nuvem AWS.
* alta disponibilidade automática, recuperação fornecida
* Cliente é propriétario dos dados
* Cliente é propriétario dos schema
* Cliente controla a rede
---
## Amazon Aurora

O Amazon Aurora é um banco de dados relacional de nível empresarial.

Considere o Amazon Aurora se suas cargas de trabalho exigem alta disponibilidade. Ele replica seis cópias de seus dados em três Zonas de Disponibilidade e faz backup contínuo de seus dados para o Amazon S3.
---
## Amazon DynamoDB
*  banco de dados não relacional
* O DynamoDB é sem servidor, o que significa que você não precisa provisionar, aplicar patches ou gerenciar servidores. 

Você também não precisa instalar, manter ou operar o software.\
* Auto Scaling
* Chave-valor
* Capacidade de produção massíva
* Potencial de tamanho de PB
* Acesso a API granular

## Amazon RedShift
O Amazon Redshift é serviço de data warehouse que você pode usar para análise de big data. Ele oferece a capacidade de coletar dados de muitas fontes além de ajudar a entender relações e tendências em todos os seus dados.

## AWS Database Migration Service (AWS DMS)
O AWS Database Migration Service (AWS DMS) permite migrar bancos de dados relacionais e não relacionais e outros tipos de armazenamentos de dados.

* O banco de dados de origem permanece totalmente operacional durante a migração
* Minimizando o tempo de inatividade das aplicações que dependem desse banco de dados.
* Os bancos de dados de origem e edestino não precisma ser do mesmo tipo.

## Amazon DocumentDB
O Amazon DocumentDB é um serviço de banco de dados de documentos compatível com cargas de trabalho do MongoDB. (MongoDB é um programa de banco de dados de documentos.)
## Amazon Neptune
O Amazon Neptune é um serviço de banco de dados de grafo.

Você pode usar o Amazon Neptune para criar e executar aplicativos que funcionam com conjuntos de dados altamente conectados, como mecanismos de recomendação, detecção de fraudes e gráficos de conhecimento.
## Amazon Quantum Ledger DAtabase (Amazon QLDB)
O Amazon Quantum Ledger Database (Amazon QLDB) é um serviço de banco de dados ledger.

Você pode usar o Amazon QLDB para revisar um histórico completo de todas as alterações feitas nos dados do aplicativo.
## Amazon Managed Blockchain
O Amazon Managed Blockchain é um serviço para criar e gerenciar redes de blockchain com estruturas de código aberto.


O Blockchain é um sistema de registro distribuído que permite que várias partes executem transações e compartilhem dados sem uma autoridade central.
## Amazon ElastiCache
O Amazon ElastiCache é um serviço que adiciona camadas de cache sobre seus bancos de dados para ajudar a melhorar os tempos de leitura de solicitações comuns.


Ele é compatível com dois tipos de armazenamentos de dados: Redis e Memcached.
## Amazon DynamoDB Accelecerator
O Amazon DynamoDB Accelerator (DAX) é um cache em memória para o DynamoDB.

Ele ajuda a melhorar os tempos de resposta de milissegundos para microssegundos.

<div id="seguranca"></div>

# 6. SEGURANÇA 👮‍♀️ 👮

## AWS Identity and Access Management (IAM)

permite que você gerencie o acesso aos serviços e recursos AWS com segurança.

## Grupos do IAM
Um grupo do IAM é um conjunto de usuários do IAM. Ao atribuir uma política do IAM a um grupo, todos os usuários do grupo recebem permissões especificadas pela política.

## Funções do IAM

Uma função do IAM é uma identidade que você pode assumir para obter acesso temporário a permissões.


## Uma função do IAM é uma identidade que você pode assumir para obter acesso temporário a permissões.

## AWS Organizations
* consolidar e gerenciar múltiplas contas AWS em um local central.
*No AWS Organizations, você pode agrupar contas em unidades organizacionais (UO) para facilitar o gerenciamento de contas com requisitos de negócios ou segurança semelhantes.
## políticas de controle de serviço (SCPs).

As SCPs permitem que você coloque restrições nos serviços AWS, recursos e ações individuais de API que os usuários e funções em cada conta podem acessar.

## AWS Artifact

O AWS Artifact é um serviço que fornece acesso sob demanda a relatórios de segurança e conformidade da AWS e a contratos on-line selecionados. O AWS Artifact tem duas seções principais: AWS Artifact Agreements e o AWS Artifact Reports.

-AWS Artifact Agreements
No AWS Artifact Agreements, você pode revisar, aceitar e gerenciar contratos para uma conta individual e para todas as suas contas no AWS Organizations.


-AWS Artifact Reports
O AWS Artifact Reports fornece relatórios de conformidade por auditores terceirizados. Esses auditores testaram e verificaram se a AWS está em conformidade com diversas normas e regulamentações de segurança globais, , regionais e específicas do setor. 

## Ataques de negação de serviço

## AWS Shield
O AWS Shield é um serviço que protege aplicativos contra ataques DDoS. O AWS Shield oferece dois níveis de proteção: Standard e Advanced.

## AWS Shield Standard
O AWS Shield Standard protege automaticamente todos os clientes AWS sem nenhum custo. Ele protege seus recursos AWS contra os tipos de ataques DDoS mais comuns e frequentes.

## AWS Shield Advanced
é um serviço pago que fornece diagnósticos detalhados de ataques e a capacidade de detectar e mitigar ataques elaborados de DDoS.


## AWS Key Management Service (AWS KMS)
permite que você execute operações de criptografia pelo uso de chaves de criptografia.
## AWS WAF
é um firewall de aplicativo web que permite monitorar solicitações de rede que entram em seus aplicativos web. 


## Amazon Inspector
O Amazon Inspector ajuda a melhorar a segurança e a conformidade dos aplicativos executando avaliações de segurança automatizadas. Ele verifica os aplicativos quanto a vulnerabilidades de segurança e desvios das práticas recomendadas de segurança, como acesso aberto a instâncias do Amazon EC2 e instalações de versões de software vulneráveis. 


## Amazon GuardDuty
O Amazon GuardDuty é um serviço que fornece detecção inteligente de ameaças para sua infraestrutura e seus recursos AWS. Ele identifica ameaças monitorando continuamente a atividade da rede e o comportamento da conta no seu ambiente AWS.


<div id="Monitoramento"></div>

# 7. Monitoramento e análise 👨‍💻 📟

## Amazon CloudWatch
* Visualizar as aplicaçoes e a sua infraestrutura em um único local 
* Acessar um Dasboard automático
* Criar o seu Dasboard(painel) pernonalizado com os serviços e métricas que deseja acompanhar
* Configurar alarmes visuais do ambiente
 
## AWS CloudTrail
O AWS CloudTrail é um serviço que possibilita governança, conformidade, auditoria operacional e auditoria riscos em sua conta AWS.

## CloudTrail Insights
Esse recurso opcional permite que o CloudTrail detecte automaticamente atividades de API incomuns em sua conta AWS. 


## AWS Config
é um serviço que permite acessar, auditar e avaliar as confoguraçoes dos recvursos da aws.

## AWS Trusted Advisor
é um serviço web que inspeciona seu ambiente AWS e faz recomendações em tempo real de acordo com as práticas recomendadas da AWS.

 faz recomendações de práticas recomendadas em cinco categorias: otimização de custos, desempenho, segurança, tolerância a falhas e limites de serviço.

<div id="preco"></div>

# 8. Definição de preços e suporte 💸 💵 ⏲

## AWS Cost Explorer
aws cost explorer é uma interfaace para visualizar, entender e gerenciar os custos e o uso da AWS ao longo do tempo
## AWS Marktplace
O AWS Marketplace é um catálogo digital com milhares de ofertas de fornecedores independentes de software. Você pode usar o AWS Marketplace para encontrar, testar e comprar software que pode ser executado na AWS. 
## AWS Budgets
é para definir orçamentos personalizados e enbviar aletergas quadndo o o uso ou os custos excede o valor orçado
No AWS Budgets, você pode criar orçamentos para planejar o uso do serviço, os custos de serviço e as reservas de instâncias.

<div id="migracao"></div>

# 9.Migração e inovação

## AWS Cloud Adoption Framework (AWS CAF)

<div id="vantagens"></div>

# 10. 
## AWS Cloud Adoption Framework (AWS CAF)
ajuda você a entender como projetar e operar sistemas confiáveis, seguros, eficientes e econômicos na nuvem AWS. 

O Well-Architected Framework se baseia em cinco pilares: 

Excelência operacional
Segurança
Confiabilidade
Eficiência de desempenho
Otimização de custos



* [Topo](#topo)

