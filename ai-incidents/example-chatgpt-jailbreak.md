# Example — ChatGPT Jailbreak → Malware Distribution

> Incidente de referência do curso (Week 8 assignment). Ilustra como jailbreaks em LLMs podem ser encadeados a distribuição de malware.

## Summary

Usuários exploraram jailbreaks em ChatGPT para obter instruções de criação de malware. O modelo, sem guardrails adequados, forneceu código malicioso reutilizável.

## MITRE ATLAS mapping

| Technique | Description |
|-----------|-------------|
| AML.T0051 | LLM Prompt Injection |
| AML.T0043 | Craft Adversarial Data |
| AML.T0048 | Exfiltration via LLM Output |

## OWASP LLM Top 10

- **LLM01** — Prompt Injection
- **LLM02** — Insecure Output Handling
- **LLM06** — Sensitive Information Disclosure

## FAIR decomposition

| Factor | Estimate |
|--------|----------|
| Threat Event Frequency (TEF) | Alta — jailbreaks publicados semanalmente |
| Vulnerability (Vuln) | Alta — ausência de output filtering |
| Loss Magnitude (LM) | Média — reputacional + possível dano a usuários |

**Expected Loss** ≈ TEF × Vuln × LM

## Mitigations

1. Output filtering e classificação de conteúdo
2. Red teaming contínuo com prompts adversariais
3. Rate limiting e monitoramento de padrões de abuso
4. Human-in-the-loop para outputs de alto risco
