# AI Incident Database

Estrutura para catalogar e analisar incidentes de IA, alinhada a **MITRE ATLAS** e **OWASP LLM Top 10**.

## Arquivos

| Arquivo | Conteúdo |
|---------|----------|
| [incident-template.md](incident-template.md) | Template para novos incidentes |
| [example-chatgpt-jailbreak.md](example-chatgpt-jailbreak.md) | Exemplo: jailbreak → malware |
| [atlas-mapping.md](atlas-mapping.md) | Mapeamento MITRE ATLAS |
| [owasp-llm-crosswalk.md](owasp-llm-crosswalk.md) | Cruzamento OWASP LLM Top 10 |

## Campos obrigatórios

1. **ID e data** do incidente
2. **Sistema afetado** (LLM, RAG, agente, pipeline)
3. **Vetor de ataque** (prompt injection, data poisoning, etc.)
4. **Impacto** (confidencialidade, integridade, disponibilidade)
5. **Mitigações aplicadas** e lições aprendidas
6. **Referência ATLAS/OWASP**
