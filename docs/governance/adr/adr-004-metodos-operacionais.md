# ADR-004: Documentação dos Métodos Operacionais

---

| Status            | [ ] proposto *[X] vigente* [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 27/09/2026                              |
| **Versão**        | v0.1.1                                  |

---

## Contexto

O projeto executa um fluxo metodológico para a seleção e coleta de dados. Etapas executadas de forma recorrente devem ser mapeadas e documentadas para garantir reprodutibilidade, consistência entre execuções e verificabilidade por terceiros. Sem documentação dedicada, o detalhamento operacional pode se dispersar entre registros de decisão, protocolos por fonte e anotações informais.

---

## Decisão

###### Decisão 1: Adoção de artefatos dedicados para métodos operacionais

Documentar cada método em artefato dedicado de forma generalizada para permitir sua reutilização entre fontes compatíveis. O artefato descreve a lógica transversal (passo a passo, regras de decisão e estrutura de registro), enquanto as especificidades de cada execução permanecem no protocolo por fonte. Essa separação evita duplicação de procedimentos, preserva a consistência e reduz o esforço de manutenção.

---

###### Decisão 2: Armazenamento, convenção e *template*

| **Nomenclatura** | `NN-metodo-<nome>.md`         |
| ---------------- | ----------------------------- |
| **Localização**  | `docs/methodology/`           |
| **Exemplo**      | `01-metodo-triagem.md`        |
| **Template**     | `metodo-operacional-template` |

---

## **Registro de Alterações**

| Versão | Data       | Alteração                                       | Autor        |
| ------ | ---------- | ----------------------------------------------- | ------------ |
| v0.1   | 27/09/2026 | Criação e redação da ADR-004.                   | Nayara Pavao |
| v0.1.1 | 10/10/2026 | Adequação à Decisão 6 da ADR-002 de Governança. | Nayara Pavao |

---
