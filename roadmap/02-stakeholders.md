# Part II — Stakeholders

Segurança de IA é inerentemente multidisciplinar. O roadmap deve equilibrar velocidade operacional com conformidade regulatória.

## Mapa de stakeholders

| Stakeholder | Prioridade | Preocupação principal |
|-------------|------------|----------------------|
| **CISO** | Disponibilidade e velocidade de resposta | Automação do LAM sem perder controle |
| **DPO / Compliance** | LGPD Art. 20 e 48 | Decisões automatizadas, direito de revisão humana |
| **SOC Analysts** | Precisão e explicabilidade | Supervisão de ações SOAR disparadas pelo LAM |
| **Engenharia de IA** | Integridade de embeddings e prompts | Pipeline RAG seguro, versionamento de modelos |
| **Engenharia de Infra** | Zero Trust, segmentação | Exposição de Vector DB e APIs de inferência |
| **Liderança executiva** | Risco reputacional e custo | Métricas de negócio (CRI, downtime) |

## Tensão central: CISO vs DPO

- **CISO** quer maximizar automação: menos MTTD, resposta 24/7, escala do SOC.
- **DPO** exige transparência: explicabilidade de decisões, logs imutáveis, revisão humana quando decisões afetam titulares de dados.

**Resolução proposta:** camada de **AI Guardrails** com sandbox de ações, logs WORM e comitê multidisciplinar mensal de governança de IA.

## Impacto nas operações

| Área | Mudança com LAM |
|------|-----------------|
| SOC | Analistas como revisores humanos de ações automatizadas |
| Engenharia de dados | Manutenção de integridade de embeddings |
| Compliance | Avaliação de decisões automatizadas sob LGPD |
| Segurança | Garantia de explicabilidade e isolamento entre camadas |
