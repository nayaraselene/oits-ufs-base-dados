# Catálogo de Fontes de Dados – OITS-UFS

---

| Status            | *[X] proposto* [ ] vigente [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 25/09/2026                              |
| **Versão**        | v0.1.1                                  |

---

## 1. Objetivo

Este documento é parte do Catálogo de Fontes de Dados do projeto Observatório de Inovação Territorial (OITS-UFS) e Hubs de Inovação da UFS (InovaHUB-UFS): Poder Local e Políticas de Inovação Potencializando as Vocações Territoriais para o Desenvolvimento Regional, desenvolvido na Universidade Federal de Sergipe com apoio do Conselho Nacional de Desenvolvimento Científico e Tecnológico (CNPq).  

O catálogo tem como objetivo registrar as fontes potencialmente relevantes para a caracterização dos municípios sergipanos e para as análises de vocações e dinâmicas territoriais no âmbito do projeto OITS-UFS.

---

## 2. Convenções

- **id_fonte:** identificador único no formato `<sigla>_<nn>` (ex.: `ibge_01`, `inpi_01`).
- **Siglas:** expandidas na primeira ocorrência.
- **Status:** `identificada` | `em_avaliacao` | `inventariada` | `descartada`
- **Abrangência:** `nacional` \| `regional` \| `estadual` \| `municipal` | `múltipla`
- **Tipo de recurso:** `microdados` \| `agregados` \| `indicadores` \| `cadastros` \| `múltiplo` | `outro`
- **Periodicidade:** `anual` | `semestral` | `trimestral` | `mensal` | `semanal` | `diária` | `decenal` | `irregular` | `única` | `contínua` | `múltipla`
- **Formato de disponibilização:** `CSV` \| `XLSX` \| `JSON` \| `API` \| `PDF` \| `outro` | `múltiplo`

---

## 3. Quadro-Síntese

| id_fonte | Instituição | Abrangência | Tipo de recurso | Status       | Data de identificação |
| -------- | ----------- | ----------- | --------------- | ------------ | --------------------- |
| ibge_01  | IBGE        | múltipla    | múltiplo        | inventariada | 15/09/2026            |
| inpi_01  | INPI        |             |                 | identificado | 18/09/2029            |

---

## 4. Fontes Identificadas

### 4.1 IBGE – Instituto Brasileiro de Geografia e Estatística

| Campo                                  | Conteúdo                                                                                                                                   |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **id_fonte**                           | ibge_01                                                                                                                                    |
| **Instituição responsável**            | Instituto Brasileiro de Geografia e Estatística                                                                                            |
| **Sigla**                              | IBGE                                                                                                                                       |
| **Etapa**                              | 3 - Triagem                                                                                                                                |
| **Abrangência**                        | `múltipla`                                                                                                                                 |
| **Endereço de acesso**                 | [ftp.ibge.gov.br](https://ftp.ibge.gov.br/)                                                                                                |
| **Tipo de recurso**                    | `múltiplo`                                                                                                                                 |
| **Descrição preliminar**               | Instituto público responsável pela produção, análise, pesquisa e disseminação de dados e informações geográficas e estatísticas do Brasil. |
| **Periodicidade:**                     | `múltipla`                                                                                                                                 |
| **Período de referência disponível**   | 1905–2026                                                                                                                                  |
| **Formato de disponibilização**        | `múltiplo`                                                                                                                                 |
| **Licença de uso**                     | Dados Abertos                                                                                                                              |
| **Dimensões potencialmente atendidas** | `demografica` \| `economica` \| `trabalho_renda` \| `social`\| `institucional` \| `inovacao_ct` \| `geografica` \| `cultural_ambiental`    |
| **Status**                             | `inventariada`                                                                                                                             |
| **Data de identificação**              | 15/09/2026                                                                                                                                 |
| **Responsável pela identificação**     | Nayara Pavao                                                                                                                               |
| **Observações**                        | [opcional]                                                                                                                                 |

### 4.2 **INPI** - Instituto Nacional da Propriedade Industrial

| Campo                                               | Conteúdo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| --------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **id_fonte**                                        | inpi_01                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Instituição responsável**                         | Instituto Nacional da Propriedade Industrial                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Sigla**                                           | INPI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Etapa**                                           | 2 - Inventário Bruto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <mark>**Abrangência**</mark>                        | `nacional` \| `regional` \| `estadual` \| `municipal` \| `múltipla`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Endereço de acesso**                              | [dados.gov.br/inpi](https://dados.gov.br/dados/organizacoes/visualizar/instituto-nacional-da-propriedade-industrial)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <mark>**Tipo de recurso**</mark>                    | `microdados` \| `agregados` \| `indicadores` \| `cadastros` \| `múltiplo` \| `outro`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <mark>**Descrição preliminar**</mark>               | `[Criado em 1970, o Instituto Nacional da Propriedade Industrial (INPI) é uma autarquia federal vinculada ao Ministério do Desenvolvimento, Indústria, Comércio e Serviços (MDIC), responsável pelo aperfeiçoamento, disseminação e gestão do sistema brasileiro de concessão e garantia de direitos de propriedade intelectual. Entre os serviços do INPI, estão o registro de marcas, desenhos industriais, indicações geográficas, programas de computador e topografias de circuitos integrados, além da concessão de patentes e da averbação de contratos de franquia e transferência de tecnologia. Na economia do conhecimento, estes direitos se transformam em diferenciais competitivos, estimulando o surgimento constante de novas identidades e soluções técnicas.]` |
| <mark>**Periodicidade**</mark>                      | `anual` \| `semestral` \| `trimestral` \| `mensal` \| `semanal` \| `diária `\| `decenal` \| `irregular` \| `única` \| `contínua` \| `múltipla`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <mark>**Período de referência disponível**</mark>   | [OBRIGATÓRIO]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <mark>**Formato de disponibilização**</mark>        | `CSV` \| `XLSX` \| `JSON` \| `API` \| `PDF` \| `outro` \| `múltiplo`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Licença de uso**                                  | Dados Abertos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <mark>**Dimensões potencialmente atendidas**</mark> | `demografica` \| `economica` \| `trabalho_renda` \| `social`\| `institucional` \| `inovacao_ct` \| `geografica` \| `cultural_ambiental`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Status**                                          | `identificada`                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Data de identificação**                           | 18/09/2026                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Responsável pela identificação**                  | Nayara Pavao                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Observações**                                     | [opcional]                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |

---

### 4.N <SIGLA> – <Nome da Instituição>

| Campo                                  | Conteúdo                                                                                                                                       |
| -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **id_fonte**                           | [OBRIGATÓRIO]                                                                                                                                  |
| **Instituição responsável**            | [OBRIGATÓRIO]                                                                                                                                  |
| **Sigla**                              | [OBRIGATÓRIO]                                                                                                                                  |
| **Etapa**                              | [OBRIGATÓRIO]                                                                                                                                  |
| **Abrangência**                        | `nacional` \| `regional` \| `estadual` \| `municipal` \| `múltipla`                                                                            |
| **Endereço de acesso**                 | [OBRIGATÓRIO]                                                                                                                                  |
| **Tipo de recurso**                    | `microdados` \| `agregados` \| `indicadores` \| `cadastros` \| `múltiplo` \| `outro`                                                           |
| **Descrição preliminar**               | [OBRIGATÓRIO]                                                                                                                                  |
| **Periodicidade**                      | `anual` \| `semestral` \| `trimestral` \| `mensal` \| `semanal` \| `diária `\| `decenal` \| `irregular` \| `única` \| `contínua` \| `múltipla` |
| **Período de referência disponível**   | [OBRIGATÓRIO]                                                                                                                                  |
| **Formato de disponibilização**        | `CSV` \| `XLSX` \| `JSON` \| `API` \| `PDF` \| `outro` \| `múltiplo`                                                                           |
| **Licença de uso**                     | [OBRIGATÓRIO]                                                                                                                                  |
| **Dimensões potencialmente atendidas** | `demografica` \| `economica` \| `trabalho_renda` \| `social`\| `institucional` \| `inovacao_ct` \| `geografica` \| `cultural_ambiental`        |
| **Status**                             | `identificada` \| `em_avaliacao` \| `inventariada` \| `descartada`                                                                             |
| **Data de identificação**              | [OBRIGATÓRIO]                                                                                                                                  |
| **Responsável pela identificação**     | [OBRIGATÓRIO]                                                                                                                                  |
| **Observações**                        | [opcional]                                                                                                                                     |

---

*(Repetir a subseção 4.N para cada fonte identificada.)*

```markdown
### 4.N <SIGLA> – <Nome da Instituição>

| Campo | Conteúdo |
| --- | --- |
| **id_fonte** | [OBRIGATÓRIO] |
| **Instituição responsável** | [OBRIGATÓRIO] |
| **Sigla** | [OBRIGATÓRIO] |
| **Etapa** | [OBRIGATÓRIO] |
| **Abrangência** | `nacional` \| `regional` \| `estadual` \| `municipal` \| `múltipla` |
| **Endereço de acesso** | [OBRIGATÓRIO] |
| **Tipo de recurso** | `microdados` \| `agregados` \| `indicadores` \| `cadastros` \| `múltiplo` \| `outro` |
| **Descrição preliminar** | [OBRIGATÓRIO] |
| **Periodicidade** | `anual` \| `semestral` \| `trimestral` \| `mensal` \| `semanal` \| `diária `\| `decenal` \| `irregular` \| `única` \| `contínua` \| `múltipla` |
| **Período de referência disponível** | [OBRIGATÓRIO] |
| **Formato de disponibilização** | `CSV` \| `XLSX` \| `JSON` \| `API` \| `PDF` \| `outro` \| `múltiplo` |
| **Licença de uso** | [OBRIGATÓRIO] |
| **Dimensões potencialmente atendidas** | `demografica` \| `economica` \| `trabalho_renda` \| `social`\| `institucional` \| `inovacao_ct` \| `geografica` \| `cultural_ambiental` |
| **Status** | `identificada` \| `em_avaliacao` \| `inventariada` \| `descartada` |
| **Data de identificação** | [OBRIGATÓRIO] |
| **Responsável pela identificação** | [OBRIGATÓRIO] |
| **Observações** | [opcional] |
---
```

---

## 5. Registro de Alterações

| Versão | Data       | Alteração                | Responsável  |
| ------ | ---------- | ------------------------ | ------------ |
| v0.1   | 15/09/2026 | Criação do catálogo      | Nayara Pavao |
| v0.1.1 | 25/09/2026 | Atualização de estrutura | Nayara Pavao |

---
