# Mapa de artefatos

`Estrutura canônica do repositório e localização dos artefatos de governança.`

---

| **Status**        | *[X] proposto* [ ] vigente [ ] obsoleto |
| ----------------- | --------------------------------------- |
| **Responsável**   | Núcleo de Dados – OITS-UFS              |
| **Atualizado em** | 10/10/2026                              |
| **Versão**        | v0.1                                    |

---

## Estrutura do repositório

```markdown
oits-ufs-base-dados/  
├───── data/                             (bases de dados do projeto)  
│ ├───── processed/                      (dados limpos e padronizados)  
│ └───── raw/                            (dados originais, imutáveis)  
├───── docs/                             (documentação metodológica e técnica)  
│ ├───── governance/                     (estrutura de governança)  
│ │ ├───── adr/                          (registros de decisão de arquitetura)  
│ │ ├───── conventions/                  (parâmetros estruturais)  
│ │ ├───── lists/                        (listas sujeitas a alteração)  
│ │ ├───── tables/                       (tabelas de referência)  
│ │ └───── templates/                    (templates operacionais)  
│ ├───── dictionary/                     (dicionário de dados e metadados)  
│ ├───── methodology/                    (documentação metodológica)  
│ └───── selection/                      (artefatos das etapas de seleção)  
├───── references/                       (fontes, catálogos e material de apoio)  
├───── .gitignore                        (arquivos e diretórios ignorados pelo Git)  
├───── LICENSE                           (termos de uso e distribuição do projeto)  
└───── README.md                         (porta de entrada e guia de navegação)
```

---

## Localização dos artefatos de governança

| Categoria      | Caminho                        | Conteúdo                                     |
| -------------- | ------------------------------ | -------------------------------------------- |
| **ADRs**       | `docs/governance/adr/`         | Registros de decisão de arquitetura          |
| **Parâmetros** | `docs/governance/conventions/` | Configuração estrutural (mapa, nomenclatura) |
| **Listas**     | `docs/governance/lists/`       | Conjuntos sujeitos a alteração recorrente    |
| **Tabelas**    | `docs/governance/tables/`      | Tabelas de referência                        |
| **Templates**  | `docs/governance/templates/`   | Estruturas reutilizáveis de documento        |

---

## Localização dos demais artefatos

| Categoria             | Caminho             | Conteúdo                              |
| --------------------- | ------------------- | ------------------------------------- |
| **Dados brutos**      | `data/raw/`         | Dados originais, imutáveis            |
| **Dados processados** | `data/processed/`   | Dados limpos e padronizados           |
| **Dicionário**        | `docs/dictionary/`  | Dicionário de dados e metadados       |
| **Metodologia**       | `docs/methodology/` | Documentação metodológica             |
| **Seleção**           | `docs/selection/`   | Artefatos das etapas de seleção       |
| **Referências**       | `references/`       | Fontes, catálogos e material de apoio |

---

## Regras de armazenamento

| Regra  | Descrição                                                               |
| ------ | ----------------------------------------------------------------------- |
| **R1** | Toda governança reside sob `docs/governance/`.                          |
| **R2** | Um tipo de recurso, uma pasta.                                          |
| **R3** | Recursos versionados no nome (`_v<maior>.<menor>`) quando aplicável.    |
| **R4** | Parâmetros não levam versão no nome; versionamento pelo repositório.    |
| **R5** | Pastas em inglês; arquivos em português.                                |
| **R6** | Dados brutos em `data/raw/`, imutáveis; derivados em `data/processed/`. |

---

## Prevalência

Em caso de divergência entre este mapa e qualquer reprodução local, prevalece este documento.

---

## **Registro de Alterações**

| Versão | Data       | Alteração                     | Autor        |
| ------ | ---------- | ----------------------------- | ------------ |
| v0.1   | 10/10/2026 | Criação do Mapa de Artefatos. | Nayara Pavao |
|        |            |                               |              |

---
