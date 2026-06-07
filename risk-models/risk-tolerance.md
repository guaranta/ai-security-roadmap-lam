# Risk Tolerance Strategies

## Apetite por stakeholder

| Stakeholder | Tolerância | Exemplo LAM |
|-------------|------------|-------------|
| CISO | Baixa para ações SOAR autônomas | Exige sandbox + revisão humana |
| DPO | Zero para decisões sem trilha LGPD | Compliance Score obrigatório |
| SOC | Média para FPR se MTTD baixo | Trade-off documentado |

## Matriz de decisão

| Risco esperado | Estratégia |
|----------------|------------|
| < tolerância | Aceitar + monitorar |
| ≈ tolerância | Reduzir (guardrails) |
| > tolerância | Evitar (desabilitar playbook) ou transferir (seguro) |
