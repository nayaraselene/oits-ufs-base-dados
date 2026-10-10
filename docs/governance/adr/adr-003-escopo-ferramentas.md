### # ADR-003: Escopo de Ferramentas

---

| Status            | [ ] proposto *[X] vigente* [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 25/09/2026                              |
| **Versão**        | v0.1                                    |

---

#### Contexto

Falta definir quais ferramentas sustentam cada etapa do fluxo de seleção e coleta e os critérios para sua escolha. Essa ausência gera dispersão de ferramentas, perda de reprodutibilidade (seção 1.3) e dependência de formatos proprietários incompatíveis com o versionamento em Git (ADR-000). O Núcleo de Dados (ADR-002) exige ferramentas de baixo custo de manutenção, amplamente documentadas e, preferencialmente, de código aberto, em linha com o princípio da proporcionalidade, considerando a equipe unipessoal.

---

#### Decisão

###### Ferramentas do fluxo metodológico

| Ferramenta            | Função                                                                             | Etapas de uso      |
| --------------------- | ---------------------------------------------------------------------------------- | ------------------ |
| Pesquisa manual       | Identificação de fontes e recursos potencialmente relevantes                       | 1                  |
| Git / GitHub          | Versionamento de dados, scripts e documentação (ADR-000)                           | Transversal (1–10) |
| MarkText v0.19.1      | Documentação de catálogo de fontes, protocolos de coleta e registros de validação  | 1, 6, 7            |
| Microsoft Excel v16.0 | Triagem, aplicação da matriz de classificação ponderada e priorização dos recursos | 2, 3, 4, 5         |
| FileZilla v3.71.1     | Acesso a servidor online, transferência em fila, gerenciamento de arquivos         | 2                  |
| Bulk Rename Utility   | Renomeação de arquivos em massa                                                    | –                  |

---

## **Registro de Alterações**

| Versão | Data       | Alteração                    | Autor        |
| ------ | ---------- | ---------------------------- | ------------ |
| v0.1   | 25/09/2026 | Criação e redação da ADR-003 | Nayara Pavao |
|        |            |                              |              |

---
