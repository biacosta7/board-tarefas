# 🗂️ Projeto: Gerenciador de Boards de Tarefas

Este projeto é uma aplicação para criação e gerenciamento de **boards de tarefas customizáveis**, com persistência dos dados em um banco MySQL. Cada board possui colunas e cards que representam o fluxo de trabalho e permitem controlar o progresso das tarefas de forma estruturada.

---

## 📌 Funcionalidades Principais

- Criar, selecionar e excluir boards.
- Adicionar colunas e cards a um board.
- Mover cards entre colunas seguindo regras específicas.
- Bloquear/desbloquear cards com justificativa.
- Cancelar tarefas.
- Relatórios de desempenho e histórico dos cards.

---

## 🚀 Tecnologias Utilizadas

- **Java**
- **MySQL**
- **Gradle**

---

## 📋 Requisitos do Projeto

### Menu Inicial

Ao iniciar, a aplicação deve exibir um menu com as seguintes opções:

1. Criar novo board  
2. Selecionar board  
3. Excluir boards  
4. Sair  

---

### Estrutura dos Boards

- Cada board deve:
  - Ter um nome único.
  - Ter **pelo menos 3 colunas**: uma inicial, uma para tarefas concluídas e uma para canceladas.
  - Permitir colunas adicionais do tipo **pendente**.
  
- Regras das colunas:
  - Devem ter: nome, ordem no board e tipo (`INICIAL`, `PENDENTE`, `FINAL`, `CANCELAMENTO`).
  - Apenas uma coluna de cada tipo (`INICIAL`, `FINAL`, `CANCELAMENTO`) por board.
  - Ordem obrigatória:
    - Inicial → Pendente(s) → Final → Cancelamento

- Cards:
  - Devem conter título, descrição, data de criação e status de bloqueio.
  - Devem seguir a ordem das colunas ao serem movidos.
  - Não podem ser movidos se estiverem bloqueados.
  - Devem ter justificativas para bloqueio e desbloqueio.

---

### Menu de Manipulação de Board Selecionado

O menu deve permitir:

- Criar card  
- Mover card para próxima coluna  
- Cancelar card  
- Bloquear/desbloquear card (com motivo)  
- Fechar board  

---

## 🌟 Funcionalidades Opcionais

1. **Registro de movimentações**: armazenar data/hora de entrada e saída dos cards em cada coluna.
2. **Relatório de tempo de execução**: tempo total e tempo por coluna até a finalização.
3. **Relatório de bloqueios**: incluir tempo bloqueado e justificativas.

---

## 🧪 Como Executar

> ⚠️ Requisitos: Java 17+, Gradle, MySQL

```bash
git clone https://github.com/seu-usuario/seu-projeto.git
cd seu-projeto
./gradlew build
./gradlew run
