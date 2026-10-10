## Template | Catálogo de Fontes

`Modelo canônico para catalogação de fontes.`

---

| Status            | *[X] proposto* [ ] vigente [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 10/10/2026                              |
| **Versão**        | v0.1                                    |

---

```markdown
# Catálogo de Fontes – OITS-UFS

---

| Status            | *[X] proposto* [ ] vigente [ ] obsoleto   |
| ----------------- | ----------------------------------------- |
| **Responsável**   | `<institucional>`                         |
| **Atualizado em** | `<data>`                                  |
| **Versão**        | `versao`                                  |

---

## 1. Objetivo

<objetivo>

---

## 2. Convenções

- **id_fonte:** identificador único no formato `<sigla>_<nn>`
  (ex.: `IBGE_01`, `INPI_01`, `RAIS_01`).
- **Siglas:** expandidas na primeira ocorrência.
- **Status:** `identificada` | `em_avaliacao` | `inventariada` |
  `descartada`.
- **Acesso:** `aberto` | `restrito` | `sob_solicitacao` |
  `[A DEFINIR]`.

---

## 3. Quadro-Síntese

| id_fonte      | Instituição | Abrangência | Tipo de recurso | Status       | Data de identificação |
| ------------- | ----------- | ----------- | --------------- | ------------ | --------------------- |
| `IBGE_01`     | IBGE        | nacional    | agregados       | inventariada | `<dd/mm/aaaa>`        |
| `[A DEFINIR]` |             |             |                 |              |                       |

---

## 4. Fontes Identificadas

### 4.N <SIGLA> – <Nome da Instituição>

| Campo                                  | Conteúdo                                                                                                                                       |
| -------------------------------------- | -----------------------------------------------------------------------------------------------------------|
| **id_fonte**                           | [OBRIGATÓRIO]                                                                                              |
| **Instituição responsável**            | [OBRIGATÓRIO]                                                                                              |
| **Sigla**                              | [OBRIGATÓRIO]                                                                                              |
| **Etapa**                              | [OBRIGATÓRIO]                                                                                              |
| **Abrangência**                        | `nacional` \| `regional` \| `estadual` \| `municipal` \| `múltipla`                                        |
| **Endereço de acesso**                 | [OBRIGATÓRIO]                                                                                              |
| **Tipo de recurso**                    | `microdados` \| `agregados` \| `indicadores` \| `cadastros` \| `múltiplo` \| `outro`                       |
| **Descrição preliminar**               | [OBRIGATÓRIO]                                                                                              |
| **Periodicidade**                      |   `anual` \| `semestral` \| `trimestral` \| `mensal` \| `semanal` \| `diária `\| `decenal` \| `irregular` \| `única` \| `contínua` \| `múltipla`                                                                                                                   |
| **Período de referência disponível**   | [OBRIGATÓRIO]                                                                                              |
| **Formato de disponibilização**        | `CSV` \| `XLSX` \| `JSON` \| `API` \| `PDF` \| `outro` \| `múltiplo`                                       |
| **Licença de uso**                     | [OBRIGATÓRIO]                                                                                              |
| **Dimensões potencialmente atendidas** | `demografica` \| `economica` \| `trabalho_renda` \| `social`\| `institucional` \| `inovacao_ct` \| `geografica` \| `cultural_ambiental`                                                                                                                               |
| **Status**                             | `identificada` \| `em_avaliacao` \| `inventariada` \| `descartada`                                         |
| **Data de identificação**              | [OBRIGATÓRIO]                                                                                              |
| **Responsável pela identificação**     | [OBRIGATÓRIO]                                                                                              |
| **Observações**                        | [opcional]                                                                                                 |                                

---

## **Registro de Alterações**

| Versão   | Data   | Alteração   | Autor   |
| -------- | ------ | ----------- | ------- |
| <versão> | <data> | <alteração> | <autor> |

---
```

---

## **Registro de Alterações**

| Versão | Data       | Alteração                                    | Autor        |
| ------ | ---------- | -------------------------------------------- | ------------ |
| v0.1   | 10/10/2026 | Criação do *template* de catálogo de fontes. | Nayara Pavao |

---
