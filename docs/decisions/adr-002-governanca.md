### # ADR-002: Estrutura de Governança

---

| **Status**              | **`proposto`**             |
| ----------------------- | -------------------------- |
| **Responsável**         | Núcleo de Dados – OITS-UFS |
| **Data de atualização** | 23/09/2029                 |
| **Versão**              | v0.1                       |

---

#### Contexto

A metodologia OITS-UFS (ADR-001) exige rastreabilidade, transparência e reprodutibilidade. As decisões com impacto metodológico relevante devem ser registradas de forma padronizada, e os artefatos devem seguir convenções únicas de nomenclatura e versionamento. Sem uma estrutura de governança definida, os artefatos tendem a se tornar inconsistentes ao longo do tempo, dificultando a rastreabilidade, a integração entre as frentes do projeto e a reprodutibilidade metodológica.

A equipe é composta por uma única pessoa responsável pela coleta, tratamento e análise de dados. A estrutura de governança deve ser proporcional a esse contexto (princípio da proporcionalidade, seção 1.3 da metodologia), sem excesso de formalismo que inviabilize a operação.

---

#### Decisão

Adotar as seguintes decisões de governança:

###### Decisão 1: Estrutura de ADRs

Adotar ADRs em formato padronizado (modelo Nygard adaptado).

```markdown
### # ADR-NNN: [Título]
---
| **Status**      | **`<status>`**               |
| --------------- | ---------------------------- |
| **Data**        | dd/mm/yyyy                   |
| **Responsável** | <responsavel>                |
---
#### Contexto
    <Contexto>

#### Decisão  
    <Decisao>

###### Decisão X: [Subtítulo]
    <Decisao>

#### Consequências (opcional)
    <Consequência positiva>
    <Consequência negativa ou risco>
    <Impacto sobre etapas subsequentes>

#### Planos futuros (opcional)
    <Planos futuros>

---
<status> = {`proposto` | `aceito` | `rejeitado` | 
`atualizado` | `obsoleto` | `substituído por ADR-NNN`}
```

---

###### Decisão 2: Convenções de nomenclatura

Adotar as seguintes convenções em todo o repositório:

| Item                     | Convenção                                                                       |
| ------------------------ | ------------------------------------------------------------------------------- |
| **ADR**                  | `adr-NNN-titulo-com-hifens.md`                                                  |
|                          | `NNN`: número sequencial de três dígitos (000, 001, ...);                       |
|                          | `titulo-com-hifens`: título conciso em kebab-case;                              |
|                          | Exemplo: `adr-002-governanca.md`.                                               |
|                          | Exceção à convenção snake_case, alinhada à convenção internacional `adr-tools`. |
| **Protocolo**            | `NN_protocolo_<fonte>.md`                                                       |
|                          | `NN`: número da etapa (08 para protocolo da coleta);                            |
|                          | `<fonte>`: identificador da fonte (`IBGE_01`, `INPI_01`);                       |
|                          | Exemplo: `08_protocolo_IBGE_01.md`                                              |
| **Artefato de seleção**  | `NN_<tipo>_<fonte>_<versao>.<ext>`                                              |
|                          | `NN`: número da etapa (01 a 10);                                                |
|                          | `<tipo>`: descrição do artefato (`bruto`, `triado`, `classificado`);            |
|                          | `<fonte>`: identificador da fonte;                                              |
|                          | `<versao>`: versão semântica (`v0.1`, `v0.2`);                                  |
|                          | Exemplo: `03_triado_ibge_v0.1.xlsx`                                             |
| **Listas de marcadores** | `NN_listas_<fonte>_<versao>.csv`                                                |
|                          | Exemplo: `04_listas_ibge_v0.1.csv`                                              |
| **Dicionário de dados**  | `dicionario_dados.csv`                                                          |
|                          | Um arquivo único, atualizado a cada nova versão.                                |

---

###### Decisão 3: Versionamento

Adotar versionamento semântico (`v<maior>.<menor>`) para artefatos e dados. Alterações que afetem a comparabilidade entre versões geram nova versão do artefato e, quando relevante, novo ADR de revisão.

---

###### Decisão 4: Preservação do dado bruto

Adotar a preservação do dado bruto e dos metadados de forma independente dos dados posteriormente tratados. Nenhuma transformação sobrescreve o registro original (metodologia, seção 1.3).

---

###### Decisão 5: Localização dos artefatos de governança

| Local               | Conteúdo                                               |
| ------------------- | ------------------------------------------------------ |
| `docs/decisions/`   | ADRs                                                   |
| `docs/methodology/` | Metodologia e catálogo de fontes                       |
| `docs/selection/`   | Artefatos das etapas de seleção e protocolos por fonte |

---

## **Registro de Alterações**

| Versão | Data       | Alteração                        | Autor        |
| ------ | ---------- | -------------------------------- | ------------ |
| v0.1   | 23/09/2026 | Criação da ADR-002               | Nayara Pavao |
| v0.1   | 25/09/2026 | Adição de Registro de Alterações | Nayara Pavao |

---
