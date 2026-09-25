### # ADR-000: Infraestrutura do repositório

 ---

| **Status**              | **`proposto`**             |
| ----------------------- | -------------------------- |
| **Responsável**         | Núcleo de Dados – OITS-UFS |
| **Data de atualização** | 23/09/2029                 |
| **Versão**              | v0.1                       |

---

#### Contexto

O projeto visa criar o Observatório de Inovação Territorial de Sergipe (OITS-UFS) e transformar os campi da Universidade Federal de Sergipe (UFS) em Hubs de Inovação regionais, conectando análise de dados e tecnologias às vocações e desafios socioeconômicos dos territórios. Para sustentar diagnósticos, dashboards e políticas públicas, é necessário um repositório versionado que centralize e documente os
dados do Núcleo de Dados.

A metodologia exige rastreabilidade, reprodutibilidade e preservação.

#### Decisão

Criar um repositório oficial no GitHub para o projeto OITS-UFS, gerenciado pelo Núcleo de Dados, centralizando dados, documentação e referências do projeto. O repositório adota a seguinte estrutura padronizada:

```
oits-ufs-base-dados/
├── data/                   (bases de dados do projeto)
│   ├── processed/          (dados limpos e padronizados)
│   └── raw/                (dados originais, imutáveis)
├── docs/                   (documentação metodológica e técnica)
│   ├── decisions/          (registros de decisão de arquitetura)
│   ├── dictionary/         (dicionário de dados e metadados)
│   ├── methodology/        (documentação metodológica)
│   └── selection/          (artefatos das etapas de seleção)
├── references/             (fontes, catálogos e material de apoio)
├── .gitignore              (arquivos e diretórios ignorados pelo Git)
├── LICENSE                 (termos de uso e distribuição do projeto)
└── README.md               (porta de entrada e guia de navegação) 
```

---

## **Registro de Alterações**

| Versão | Data       | Alteração                        | Autor        |
| ------ | ---------- | -------------------------------- | ------------ |
| v0.1   | 23/09/2026 | Criação da ADR-000               | Nayara Pavao |
| v0.1   | 25/09/2026 | Adição de Registro de Alterações | Nayara Pavao |

---
