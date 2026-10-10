### # ADR-002: Estrutura de Governança

---

| Status            | [ ] proposto *[X] vigente* [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 03/10/2026                              |
| **Versão**        | v0.2                                    |

---

#### Contexto

A metodologia OITS-UFS (ADR-001) exige rastreabilidade, transparência e reprodutibilidade. As decisões com impacto metodológico relevante devem ser registradas de forma padronizada, e os artefatos devem seguir convenções únicas de nomenclatura e versionamento. Sem uma estrutura de governança definida, os artefatos tendem a se tornar inconsistentes ao longo do tempo, dificultando a rastreabilidade, a integração entre as frentes do projeto e a reprodutibilidade metodológica.

A equipe é composta por uma única pessoa responsável pela coleta, tratamento e análise de dados. A estrutura de governança deve ser proporcional a esse contexto (princípio da proporcionalidade, seção 1.3 da metodologia), sem excesso de formalismo que inviabilize a operação.

**v0.2:** A descrição de recursos operacionais em ADRs dificulta o acesso, a leitura e a revisão de recursos. Reproduções divergentes em múltiplos arquivos de documentação fragilizam a confiança no conteúdo e aumentam o custo de manutenção do repositório.

---

#### Decisão

Adotar as seguintes decisões de governança:

###### Decisão 1: Localização dos artefatos de governança

Armazenar os artefatos de governança nos caminhos definidos no mapa de artefatos. Este, bem como os demais artefatos de governança, são versionados independentemente desta ADR. Em caso de divergência com qualquer reprodução local, prevalece o documento canônico.

Artefato: `docs/governance/conventions/mapa-artefatos.md`

---

###### Decisão 2: Estrutura de ADRs

Adotar ADRs em formato padronizado (modelo Nygard adaptado).

Os campos obrigatórios são: `Status`, `Data`, `Responsável`, `Contexto`, `Decisão`. Os campos `Consequências` e `Planos futuros` são opcionais.

Artefato: `adr-template.md`

---

###### Decisão 3: Convenções de nomenclatura

Adotar um critério uniforme de nomenclatura em todo o repositório.

Artefato: `nomenclatura.md`

---

###### Decisão 4: Versionamento

Adotar versionamento semântico (`v<maior>.<menor>`) para artefatos e dados. Alterações que afetem a comparabilidade entre versões geram nova versão do artefato e, quando relevante, novo ADR de revisão.

---

###### Decisão 5: Preservação do dado bruto

Adotar a preservação do dado bruto e dos metadados de forma independente dos dados posteriormente tratados. Nenhuma transformação sobrescreve o registro original (metodologia, seção 1.3).

---

###### Decisão 6: Documentação de recursos operacionais

Manter os recursos operacionais em artefatos próprios, sob fonte única e versionamento independente. O ADR institui o uso e referencia o caminho e a versão do recurso, sem reproduzi-lo. A implementação dessa decisão requer a extração desses itens previamente armazenados em ADRs a fim de eliminar cópias paralelas, garantir um único modelo canônico por tipo de documentação e desacoplar a revisão do recurso da revisão da decisão.

---

## **Registro de Alterações**

| Versão | Data       | Alteração                        | Autor        |
| ------ | ---------- | -------------------------------- | ------------ |
| v0.1   | 23/09/2026 | Criação da ADR-002               | Nayara Pavao |
| v0.1.1 | 25/09/2026 | Adição de Registro de Alterações | Nayara Pavao |
| v0.2   | 03/10/2026 | Adição e adequação à Decisão 6   | Nayara Pavao |

---
