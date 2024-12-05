# Projeto: Neo Cabelos

## Participantes:
- **Celso Gabriel** - Matrícula: 12345 - Documentador/Testador (Responsável pelo planejamento e supervisão geral dos documentos e execução de testes).
- **Daniele Barbosa** - Matrícula: 67890 - Testadora/Codificadora (Responsável pela criação de código e execução de testes).
- **Luiz Fernando de Sena** - Matrícula: 11223 - Testador/Codificador (Auxiliou na criação de código e execução de testes).
- **Leonardo dos Santos** - Matrícula: 44556 - Testador/Codificador (Participou do desenvolvimento de funcionalidades e testes).
- **Rafael Malheiro** - Matrícula: 77889 - Documentador/Codificador (Responsável por documentar e codificar funcionalidades).
- **Thiago Henrique** - Matrícula: 99001 - Testador/Codificador (Contribuiu na implementação de código e testes).

---

## Sumário
1. [Resumo](#resumo)
2. [Cenários de Teste](#cenários-de-teste)
   - Identificação do Cenário
   - Descrição do Cenário
   - Pré-condições
   - Passos para Execução
   - Dados de Entrada
   - Resultados Esperados
   - Pós-condições
3. [Critérios de Aceitação](#critérios-de-aceitação)

---

## Resumo

### História do Usuário:
O projeto **Neo Cabelos** foi criado para atender a demanda de salões de beleza por soluções tecnológicas que facilitem o agendamento de serviços, como cortes de cabelo, maquiagem e design de sobrancelhas. Seu público-alvo são mulheres e homens que buscam praticidade e agilidade ao marcar horários nos salões.

### Objetivo:
- Automatizar o processo de agendamento para otimizar o tempo dos salões e garantir uma experiência mais intuitiva para os clientes.
- Fornecer uma plataforma moderna que simplifique o acesso aos serviços e contribua para a fidelização dos clientes.

### Tecnologia Utilizada:
- **Banco de Dados:** PostgreSQL, estruturado para oferecer performance e integridade de dados no gerenciamento de usuários, serviços e agendamentos.
- **Ferramentas de Teste:**
  - Trello para organização de tarefas relacionadas ao ciclo de desenvolvimento e testes.
  - Ferramentas manuais para testes de interface.
  - Selenium
- **IDE:** IntelliJ IDEA e VSCode para codificação e depuração.

---

## Cenários de Teste

### Cenário 1: Login de Acesso
- **Descrição:** Verificar a funcionalidade de autenticação do sistema.
- **Pré-condições:** Usuário cadastrado com credenciais válidas e sistema operacional.
- **Passos para Execução:**
  1. Acesse a página de login.
  2. Insira nome de usuário e senha nos campos apropriados.
  3. Clique em "Entrar".
  4. Verifique se o sistema redireciona o usuário para a página inicial.
  5. Tente realizar login com credenciais inválidas e verifique se o sistema exibe mensagem de erro.
- **Dados de Entrada:** Nome de usuário e senha.
- **Resultados Esperados:**
  - Acesso autorizado para credenciais válidas.
  - Mensagem "Credenciais inválidas" para login incorreto.
- **Pós-condições:** Usuário logado no sistema, com sessão iniciada.

---

### Cenário 2: Agendamento de Serviço
- **Descrição:** Testar o processo completo de agendamento.
- **Pré-condições:** Usuário logado no sistema e serviços disponíveis.
- **Passos para Execução:**
  1. Acesse a página de agendamento.
  2. Escolha data, horário e serviço desejados.
  3. Confirme o agendamento.
  4. Verifique se o sistema registra corretamente o agendamento.
  5. Tente agendar para horários já ocupados ou inválidos.
- **Dados de Entrada:** Data, horário e serviço.
- **Resultados Esperados:**
  - Mensagem de "Agendamento confirmado" para dados válidos.
  - Mensagem de erro para horários ou datas inválidos.
- **Pós-condições:** Agendamento registrado no banco de dados.

---

### Cenário 3: Cancelamento de Agendamento
- **Descrição:** Verificar se o usuário pode cancelar um agendamento futuro.
- **Pré-condições:** Agendamento existente e usuário logado.
- **Passos para Execução:**
  1. Acesse "Meus Agendamentos".
  2. Selecione o agendamento e clique em "Cancelar".
  3. Confirme o cancelamento.
  4. Verifique se o sistema remove o agendamento da lista.
- **Dados de Entrada:** Identificação do agendamento.
- **Resultados Esperados:** Mensagem de "Agendamento cancelado".
- **Pós-condições:** Agendamento removido do banco de dados.

---

## Critérios de Aceitação
1. Login deve redirecionar para a página principal apenas com credenciais válidas.
2. Agendamento deve permitir somente horários e datas disponíveis.
3. Cancelamentos devem ser aplicáveis apenas a agendamentos futuros.
4. Testes de carga e estresse devem demonstrar estabilidade com até 100 usuários simultâneos.
5. PostgreSQL deve manter a integridade dos dados durante operações de inserção, atualização e remoção.
