# Protocolo de Seleção e Coleta – IBGE_01

---

| **Status**              | **`proposto`**             |
| ----------------------- | -------------------------- |
| **Responsável**         | Núcleo de Dados – OITS-UFS |
| **Data de atualização** | 23/09/2029                 |
| **Versão**              | v0.1                       |

---

**Status do protocolo:** `planejado` | `em_execucao` | `concluido` | `revisado`

---

## 1. Identificação da Fonte

| Campo                                  | Conteúdo                                                                                                   |
| -------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **id_fonte**                           | IBGE_01                                                                                                    |
| **Instituição responsável**            | Instituto Brasileiro de Geografia e Estatística                                                            |
| **Sigla**                              | IBGE                                                                                                       |
| **Abrangência**                        | `nacional`                                                                                                 |
| **Endereço de acesso**                 | [ftp.ibge.gov.br](https://ftp.ibge.gov.br/)                                                                |
| **Tipo de recurso predominante**       |                                                                                                            |
| **Licença de uso**                     | Dados Abertos                                                                                              |
| **Acesso**                             | `aberto`                                                                                                   |
| **Dimensões potencialmente atendidas** | Demográfica; Econômica; Trabalho e Renda; Social; Institucional; Inovação; Geográfica; Cultural; Ambiental |
| **Data de identificação**              | 01/09/2026                                                                                                 |
| **Responsável pela identificação**     | `Nayara Pavao`                                                                                             |

**Referência:** `01_fontes_catalogo.md`, entrada `IBGE_01`.

---

## 2. Registro de Execução por Etapa

Esta seção registra, para cada etapa do fluxo metodológico (seção 2.1 da metodologia), o passo a passo efetivamente executado, os artefatos produzidos e as decisões tomadas.

### Etapa 1 – Identificação

| Campo                  | Conteúdo                |
| ---------------------- | ----------------------- |
| **Data de execução**   | 13/09/2026              |
| **Responsável**        | `Nayara Pavao`          |
| **Artefato produzido** | `01_fontes_catalogo.md` |
| **Decisões tomadas**   | `[opcional]`            |
| **Observações**        | `[opcional]`            |

---

### Etapa 2 – Inventário Bruto

| Campo                            | Conteúdo                                                                                                                                                                                                                         |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Data de execução**             | 18/09/2026                                                                                                                                                                                                                       |
| **Responsável**                  | `Nayara Pavao`                                                                                                                                                                                                                   |
| **Método**                       | `ftp_filezilla_listagem`                                                                                                                                                                                                         |
| **Ferramenta utilizada**         | ``Filezilla v3.71.1``, `Microsoft Excel v16.0`                                                                                                                                                                                   |
| **Passo a passo**                | **Filezilla**<br>1. Conectar ao servidor FTP do IBGE<br>2. Selecionar todos os diretórios<br>3. Adicionar arquivos à fila <br>4. Exportar fila em XML<br>**Excel**<br>5. Obter dados de arquivo XML<br>6. Salvar listagem em CSV |
| **Artefato produzido**           | `02_bruto_ibge.csv`                                                                                                                                                                                                              |
| **Nº de recursos inventariados** | 130.571                                                                                                                                                                                                                          |

---

### Etapa 3 – Triagem

| Campo                          | Conteúdo                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Data de execução**           | 19/09/2026                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Responsável**                | `Nayara Pavao`                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Método**                     | <mark>`definir tag para métodos de triagem` </mark>                                                                                                                                                                                                                                                                                                                                                                                   |
| **Ferramenta utilizada**       | `Excel`                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Flags aplicadas**            | `flag_territorial`, `flag_granularidade`, `flag_temporal`                                                                                                                                                                                                                                                                                                                                                                             |
| **Passo a passo**              | **Excel**<br>1. Obter dados do arquivo 02_bruto_ibge.csv<br>2. Transformar dados<br>**Power Query**<br>3. Derivar caminho normalizado<br>4. Extrair ano de referência<br>5. Adicionar flag_temporal<br>6. Inserir dados de marcadores territoriais<br>7. Adicionar flag_territorial<br>8. Inserir dados de marcadores de granularidade<br>9. Adicionar flag_granularidade<br>10. Adicionar flag_vetor<br>11. Adicionar flag_final<br> |
| **Artefato produzido**         | `03_triado_ibge_<versao>.xlsx`                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Nº de recursos elegíveis**   | 228                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Nº de recursos inelegíveis** | 120.725                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Nº de recursos em revisão**  | 9.618                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Listas documentadas**        | `marcador_territorial`, `marcador_granularidade`                                                                                                                                                                                                                                                                                                                                                                                      |
| **ADR relacionado**            | `adr-<xxx>-<id>`                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Observações**                | `[opcional]`                                                                                                                                                                                                                                                                                                                                                                                                                          |

---

### Etapa 4 – Classificação

| Campo                          | Conteúdo                                                                                   |
| ------------------------------ | ------------------------------------------------------------------------------------------ |
| **Data de execução**           | `<dd/mm/aaaa>`                                                                             |
| **Responsável**                | `[OBRIGATÓRIO]`                                                                            |
| **Método**                     | `matriz_ponderada` (seção 7 da metodologia)                                                |
| **Pesos aplicados**            | Cobertura municipal: 3; Relevância temática: 3; Atualidade: 2; Facilidade de integração: 2 |
| **Passo a passo**              | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>`                                               |
| **Artefato produzido**         | `04_classificado_<fonte>_<versao>.xlsx`                                                    |
| **Pontuação máxima observada** | `[OBRIGATÓRIO]`                                                                            |
| **Pontuação mínima observada** | `[OBRIGATÓRIO]`                                                                            |
| **Decisões tomadas**           | `[opcional]`                                                                               |
| **ADR relacionado**            | `adr-<xxx>-<id>`                                                                           |
| **Observações**                | `[opcional]`                                                                               |

---

### Etapa 5 – Priorização

| Campo                               | Conteúdo                                     |
| ----------------------------------- | -------------------------------------------- |
| **Data de execução**                | `<dd/mm/aaaa>`                               |
| **Responsável**                     | `[OBRIGATÓRIO]`                              |
| **Regra de conversão**              | Alta: 20–30; Média: 10–19; Baixa: 0–9        |
| **Passo a passo**                   | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>` |
| **Artefato produzido**              | `05_priorizado_<fonte>_<versao>.xlsx`        |
| **Nº de recursos alta prioridade**  | `[OBRIGATÓRIO]`                              |
| **Nº de recursos média prioridade** | `[OBRIGATÓRIO]`                              |
| **Nº de recursos baixa prioridade** | `[OBRIGATÓRIO]`                              |
| **Decisões tomadas**                | `[opcional]`                                 |
| **Observações**                     | `[opcional]`                                 |

---

### Etapa 6 – Validação

| Campo                              | Conteúdo                                     |
| ---------------------------------- | -------------------------------------------- |
| **Data de execução**               | `<dd/mm/aaaa>`                               |
| **Responsável**                    | `[OBRIGATÓRIO]`                              |
| **Casos limítrofes identificados** | `[OBRIGATÓRIO]` (pontuações 9, 10, 19, 20)   |
| **Passo a passo**                  | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>` |
| **Artefato produzido**             | `06_validado_<fonte>_<versao>.xlsx`          |
| **Decisões confirmadas**           | `[OBRIGATÓRIO]`                              |
| **Decisões modificadas**           | `[OBRIGATÓRIO]`                              |
| **ADRs gerados**                   | `adr-<xxx>-<id>`                             |
| **Observações**                    | `[opcional]`                                 |

---

### Etapa 7 – Planejamento da Coleta

| Campo                                 | Conteúdo                                     |
| ------------------------------------- | -------------------------------------------- |
| **Data de execução**                  | `<dd/mm/aaaa>`                               |
| **Responsável**                       | `[OBRIGATÓRIO]`                              |
| **Recursos com protocolo definido**   | `[OBRIGATÓRIO]`                              |
| **Passo a passo**                     | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>` |
| **Artefato produzido**                | `07_protocolo_<fonte>.md` (este documento)   |
| **Métodos de extração definidos**     | `download_direto` \\                         |
| **Estrutura de repositório definida** | `/bruto/<id_fonte>/<id_recurso>/<versao>/`   |
| **Decisões tomadas**                  | `[opcional]`                                 |
| **ADR relacionado**                   | `adr-<xxx>-<id>`                             |
| **Observações**                       | `[opcional]`                                 |

---

### Etapa 8 – Coleta

| Campo                       | Conteúdo                                                    |
| --------------------------- | ----------------------------------------------------------- |
| **Data de execução**        | `<dd/mm/aaaa>`                                              |
| **Responsável**             | `[OBRIGATÓRIO]`                                             |
| **Recursos coletados**      | `[OBRIGATÓRIO]`                                             |
| **Método executado**        | `download_direto` \\                                        |
| **Passo a passo**           | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>`                |
| **Artefatos produzidos**    | `08_bruto_<fonte>_<versao>.<ext>`<br>`metadados_coleta.csv` |
| **Hash de verificação**     | `SHA-256: <hash>`                                           |
| **Data de cálculo do hash** | `<dd/mm/aaaa>`                                              |
| **Volume coletado**         | `[OBRIGATÓRIO]` (nº de registros ou MB)                     |
| **Decisões tomadas**        | `[opcional]`                                                |
| **Observações**             | `[opcional]`                                                |

---

### Etapa 9 – Controle de Qualidade

| Campo                             | Conteúdo                                                                                                                                                  |
| --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Data de execução**              | `<dd/mm/aaaa>`                                                                                                                                            |
| **Responsável**                   | `[OBRIGATÓRIO]`                                                                                                                                           |
| **Verificações aplicadas**        | Integridade; Estrutura; Cobertura municipal; Identificador territorial; Duplicidades; Valores ausentes; Consistência temporal; Consistência com metadados |
| **Limiares aplicados**            | `[A DEFINIR]`                                                                                                                                             |
| **Passo a passo**                 | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>`                                                                                                              |
| **Artefato produzido**            | `09_qualidade_<fonte>_<versao>.csv`                                                                                                                       |
| **Inconformidades identificadas** | `[OBRIGATÓRIO]`                                                                                                                                           |
| **Providências adotadas**         | `[OBRIGATÓRIO]`                                                                                                                                           |
| **Decisões tomadas**              | `[opcional]`                                                                                                                                              |
| **ADR relacionado**               | `adr-<xxx>-<id>`                                                                                                                                          |
| **Observações**                   | `[opcional]`                                                                                                                                              |

---

### Etapa 10 – Incorporação

| Campo                      | Conteúdo                                      |
| -------------------------- | --------------------------------------------- |
| **Data de execução**       | `<dd/mm/aaaa>`                                |
| **Responsável**            | `[OBRIGATÓRIO]`                               |
| **Recursos incorporados**  | `[OBRIGATÓRIO]`                               |
| **Passo a passo**          | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>`  |
| **Artefato produzido**     | `10_incorporado_<fonte>_<versao>.<ext>`       |
| **Camada de destino**      | `intermediaria` \\                            |
| **Relação com dado bruto** | `[OBRIGATÓRIO]` (referência ao hash e versão) |
| **Decisões tomadas**       | `[opcional]`                                  |
| **Observações**            | `[opcional]`                                  |

---

## 3. Quadro-Síntese da Execução

| Etapa                    | Data           | Responsável | Artefato                                | Status        |
| ------------------------ | -------------- | ----------- | --------------------------------------- | ------------- |
| 1. Identificação         | `<dd/mm/aaaa>` | `<nome>`    | `01_fontes_catalogo.md`                 | `concluida`   |
| 2. Inventário Bruto      | `<dd/mm/aaaa>` | `<nome>`    | `02_bruto_<fonte>.csv`                  | `concluida`   |
| 3. Triagem               | `<dd/mm/aaaa>` | `<nome>`    | `03_triado_<fonte>_<versao>.xlsx`       | `concluida`   |
| 4. Classificação         | `<dd/mm/aaaa>` | `<nome>`    | `04_classificado_<fonte>_<versao>.xlsx` | `concluida`   |
| 5. Priorização           | `<dd/mm/aaaa>` | `<nome>`    | `05_priorizado_<fonte>_<versao>.xlsx`   | `concluida`   |
| 6. Validação             | `<dd/mm/aaaa>` | `<nome>`    | `06_validado_<fonte>_<versao>.xlsx`     | `concluida`   |
| 7. Planejamento          | `<dd/mm/aaaa>` | `<nome>`    | `07_protocolo_<fonte>.md`               | `em_execucao` |
| 8. Coleta                | `<dd/mm/aaaa>` | `<nome>`    | `08_bruto_<fonte>_<versao>.<ext>`       | `planejada`   |
| 9. Controle de Qualidade | `<dd/mm/aaaa>` | `<nome>`    | `09_qualidade_<fonte>_<versao>.csv`     | `planejada`   |
| 10. Incorporação         | `<dd/mm/aaaa>` | `<nome>`    | `10_incorporado_<fonte>_<versao>.<ext>` | `planejada`   |

**Fonte:** elaboração própria, `<ano>`.

---

## 4. Decisões Arquiteturais Relacionadas

| ADR              | Título     | Data           | Impacto       |
| ---------------- | ---------- | -------------- | ------------- |
| `adr-<xxx>-<id>` | `<titulo>` | `<dd/mm/aaaa>` | `<descricao>` |

---

## **Registro de Alterações**

| Versão | Data       | Alteração                        | Autor        |
| ------ | ---------- | -------------------------------- | ------------ |
| v0.1   | 24/09/2026 | Criação da Metodologia           | Nayara Pavao |
| v0.1   | 25/09/2026 | Adição de Registro de Alterações | Nayara Pavao |

---
