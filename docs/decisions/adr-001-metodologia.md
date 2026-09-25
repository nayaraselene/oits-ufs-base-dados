# ADR-001: Adoção da metodologia de seleção e coleta

---

| **Status**              | **`proposto`**             |
| ----------------------- | -------------------------- |
| **Responsável**         | Núcleo de Dados – OITS-UFS |
| **Data de atualização** | 23/09/2029                 |
| **Versão**              | v0.1                       |

---

#### Contexto

O projeto tem como objetivo subsidiar políticas públicas de inovação territorial no Estado de Sergipe. Para tanto, necessita de processo sistemático para identificar, selecionar, priorizar e coletar os dados que constituirão a Base OITS-UFS v1.0.

A operacionalização da inovação territorial exige dados que capturem não apenas a dimensão econômica, mas também as capacidades institucionais, sociais e produtivas dos 75 municípios sergipanos. Sem metodologia estruturada, o processo decisório tende a se tornar inconsistente, dificultando a rastreabilidade, a reprodutibilidade e a auditoria das escolhas realizadas.

A metodologia deve observar os princípios de rastreabilidade, reprodutibilidade, consistência, adequação ao objetivo, interoperabilidade e preservação (seção 1.3).

---

#### Decisão

Adotar a Metodologia de Seleção e Coleta de Conjuntos de Dados, registrada em `docs/methodology/00_metodologia.md`, como documento de referência para todas as etapas de identificação, seleção, priorização e coleta de dados do projeto. A  metodologia compreende:

```markdown
### Decisão 1: Estrutura em dez etapas

Adotar o fluxo metodológico em dez etapas sequenciais:

1. Identificação de fontes e recursos potencialmente relevantes;
2. Inventário bruto dos recursos identificados;
3. Triagem e definição de elegibilidade;
4. Classificação por matriz ponderada;
5. Priorização (Alta / Média / Baixa);
6. Validação de casos limítrofes e decisões excepcionais;
7. Planejamento da coleta;
8. Coleta (extração e preservação do dado bruto);
9. Controle de qualidade;
10. Consolidação na Base OITS-UFS.

Cada etapa produz artefato específico, preservado para auditoria e
reprodução, conforme o Quadro 1 da metodologia.

### Decisão 2: Princípios norteadores

Adotar os dez princípios norteadores: atualidade; granularidade
territorial; relevância; confiabilidade; interoperabilidade;
rastreabilidade; reprodutibilidade; preservação; transparência;
proporcionalidade (seção 1.3).

### Decisão 3: Critérios de triagem

Adotar os seis critérios de elegibilidade: adequação temática;
adequação territorial; disponibilidade; identificabilidade;
não duplicidade; integridade mínima da documentação (seção 2.2).
Cada critério produz os resultados: Atende / Não atende / Revisar.

### Decisão 4: Matriz de classificação ponderada

Adotar a matriz de classificação com pesos fixos: cobertura municipal
(3); relevância temática (3); atualidade (2); facilidade de integração
(2). Pontuação máxima: 30. Conversão em prioridade: Alta (20–30);
Média (10–19); Baixa (0–9). Casos limítrofes (9, 10, 19, 20) são
sinalizados para revisão manual (seção 2.3).

### Decisão 5: Estrutura de registros

Adotar as estruturas de registro de triagem (seção 2.2) e de
classificação (seção 2.3), com os campos mínimos definidos na
metodologia.

### Decisão 6: Preservação do dado bruto

Adotar a preservação do dado bruto em sua forma original ou mais
próxima possível. Transformações posteriores não sobrescrevem o
registro original. A estrutura de diretórios separa dados brutos
(`data/raw/`), dados processados (`data/processed/`) e artefatos
de processo (`docs/selection/`), conforme ADR-000.

### Decisão 7: Governança

Adotar ADRs para decisões com impacto metodológico relevante,
conforme ADR-002. Adotar versionamento semântico (`v0.1`, `v0.2`)
para artefatos e dados.
```

---

## **Registro de Alterações**

| Versão | Data       | Alteração                        | Autor        |
| ------ | ---------- | -------------------------------- | ------------ |
| v0.1   | 23/09/2026 | Criação da ADR-001               | Nayara Pavao |
| v0.1   | 25/09/2026 | Adição de Registro de Alterações | Nayara Pavao |

---
