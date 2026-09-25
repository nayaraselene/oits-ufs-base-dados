# Metodologia de Seleção e Coleta de Conjuntos de Dados – OITS-UFS

---

| **Status**              | **`proposto`**             |
| ----------------------- | -------------------------- |
| **Responsável**         | Núcleo de Dados – OITS-UFS |
| **Data de atualização** | 25/09/2029                 |
| **Versão**              | v0.1                       |

---

## 1. Fundamentos

### 1.1 Objetivo

Definir critérios, etapas e registros para identificar, selecionar, priorizar e coletar os dados que constituirão a Base OITS-UFS v1.0. A metodologia visa subsidiar o desenvolvimento de políticas públicas de inovação territorial no Estado de Sergipe, garantindo que o processo decisório seja **rastreável**, **reproduzível** e **consistente**.

A operacionalização da inovação territorial exige dados que capturem não apenas a dimensão econômica, mas também as capacidades institucionais, sociais e produtivas dos municípios sergipanos. A metodologia aqui descrita produz o conjunto de dados elegíveis, priorizados e documentados que sustentarão essa análise.

### 1.2 Escopo

**A metodologia cobre:**

1. Identificação de fontes potencialmente relevantes;
2. Inventário bruto dos recursos identificados;
3. Triagem e definição de elegibilidade;
4. Classificação e priorização;
5. Registro de decisões e justificativas;
6. Planejamento e execução da coleta;
7. Preservação do dado bruto e metadados;
8. Controle de qualidade;
9. Incorporação à Base OITS-UFS.

**A metodologia não cobre:**

- Tratamento analítico aprofundado, modelagem estatística ou interpretação substantiva;
- Definição das dimensões analíticas do diagnóstico territorial (escopo conceitual do projeto);
- Coleta de dados primários mediante *survey* ou entrevista;
- Políticas de acesso e licenciamento dos dados após incorporação.

### 1.3 Princípios Norteadores

| Princípio                     | Descrição                                                                                                                                                                                              |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Atualidade**                | Priorizar dados com período de referência recente, considerando a natureza e periodicidade da variável. Dados históricos mantêm-se elegíveis quando justificada a necessidade analítica.               |
| **Granularidade territorial** | Priorizar conjuntos que permitam identificar os 75 municípios sergipanos individualmente ou cuja granularidade superior permita derivação documentada.                                                 |
| **Relevância**                | Priorizar dados cuja relação com os objetivos do projeto e com as dimensões do diagnóstico territorial possa ser explicitamente justificada.                                                           |
| **Confiabilidade**            | Dar preferência a dados produzidos ou disponibilizados por fontes institucionais, administrativas, científicas ou técnicas reconhecidas.                                                               |
| **Interoperabilidade**        | Priorizar formatos, identificadores e estruturas que facilitem a integração com outros conjuntos, especialmente mediante códigos municipais do Instituto Brasileiro de Geografia e Estatística (IBGE). |
| **Rastreabilidade**           | Preservar informações suficientes para identificar origem, versão, data de acesso, procedimento de coleta e transformações aplicadas.                                                                  |
| **Reprodutibilidade**         | Documentar critérios, procedimentos e decisões de modo que o processo possa ser repetido por outro pesquisador sob condições equivalentes.                                                             |
| **Preservação**               | Manter dados e metadados de forma que a versão utilizada possa ser identificada e, quando tecnicamente possível, recuperada.                                                                           |
| **Transparência**             | Registrar decisões de inclusão e de exclusão, com critérios e justificativas correspondentes.                                                                                                          |
| **Proporcionalidade**         | O esforço de avaliação, coleta e documentação deve ser compatível com a relevância e complexidade do recurso.                                                                                          |

---

## 2. Processo Decisório

### 2.1 Fluxo Metodológico

O fluxo compreende dez etapas sequenciais. Cada etapa produz artefato específico, preservado para auditoria e reprodução.

```
[1] Identificação → [2] Inventário Bruto → [3] Triagem
                                                  ▼
                             ┌────────────────────┴────────────────────┐
                             │                                         │
                        INELEGÍVEL                                 ELEGÍVEL
                             │                                         │
                             ▼                                         ▼
                      Registro de exclusão              [4] Classificação (matriz ponderada)
                                                                       ↓
                                                        [5] Priorização (Alta/Média/Baixa)
                                                                       ↓
                                                        [6] Validação (casos limítrofes e ADRs)
                                                                       ↓
                                                        [7] Protocolo de Coleta
                                                                       ↓
                                                        [8] Coleta (extração + preservação)
                                                                       ↓
                                                        [9] Controle de Qualidade
                                                                       ↓
                                                        [10] Consolidação na Base OITS-UFS
```

###### Quadro 1 – Fluxo metodológico e produtos associados

| Etapa                    | Produto Principal                                           |
| ------------------------ | ----------------------------------------------------------- |
| 1. Identificação         | `01_fontes_catalogo.md`                                     |
| 2. Inventário Bruto      | `02_bruto_<fonte>.csv`                                      |
| 3. Triagem               | `03_triado_<fonte>_<versao>.xlsx`                           |
| 4. Classificação         | `04_classificado_<fonte>_<versao>.xlsx`                     |
| 5. Priorização           | `05_priorizado_<fonte>_<versao>.xlsx`                       |
| 6. Validação             | `06_validado_<fonte>_<versao>.xlsx`                         |
| 7. Protocolo             | `07_protocolo_<fonte>.md`                                   |
| 8. Coleta                | `08_coleta_<fonte>_<versao>.<ext>` + `metadados_coleta.csv` |
| 9. Controle de Qualidade | `09_qualidade_<fonte>_<versao>.csv`                         |
| 10. Consolidação         | `10_consolidado_<fonte>_<versao>.<ext>`                     |

---

### 2.2 Critérios de Triagem

A triagem determina a elegibilidade dos recursos. Aplica-se antes da classificação. Cada critério produz: Atende, Não atende ou Revisar.

###### Quadro 2 – Critérios de elegibilidade.

| Critério                               | Regra de avaliação                                                                                                                  | Resultado                     |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- |
| **Adequação temática**                 | O recurso possui relação identificável com ao menos uma dimensão contemplada pelos objetivos do projeto.                            | Atende / Não atende / Revisar |
| **Adequação territorial**              | O recurso permite identificar informações referentes aos municípios sergipanos, diretamente ou mediante derivação documentável.     | Atende / Não atende / Revisar |
| **Disponibilidade**                    | O recurso pode ser acessado ou obtido por mecanismo identificável e documentável.                                                   | Atende / Não atende / Revisar |
| **Identificabilidade**                 | É possível identificar o conteúdo, a unidade de observação e, quando aplicável, o período de referência.                            | Atende / Não atende / Revisar |
| **Não duplicidade**                    | O recurso não é integralmente redundante em relação a outro já selecionado, salvo justificativa para manutenção de ambas as fontes. | Atende / Redundante / Revisar |
| **Integridade mínima da documentação** | Existem informações mínimas que permitam compreender origem e natureza do recurso.                                                  | Atende / Não atende / Revisar |

**Critérios temporais:** A temporalidade constitui critério de avaliação, não de exclusão automática. Recursos anteriores ao horizonte preferencial permanecem elegíveis quando contribuírem para: séries históricas, comparação entre períodos, linha de base, análise de evolução territorial ou complementação de informações atuais inexistentes. A justificativa deve constar do registro de triagem.

**Critérios territoriais:** Distinguem-se três conceitos: abrangência da fonte (território coberto pela instituição provedora), cobertura do recurso (território efetivamente representado no conjunto) e granularidade (nível territorial dos dados). Recursos de abrangência nacional, regional ou estadual são elegíveis quando contiverem registros individualizados dos municípios sergipanos.

**Redundância:** Dois recursos podem ser mantidos quando diferirem em: metodologia de produção, período de referência, cobertura territorial, periodicidade, granularidade, definição de variáveis, atualização, qualidade ou documentação. Quando integralmente redundantes, registra-se o recurso mantido como referência e o fundamento da exclusão.

**Registro de triagem:** Toda decisão deve ser registrada:

```text
id_recurso
status_triagem          # elegivel | inelegivel | revisao
criterio_avaliado
resultado               # atende | nao_atende | revisar | redundante
motivo
observacao
responsavel
data_avaliacao
```

Recursos inelegíveis não são removidos do inventário bruto. O registro preserva o universo inicialmente considerado. Recursos em revisão são encaminhados para avaliação complementar antes da classificação.

---

### 2.3 Matriz de Classificação Ponderada

A classificação estima a prioridade relativa dos recursos elegíveis. Recursos inelegíveis não recebem pontuação.

###### Quadro 3 – Critérios e pesos da matriz de classificação.

| Critério                 | Peso | Escala | Pontuação máxima |
| ------------------------ | ---- | ------ | ---------------- |
| Cobertura municipal      | 3    | 0–3    | 9                |
| Relevância temática      | 3    | 0–3    | 9                |
| Atualidade               | 2    | 0–3    | 6                |
| Facilidade de integração | 2    | 0–3    | 6                |
| **Total**                | —    | —      | **30**           |

**Fórmula:** $P= \sum_{i=1}^{4}(p_i \times w_i)$, onde:

- $p_i$: pontuação do critério $i$

- $w_i$ peso do critério $i$

**Cobertura municipal:**

| Pontuação | Critério                                                       |
|:---------:| -------------------------------------------------------------- |
| 0         | Não contém informação identificável para municípios sergipanos |
| 1         | Menos de 50% dos municípios (até 37 de 75)                     |
| 2         | 50% a 99% dos municípios (38 a 74 de 75)                       |
| 3         | 100% dos municípios (75 de 75)                                 |

**Relevância temática:**

| Pontuação | Critério                                                               |
|:---------:| ---------------------------------------------------------------------- |
| 0         | Relação inexistente ou marginal com os objetivos do projeto            |
| 1         | Informação predominantemente contextual ou complementar                |
| 2         | Contribui diretamente para uma ou mais dimensões do diagnóstico        |
| 3         | Mede diretamente uma dimensão prioritária para os objetivos do projeto |

**Atualidade:**

| Pontuação | Critério                                        |
|:---------:| ----------------------------------------------- |
| 0         | Período de referência superior a 5 anos         |
| 1         | Período de referência entre 3 e 5 anos          |
| 2         | Período de referência entre 2 e menos de 3 anos |
| 3         | Período de referência inferior a 2 anos         |

A idade é calculada a partir do **período de referência**, não da data de publicação ou atualização da página.

**Facilidade de integração:**

| Pontuação | Critério                                                                      |
|:---------:| ----------------------------------------------------------------------------- |
| 0         | Não possui identificador territorial utilizável                               |
| 1         | Associação municipal depende de tratamento manual ou procedimento complexo    |
| 2         | Possui identificador padronizado, mas requer transformação ou correspondência |
| 3         | Utiliza diretamente código oficial do município do IBGE                       |

**Classificação da prioridade:**

| Prioridade | Pontuação | Finalidade                                                       |
|:----------:|:---------:| ---------------------------------------------------------------- |
| **Alta**   | 20–30     | Priorizar processamento e coleta                                 |
| **Média**  | 10–19     | Processar após alta prioridade ou conforme necessidade analítica |
| **Baixa**  | 0–9       | Manter como recurso complementar                                 |

**Casos limítrofes:** Serão sinalizados para revisão manual os recursos com pontuação 9, 10, 19 ou 20. A revisão pode confirmar, corrigir ou registrar decisão excepcional.

**Registro de classificação:**

```text
id_recurso
cobertura_municipal
relevancia_tematica
atualidade
facilidade_integracao
pontuacao_total
prioridade              # alta | media | baixa
revisar                 # sim | nao
justificativa
responsavel
data_avaliacao
```

---

## 3. Operação

### 3.1 Protocolo de Coleta

Cada recurso selecionado possui protocolo registrado em `07_protocolo_<fonte>.md`, contemplando:

```text
id_recurso
fonte
metodo_extracao          # download direto | API | scraping | solicitacao
formato_original
mecanismo_acesso
periodicidade
periodo_referencia
hash_verificacao         # MD5 ou SHA-256 do arquivo original
responsavel_coleta
data_acesso
estrutura_repositorio
convencoes_armazenamento
metadados_obrigatorios
```

**Preservação do dado bruto.** Os dados coletados são armazenados na forma original ou mais próxima possível. Transformações posteriores não sobrescrevem o registro original. A estrutura de diretórios separa dados brutos (`/bruto/`), metadados (`/metadados/`) e artefatos de processo (`/processo/`). Essa separação é prática recomendada para reprodutibilidade e arquivamento .

### 3.2 Controle de Qualidade

As verificações são compatíveis com a natureza do conjunto e produzem registro em `09_qualidade_<fonte>_<versao>.csv`.

###### Quadro 4 – Verificações de qualidade e limiares.

| Verificação                    | Procedimento                                                          | Limiar de aceitação                            |
| ------------------------------ | --------------------------------------------------------------------- | ---------------------------------------------- |
| **Integridade**                | Hash SHA-256 do arquivo coletado comparado ao registrado no protocolo | Correspondência exata                          |
| **Estrutura**                  | Número de colunas, tipos de dados, codificação                        | Ausência de truncamento; codificação declarada |
| **Cobertura municipal**        | Contagem de municípios sergipanos representados                       | <mark>[A DEFINIR]</mark> municípios mínimos    |
| **Identificador territorial**  | Presença de código IBGE de 7 dígitos                                  | 100% dos registros municipais                  |
| **Duplicidades**               | Registros duplicados por chave primária                               | Zero duplicidades                              |
| **Valores ausentes**           | Percentual de nulos por variável crítica                              | ≤ <mark>[A DEFINIR]</mark>% por variável       |
| **Consistência temporal**      | Período de referência declarado vs. conteúdo                          | Correspondência                                |
| **Consistência com metadados** | Variáveis descritas vs. variáveis presentes                           | Correspondência ≥ 95%                          |

Os valores <mark>[A DEFINIR]</mark> dependem de calibração empírica na primeira rodada de coleta.

### 3.3 Tratamento e Preparação para Análise

Após aprovação no controle de qualidade, os dados passam a tratamento padronizado:

1. **Padronização de identificadores IBGE:** conversão de códigos municipais para o padrão de 7 dígitos do IBGE;
2. **Normalização de unidades:** conversão de unidades monetárias para valores correntes ou constantes conforme período de referência;
3. **Normalização de períodos:** alinhamento de períodos de referência a granularidade anual ou municipal;
4. **Documentação de transformações:** registro em `dicionario_dados.csv` de cada variável, incluindo definição original, transformação aplicada e unidade final.

---

## 4. Governança

### 4.1 Registro de Decisões Arquiteturais (ADRs)

Decisões com impacto metodológico relevante são registradas em `adr-NNN-titulo-com-hifens.md`, no formato:

```markdown
### # ADR-NNN: [Título]
---
| **Status**      | **`<status>`**               |
| --------------- | ---------------------------- |
| **Data**        | dd/mm/yyyy                   |
| **Responsável** | <responsavel>                |
---
#### Contexto
    <contexto>

#### Decisão  
    <decisao>

###### Decisão X: [Subtítulo]
    <decisao>

#### Consequências (opcional)
    <Consequência positiva>
    <Consequência negativa ou risco>
    <Impacto sobre etapas subsequentes>

---
<status> = {`proposto` | `aceito` | `rejeitado` | 
`atualizado` | `obsoleto` | `substituído por ADR-NNN`}
```

**Decisões que exigem ADR:**

- Alteração de pesos da matriz de classificação;
- Exceção a critério de elegibilidade;
- Exclusão de recurso por redundância integral;
- Manutenção de recurso com pontuação de atualidade 0;
- Alteração de limiares de qualidade.

### 4.2 Versionamento e Preservação

- **Dados brutos:** imutáveis após coleta. Nova coleta gera nova versão;
- **Artefatos de processo:** versionados.

---

# Apêndice: Templates

## 01_fontes_catalogo.md

---

**Finalidade:** registrar o catálogo de fontes identificadas na Etapa 1, com informações suficientes para localizar, caracterizar e rastrear cada fonte provedora de dados. O catálogo é o ponto de entrada do fluxo metodológico e alimenta o inventário bruto (Etapa 2).

**Escopo:** uma entrada por **fonte** (instituição provedora). Recursos específicos de cada fonte são registrados no artefato `02_bruto_<fonte>.csv`.

```markdown
# Catálogo de Fontes – OITS-UFS

**Versão:** v<0.x>
**Data:** <dd/mm/aaaa>
**Responsável:** <nome>
**Projeto:** OITS-UFS + InovaHUB-UFS

---

## 1. Objetivo

Registrar as fontes potencialmente relevantes para a caracterização
dos municípios sergipanos e para as análises de vocações e dinâmicas
territoriais no âmbito do projeto OITS-UFS.

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

## 3. Fontes Identificadas

### 3.1 <SIGLA> – <Nome da Instituição>

| Campo | Conteúdo |
|---|---|
| **id_fonte** | `[OBRIGATÓRIO]` |
| **Instituição responsável** | `[OBRIGATÓRIO]` |
| **Sigla** | `[OBRIGATÓRIO]` |
| **Abrangência** | `nacional` \| `regional` \| `estadual` \| `municipal` |
| **Endereço de acesso** | `[OBRIGATÓRIO]` (URL principal) |
| **Tipo de recurso** | `microdados` \| `agregados` \| `indicadores` \| `cadastros` \| `outro` |
| **Descrição preliminar** | `[OBRIGATÓRIO]` (2–4 linhas) |
| **Periodicidade declarada** | `anual` \| `mensal` \| `irregular` \| `[A DEFINIR]` |
| **Período de referência disponível** | `[OBRIGATÓRIO]` |
| **Formato de disponibilização** | `CSV` \| `XLSX` \| `JSON` \| `API` \| `PDF` \| `outro` |
| **Licença de uso** | `[A DEFINIR]` |
| **Acesso** | `aberto` \| `restrito` \| `sob_solicitacao` |
| **Dimensões potencialmente atendidas** | `[A DEFINIR]` (econômica, educacional, inovação, trabalho, institucional, etc.) |
| **Status** | `identificada` \| `em_avaliacao` \| `inventariada` \| `descartada` |
| **Data de identificação** | `[OBRIGATÓRIO]` |
| **Responsável pela identificação** | `[OBRIGATÓRIO]` |
| **Observações** | `[opcional]` |

*(Repetir a subseção 3.N para cada fonte identificada.)*

---

## 4. Quadro-Síntese

| id_fonte | Instituição | Abrangência | Tipo de recurso | Status | Data de identificação |
|---|---|---|---|---|---|
| `IBGE_01` | IBGE | nacional | agregados | inventariada | `<dd/mm/aaaa>` |
| `[A DEFINIR]` | | | | | |

**Fonte:** elaboração própria, `<ano>`.

---

## 5. Registro de Alterações

| Versão | Data | Alteração | Responsável |
|---|---|---|---|
| v0.1 | `<dd/mm/aaaa>` | Criação do catálogo | `<nome>` |
| | | | |

---

## 6. Referências

- Metodologia de Seleção e Coleta de Conjuntos de Dados – OITS-UFS, v0.1, seção 4, Etapa 1.
- [Outras referências aplicáveis]
```

## 07_protocolo_<id_fonte>.md

---

**Finalidade:** registrar o planejamento da coleta (Etapa 7) de cada recurso selecionado, definindo método de extração, formato, período de referência, hash de verificação, responsável e data de acesso. O protocolo deve ser suficientemente detalhado para permitir execução consistente e reproduzível por outro pesquisador.

**Escopo:** um protocolo por **recurso** (conjunto/base candidato) selecionado. O nome do arquivo segue o padrão `07_protocolo_<fonte>.md`, onde `<fonte>` corresponde ao `id_fonte` do catálogo.

```markdown
# Protocolo de Coleta – <id_recurso>

**Versão:** v<0.x>
**Data:** <dd/mm/aaaa>
**Responsável:** <nome>
**Projeto:** OITS-UFS + InovaHUB-UFS
**Fonte:** <id_fonte> – <Nome da Instituição>
**Status do protocolo:** `planejado` | `em_execucao` | `concluido` | `revisado`

---

## 1. Identificação do Recurso

| Campo | Conteúdo |
|---|---|
| **id_recurso** | `[OBRIGATÓRIO]` |
| **Nome do recurso** | `[OBRIGATÓRIO]` |
| **Descrição** | `[OBRIGATÓRIO]` (2–4 linhas) |
| **Unidade de observação** | `[OBRIGATÓRIO]` (município, estabelecimento, vínculo, etc.) |
| **Granularidade territorial** | `municipal` \| `estadual` \| `nacional` \| `outra` |
| **Período de referência** | `[OBRIGATÓRIO]` |
| **Periodicidade** | `anual` \| `mensal` \| `irregular` |
| **Prioridade atribuída** | `alta` \| `media` \| `baixa` |
| **Pontuação na matriz** | `[OBRIGATÓRIO]` (0–30) |
| **Dimensão analítica** | `[A DEFINIR]` |

---

## 2. Método de Extração

| Campo | Conteúdo |
|---|---|
| **Método** | `download_direto` \| `api` \| `scraping` \| `solicitacao` \| `outro` |
| **Mecanismo de acesso** | `[OBRIGATÓRIO]` (URL, endpoint, formulário) |
| **Autenticação** | `nenhuma` \| `token` \| `credencial_institucional` |
| **Formato original** | `CSV` \| `XLSX` \| `JSON` \| `XML` \| `PDF` \| `outro` |
| **Codificação** | `UTF-8` \| `Latin-1` \| `[A DEFINIR]` |
| **Delimitador** | `,` \| `;` \| `\t` \| `[A DEFINIR]` |
| **Volume estimado** | `[A DEFINIR]` (nº de registros ou MB) |
| **Frequência de coleta** | `única` \| `anual` \| `mensal` |
| **Procedimento passo a passo** | 1. `<passo>`<br>2. `<passo>`<br>3. `<passo>` |

---

## 3. Preservação do Dado Bruto

| Campo | Conteúdo |
|---|---|
| **Diretório de armazenamento** | `/bruto/<id_fonte>/<id_recurso>/<versao>/` |
| **Nome do arquivo original** | `08_bruto_<fonte>_<versao>.<ext>` |
| **Hash de verificação** | `SHA-256: <hash>` |
| **Data de cálculo do hash** | `<dd/mm/aaaa>` |
| **Responsável pela coleta** | `[OBRIGATÓRIO]` |
| **Data de acesso** | `[OBRIGATÓRIO]` |
| **Regra de imutabilidade** | O arquivo bruto não deve ser sobrescrito. Nova coleta gera nova versão. |
| **Backup** | `[A DEFINIR]` (local, nuvem institucional) |

---

## 4. Metadados Obrigatórios

| Campo | Conteúdo |
|---|---|
| **Título** | `[OBRIGATÓRIO]` |
| **Fonte** | `<id_fonte>` |
| **Versão** | `<versao>` |
| **Data de coleta** | `<dd/mm/aaaa>` |
| **Período de referência** | `[OBRIGATÓRIO]` |
| **Cobertura territorial** | `[OBRIGATÓRIO]` |
| **Unidade de medida** | `[OBRIGATÓRIO]` |
| **Identificador territorial** | `codigo_ibge_7` \| `outro` |
| **Licença** | `[A DEFINIR]` |
| **Observações** | `[opcional]` |

---

## 5. Controle de Qualidade

| Verificação | Procedimento | Limiar | Resultado |
|---|---|---|---|
| **Integridade** | Comparação SHA-256 | Correspondência exata | `[ ]` |
| **Estrutura** | Nº de colunas, tipos, codificação | Ausência de truncamento | `[ ]` |
| **Cobertura municipal** | Contagem de municípios sergipanos | `[A DEFINIR]` | `[ ]` |
| **Identificador territorial** | Presença de código IBGE 7 dígitos | 100% | `[ ]` |
| **Duplicidades** | Chave primária | Zero | `[ ]` |
| **Valores ausentes** | Percentual de nulos por variável crítica | ≤ `[A DEFINIR]`% | `[ ]` |
| **Consistência temporal** | Período declarado vs. conteúdo | Correspondência | `[ ]` |
| **Consistência com metadados** | Variáveis descritas vs. presentes | ≥ 95% | `[ ]` |

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

| Versão | Data       | Alteração                        | Autor        |
| ------ | ---------- | -------------------------------- | ------------ |
| v0.1   | 24/09/2026 | Criação da Metodologia           | Nayara Pavao |
| v0.1   | 25/09/2026 | Adição de Registro de Alterações | Nayara Pavao |

---
