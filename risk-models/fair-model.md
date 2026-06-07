# FAIR Model — Factor Analysis of Information Risk

## Decomposição

```
Risk = Loss Event Frequency (LEF) × Loss Magnitude (LM)

LEF = Threat Event Frequency (TEF) × Vulnerability (Vuln)
```

## Aplicação ao LAM

| Fator | Exemplo LAM |
|-------|-------------|
| **TEF** | Tentativas de prompt injection por dia |
| **Vuln** | Probabilidade de bypass dos guardrails |
| **LM** | Custo de downtime + multas LGPD + reputação |

## Exemplo numérico (ilustrativo)

| Fator | Valor | Unidade |
|-------|-------|---------|
| TEF | 50 | tentativas/dia |
| Vuln | 0.05 | 5% bypass rate |
| LM | R$ 500.000 | por incidente grave |

**LEF** = 50 × 0.05 = 2.5 eventos de perda/dia  
**Risco anual** ≈ 2.5 × 365 × R$ 500.000 × (taxa de materialização)

> Valores ilustrativos para framework — calibrar com dados reais do SOC.
