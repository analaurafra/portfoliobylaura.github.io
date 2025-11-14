---
layout: post
title: "Fundamentos da IA Generativa com Bedrock"
categories: junk
author:
- Ana Laura Martins
meta: "Springfield"
modified_date: 2025-11-13
---

### Fundamentos da IA Generativa com Bedrock - Nexa 

Anotações e práticas do Bootcamp de **Fundamentos da IA Generativa com Bedrock**.
Treinamento imersivo sobre os **Fundamentos da Inteligência Artificial Generativa** e treinamento prático utilizando os serviços da **AWS**, como:

-  **Amazon Bedrock;**
- **PartyRock;**
- **Amazon Nova;**
- **AgentCore**.

Trilha de aprendizado para aplicação da IA em soluções reais.


#### MACHINE LEARNING

É uma área da inteligência artificial que procura ensinar máquinas via dados de entrada.

Machine Learning = A máquina aprender com você ou com uma massa de dados de outras pessoas.

Machine Learning aprende com várias pessoas. Oferecendo conteúdo personalizados.



#### MODELOS DE ALGORITMOS DAS IAS

- **Algoritmo de Aprendizado Supervisionado:**

Modelos de dados de entrada com respostas corretas, onde serão abstraídos os dados corretos, cujo o modelo buscará padrões de forma mais facilitada. O profissional de machine learning tem um papel de "professor".

- **Algoritmo de Aprendizado Não Supervisionado:**

Neste modelo, eu tenho uma massa de entrada apenas e o algoritmo me ajuda a agrupar e facilitar a análise dos mesmos.

- **Algoritmo de Aprendizado por Reforço:**

O agente aprende com o usuário interagindo com o ambiente, recebendo recompensas mediante acertos e punições mediante erros. 


#### VISÃO COMPUTACIONAL

- **Redes Neurais Convulacionais:**

Inspirada no funcionamento do cérebro humano, possui capacidade de identificar padrões para reconhecimento de controles (exemplo: formato de um objetivo, animal, objetos, imagens, detectar sentimentos, movimentos humanos ou não humanos, compreensão do ambiente etc).

É possível imputar uma massa de dados maior, porém o sistema consegue diferenciar, exemplo: sistema de um carro autônomo, como um Tesla.

- **Detecção e Reconhecimento Facial:**

Utilizado em várias tecnologias como sistemas de banco, vigilância, ticketsde shows e etc. Identificando padrões através destes recursos.


#### PROCESSO DE LINGUAGEM NATURAL (PNL)

É uma subárea da inteligência artificial, que busca permitir que computadores compreendam e interajam através da linguagem humana.

Utiliza um algoritmo de Redes Neurais para utilizar a linguagem natural para extrair informações.

São treinados via textos, onde posteriormente eles reconhecerão padrões e atribuem probabilidades dentro do contexto atual, comparando as massas de dados.

O algoritmo utiliza um modelo matemático no backend (token) para chegar próximo da resposta do contexto do usuário.

- **Desambiguação Semântica:**

Uma mesma palavra ou frase pode ter o mesmo significado, a desambiguação semântica analisa a ambiguidade das palavras. Também utiliza o contexto para identificar quais informações são mais adequadas ao contexto de forma mais coerente. 

- **Redes Neurais de Linguagem:**

O processo de geração de texto utiliza um volume gigante de textos como massa de dados, com vários modelos de abstração da gramática. 

O prompt gera respostas coerentes. 


#### ROBÓTICA


A robótica está presente no nosso dia a dia e de forma acessível. É uma área multidisciplinar que engloba várias tecnologias. Com a intenção de trazer autonomia a esses equipamentos como: Alexa,acho dots Echo Dots, etc.

Os robôs são equipados com câmeras e sensores, que interpretam objetos e reconhecem imagens. Utilizam sensores táteis e emocionais mediante diversos algoritmos de aprendizagem de máquina, por reforço (aprendizagem com base em recompensas e Deep learning).


#### DESMISTIFICANDO A INTELIGÊNCIA ARTIFICIAL

**IAs Generativas Aplicadas:**

São sistemas capazes de criar, adaptar e aprimorar conteúdos de maneira autônoma, sempre aprendendo e se aperfeiçoando. GPT

|**Chatbots:**|
|----|
|ChatGPT - Chatbot - Open IA|
|Bing Chat - Microsoft|
|Google Bard - Google|

|**Assistentes Virtuais:**|
|----|
|Google Assistant - Google|
|Alexa - Amazon |
|Siri - Apple|


**Gamma App - IA de Geração de Apresentações de Slides**

Chatbots (IAs Generativas):

Ferramenta de consulta a uma IA utilizando linguagem natural. 

- Bard - Precisa criar uma conta - Exclusivo do Google

- Bing Chat - Não precisa criar uma conta - Inspirado no modelo da Open AI (tem parceria com a Open AI)

- Chat GPT - Precisa criar uma conta - Inspirado no Modelo da Open IA (Tem parceria com a Open AI)

#### NA PRÁTICA

Vamos testar uma API da Open IA para gerar mensagem de voz, faça um cadastro na plataforma.

<img src="{{ '/assets/img/img_25.png' | relative_url }}" alt="img_25"/>
<br>
<br>


Localize a API da Open IA para execução e testes no **Postman**:

<img src="{{ '/assets/img/img_22.png' | relative_url }}" alt="img_22"/>
<br>
<br>

A seguir localize o campo relacionado a áudios:

<img src="{{ '/assets/img/img_23.png' | relative_url }}" alt="img_23"/>
<br>
<br>

- Exemplo para gerar áudio **Create Speech** utilizando os comando abaixo:

**Método: POST**
URL: [https://api.openai.com/v1/audio/speech](https://api.openai.com/v1/audio/speech)

**HEADERS:**

```
Authorization: Bearer SEU_TOKEN_AQUI
Content-Type: application/json

```

A seguir será necessário gerar um **Token** acesse: [openai.com/api-keys](https://platform.openai.com/api-keys).

<img src="{{ '/assets/img/img_24.png' | relative_url }}" alt="img_24"/>
<br>
<br>

Gere o **Secret Key**, copie e cole e o salve em um local que possa ser recuperado posteriormente.

**Atenção: Para realizar este teste até concluí-lo é necessário possuir créditos na Open Ia.**


Na aba **Body** substitua o Json de exemplo pelo json:

```
{
  "model": "gpt-4o-mini-tts",
  "voice": "alloy",
  "input": "Olá! Este é um teste de áudio gerado pela API."
}

```

**Depois que enviar, o Postman vai baixar o arquivo .mp3 como resposta — você pode ouvir o áudio.**
