## Template | 07_protocolo_<id_fonte>.md

`Modelo canônico para documentação do protocolo de coleta por fonte.`

---

| Status            | *[X] proposto* [ ] vigente [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 10/10/2026                              |
| **Versão**        | v0.1                                    |

---

```markdown
# Protocolo de Coleta – <id_recurso>

---

| Status            | *[X] proposto* [ ] vigente [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | `<institucional>`                       |
| **Atualizado em** | `<data>`                                |
| **Versão**        | `<versao>`                              |

---

## 1. Identificação do Recurso

| Campo                         | Conteúdo                                                    |
| ----------------------------- | ----------------------------------------------------------- |
| **id_recurso**                | `[OBRIGATÓRIO]`                                             |
| **Nome do recurso**           | `[OBRIGATÓRIO]`                                             |
| **Descrição**                 | `[OBRIGATÓRIO]` (2–4 linhas)                                |
| **Unidade de observação**     | `[OBRIGATÓRIO]` (município, estabelecimento, vínculo, etc.) |
| **Granularidade territorial** | `municipal` \| `estadual` \| `nacional` \| `outra`          |
| **Período de referência**     | `[OBRIGATÓRIO]`                                             |
| **Periodicidade**             | `anual` \| `mensal` \| `irregular`                          |
| **Prioridade atribuída**      | `alta` \| `media` \| `baixa`                                |
| **Pontuação na matriz**       | `[OBRIGATÓRIO]` (0–30)                                      |
| **Dimensão analítica**        | `[A DEFINIR]`                                               |

---

## 2. Método de Extração

| Campo                          | Conteúdo                                                             |
| ------------------------------ | -------------------------------------------------------------------- |
| **Método**                     | `download_direto` \| `api` \| `scraping` \| `solicitacao` \| `outro` |
| **Mecanismo de acesso**        | `[OBRIGATÓRIO]` (URL, endpoint, formulário)                          |
| **Autenticação**               | `nenhuma` \| `token` \| `credencial_institucional`                   |
| **Formato original**           | `CSV` \| `XLSX` \| `JSON` \| `XML` \| `PDF` \| `outro`               |
| **Codificação**                | `UTF-8` \| `Latin-1` \| `[A DEFINIR]`                                |
| **Delimitador**                | `,` \| `;` \| `\t` \| `[A DEFINIR]`                                  |
| **Volume estimado**            | `[A DEFINIR]` (nº de registros ou MB)                                |
| **Frequência de coleta**       | `única` \| `anual` \| `mensal`                                       |
| **Procedimento passo a passo** | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>`                         |

---

## 3. Preservação do Dado Bruto

| Campo                          | Conteúdo                                                                |
| ------------------------------ | ----------------------------------------------------------------------- |
| **Diretório de armazenamento** | `/bruto/<id_fonte>/<id_recurso>/<versao>/`                              |
| **Nome do arquivo original**   | `08-bruto-<fonte>-<versao>.<ext>`                                       |
| **Hash de verificação**        | `SHA-256: <hash>`                                                       |
| **Data de cálculo do hash**    | `<dd/mm/aaaa>`                                                          |
| **Responsável pela coleta**    | `[OBRIGATÓRIO]`                                                         |
| **Data de acesso**             | `[OBRIGATÓRIO]`                                                         |
| **Regra de imutabilidade**     | O arquivo bruto não deve ser sobrescrito. Nova coleta gera nova versão. |
| **Backup**                     | `[A DEFINIR]` (local, nuvem institucional)                              |

---

## 4. Metadados Obrigatórios

| Campo                         | Conteúdo                   |
| ----------------------------- | -------------------------- |
| **Título**                    | `[OBRIGATÓRIO]`            |
| **Fonte**                     | `<id_fonte>`               |
| **Versão**                    | `<versao>`                 |
| **Data de coleta**            | `<dd/mm/aaaa>`             |
| **Período de referência**     | `[OBRIGATÓRIO]`            |
| **Cobertura territorial**     | `[OBRIGATÓRIO]`            |
| **Unidade de medida**         | `[OBRIGATÓRIO]`            |
| **Identificador territorial** | `codigo_ibge_7` \| `outro` |
| **Licença**                   | `[A DEFINIR]`              |
| **Observações**               | `[opcional]`               |

---

## 5. Controle de Qualidade

| Verificação                    | Procedimento                             | Limiar                  | Resultado |
| ------------------------------ | ---------------------------------------- | ----------------------- | --------- |
| **Integridade**                | Comparação SHA-256                       | Correspondência exata   | `[ ]`     |
| **Estrutura**                  | Nº de colunas, tipos, codificação        | Ausência de truncamento | `[ ]`     |
| **Cobertura municipal**        | Contagem de municípios sergipanos        | `[A DEFINIR]`           | `[ ]`     |
| **Identificador territorial**  | Presença de código IBGE 7 dígitos        | 100%                    | `[ ]`     |
| **Duplicidades**               | Chave primária                           | Zero                    | `[ ]`     |
| **Valores ausentes**           | Percentual de nulos por variável crítica | ≤ `[A DEFINIR]`%        | `[ ]`     |
| **Consistência temporal**      | Período declarado vs. conteúdo           | Correspondência         | `[ ]`     |
| **Consistência com metadados** | Variáveis descritas vs. presentes        | ≥ 95%                   | `[ ]`     |

**Registro de inconformidades:**

```text
id_verificacao
descricao_inconformidade
providencia_adotada
responsavel
data 
```

---

## **Registro de Alterações**

| Versão   | Data   | Alteração   | Autor   |
| -------- | ------ | ----------- | ------- |
| <versão> | <data> | <alteração> | <autor> |

---
```

---

## **Registro de Alterações**

| Versão | Data       | Alteração                                               | Autor        |
| ------ | ---------- | ------------------------------------------------------- | ------------ |
| v0.1   | 10/10/2026 | Criação do *template* do protocolo de coleta por fonte. | Nayara Pavao |

---
