# ADR-001: Seleção de Variáveis Prioritárias

**Status:** Aceita
**Contexto:** O projeto precisa de indicadores que reflitam desenvolvimento econômico e social. As fontes disponíveis são numerosas e com diferentes níveis de granularidade.
**Decisão:** Priorizamos variáveis de renda, emprego formal (RAIS/CAGED) e educação (INEP) por serem os pilares do IDH e estarem disponíveis para todos os municípios.
**Alternativas Consideradas:** Utilizar dados de saúde (DATASUS) como proxy de qualidade de vida, mas descartamos por serem muito específicos e com sazonalidade.
**Consequências:** A base terá um viés econômico-educacional; para análise de saúde, será necessário um esforço complementar.
