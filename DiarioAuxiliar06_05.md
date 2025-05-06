# 📅 AULA - 06/05/2025

## ✨ ATIVIDADE EM GRUPO  
### 📌 Tema: SISTEMA DE CONTROLE DE EMPRÉSTIMO DE MATERIAIS  
- 🧠 Melhorar o diagrama de casos de uso com base no feedback do professor  
- 📝 Revisar e organizar os requisitos levantados na aula anterior  
- 💬 Discutir sobre **funcionalidades principais** e **relacionamentos entre os elementos**  

## 🔧 Melhorias com auxílio do professor  
- Adicionamos **relacionamento `include`** entre "Cadastrar Empréstimo" e "Solicitar um Empréstimo"  
- Reorganização de casos de uso relacionados a **objetos achados e perdidos**  
- Padronização dos nomes e agrupamento dos atores  
- Verificação de **ações exclusivas do administrador** e do **usuário comum**

## 📊 Diagrama de Casos de Uso (PlantUML)

\`\`\`plantuml
@startuml
left to right direction
skinparam actorPosition top
skinparam actorStyle awesome

actor Administrador as A
actor Usuario as U

rectangle "Sistema de Controle de Empréstimo de Materiais do Campus" {
  
  usecase "Cadastrar Empréstimo" as CE1
  usecase "Cadastrar entrada de Material" as CE2
  usecase "Cadastrar saida de Material" as CE3
  usecase "Cadastrar Usuário" as CE4
  usecase "Socilitar um Empréstimo" as CE5
  usecase "Cadastrar Administrador" as CE6
  usecase "Verificar Disponibilidade do Material" as CE7
  usecase "Cadastrar Objeto Achado" as CO1
  usecase "Cadastrar Saida do Objeto" as CO2

  A --> CE1
  A --> CE2
  A --> CE3
  A --> CE4
  A --> CO1
  A --> CO2

  U --> CE5

  CE1 .-> CE5 : <<include>>
}
@enduml
\`\`\`

## 📋 Levantamento de Requisitos (Aprimorado)

### 🔹 [LRP001] Realizar o controle de empréstimo de materiais  
#### 🔸 [LRE001] Permitir que o responsável realize o registro de entrada e saída de materiais de uso coletivo do campus  
- **[AR01-001] Cadastro de Administrador**  
  - Campos: \*E-mail, \*Senha, \*Nome  
- **[AR01-003] Cadastro de material**  
  - Campos: \*ID, Número patrimônio, \*Nome, \*Tipo, local, \*Data entrada  
- **[AR01-004] Quem fez o empréstimo (usuário)**  
  - Campos: \*Nome, \*E-mail  
- **[AR01-005] Cadastro de empréstimo**  
  - Campos: \*ID, \*Material, \*Data saída, \*Data devolução  
  - Relacionamento com:  
    - [AR01-004] (Usuário)  
    - [AR01-003] (Material)  

#### 🔸 [LRE002] Permitir que o responsável realize o controle de entrada e saída de materiais achados e perdidos do campus  
- [AR01-001], [AR01-003]  
- **[AR02-001] Cadastro de Objetos Achados**  
  - Campos: \*Nome, \*Local, \*Data  
- **[AR02-002] Registro de retirada de objeto**  
  - Campos: \*Objeto, \*Responsável pela retirada, \*Data retirada  

> **Nota:** Campos com `*` são obrigatórios.

## 🗣️ Discussões  
- A separação entre **materiais emprestáveis** e **objetos perdidos** deixou o sistema mais organizado  
- Houve dúvidas sobre como modelar **relacionamentos entre objetos e usuários**, resolvidas com auxílio do professor  
- Reforçamos a importância de **nomes claros** e **agrupamento funcional** dos casos de uso  

## 🎖️ Autoavaliação: **Dev**
