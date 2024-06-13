# Estudo das ferramentas em nuvens comerciais que fornecem soluções de PLN.

&emsp;&emsp;PLN ou Processamento de Linguagem Natural, é uma área do machine learning, que possibilita ao computador interpretar, manipular e entender a linguagem humana. Atualmente, dados são muito valiosos e cada vez mais utilizados em grandes escalas e volumes, tanto em forma de texto, como de voz, em diversos canais, como e-mails, canais de atendimento, mensagens de texto, etc. Para isso, podemos automatizar, optimizar e melhoras esses atendimentos, via o uso de modelos de PLN, que processam e analisam esses dados, podendo responder em tempo real de forma humana, analisar os sentimentos e a intenção daquela mensagem.

&emsp;&emsp;Existem diversas empresas que possuem modelos de PLN, entretanto, para essa ponderada, levaremos em condição apenas a AWS e os modelos de PLN disponíveis em seu site (https://aws.amazon.com/pt/what-is/nlp/).

1. **Amazon Comprehend:** O Amazon Comprehend ajuda a descobrir insights e relacionamentos em textos, ao mesmo tempo que textos, key-words e key-phrases, tópicos e sentimentos de documentos. Um exemplo de aplicação do Amazon Comprehend seria o da organização FINRA, de serviços financeiros, que utiliza o Amazon Comprehend para extrair textos e partes chaves de documentos, em seus processos de investigação, exame e conformidade de processos financeiros alheios. Onde, antes eles precisavam ler e examinar manualmente os documentos, página por página, agora podem extrair frases e palavras chave, além de textos e seções específicas.

2. **Amazon Transcribe**: O Amazon Transcribe, realiza reconhecimento automático de fala, podendo: obter insights de conversas com clientes, criar legendas e apontamentos de reuniões, detectar conteúdos tóxicos em faixas de áudio, entre outras funções. Um exemplo de aplicação prática do Amazon Transcribe, seria o da empresa Nascar, de automobilismo, que utilizou o Amazon Transcribe para construir um sistema automatizado para controlar como personalizar o reconhecimento de voz na habilitação do seu conteúdo de VOD em 29 diferentes idiomas, que desde a implementação do Amazon Transcribe, adicionaram automaticamente legendas a 99% no conteúdo VOD.

3. **Amazon Translate**: O Amazon Translate é o serviço de tradução em larga escala da Amazon, que possibilita traduzir e analisar grandes volumes de texto multilinguais. Um exemplo prático de uma aplicação do Amazon Translate, seria o da empresa Mercado Livre, que traduz listas de E-Commerce em inglês para Espanhol e Português, fazendo em média, 2 milhões de traduções por semana em uma velocidade de 10 milhões de caracteres analisados por hora.

4. **Amazon Polly**: O Amazon Polly consiste em um serviço de transformação de texto em fala, com voz natural feita por deep learning para sintetizar a fala humana. Um exemplo de aplicação prática do Amazon Polly, seria o da empresa de mídia The Washington Post, que usa o Amazon Polly para converter seus artigos escritos, em falados por voz humana sintética, feita pelo Amazon Polly em sua plataforma digital. 

5. **Amazon Lex**: O Amazon Lex é o serviço da Amazon de criação de chatbots feitos com modelos avançados de PLN para criar interfaces de conversação em aplicações, possibilitando: Atendimento ao cliente, roteamento inteligente, produtividade empresarial, vendas e marketing de produtos. Um exemplo de aplicação prática, seria o da empresa dona da rede de supermercados Morrisons, que em 8 semanas montou uma central de contato de autoatendimento com o Amazon Lex, reduzindo o tempo de alteração de mensagens automatizadas de 5 a 10 dias para minutos, e aumentando a equipe da central de atendimento durante a pandemia de COVID-19.

6. **Amazon Kendra**: O Amazon Kendra é um serviço de serviço de pesquisa empresarial inteligente para encontro de conteúdos específicos. Um exemplo de aplicação prática do Amazon Kendra, foi o da empresa Gilead, que queria aumentar a produtividade dos funcionários e agilizar os processos internos de gerenciamento de dados, que, para trabalhar nesse sentido, a empresa queria desenvolver uma ferramenta de pesquisa corporativa escalável que usasse machine learning para fornecer análises preditivas e localizar documentos, conhecimentos e dados importantes em um local centralizado, e para isso, utilizou o Amazon Kendra.

7. **Amazon SageMaker:** O Amazon SageMaker facilita a preparação de dados e a criação, treinamento e implantação de modelos de Machine Learning para qualquer caso que possua infraestrutura, ferramentas e fluxos de trabalho, com ferramentas como: cadernos, depuradores, perfiladores, pipelines, MLOps, entre outros, em uma IDE. Um exemplo de aplicação prática do Amazon SageMaker, é o da empresa LG, que em sua subárea LG AI Research, escalou o desenvolvimento de modelos IA básicos com o uso do SageMaker, criando o EXAONE, um modelo básico que pode ser usado para transformar processos de negócios, usando o Amazon SageMaker, ampliando o acesso à IA em vários setores, como moda, manufatura, pesquisa, educação e finanças.

#### Requisições HTTP

&emsp;&emsp;Para executar as operações do AWS via requisições HTTP, é necessário utilizar o método POST no cabeçalho da solicitação. 

- A seguir, um exemplo das exigências no cabeçalho para fazer uma requisição HTTP pelo AWS Data Pipeline:

-----------------------------

POST / HTTP/1.1

host: https://datapipeline.us-east-1.amazonaws.com

x-amz-date: Mon, 12 Nov 2012 17:49:52 GMT

x-amz-target: DataPipeline_20121129.CreatePipeline

Authorization: AuthParams

Content-Type: application/x-amz-json-1.1

Content-Length: 50

Connection: Keep-Alive

{"name": "MyPipeline",

 "uniqueId": "12345ABCDEFG"}
                    

----------------

- Resposta do AWS Data Pipeline:

--------------------------

HTTP/1.1 200

x-amzn-RequestId: b16911ce-0774-11e2-af6f-6bc7a6be60d9

x-amz-crc32: 2215946753

Content-Type: application/x-amz-json-1.0

Content-Length: 2

Date: Mon, 16 Jan 2012 17:50:53 GMT

{"pipelineId": "df-00627471SOVYZEXAMPLE"}
                    
------------------


### Referências

- [Realizando Requisições HTTP com AWS Data Pipeline](https://docs.aws.amazon.com/pt_br/datapipeline/latest/DeveloperGuide/dp-make-http-request.html)
- [Casos de Sucesso dos Clientes do Amazon Comprehend](https://aws.amazon.com/pt/comprehend/customers/?pg=ln&sec=c)
- [Amazon Comprehend](https://aws.amazon.com/pt/comprehend/)
- [Gerenciamento de Taxa de Transferência com Amazon API Gateway](https://docs.aws.amazon.com/pt_br/apigateway/latest/developerguide/http-api-throttling.html)
- [Amazon Transcribe](https://aws.amazon.com/pt/transcribe/)
- [Casos de Sucesso dos Clientes do Amazon Transcribe](https://aws.amazon.com/pt/transcribe/customers/)
- [Amazon Translate](https://aws.amazon.com/pt/translate/)
- [Estudo de Caso do Mercado Livre usando AI/ML da AWS](https://aws.amazon.com/pt/solutions/case-studies/mercado-libre-ai-ml/)
- [O que é Processamento de Linguagem Natural (NLP) na AWS?](https://aws.amazon.com/pt/what-is/nlp/)
- [Amazon Polly](https://aws.amazon.com/pt/polly/)
- [Amazon Lex](https://aws.amazon.com/pt/lex/)
- [Estudo de Caso da Morrisons Connect usando AWS](https://aws.amazon.com/pt/solutions/case-studies/Morrisons-Connect-case-study/)
- [Amazon Kendra](https://aws.amazon.com/pt/kendra/)
- [Estudo de Caso da Gilead usando AWS](https://aws.amazon.com/pt/solutions/case-studies/gilead-case-study/)
- [Estudo de Caso da LG AI Research usando AWS](https://aws.amazon.com/pt/solutions/case-studies/lg-ai-research-case-study/)
- [AWS Data Pipeline: Realizando Requisições HTTP](https://docs.aws.amazon.com/pt_br/datapipeline/latest/DeveloperGuide/dp-make-http-request.html)
- [Amazon SageMaker](https://aws.amazon.com/pt/sagemaker/)



            


