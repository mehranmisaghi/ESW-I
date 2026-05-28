---
title: 'Requisitos de Software'
description: 'Engenharia de Requisitos'
permalink: requisitos.md
---
# Material para estudar Requisitos de Software
- [Capítulo 4 - Sommerville](https://mehranmisaghi.github.io/ESW-I/materiais/Cap4-sommerville.pdf)
- [Capítulo 3 - Engenharia de Software Moderna](https://engsoftmoderna.info/cap3.html)
- [Slides de Requisitos de Software](https://canva.link/gv2gi8kyg3cdmyb)
---

# Requisitos de Software — Resumo dos slides

> **Disciplina:** Engenharia de Software  
> **Professores:** Raquel Nitsche dos Santos, Marcela Leite, Marco Antonio Torrez Rojas e Mehran Misaghi (IFC)  
> **Contato:** mehran.misaghi@ifc.edu.br

---

## 1. Definição do Problema

Antes de iniciar o levantamento de requisitos, é fundamental entender e definir claramente o problema que o sistema irá resolver.

Algumas perspectivas comuns para definir o problema:

- Reduzir o tempo de...
- Aumentar a produtividade...
- Atender mais clientes...
- Aumentar a segurança sobre...
- Diminuir o volume de...

---

## 2. O que é um Requisito?

Um requisito é:

- Um **serviço (funcionalidade)** que o sistema deve ser capaz de executar.
- Uma **restrição** sobre os serviços.
- Uma **característica, atributo, habilidade ou qualidade** que o sistema deve prover para ser útil a seus usuários.

> Os requisitos devem informar **"o que deve ser feito ou atendido"** para resolver o problema do usuário — e não como deve ser feito.

---

## 3. Tipos de Requisitos

### 3.1 Requisitos de Usuário

Declarações em linguagem natural de quais serviços o sistema deverá fornecer aos seus usuários e as restrições com as quais este deve operar. *(Sommerville, 2011)*

**Exemplo:**
> O portal da clínica deve gerar relatórios mensais que mostrem o custo dos medicamentos para cada clínica.

---

### 3.2 Requisitos de Sistema

Descrições mais detalhadas das funções, serviços e restrições operacionais do sistema. Compõem a **especificação funcional** e fazem parte do contrato de desenvolvimento. *(Sommerville, 2011)*

**Exemplos:**
1. No último dia de cada mês deve ser gerado um resumo de medicamentos prescritos, seus custos e as prescrições de cada clínica.
2. O sistema deve gerar automaticamente o relatório após às 17:00 do último dia do mês.
3. Um relatório será criado para cada clínica.
4. Devem ser criados relatórios separados por unidades.

---

## 4. Requisitos Funcionais (RF)

Descrevem o que o sistema deve **fazer**.

**Formato padrão:**
```
RF<NNN> - O sistema deve <descrição da funcionalidade>.
```

**Exemplo:**
> RF001 - O sistema deve permitir manter clientes.  
> *(manter = consultar, incluir, editar e excluir)*

---

## 5. Histórias de Usuário

Formato ágil para descrever requisitos do ponto de vista do usuário. As histórias equivalem aos Requisitos Funcionais, mas escritas de forma mais próxima ao usuário.

**Formato padrão:**
```
Como <papel/tipo de usuário>, eu gostaria de <ação desejada>.
```

### 5.1 Exemplo — Sistema de Biblioteca

**3 tipos de usuários:** Aluno, Professor e Funcionário da Biblioteca.

| Usuário | Exemplos de Histórias |
|---|---|
| Aluno | Realizar empréstimos, devolver livros, renovar empréstimos, pesquisar acervo, reservar livros |
| Professor | Empréstimos com prazo mais longo, sugerir/doar livros, devolver em outras bibliotecas |
| Funcionário | Cadastrar usuários/livros, aplicar multas, enviar e-mails de cobrança |

# Paramos no slide 21 (04/05)
### 5.2 Histórias Épicas

Histórias maiores e mais complexas que podem (e devem) ser **decompostas em histórias menores**.

**Exemplo — Sistema de Ensino a Distância (Moodle):**

- **Épica:** Como professor, eu gostaria de poder aplicar provas online.
- **Decomposição:**
  - Como professor, eu gostaria de criar um banco de questões.
  - Como professor, eu gostaria de criar e configurar uma prova online.
  - Como aluno, eu gostaria de fazer uma prova online.
  - Como professor, eu gostaria que uma prova fosse corrigida automaticamente.
  - Como aluno, eu gostaria de ver o resultado da correção de uma prova que fiz.
  - Como professor, eu gostaria de baixar um arquivo com as notas de uma prova.

### 5.3 Características de Boas Histórias (INVEST)

| Letra | Característica | Significado |
|---|---|---|
| I | Independentes | Não devem depender de outras histórias |
| N | Negociáveis | Abertas para negociação entre time e cliente |
| V | Valuable (Valor) | Devem agregar valor ao usuário/negócio |
| E | Estimáveis | Devem ser possíveis de estimar em esforço |
| S | Sucintas | Devem ser pequenas o suficiente para caber em uma sprint |
| T | Testáveis | Devem permitir a criação de testes de aceitação |

---

## 6. Requisitos Não Funcionais (RNF)

Descrevem **restrições ou qualidades** do sistema, como desempenho, segurança, compatibilidade, usabilidade, etc.

**Formato padrão:**
```
RNF<NNN> - O sistema deve <restrição ou qualidade>.
```

**Exemplo:**
> RNF007 - O sistema deve funcionar no browser Google Chrome, versão 136.

> ⚠️ **Atenção:** Evitar expressões como "versão X ou superior", pois não há controle sobre versões futuras.

### 6.1 Problema Comum com RNFs

RNFs costumam ser propostos como **metas gerais**, que estabelecem boas intenções mas deixam margem para interpretação e disputas na entrega. *(Sommerville, 2011)*

**Exemplo de meta (ruim):**
> O sistema deve ser de fácil uso pelo pessoal médico e deve ser organizado de tal maneira que os erros dos usuários sejam minimizados.

**Reescrito como RNF testável (bom):**
> A equipe médica deve ser capaz de usar todas as funções do sistema após quatro horas de treinamento. Após este treinamento, o número médio de erros cometido por usuários experientes não deve exceder dois por hora de uso do sistema.

### 6.2 Tipos de Requisitos Não Funcionais

Os RNFs podem ser categorizados em diversas dimensões, como:

- **Desempenho** — tempo de resposta, throughput, capacidade.
- **Segurança** — autenticação, autorização, criptografia.
- **Usabilidade** — facilidade de uso, acessibilidade.
- **Confiabilidade** — disponibilidade, tolerância a falhas.
- **Compatibilidade** — browsers, sistemas operacionais, integrações.
- **Manutenibilidade** — facilidade de manutenção e evolução.
- **Escalabilidade** — capacidade de crescimento.

### 6.3 RNFs no Definition of Done

RNFs podem integrar o critério de **pronto** (Definition of Done) das histórias.

**Exemplo — Desempenho como RNF importante:**
> Para uma história ser considerada pronta, ela deve:
> - Passar por uma revisão de código focada em desempenho.
> - Passar por testes de desempenho com carga real.

---

## 7. Testes / Critérios de Aceitação

Definem **quando uma história está completa e correta**. São essenciais para garantir que o requisito foi atendido conforme esperado.

**Exemplo — Fechar formulário para novas respostas (Google Forms):**

História:
> "Como criador de um formulário, eu gostaria de fechar o mesmo para recebimento de novas respostas."

Critérios de aceitação:
1. Criar um formulário e enviar respostas → respostas são registradas.
2. Fechar o formulário.
3. Tentar enviar nova resposta → sistema bloqueia e exibe mensagem adequada.
4. Reabrir o formulário → novas respostas voltam a ser aceitas.

---

## 8. Regras de Negócio (RN)

Regras que definem ou restringem algum aspecto do negócio. Podem ser:

- **Validações** — dados obrigatórios, formatos aceitos.
- **Restrições** — limites de acesso, permissões.
- **Cálculos** — fórmulas, taxas, descontos.
- **Leis/Regulamentos** — normas legais que o sistema deve seguir.
- **Regras específicas de caso de uso** — fluxos e condições de negócio.

**Formato padrão:**
```
RN.<NNN> - <descrição da regra>.
```

---

## 9. Qualidade dos Requisitos

### 9.1 Critérios de Completude

- O requisito está escrito no formato estabelecido?
- O requisito representa uma **necessidade** e não uma solução?
- O requisito é **único** no sistema (sem duplicatas por conteúdo)?
- O requisito **não contradiz** outro requisito?

### 9.2 Critérios de Ausência de Ambiguidade

- O requisito tem **uma única interpretação possível**?
- Não há informações conflitantes no documento?

**Palavras suspeitas que indicam ambiguidade:**

> alcançável, adequado, aproximadamente, completo, eficiente, minimizar, maximizar, flexível, modular, nominal, normalmente, otimizado, tipicamente, usualmente, geralmente, frequentemente, fácil, simples, muitos, vários, alguns, poucos, tanto quanto possível, pequeno, grande, baixo, alto, versátil, amigável, escalável, e/ou.

### 9.3 Critérios de Testabilidade

- É possível **verificar objetivamente** se o requisito foi atendido?
- O requisito possui **métricas ou critérios mensuráveis**?

### 9.4 Critérios de Viabilidade

- É tecnicamente e economicamente possível **implementar** o requisito?

---

## 10. Lembrete sobre Cronograma restante da Disciplina

| Datas | Conteúdo |
|---|---|
| 28/04 | Kanban |
| 30/04 | Palestra|
| 05/05 | Ver Trello|
| 05/05 a 26/05 | Engenharia de Requisitos |
| 28/05 | Detalhamento dos temas e Seminários |
| 02/06 | Prova II |
| 28/05 a 11/06 | Preparação de Seminários |
| 18/06 a 30/06 | Apresentação de Seminários |
| 23/06 | Visita TOTVS |

---

## Bora exercitar em alguns cenários! (14/05)
> Nos cenários a seguir elobarem RF, RNF e RN.

1. Sistema de E-commerce com Marketplace (cliente, vendedor, administrador)
  - Henrique, Tomas e Paulo
2. Sistema de Carros Autônomos (carro, cliente e um sistema centralizado)
 - Carlos, Felipe e Brunno
3. Sistema de Detecção de Fraudes Financeiras (cliente, banco, sistema)
 - Hugo, Vitor, Thiago e Arthur Israel
4. Sistema de Cidade Inteligente (para integrar trânsito, iluminação pública, segurança e transporte) (cidadão, prefeitura, operadoras e sensores IoT)
 - Leonardo, Haniero e Arthur Mendonça
5. Sistema de Monitoramento Inteligente de Plantação (umidade do solo, temperatura e nutrientes) (produtor, sistema IoT, técnico)
 - Luís e Jose
6. Sistema de Supermercado para Condomínios
 - Heloisa, Mirella, Guilherme, Kelvin e Maurício
---
 ### Observações sobre o trabalho:

 1. As apresentações ocorrerão nos dias 19 e 21 de maio. Mas **todos os grupos deverão deixar prontas as suas apresentações para o dia 19 de maio**.
 2. O tempo de apresentação poderá ser até 30 minutos
 3. Os grupos poderão aprsentar o documento compartilhando e explicando o que cada membro fez ou fazer no quadro ou outras modalidades.
 4. Os grupos poderão desenvolver partes da aplicação para apresentar.
 5. Caso o grupo tenha usado alguma ferramenta de **IA**, a mesma tem que ser especificada e fornecida *prompt utilizada*.
---
## Próxima aula
- [Um pouco de DevOps](devops.md)