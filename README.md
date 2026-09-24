# Estudos_NotebookLM_DIO

# 📓 Meu Caderno Temático: Design de APIs e Clean Code

🔗 [Clique aqui para acessar meu caderno público no NotebookLM](https://notebook.google.com/notebook/0b97fccc-1d4e-4a22-b218-06c761423dc0?authuser=1)

# 📝Tema Escolhido: Design de APIs e Clean Code (Código Limpo).
**Contexto:**
No ecossistema de desenvolvimento de software atual, as APIs (Application Programming Interfaces) são a espinha dorsal da comunicação entre sistemas, microsserviços e aplicações frontend (como web e mobile). No entanto, não basta apenas que uma API funcione; ela precisa ser intuitiva, segura e escalável. Aliado a isso, os princípios de Clean Code garantem que a base de código por trás dessas APIs seja legível, testável e de fácil manutenção a longo prazo, reduzindo o débito técnico.

Objetivos de Estudo:
   1. Compreender as melhores práticas: Mapear os princípios fundamentais para o design de APIs RESTful eficientes (como padronização de rotas, status HTTP e versionamento).
   2. Aplicar o Código Limpo: Entender como os conceitos de Clean Code e SOLID se aplicam diretamente no desenvolvimento e na arquitetura de APIs.
   3. Consolidar o conhecimento com IA: Utilizar o NotebookLM para processar fontes de referência, extrair resumos valiosos e criar um miniguia de consulta rápida para o dia a dia do desenvolvimento.

# 🧠 Engenharia de Prompts e "Cicatrizes"

Nesta seção, documento o processo de tentativa e erro (troubleshooting) até encontrar os prompts ideais para extrair o melhor conteúdo do NotebookLM.

**Teste 1:** Prompt Inicial (A Primeira tentativa)
   
   **Prompt utilizado:** "Resuma o que é Clean Code e como fazer uma boa API REST com base nas fontes."O que a IA entregou: Um texto corrido, muito teórico e genérico, parecendo um artigo da Wikipédia. Ela separou os assuntos e não conectou o "Código Limpo" com o "Design da API".
   
   **A Cicatriz/Problema:** Faltou direcionamento e formatação. A resposta não gerou valor prático para um desenvolvedor.

**Teste 2:** Prompt Estruturado (Aplicação de alguns recursos presente nas fontes)
   
   **Prompt utilizado:** "Com base nas fontes anexadas, liste as boas práticas para criar uma API RESTful. Mostre como o Clean Code ajuda nisso. Dê exemplos de rotas."O que a IA entregou: A IA trouxe os exemplos de rotas e conectou bem os assuntos. Mencionou os vídeos da Rocketseat e do Filipe Deschamps.
   
   **A Cicatriz/Problema:** As respostas vieram em blocos de texto muito grandes. Faltou utilizar melhor os conceitos mais técnicos, como o Modelo de Maturidade de Richardson.

**Teste 3:** O Prompt Engenheirado (Extração total das informações presente nas fontes)
   
   **Prompt utilizado:**
   "Atue como um Arquiteto de Software Sênior. Analise as fontes fornecidas (especialmente o Google API Design Guide, o artigo do Martin Fowler e o vídeo da Rocketseat). Crie um guia direto e estruturado em Markdown sobre como aplicar Clean Code no Design de APIs RESTful. Sua resposta DEVE conter: 1. Uma tabela comparativa de Endpoints Ruins (acoplados/verbosos) vs Endpoints Limpos (orientados a recursos). 2. A relação entre o Modelo de Maturidade de Richardson e a legibilidade da API. 3. Cite a fonte de onde tirou cada afirmação."
   
   O que a IA entregou: Um material de altíssima qualidade. Ela gerou a tabela comparativa solicitada, usou a formatação Markdown perfeitamente, relacionou a semântica dos verbos HTTP com a clareza do código e citou os documentos de origem, entregando um mini-artigo digno de documentação técnica sênior.

# 🎓 Miniguia de Estudo: Design de APIs e Clean Code

Após processar as fontes e refinar os prompts, este é o guia consolidado gerado a partir do NotebookLM:

**1. Resumo Estruturado**

O Casamento entre Código Limpo e APIs RESTful

   **Nomenclatura Importa (Clean Code):** Assim como variáveis e funções devem ter nomes claros e revelar sua intenção (como defende Filipe Deschamps e o Clean Code), os Endpoints de uma API devem ser orientados a recursos (substantivos) e não a ações (verbos).

   ❌ Ruim: POST /criarUsuario ou GET /pegarClientes

   ✅ Bom: POST /usuarios ou GET /clientes

   **Deixe o HTTP fazer o trabalho dele:** A MDN e o Guia do Google reforçam que os verbos HTTP (GET, POST, PUT, PATCH, DELETE) já indicam a ação. Usá-los corretamente reduz a necessidade de criar rotas verbosas e confusas.

   **Maturidade da API:** Segundo o Modelo de Maturidade de Richardson (Martin Fowler), uma API atinge seu nível mais alto (Nível 3) quando utiliza HATEOAS, ou seja, quando a própria resposta da API fornece os links para as próximas ações possíveis, tornando-a autoexplicativa e independente.

**2. Glossário de Conceitos**

   **API RESTful**: Uma API que respeita as restrições arquiteturais do REST, utilizando corretamente os métodos HTTP, sendo stateless (sem estado) e orientada a recursos.

   **Resource-Oriented Design (Design Orientado a Recursos):** Padrão de design onde a API é modelada em torno de entidades de negócios (ex: "pedidos", "clientes") em vez de operações.

   **HATEOAS (Hypermedia as the Engine of Application State):** Conceito onde a API retorna, além dos dados, links navegáveis informando ao cliente o que ele pode fazer a seguir com aquele recurso.

   **Status Codes (Códigos de Status HTTP):** Respostas padronizadas do servidor (ex: 200 OK, 201 Created, 404 Not Found). Em uma API limpa, você nunca deve retornar um erro genérico 500 quando a culpa foi do cliente (400 Bad Request).

   **Débito Técnico:** O custo implícito de escolher uma solução fácil e rápida agora, em vez da abordagem melhor (Clean Code), que exigirá refatoração no futuro.

**3. Prompts Reutilizáveis (Para futuras revisões)**

Caso você ou outro desenvolvedor queira explorar mais esse caderno no NotebookLM, utilize estes prompts testados:

   💡 "Analise as fontes e crie um checklist de 5 passos para revisar o código de uma rota de API, focando em legibilidade e tratamento correto de erros HTTP."

   💡 "Explique o Modelo de Maturidade de Richardson como se você estivesse ensinando a um desenvolvedor Júnior, utilizando uma analogia com um restaurante."

   💡 "Quais são os principais 'code smells' (cheiros de código ruim) no design de uma API segundo o guia do Google e os princípios do Clean Code?"
   
# 📚 Curadoria de Fontes

Para alimentar a inteligência do NotebookLM e garantir que os resumos e guias fossem baseados em referências sólidas e de mercado, foram selecionadas as seguintes fontes (artigos, documentações e vídeos):

   1. Google API Design Guide: Referência da indústria sobre como construir APIs orientadas a recursos, cobrindo padronização, nomenclatura e versionamento.
      Link: https://cloud.google.com/apis/design
      
   2. Clean Code JavaScript (Ryan McDermott): Adaptação open-source dos princípios do livro "Clean Code" do Uncle Bob, essencial para manter a base de código da API legível e manutenível.
      Link: https://github.com/ryanmcdermott/clean-code-javascript
      
   3. MDN Web Docs - HTTP: Documentação oficial e detalhada sobre o funcionamento do protocolo HTTP, métodos (verbos) e status codes.
      Link: https://developer.mozilla.org/pt-BR/docs/Web/HTTP
      
   4. The Twelve-Factor App: Metodologia consolidada para construção de aplicações (SaaS/APIs) escaláveis, independentes e declarativas.
      Link: https://12factor.net/pt_br/
      
   5. Richardson Maturity Model (Martin Fowler): Artigo de um dos maiores especialistas em arquitetura de software, detalhando os níveis de maturidade para alcançar uma verdadeira API RESTful.
      Link: https://martinfowler.com/articles/richardsonMaturityModel.html
      
   Vídeo 1: O que é API? REST e RESTful? (Rocketseat): Explicação didática sobre os conceitos e restrições da arquitetura REST.
      Link: https://www.youtube.com/watch?v=ghTrp1x_1As
   
   Vídeo 2: CLEAN CODE #1: Introdução (Filipe Deschamps): Reflexão essencial sobre a importância de manter um código legível para a saúde do projeto.
     Link: https://www.youtube.com/watch?v=9w3o9NHXqu0
