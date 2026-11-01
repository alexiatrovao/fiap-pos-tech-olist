# Prompts dos agentes OLI

Esta pasta concentra os prompts de sistema dos especialistas usados pelo orquestrador LangGraph. O carregamento ocorre em `app/agents.py` por meio da constante `PROMPT_DIR`, quando `APP_MODE=openai`.

| Arquivo | Especialista | Responsabilidade |
| --- | --- | --- |
| `01_OLI_Logistics_Copilot.md` | OLI Logistics Copilot | Atrasos, prazos de entrega e indicadores logísticos |
| `02_OLI_Voice_of_Customer.md` | OLI Voice of Customer | Avaliações, insatisfação e experiência do cliente |
| `03_OLI_Customer_Service_Engagement.md` | OLI Customer Service & Engagement | Recuperação, segmentação histórica e reengajamento analítico |

Cada prompt define identidade, fontes autorizadas, metodologia e restrições. Ao final, contém o **Protocolo de investigação estruturada**, composto pelas etapas: Delimitar, Investigar, Comparar, Interpretar, Decidir e Verificar.

As saídas são verificadas conforme `config/schema_saida.json`. As evidências quantitativas e seus identificadores são produzidos por ferramentas governadas, não criados pelo modelo. O modelo não tem autorização para realizar contatos externos nem executar operações de alteração em bases de clientes.

No modo `offline`, os arquivos permanecem como documentação dos papéis dos especialistas; a execução dos agentes utiliza o mesmo grafo de orquestração com análise determinística.
