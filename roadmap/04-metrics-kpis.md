# Part IV — Metrics & Risk Quantification

## Métricas técnicas

| Métrica | Definição | Alvo |
|---------|-----------|------|
| **MTTD** | Mean Time to Detect | < 5 min para alertas críticos |
| **MTTR** | Mean Time to Respond | < 15 min com LAM + revisão humana |
| **FPR** | False Positive Rate do LAM | < 2% em playbooks automatizados |
| **PIS** | Prompt/Embedding Integrity Score | > 99.5% validação pré-inferência |

## Métricas de negócio

| Métrica | Definição |
|---------|-----------|
| **Downtime** | Horas de interrupção causadas por falsos positivos SOAR |
| **CRI** | Cost of Incidents — custo financeiro de incidentes de IA |
| **Compliance Score** | % de decisões automatizadas com trilha de auditoria completa |

## Alinhamento regulatório

- **LGPD Art. 20:** direito de revisão de decisões automatizadas → métrica de revisão humana
- **ISO 27001/27701:** controles de acesso e logging → Compliance Score
- **NIST AI RMF:** governança, mapeamento de risco, monitoramento contínuo

## Fórmula de risco operacional

```
Risco = P(incidente) × Impacto(incidente) × Exposição
```

Onde **Exposição** captura a autonomia do LAM (ações sem revisão humana) e a superfície do Vector DB.
