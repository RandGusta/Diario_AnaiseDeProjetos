# 📅 AULA - 22/04/2025

## UML(Unified Modeling Language)
 * Dois tipo:
     ➡ Estrutural: define as estruturas do sistema (Diagrama de Classes)
     ➡ Comportamental: Define os comportamentos ➡ ajudam o cliente entende e validar
* O investimento em documenação **depende** da empresa

🧩 Elementos do Diagrama 

| Elemento         | Símbolo     | Descrição                                                                 |
|------------------|-------------|---------------------------------------------------------------------------|
| **Ator**         | Boneco      | Entidade externa que interage com o sistema (usuário, sistema, dispositivo).      |
| **Caso de Uso**  | Elipse      | Funcionalidade ou serviço oferecido pelo sistema.                         |
| **Sistema**      | Retângulo   | Representa o escopo do sistema e contém os casos de uso.                 |
| **Associação**   | Linha reta  | Conecta um ator ao caso de uso com o qual interage.                      |
| **Include**      | Linha tracejada com `<<include>>` | Um caso de uso inclui sempre o comportamento de outro.     |
| **Extend**       | Linha tracejada com `<<extend>>`  | Um caso de uso pode opcionalmente estender outro.     |
| **Generalização**| Linha com seta aberta | Relaciona atores ou casos de uso com comportamentos similares. |
