
# Integração de Defects no App Case com Jira

## Criando um novo defect no Qase

### Quando devo criar um defect?
Para criar um novo defect no Qase, basta que o test run tenha apresentado um erro. O erro deve ser descrito e reportado conforme os requisitos solicitados no plano de teste.

**Exemplo de um erro:**

> **Pre-condições:** O usuário deve estar logado com credenciais válidas.  
> **Parâmetros:** Modal de arquivamento de modelo.  
> Botão "Não, voltar".

O erro apresentado foi o seguinte:

![Captura de Tela 2025-02-24 às 19:49:54](https://github.com/user-attachments/assets/f6f73e1a-cf19-4e72-a70a-7d10ae57543d)

## Como devo criar o defect?
Assim que o erro for reportado nos passos de execução, uma nova janela será aberta em formato de modal na tela do QA.

### Adicionando um Resultado

![Captura de Tela 2025-02-24 às 19:57:34](https://github.com/user-attachments/assets/c3c52ea4-98e7-450a-a4fe-fcd6abf89034)

#### Campos

- **Result**: Deve ser preenchido conforme o resultado do erro.
- **Comment**: Campo utilizado para descrever o resultado atual do passo que foi realizado. Este campo não será exibido ao desenvolvedor na criação da issue, mas sua descrição estará presente no arquivo `.md`, que conterá a descrição da issue e o report do erro na integração com o Jira.
- **Attachments**: Campo responsável por receber um arquivo demonstrando o erro na prática, como um print ou vídeo detalhando o comportamento.
- **Create/Attach Defect**: Este campo deve estar **marcado** para que o defect seja criado no próximo passo.

> **Observação:** Lembre-se de editar o seu test run para que todos os passos sejam preenchidos corretamente com os resultados!

### Criando o Defect

![Captura de Tela 2025-02-24 às 19:57:57](https://github.com/user-attachments/assets/51802bc9-92bb-4aed-988d-876f2b8da972)

#### Campos

- **Defect Title**: O título do defect deve estar relacionado ao plano de teste. Seguindo o exemplo anterior, o título do defect seria: "Validação do modal de arquivamento de modelo de pneu." Esse título será transferido para o título da issue na integração com o Jira.
- **Actual Result**: Deve conter uma descrição detalhada do erro, pois esse campo será utilizado como descrição da falha na integração com o Jira. Como os desenvolvedores não têm acesso ao Qase, é essencial que a descrição seja clara e intuitiva.
- **Milestone**: Este campo não será utilizado.
- **Severity**: Este campo deve ser preenchido de acordo com a prioridade do problema.

    > Seguir documentação na criação de prioridade.

- **Assignee**: Este campo deverá ser associado ao QA que reportou o erro (assign yourself).
- **Choose Integration**: Neste campo a integração deverá ser realizada com o Jira.

### Documentação de Prioridade
![Imagem](https://github.com/user-attachments/assets/252b449e-bcb5-43fe-828f-d89a15d7ac2b)

## Jira Cloud Issue - Criando Integração

> Apenas preencher os campos prioritários!

![Captura de Tela 2025-02-24 às 19:59:00](https://github.com/user-attachments/assets/86ada913-7dce-4182-8183-7d3f23eb4ff9)

- **Title**: Utilizar o título do plano de teste.
- **Description**: No campo ```actual result``` editar o markdown e descrever de forma detalhada o comportamento do erro.
- **Project**: Buscar por "zuq performance - gestão inteligente de pneus".

![Captura de Tela 2025-02-24 às 19:59:56](https://github.com/user-attachments/assets/5d0461e1-a68c-423e-98e6-2c8a50cad25f)

- **Issue Type**: Reportar como um bug.

![Captura de Tela 2025-02-24 às 20:00:17](https://github.com/user-attachments/assets/b1f5b908-2fed-4026-9988-9564371dbec8)

- **Components**: Não estamos utilizando este campo.
- **Assignee**: Atribuir ao Adriano enquanto não houver um perfil para a célula de testes.
- **Sprint**: Digite "pneu" e encontre a sprint com label ```Active```.
- **Parent**: Caso o seu plano de teste esteja relacionado a algum parent, atribuir. Exemplo: "Listagem de modelos de pneus".
- **Priority**: Utilizar documentação de prioridade.
- **Severity**: Utilizar documentação de prioridade.
- **Due Date**: Não estamos utilizando este campo.
- **Linked Issue**: Não estamos utilizando este campo.

![Captura de Tela 2025-02-24 às 20:00:43](https://github.com/user-attachments/assets/92c2823b-e05b-4693-8fee-c1267a5e594b)

- **Labels**: Não estamos utilizando este campo.
- **Reporter**: Atribuir ao Adriano enquanto não houver um perfil para a célula de testes.

![Captura de Tela 2025-02-24 às 21:04:57](https://github.com/user-attachments/assets/4120440f-1934-4e17-a42f-42eb3ae215ab)

### Conferindo 

Seu defect foi criado com sucesso e logo aparecerá na aba ```Defects``` do seu testRun dessa forma: 

![Captura de Tela 2025-02-24 às 21 24 48](https://github.com/user-attachments/assets/2ef31a28-da7a-4d21-8ad2-663b4f148863)

Após ser criado o Defect poderá ser editado, caso sinta necessidade para tal.

![Captura de Tela 2025-02-24 às 21 25 23](https://github.com/user-attachments/assets/c7e084cc-aa6d-4d1a-9333-1f002c2c7b89)

> Caso seu teste ja tenha sido executado e um erro foi reportado, para cadastrar um defect será necessário retestar!
