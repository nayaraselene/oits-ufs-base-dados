# Nomenclatura

Convenções únicas de nomenclatura para artefatos do repositório.

---

| Status            | *[X] proposto* [ ] vigente [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 10/10/2026                              |
| **Versão**        | v0.1                                    |

---

## Princípio

Adotar **kebab-case** (`palavras-separadas-por-hifen`) em todo o repositório, para arquivos e diretórios.

---

## Artefatos de governança

| Item          | Convenção                                                         |
| ------------- | ----------------------------------------------------------------- |
| **ADR**       | `adr-NNN-titulo-com-hifens.md`                                    |
|               | `NNN`: número sequencial de três dígitos (000, 001, ...);         |
|               | `titulo-com-hifens`: título conciso em kebab-case;                |
|               | Exemplo: `adr-002-estrutura-governanca.md`.                       |
| **Parâmetro** | `<tema>.md`                                                       |
|               | Sem prefixo e sem versão no nome; versionamento pelo repositório; |
|               | Exemplos: `nomenclatura.md`, `mapa-artefatos.md`.                 |
| **Lista**     | `lista-<tema>-<versao>.md`                                        |
|               | `<tema>`: descritivo em kebab-case;                               |
|               | `<versao>`: versão semântica (`v0.1`, `v0.2`);                    |
|               | Exemplo: `lista-marcadores-territoriais-v0.1.md`.                 |
| **Tabela**    | `tabela-<tema>-<versao>.md`                                       |
|               | Exemplo: `tabela-score-destino-v0.1.md`.                          |
| **Template**  | `template-<tipo-de-documento>.md`                                 |
|               | `<tipo-de-documento>`: descritivo em kebab-case;                  |
|               | Exemplo: `template-adr.md`.                                       |

---

## Artefatos operacionais

| Item                    | Convenção                                                            |
| ----------------------- | -------------------------------------------------------------------- |
| **Protocolo**           | `NN-protocolo-<fonte>.md`                                            |
|                         | `NN`: número da etapa (08 para protocolo da coleta);                 |
|                         | `<fonte>`: identificador da fonte (`ibge-01`, `inpi-01`);            |
|                         | Exemplo: `08-protocolo-ibge-01.md`.                                  |
| **Artefato de seleção** | `NN-<tipo>-<fonte>-<versao>.<ext>`                                   |
|                         | `NN`: número da etapa (01 a 10);                                     |
|                         | `<tipo>`: descrição do artefato (`bruto`, `triado`, `classificado`); |
|                         | `<fonte>`: identificador da fonte;                                   |
|                         | `<versao>`: versão semântica (`v0.1`, `v0.2`);                       |
|                         | Exemplo: `03-triado-ibge-v0.1.xlsx`.                                 |
| **Método operacional**  | `metodo-<nome>.md`                                                   |
|                         | `<nome>`: descritivo do método;                                      |
|                         | Exemplo: `metodo-triagem-automatizada.md`.                           |
| **Dicionário de dados** | `dicionario-dados.csv`                                               |
|                         | Um arquivo único, atualizado a cada nova versão.                     |

---

## Diretórios

| Item      | Convenção                                                              |
| --------- | ---------------------------------------------------------------------- |
| **Geral** | kebab-case, em inglês;                                                 |
|           | Exemplos: `governance/`, `conventions/`, `methodology/`, `selection/`. |

---

## Convenções gerais

| Item           | Convenção                                                            |
| -------------- | -------------------------------------------------------------------- |
| **Caixa**      | Minúsculas em todos os nomes de arquivo e diretório.                 |
| **Separador**  | Hífen (`-`) em todos os nomes.                                       |
| **Acentuação** | Sem acentos em nomes de arquivo e diretório.                         |
| **Extensão**   | Sempre explícita (`.md`, `.csv`, `.xlsx`).                           |
| **Versão**     | Sufixo `-v<maior>.<menor>` quando o artefato for versionado no nome. |

---

## Prevalência

Em caso de divergência entre esta convenção e qualquer outra fonte, prevalece este documento.

---

## **Registro de Alterações**

| Versão | Data       | Alteração                            | Autor        |
| ------ | ---------- | ------------------------------------ | ------------ |
| v0.1   | 10/10/2026 | Criação do artefato de Nomenclatura. | Nayara Pavao |
|        |            |                                      |              |

---
