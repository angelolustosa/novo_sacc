# Resumo de Melhorias, Sugestões, Erros e Comentários

**Autor:** Angelo Lustosa

**Turma:** CGE-02
<!-- --- -->

## **20/01/24**

### **Melhorias**
- **Identidade Visual do Template**:
  - Alterar a identidade visual do template para incluir a identidade visual do estado nos e-mails e documentos.

- **Alterações Contratuais**:
  - Incluir a funcionalidade de **Corrigenda** como uma opção de alteração contratual, além de ADI e APO.

- **Perfis e Autorizações**:
  - Permitir que um perfil tenha diferentes visualizações dependendo do tipo de contrato.

- **Validação de Documentos**:
  - Implementar validação automática de documentos, como certidões, para evitar a necessidade de validação manual.

- **Cadastro de CNPJ**:
  - Criar um cadastro de CNPJ para cada item do contrato, evitando duplicidades e facilitando a gestão.

- **Linha do Tempo**:
  - Melhorar a visibilidade da análise financeira e jurídica na linha do tempo, para que seja possível identificar quem realizou a análise.

- **Assinatura Digital**:
  - Implementar a funcionalidade de assinatura digital para documentos como pareceres jurídicos.

- **Status de Erro**:
  - Melhorar a visibilidade do status de erro na aba de Publicação, com retentativas automáticas e feedback claro.

### **Sugestões**
- **Filtros na Tela de Solicitações**:
  - Adicionar filtros na tela de Solicitações de Contratação, especialmente para a aba "Em Andamento".

- **Feedback de Negação**:
  - Incluir feedback para o usuário quando uma solicitação for negada, com justificativa.

- **Relatórios**:
  - Adicionar cabeçalhos, rodapés e paginação aos relatórios.
  - Implementar relatórios de auditoria para todos os usuários.

- **Cadastro de Signatários**:
  - Alertar quando um órgão ficar sem signatários, evitando problemas no processo de contratação.

- **CEP e Endereço**:
  - Melhorar a base de CEP para incluir endereços completos e evitar erros no cadastro de usuários.

### **Erros**
- **Documentos sem Identidade Visual**:
  - Os e-mails e documentos estão sendo gerados sem a identidade visual do estado.

- **Validação de CPF**:
  - Erro ao tentar cadastrar um CPF que já existe no sistema.

- **Tempo de Homologação**:
  - O ambiente de homologação está lento (em torno de 3 minutos), enquanto em produção leva 30 minutos.

- **Tipos de Documentos**:
  - Erro ao tentar acessar a funcionalidade de tipos de documentos.

### **Comentários**
- **Representante Legal**:
  - Um representante pode ter mais de um CNPJ e escolher qual empresa deseja representar ao logar.

- **Status de Conclusão**:
  - O contrato só é marcado como concluído após a validação da área finalística.

- **Tempo para Assinatura**:
  - Há um prazo para assinatura dos signatários dentro do prazo de validade do contrato.

<!-- --- -->

## **21/01/24**

### **Melhorias**
- **Cadastro de Fornecedores**:
  - Notificar o solicitante quando um cadastro de fornecedor for negado.

- **Análise Financeira e Jurídica**:
  - Melhorar a visibilidade do status de análise financeira e jurídica na caixa de entrada.

- **Cronograma**:
  - Exibir o saldo disponível ao adicionar itens ao cronograma, evitando que o usuário ultrapasse o valor total permitido.

- **Documentos Definitivos**:
  - Incluir data de emissão e hashcode nos documentos definitivos para garantir sua autenticidade.

- **Relatórios de Gestor**:
  - Permitir a emissão de relatórios consolidados para contratos em andamento, liquidados e concluídos.

- **Matriz de Risco**:
  - Corrigir a nomenclatura de "Matriz de Risco" para "Mapa de Risco".

### **Sugestões**
- **Ata de Preço**:
  - Implementar funcionalidade de Ata de Preço.

- **Suspensão de Contratos**:
  - Incluir justificativas de suspensão no banco de dados, permitindo a geração de relatórios sem a necessidade de abrir documentos PDF.

- **Encerramento de Contratos**:
  - Exibir todas as pendências no encerramento do contrato, facilitando a conclusão.

### **Erros**
- **Duplicação de Análise Jurídica**:
  - Erro ao duplicar a análise jurídica, exigindo a assinatura de dois documentos.

- **Tempo de Assinatura**:
  - O sistema não diferencia entre documentos provisórios e definitivos na assinatura.

### **Comentários**
- **Ordem de Execução**:
  - A ordem de execução é assinada apenas pela contratante.

- **Sanções**:
  - As sanções são cadastradas no sistema, mas o processo judicial é realizado fora dele.

<!-- --- -->

## **22/01/24**

### **Melhorias**
- **Cadastro de CNPJ**:
  - Exibir CNPJs já utilizados como desabilitados ou tachados, evitando confusão.

- **Data de Ordem de Execução**:
  - Preencher automaticamente as datas de início e fim da ordem de execução com base na vigência do contrato.

- **Parecer Jurídico**:
  - Incluir dados do contrato no documento editável do parecer jurídico.

### **Sugestões**
- **Filtros na Tela de Solicitações**:
  - Adicionar filtros para facilitar a busca por responsáveis na tela de Solicitações de Contratação.

- **Modelos de Documentos**:
  - Permitir a criação de diretórios para organizar modelos de documentos.

### **Erros**
- **CPF não Permitido**:
  - Erro ao tentar cadastrar um CPF que não é permitido.

- **Máscara de Telefone**:
  - O campo de telefone só permite máscara de telefone fixo, não de celular.

### **Comentários**
- **Representante Legal**:
  - O representante legal pode ser diferente do gestor do contrato.

- **Juntada de Documentos**:
  - O contratado pode seguir sem anexar documentos se todos forem opcionais.

<!-- --- -->

## **23/01/24**

### **Melhorias**
- **Contratos de Obras**:
  - Integração com SIGSOP para carregar dados automaticamente.
  - Incluir funcionalidade para cadastrar vídeos e fotos das obras.

- **Contratos Corporativos**:
  - Implementar relatórios gerenciais para visualizar o total empenhado e pago de todos os contratos.

- **Relatórios**:
  - Adicionar campo multiselect para filtrar tipos de relatórios.

### **Sugestões**
- **Comissão de Avaliação**:
  - Informar na tela que a comissão de avaliação deve ter no mínimo 3 pessoas.

- **Ordem de Paralisação**:
  - Solicitar a inclusão da ordem de paralisação no serviço do SIGSOP.

### **Erros**
- **Labels Afastadas**:
  - As labels nas informações gerais dos contratos de obras ficam muito afastadas dos valores.

### **Comentários**
- **Contratos Sigilosos**:
  - Não existe contrato sigiloso no sistema.

- **Publicação no PNCP**:
  - Todos os tipos de formalização de contratação (Contrato, Dispensa de Razão de Valor e Compra Sem Obrigação Futura) são publicados no PNCP.

---

**Nota**: Essa categorização pode ser usada para priorizar melhorias, corrigir erros e implementar sugestões no sistema.
