# Part I — Problem Statement

## Organização e contexto nacional

**X-Core Cyber Defense** é uma empresa brasileira de alta tecnologia que constrói plataformas de cibersegurança orientadas por IA. A missão é proteger infraestruturas críticas combinando **NDR, XDR, SIEM e SOAR** com um sistema de automação cognitiva — o **LAM (Large Action Model)**.

A empresa atende agências governamentais (BCB, INSS), operadoras de telecom, energia e instituições financeiras — setores sujeitos a ataques sofisticados e regulamentação rigorosa:

- LGPD e diretrizes ANPD
- Normas do Banco Central para instituições supervisionadas
- ISO 27001/27701
- NIST Cybersecurity Framework e NIST AI RMF

## Tecnologia em foco

O **LAM** interpreta alertas, consulta bancos vetoriais, analisa anomalias e dispara ações automatizadas via SOAR. O ecossistema inclui:

| Componente | Função |
|------------|--------|
| NDR/XDR | Visibilidade e detecção |
| SIEM | Correlação de eventos |
| SOAR | Orquestração de resposta |
| Vector DB (Pinecone) | Retrieval de embeddings |
| GPU clusters | Inferência do modelo |
| API Gateway + OIDC/MFA | Identidade federada |

O LAM **não apenas interpreta sinais — ele age**. Isso reduz MTTD/MTTR, mas expande a superfície de ataque e exige governança forte.

## Vulnerabilidades identificadas

### a) Vulnerabilidades de IA
- Prompt injection
- Embedding poisoning
- Model inversion
- Ações autônomas com impacto operacional real

### b) Identidade e autorização
- IAM não diferencia identidades humanas de agentes
- Escopos de API excessivamente permissivos
- Ausência de MFA para máquinas
- Violações do princípio de menor privilégio

### c) Integridade e auditabilidade
- Logs suscetíveis a adulteração
- Auditoria incompleta de prompts e decisões
- Riscos de conformidade LGPD/ANPD (Art. 20 — decisões automatizadas)
- Ausência de cadeias de evidência imutáveis

### d) Dependências arquiteturais
- Bancos vetoriais expostos
- Pipelines de inferência distribuída vulneráveis
- Zero Trust implementado parcialmente

## Risco sistêmico

O problema não é apenas "o LAM pode ser atacado", mas como uma falha em uma camada propaga efeitos:

```
Prompt malicioso → contamina RAG → desvia inferência → SOAR errado → interrupção de serviços
Embedding envenenado → decisões erradas por semanas
Falha IAM → ações não autorizadas pelo LAM
Sem auditabilidade → impossibilidade de defesa legal/regulatória
```

Dimensões afetadas: segurança, operações, compliance, confiança pública.
