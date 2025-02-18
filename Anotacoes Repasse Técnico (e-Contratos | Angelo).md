# Repasse Técnico Front | e-Contrato

# >>  (17/02/2025)
Apresentação das Equipes

### Canix
 - Max: Líder técnico.
 - Bruno: mais tempo no desenvolvimento do projeto.

### COTIC

- Sacc

  - Yury Vidal: Líde Técnico
  - Tiago Mateus: Analista  e tem base em react em 2018 e trabalhado com Vue.js
  - Gabriel Vidal: Começou agora a ter contato com o React e Vue.

- e-Parcerias

  - Eliezer
  - Angelo
  - Juarez
  - Davi
  - Charles

---

# 1. Visão Geral - Negócio

Gestão de Contratação (Verde) e Portal do Contratado(Laranja)

- O único modelo que tem no Front de Gestão e não tem do Contratado é o de Relatório.
- A API de Serviço é um serviço separado com autenticação  separada e desacoplada, para ser disponibilizado para quem irá consumir.

# 2. Visão Geral  - Macroprocessos

- Solicitação da Contratação -> Formalização e Publicação da Contratação -> Acompanahamento do Instrumento Contratual -> Encerramento do Contrato

# 2.1. Arquitetura

![image](https://github.com/user-attachments/assets/9f0959be-e403-4653-93fa-0149cc0f1653)

- Utilização do [IndexedDB](https://dev.to/esponges/indexeddb-your-offline-and-serverless-db-in-your-browser-with-react-3hm7) para utilização de cache no front.


# 2.2. Infra

![image](https://github.com/user-attachments/assets/603fb789-e64d-4a03-ba4a-081a1a66e7d8)

- Utilização do ELS com a indexação com os dados do contratos tabulares e dos instruentos
- Redis para a seção de usuários e guardar o cache e mensageria.
- Ngix está como API gateway
- Réplica do banco apenas para leitura para consumo da API externa.

# 2.3. Vesoes Tecnologias

 - Java 17
 - PostgresSQL 14
 - Spring Boot 3

---

# 3. Arquitetura Front

![image](https://github.com/user-attachments/assets/d0e116d2-b165-40a5-9881-d7639c93cbe8)

Interceptor

- Intercepta cada requisição e colocar o access Token.
- Como toda requisição está sujeita a falhas o Interceptor direciona para as exceções.
- No front interceptor.js
- Pegar o refresh token e enviar para o Back para que seja enviado um novo token para continuar a fila de requests.

# 3.1. Estrutura de Pastas

![image](https://github.com/user-attachments/assets/19230769-40c5-4afb-8a4d-587f985b9047)


# 3.1.1. _.vscode_
- Ao abrir o projeto é alterado as cores do VsCode para diferenciar de forma visual na IDE em quam projeto estamos

![image](https://github.com/user-attachments/assets/399c6968-9a68-475b-8d42-bef8c0a029bf)

# 3.1.1. _conf_

![image](https://github.com/user-attachments/assets/4c171627-620f-4b52-8f26-ec5790de48aa)

# 3.1.1. _docs_

- Utiliza a lib [Docusaurus](https://docusaurus.io/)
- Todas as docs do sistema em _.md_
- Arquitetura
- Desenvolvimento
- Testes
- Ultilitários
- está ligado ao /website

# 3.1.1. _node_modules_

- Dependências instaladas pelo projeto

# 3.1.2. _public_

- Arquivos que serão utilizado por toda a aplicação, principalmente durante o build
- E tem os paths que se for atualizado o serviceWorker é que gerencia os redirecionamentos.

# 3.1.3. _dist_

- Pasta gerada pelo build
- npm run prev roda os arquivos estáticos que irão para prod

# 3.1.4. _website_

- Pasta gerada pelo Docusaurus para a documentação

# 3.1.5. _.editorconfig_

- Configuração do prettier

# 3.1.5. Arquivos _.env_

- Dentro do env está o APP_VERSION e o SPRINT_VERSION que é incrementado manualmente, mas lá pela CANIX de forma automática.

---

# >>  (18/02/2025)

# Estruturas de Pastas e Nomemclaturas

- ExemploComponent
- Se ele possuir subcomponentes, criar uma subpasta: /PrimeiroComponent e dentro dele um index.tsx;
- Se o componente acima for um formuláro e possuir steps, criar o PrimeiroStep e dentro dela /components. Obs: só pode ter duas pastas compoenets para cada compenent macro;
- Arquivo de teste fica na raiz com o mesmo no da pasta .spec.tsx;
- Todos os componentes do sistema estão cobertos por teste? Não sabe, pois era feito em momentos de folga entre uma sprint e outra.
- Para executar os testes é o vite test, que por baixo usa o Jest.
