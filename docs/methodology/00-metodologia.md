# Metodologia de Seleção e Coleta de Conjuntos de Dados – OITS-UFS

---

| Status            | *[X] proposto* [ ] vigente [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 10/10/2026                              |
| **Versão**        | v0.1.2                                  |

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

| Princípio                     | Descrição                                                    |
| ----------------------------- | ------------------------------------------------------------ |
| **Atualidade**                | Dados recentes; históricos quando justificados.              |
| **Granularidade territorial** | 75 municípios sergipanos ou derivação documentada.           |
| **Relevância**                | Relação justificável com os objetivos do projeto.            |
| **Confiabilidade**            | Fontes reconhecidas.                                         |
| **Interoperabilidade**        | Integração facilitada, especialmente por códigos do IBGE.    |
| **Rastreabilidade**           | Origem, versão, acesso, coleta e transformações preservadas. |
| **Reprodutibilidade**         | Processo repetível sob condições equivalentes.               |
| **Preservação**               | Versão identificável e recuperável.                          |
| **Transparência**             | Inclusões e exclusões registradas com justificativa.         |
| **Proporcionalidade**         | Esforço compatível com relevância e complexidade.            |

---

## 2. Processo Decisório

### 2.1 Fluxo Metodológico

O fluxo compreende dez etapas sequenciais. Cada etapa produz ou complementa artefato específico, preservado para auditoria e reprodução.

```markdown
# [1] Identificação → [2] Inventário Bruto → [3] Triagem
                                                   ▼
                              ┌────────────────────┴────────────────────┐
                              │                                         │
#                        INELEGÍVEL                                 ELEGÍVEL
                              │                                         │
                              ▼                                         ▼
#                      Registro de exclusão              [4] Classificação (matriz ponderada)
                                                                        ↓
#                                                        [5] Priorização (Alta/Média/Baixa)
                                                                        ↓
#                                                        [6] Validação (casos limítrofes e ADRs)
                                                                        ↓
#                                                        [7] Protocolo de Coleta
                                                                        ↓
#                                                        [8] Coleta (extração + preservação)
                                                                        ↓
#                                                        [9] Controle de Qualidade
                                                                        ↓
#                                                        [10] Consolidação na Base OITS-UFS
```

###### Quadro 1 – Fluxo metodológico e produtos associados

| Etapa                    | Produto Principal                                           |
| ------------------------ | ----------------------------------------------------------- |
| 1. Identificação         | `01-fontes-catalogo.md`                                     |
| 2. Inventário Bruto      | `02-bruto-<fonte>.csv`                                      |
| 3. Triagem               | `03-triado-<fonte>-<versao>.xlsx`                           |
| 4. Classificação         | `04-classificado-<fonte>-<versao>.xlsx`                     |
| 5. Priorização           | `05-priorizado-<fonte>-<versao>.xlsx`                       |
| 6. Validação             | `06-validado-<fonte>-<versao>.xlsx`                         |
| 7. Protocolo             | `07-protocolo-<fonte>.md`                                   |
| 8. Coleta                | `08-coleta-<fonte>-<versao>.<ext>` + `metadados-coleta.csv` |
| 9. Controle de Qualidade | `09-qualidade-<fonte>-<versao>.csv`                         |
| 10. Consolidação         | `10-consolidado-<fonte>-<versao>.<ext>`                     |

---

### 2.2 Critérios de Triagem

A triagem determina a elegibilidade dos recursos. Aplica-se antes da classificação. Cada critério produz: Conforme, Não Conforme ou Pendente.

###### Quadro 2 – Critérios de elegibilidade.

| Critério                               | Regra de avaliação                                                                     | Resultado  |
| -------------------------------------- | -------------------------------------------------------------------------------------- | ---------- |
| **Adequação temática**                 | Relação identificável com ao menos uma dimensão dos objetivos do projeto.              | C / NC / P |
| **Adequação territorial**              | Informações sobre os municípios sergipanos, direta ou mediante derivação documentável. | C / NC / P |
| **Disponibilidade**                    | Acesso ou obtenção por mecanismo identificável e documentável.                         | C / NC / P |
| **Identificabilidade**                 | Conteúdo, unidade de observação e período de referência identificáveis.                | C / NC / P |
| **Não duplicidade**                    | Não redundante em relação a outro recurso já selecionado, salvo justificativa.         | C / NC / P |
| **Integridade mínima da documentação** | Informações mínimas sobre origem e natureza do recurso.                                | C / NC / P |

**Critérios temporais:** A temporalidade é critério de avaliação, não de exclusão automática. Recursos anteriores ao horizonte preferencial permanecem elegíveis quando contribuírem para séries históricas, comparação entre períodos, linha de base, análise de evolução territorial ou complementação de informações atuais inexistentes. A justificativa deve constar do registro de triagem.

**Critérios territoriais:** Distinguem-se três conceitos: abrangência da fonte (território coberto pela instituição provedora), cobertura do recurso (território efetivamente representado no conjunto) e granularidade (nível territorial dos dados). Recursos de abrangência nacional, regional ou estadual são elegíveis quando contiverem registros individualizados dos municípios sergipanos.

**Redundância:** Dois recursos podem ser mantidos quando diferirem em metodologia de produção, período de referência, cobertura territorial, periodicidade, granularidade, definição de variáveis, atualização, qualidade ou documentação. Quando integralmente redundantes, registra-se o recurso mantido como referência e o fundamento da exclusão.

**Registro de triagem:** Toda decisão deve ser registrada:

```text
id_recurso
status_triagem          # elegivel | inelegivel | revisao
criterio_avaliado
resultado               # conforme | nao_conforme | pendente | redundante
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

- $p_i$ pontuação do critério $i$
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

Cada fonte selecionada possui protocolo registrado em `07-protocolo-<fonte>.md`, contemplando:

```text
id_fonte
metodo_extracao          # download direto | API | scraping | solicitacao
formato_original
mecanismo_acesso
periodicidade
periodo_referencia
responsavel_coleta
data_acesso
estrutura_repositorio
convencoes_armazenamento
metadados_obrigatorios
```

**Preservação do dado bruto.** Os dados coletados são armazenados na forma original ou mais próxima possível. Transformações posteriores não sobrescrevem o registro original.

### 3.2 Controle de Qualidade

As verificações são compatíveis com a natureza do conjunto e produzem registro em `09_qualidade_<fonte>_<versao>.csv`.

###### Quadro 4 – Verificações de qualidade e limiares.

| Verificação                    | Procedimento                                                          | Limiar de aceitação                            |
| ------------------------------ | --------------------------------------------------------------------- | ---------------------------------------------- |
| **Integridade**                | Hash SHA-256 do arquivo coletado comparado ao registrado no protocolo | Correspondência exata                          |
| **Estrutura**                  | Número de colunas, tipos de dados, codificação                        | Ausência de truncamento; codificação declarada |
| **Cobertura municipal**        | Contagem de municípios sergipanos representados                       | 37 municípios mínimos                          |
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

## **Registro de Alterações**

| Versão | Data       | Alteração                          | Autor        |
| ------ | ---------- | ---------------------------------- | ------------ |
| v0.1   | 24/09/2026 | Criação da Metodologia             | Nayara Pavao |
| v0.1.1 | 25/09/2026 | Adição de Registro de Alterações   | Nayara Pavao |
| v0.1.2 | 10/10/2026 | Adequação estrutural e atualização | Nayara Pavao |

---
