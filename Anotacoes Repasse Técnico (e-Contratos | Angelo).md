# Repasse Técnico Front | e-Contrato (17/02/2025)
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
