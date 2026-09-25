# OITS-UFS – Base de Dados

---

| **Status**              | **`proposto`**             |
| ----------------------- | -------------------------- |
| **Responsável**         | Núcleo de Dados – OITS-UFS |
| **Data de atualização** | 25/09/2029                 |
| **Versão**              | v0.1                       |

---

Repositório oficial do Núcleo de Dados do **Observatório de Inovação Territorial de Sergipe (OITS-UFS)**, iniciativa da Universidade Federal de Sergipe (UFS) com apoio do Conselho Nacional de Desenvolvimento Científico e Tecnológico (CNPq).

---

## Sobre o projeto

O OITS-UFS tem como objetivo transformar os campi da Universidade Federal de Sergipe em Hubs de Inovação regionais, conectando análise de dados e tecnologias às vocações e desafios socioeconômicos dos territórios sergipanos. O projeto busca subsidiar diagnósticos, dashboards e políticas públicas de inovação territorial, considerando não apenas a dimensão econômica, mas também as capacidades institucionais, sociais e produtivas dos 75 municípios de Sergipe.

Para sustentar esse propósito, o repositório centraliza, versiona e documenta os dados produzidos e curados pelo Núcleo de Dados, adotando os princípios de **rastreabilidade**, **reprodutibilidade**, **consistência**, **interoperabilidade** e **preservação**. A metodologia que orienta todo o processo decisório é pública e registrada neste repositório, de modo que qualquer pesquisador possa compreender, auditar e reproduzir as escolhas realizadas.

---

## Estrutura do repositório

O repositório segue a estrutura definida no ADR-000, separando dados, documentação e referências:

```markdown
oits-ufs-base-dados/
├── data/                   (bases de dados do projeto)
│   ├── processed/          (dados limpos e padronizados)
│   └── raw/                (dados originais, imutáveis)
├── docs/                   (documentação metodológica e técnica)
│   ├── decisions/          (registros de decisão de arquitetura — ADRs)
│   ├── dictionary/         (dicionário de dados e metadados)
│   ├── methodology/        (documentação metodológica)
│   └── selection/          (artefatos das etapas de seleção)
├── references/             (fontes, catálogos e material de apoio)
├── .gitignore              (arquivos e diretórios ignorados pelo Git)
├── LICENSE                 (termos de uso e distribuição do projeto)
└── README.md               (este documento)
```

---

## Metodologia

A **Metodologia de Seleção e Coleta de Conjuntos de Dados** (v0.1) define critérios, etapas e registros para identificar, selecionar, priorizar e coletar os dados que constituirão a Base OITS-UFS v1.0.

O fluxo metodológico compreende dez etapas sequenciais, cada uma produzindo artefato específico e preservado para auditoria e reprodução: identificação de fontes; inventário bruto; triagem e elegibilidade; classificação por matriz ponderada; priorização (Alta / Média / Baixa); validação de casos limítrofes; planejamento da coleta; coleta e preservação do dado bruto; controle de qualidade; e consolidação na Base OITS-UFS.

---

## Governança

As decisões com impacto metodológico relevante são registradas em **ADRs (Architecture Decision Records)**, no formato Nygard adaptado, e ficam disponíveis em `docs/decisions/`.

A estrutura de governança (ADR-002) define convenções únicas de nomenclatura, regras de versionamento semântico, política de preservação do dado bruto e localização padronizada dos artefatos. A governança é proporcional ao contexto atual do projeto, operado por uma única responsável pela coleta, tratamento e análise de dados.

---

## Estado atual

O projeto encontra-se em desenvolvimento da **Base OITS-UFS v0.1**. As fontes atualmente registradas no Catálogo são o **IBGE** (`IBGE_01`) e o **INPI** (`INPI_01`). O fluxo de triagem do IBGE já foi executado sobre 130.571 recursos inventariados, com 228 elegíveis, 120.725 inelegíveis e 9.618 sinalizados para revisão. Etapas seguintes estão em andamento.

---

## Licença

Os termos de uso e distribuição do projeto estão definidos no arquivo `LICENSE`.

---

## **Registro de Alterações**

| Versão | Data       | Alteração         | Autor        |
| ------ | ---------- | ----------------- | ------------ |
| v0.1   | 25/09/2026 | Criação do README | Nayara Pavao |

---