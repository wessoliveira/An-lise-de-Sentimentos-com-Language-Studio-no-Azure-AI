# Análise de Sentimentos com Azure Speech Studio e Language Studio no Azure AI
Este documento serve como um material de apoio consolidado sobre as ferramentas de Inteligência Artificial da Microsoft, com foco no Azure AI Language Studio e no Azure AI Speech Studio. O objetivo é fornecer anotações e insights sobre como estas plataformas permitem a análise avançada de texto e fala, servindo como base para estudos e futuras implementações.

## 1. Conhecendo o Language Studio
O Azure AI Language Studio é um portal unificado que oferece uma interface visual (low-code/no-code) para explorar, testar e implementar os recursos do Serviço de Linguagem do Azure. Ele permite que programadores e especialistas de domínio integrem facilmente a compreensão de linguagem natural em suas aplicações.

### Principais Capacidades:

- Análise de Sentimento e Mineração de Opinião: Determina se um texto é positivo, negativo, neutro ou misto.

- Extração de Entidades e Frases-Chave: Identifica os principais conceitos e entidades (pessoas, locais, organizações) num texto.

- Sumarização de Texto: Gera resumos automáticos de documentos e conversas.

- Resposta a Perguntas (Question Answering): Cria bases de conhecimento que respondem a perguntas em linguagem natural.

- Compreensão da Linguagem Coloquial (CLU): O pilar para entender as intenções do utilizador em conversas.

## 2. Análise de Texto e Resposta a Perguntas
Dentro do Language Studio, estas são duas das funcionalidades mais utilizadas:

### a) Análise de Sentimentos
Esta funcionalidade avalia o tom emocional de um texto. É crucial para monitorizar a satisfação do cliente.

- Como funciona: A API devolve uma pontuação de sentimento para o documento como um todo e para cada frase individualmente.

- Categorias: Positivo, Negativo, Neutro e Misto.

- Caso de Uso: Analisar automaticamente o feedback de clientes em e-mails, redes sociais ou inquéritos para identificar tendências e problemas urgentes.

### b) Resposta a Perguntas (Question Answering)

Este recurso permite criar um serviço de perguntas e respostas a partir de conteúdo existente.

- Como funciona: Você "alimenta" o serviço com os seus próprios dados (FAQs, manuais de produtos, bases de conhecimento). A IA então indexa essa informação e torna-se capaz de encontrar a melhor resposta para uma pergunta feita em linguagem natural.

- Caso de Uso: Criar um "chatbot" de suporte de primeira linha que responde às perguntas mais comuns dos clientes, reduzindo a carga sobre os agentes humanos.

## 3. Compreensão da Linguagem Coloquial (CLU)

Esta é uma das funcionalidades mais avançadas e a base para a criação de assistentes virtuais e bots robustos. É o sucessor do LUIS (Language Understanding Intelligent Service).

### O que faz:

O CLU foi projetado para "descodificar" o que um utilizador quer dizer numa conversa informal. Ele faz isso identificando duas coisas:

- Intenção (Intent): O objetivo ou a ação que o utilizador quer realizar (ex: ReservarVoo, VerificarEstadoEncomenda).

- Entidades (Entities): Os pedaços de informação cruciais dentro da frase que dão contexto à intenção (ex: Lisboa como destino, amanhã como data).

### Exemplo Prático:

-	Frase do utilizador: "Eu quero marcar uma passagem de avião para o Porto para depois de amanhã."

-	Intenção: MarcarVoo

-	Entidades: Meio: avião, Destino: Porto, Data: depois de amanhã.

### Importância: 

É o "cérebro" que permite que um bot entenda o pedido do utilizador e saiba quais os próximos passos a tomar.

## 4. Conhecendo o Estúdio de Fala (Speech Studio)

O Azure AI Speech Studio é o portal análogo ao Language Studio, mas focado em tudo o que envolve voz. Ele fornece ferramentas para testar e implementar os recursos do Serviço de Fala do Azure.

### Principais Pilares:

- Reconhecimento de Fala (Speech-to-Text): Converte áudio em texto de forma precisa e rápida. Suporta transcrição em tempo real (para legendas) e em lote (para transcrever ficheiros de áudio).

- Síntese de Fala (Text-to-Speech): Converte texto em áudio com vozes neurais extremamente realistas e naturais. Permite customizar o estilo de fala (alegre, triste), a velocidade e o tom.

- Tradução de Fala: Fornece tradução de voz para voz ou de voz para texto em tempo real.

- Reconhecimento do Orador: Permite identificar quem está a falar com base nas suas características vocais únicas.

## 5. Serviço de Bot do Azure (Azure Bot Service)

O Azure Bot Service não é um serviço de análise, mas sim o framework que une tudo. É a plataforma que permite construir, implementar e gerir um bot.

### Como se integra: 

Um bot criado com o Azure Bot Service funciona como o orquestrador:

- O utilizador fala com o bot.

- O Speech Studio (Speech-to-Text) converte a fala em texto.

- O texto é enviado para o Language Studio (CLU) para identificar a intenção e as entidades.

- Com base na intenção, o bot executa a sua lógica (ex: consultar uma base de dados).

- O bot formula uma resposta em texto.

- O Speech Studio (Text-to-Speech) converte a resposta em áudio e "fala" de volta para o utilizador.

Esta arquitetura permite a criação de assistentes de voz totalmente interativos e inteligentes.

## 6. Links Úteis

- Azure AI Language Studio: https://language.cognitive.azure.com/

Ideal para testar extração de entidades, análise de sentimentos e treinar modelos CLU.

- Azure AI Speech Studio: https://speech.microsoft.com/

Ideal para testar a qualidade das vozes neurais (Text-to-Speech) e a precisão da transcrição (Speech-to-Text).


