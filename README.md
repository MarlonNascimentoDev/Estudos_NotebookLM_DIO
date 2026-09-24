<div align="center">
  <h1>📓 Caderno Temático: Design de APIs e Clean Code</h1>
  <p>
    <img src="[https://img.shields.io/badge/Google-NotebookLM-4285F4?style=for-the-badge&logo=google&logoColor=white](https://img.shields.io/badge/Google-NotebookLM-4285F4?style=for-the-badge&logo=google&logoColor=white)" alt="NotebookLM Badge">
    <img src="[https://img.shields.io/badge/Architecture-RESTful%20API-FF7139?style=for-the-badge&logo=postman&logoColor=white](https://img.shields.io/badge/Architecture-RESTful%20API-FF7139?style=for-the-badge&logo=postman&logoColor=white)" alt="REST API">
    <img src="[https://img.shields.io/badge/Code-Clean%20Code-00C7B7?style=for-the-badge&logo=clean-code&logoColor=white](https://img.shields.io/badge/Code-Clean%20Code-00C7B7?style=for-the-badge&logo=clean-code&logoColor=white)" alt="Clean Code">
  </p>
  <p>
    <em>Estudo prático utilizando Inteligência Artificial para destrinchar e resumir as melhores práticas de desenvolvimento, arquitetura de APIs e Código Limpo.</em>
  </p>
</div>

> 🔗 **[Acesse meu caderno público e interativo no NotebookLM clicando aqui!](https://notebook.google.com/notebook/0b97fccc-1d4e-4a22-b218-06c761423dc0?authuser=1)**

---

## 📑 Índice
- [Contexto e Objetivos](#-contexto-e-objetivos)
- [Miniguia de Estudo](#-miniguia-de-estudo-design-de-apis-e-clean-code)
- [Engenharia de Prompts (Troubleshooting)](#-engenharia-de-prompts-e-cicatrizes)
- [Prompts Reutilizáveis](#-prompts-reutilizáveis)
- [Curadoria de Fontes](#-curadoria-de-fontes)

---

## 📝 Contexto e Objetivos

No ecossistema de desenvolvimento de software atual, as **APIs (Application Programming Interfaces)** são a espinha dorsal da comunicação entre sistemas, microsserviços e aplicações *frontend* (como web e mobile). No entanto, não basta apenas que uma API funcione; ela precisa ser intuitiva, segura e escalável. 

Aliado a isso, os princípios de **Clean Code** garantem que a base de código por trás dessas APIs seja legível, testável e de fácil manutenção a longo prazo, reduzindo o temido débito técnico.

### 🎯 Objetivos do Estudo
1. **Compreender as melhores práticas:** Mapear os princípios fundamentais para o design de APIs RESTful eficientes (como padronização de rotas, status HTTP e versionamento).
2. **Aplicar o Código Limpo:** Entender como os conceitos de Clean Code e SOLID se aplicam diretamente no desenvolvimento e na arquitetura de APIs.
3. **Consolidar o conhecimento com IA:** Utilizar o Google NotebookLM para processar fontes de referência, extrair resumos valiosos e criar um miniguia de consulta rápida para o dia a dia do desenvolvimento.

---

## 🎓 Miniguia de Estudo: Design de APIs e Clean Code

Após processar as fontes e refinar os prompts, este é o guia consolidado gerado a partir do NotebookLM:

### 1. O Casamento entre Código Limpo e APIs RESTful

**Nomenclatura Importa (Clean Code):** 
Assim como variáveis e funções devem ter nomes claros e revelar sua intenção (como defende Filipe Deschamps e o Clean Code), os Endpoints de uma API devem ser **orientados a recursos (substantivos)** e não a ações (verbos).

| Operação | ❌ Ruim (Acoplado/Verboso) | ✅ Bom (Orientado a Recursos) |
| :--- | :--- | :--- |
| **Criação** | `POST /criarUsuario` | `POST /usuarios` |
| **Busca** | `GET /pegarClientes` | `GET /clientes` |

**Deixe o HTTP fazer o trabalho dele:** 
A MDN e o Guia do Google reforçam que os verbos HTTP (`GET`, `POST`, `PUT`, `PATCH`, `DELETE`) já indicam a ação. Usá-los corretamente reduz a necessidade de criar rotas verbosas e confusas.

**Maturidade da API:** 
Segundo o *Modelo de Maturidade de Richardson* (Martin Fowler), uma API atinge seu nível mais alto (Nível 3) quando utiliza **HATEOAS**, ou seja, quando a própria resposta da API fornece os links para as próximas ações possíveis, tornando-a autoexplicativa e independente.

### 2. Glossário de Conceitos

- 🌐 **API RESTful:** Uma API que respeita as restrições arquiteturais do REST, utilizando corretamente os métodos HTTP, sendo *stateless* (sem estado) e orientada a recursos.
- 📦 **Resource-Oriented Design:** Padrão de design onde a API é modelada em torno de entidades de negócios (ex: "pedidos", "clientes") em vez de operações.
- 🔗 **HATEOAS:** *(Hypermedia as the Engine of Application State)*. Conceito onde a API retorna, além dos dados, links navegáveis informando ao cliente o que ele pode fazer a seguir com aquele recurso.
- 🚦 **Status Codes:** Respostas padronizadas do servidor. Em uma API limpa, você nunca deve retornar um erro genérico `500 Internal Server Error` quando a culpa foi de uma requisição malformada do cliente (`400 Bad Request`).
- 💳 **Débito Técnico:** O custo implícito de escolher uma solução fácil e rápida agora, em vez da abordagem correta (Clean Code), que exigirá refatoração e dores de cabeça no futuro.

---

## 🧠 Engenharia de Prompts e "Cicatrizes"

Abaixo está documentado o processo de tentativa e erro (*troubleshooting*) até encontrar as instruções ideais para extrair o melhor conteúdo da IA.

<details>
<summary><b>❌ Teste 1: O Prompt Inicial (A Primeira tentativa)</b></summary>
<br>

> **Prompt utilizado:** *"Resuma o que é Clean Code e como fazer uma boa API REST com base nas fontes."*

- **O que a IA entregou:** Um texto corrido, muito teórico e genérico, parecendo um artigo da Wikipédia. Ela separou os assuntos e não conectou o "Código Limpo" com o "Design da API".
- **A Cicatriz/Problema:** Faltou direcionamento e formatação. A resposta não gerou valor prático para um desenvolvedor.
</details>

<details>
<summary><b>⚠️ Teste 2: O Prompt Estruturado (Melhoria parcial)</b></summary>
<br>

> **Prompt utilizado:** *"Com base nas fontes anexadas, liste as boas práticas para criar uma API RESTful. Mostre como o Clean Code ajuda nisso. Dê exemplos de rotas."*

- **O que a IA entregou:** A IA trouxe os exemplos de rotas e conectou bem os assuntos. Mencionou os vídeos da Rocketseat e do Filipe Deschamps.
- **A Cicatriz/Problema:** As respostas vieram em blocos de texto muito grandes. Faltou utilizar melhor os conceitos mais técnicos, como o Modelo de Maturidade de Richardson.
</details>

<details>
<summary><b>✅ Teste 3: O Prompt Engenheirado (Sucesso total)</b></summary>
<br>

> **Prompt utilizado:** *"Atue como um Arquiteto de Software Sênior. Analise as fontes fornecidas (especialmente o Google API Design Guide, o artigo do Martin Fowler e o vídeo da Rocketseat). Crie um guia direto e estruturado em Markdown sobre como aplicar Clean Code no Design de APIs RESTful. Sua resposta DEVE conter: 1. Uma tabela comparativa de Endpoints Ruins (acoplados/verbosos) vs Endpoints Limpos (orientados a recursos). 2. A relação entre o Modelo de Maturidade de Richardson e a legibilidade da API. 3. Cite a fonte de onde tirou cada afirmação."*

- **O que a IA entregou:** Um material de altíssima qualidade. Ela gerou a tabela comparativa solicitada, usou a formatação Markdown perfeitamente, relacionou a semântica dos verbos HTTP com a clareza do código e citou os documentos de origem, entregando um mini-artigo digno de documentação técnica sênior.
</details>

---

## 🤖 Prompts Reutilizáveis 

Caso você ou outro desenvolvedor queira explorar mais esse caderno no NotebookLM, utilize estes *prompts* já testados e validados. É só copiar e colar:

> 💡 **Prompt 1: Revisão de Código (Code Review)**  
> *"Analise as fontes e crie um checklist de 5 passos para revisar o código de uma rota de API, focando em legibilidade e tratamento correto de erros HTTP."*

> 💡 **Prompt 2: Explicação Didática (Técnica Feynman)**  
> *"Explique o Modelo de Maturidade de Richardson como se você estivesse ensinando a um desenvolvedor Júnior, utilizando uma analogia com um restaurante."*

> 💡 **Prompt 3: Identificação de Anti-padrões**  
> *"Quais são os principais 'code smells' (cheiros de código ruim) no design de uma API segundo o guia do Google e os princípios do Clean Code?"*

---

## 📚 Curadoria de Fontes

Para alimentar a inteligência do NotebookLM e garantir que os resumos e guias fossem baseados em referências sólidas e de mercado, foram selecionadas as seguintes fontes:

| Tipo | Fonte / Título | Descrição | Link |
| :---: | :--- | :--- | :--- |
| 📄 | **Google API Design Guide** | Referência da indústria sobre como construir APIs orientadas a recursos, cobrindo padronização, nomenclatura e versionamento. | [Acessar](https://cloud.google.com/apis/design) |
| 💻 | **Clean Code JavaScript** | Adaptação open-source dos princípios do livro "Clean Code" do Uncle Bob, essencial para manter a API manutenível. | [Acessar](https://github.com/ryanmcdermott/clean-code-javascript) |
| 📖 | **MDN Web Docs - HTTP** | Documentação oficial e detalhada sobre o funcionamento do protocolo HTTP, métodos (verbos) e status codes. | [Acessar](https://developer.mozilla.org/pt-BR/docs/Web/HTTP) |
| 🏗️ | **The Twelve-Factor App** | Metodologia consolidada para construção de aplicações (SaaS/APIs) escaláveis, independentes e declarativas. | [Acessar](https://12factor.net/pt_br/) |
| 🏛️ | **Richardson Maturity Model** | Artigo de Martin Fowler detalhando os níveis de maturidade para alcançar uma verdadeira API RESTful. | [Acessar](https://martinfowler.com/articles/richardsonMaturityModel.html) |
| 🎥 | **Rocketseat: REST e RESTful** | Explicação didática sobre os conceitos e restrições da arquitetura REST. | [Assistir](https://www.youtube.com/watch?v=ghTrp1x_1As) |
| 🎥 | **Filipe Deschamps: Clean Code** | Reflexão essencial sobre a importância de manter um código legível para a saúde do projeto. | [Assistir](https://www.youtube.com/watch?v=9w3o9NHXqu0) |

---
<p align="center">
  Desenvolvido durante os estudos sobre Arquitetura e Engenharia de Prompts 🚀
</p>
