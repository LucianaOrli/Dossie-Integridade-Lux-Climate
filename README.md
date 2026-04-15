 🛡️ Dossiê de Integridade / Edge Case Integrity Suite
  
 Desenvolvi a suíte 'Edge Case Integrity' para a Energy Or, focada em detectar violações de lógica arquitetural em sistemas de monitoramento térmico de alta complexidade (Lux-Climate).

Advanced Logic & Architectural Audit | Project: Lux-Climate.

Este módulo opera como uma camada de Inteligência de Qualidade apartada da automação funcional convencional. Enquanto a automação padrão valida a estabilidade do sistema, a suíte Energy Or é projetada para detectar Violações de Lógica Arquitetural e Inconsistências Conceituais em sistemas de missão crítica.

🎯 Objetivo Estratégico

A suíte foca na detecção proativa de desvios técnicos que comprometem a integridade operacional do software Lux-Climate, especificamente em cenários onde a implementação diverge dos modelos físicos e meteorológicos reais.

Este repositório é dedicado EXCLUSIVAMENTE à documentação de falhas de lógica, inconsistências físicas e vulnerabilidades de segurança identificadas no projeto Lux-Climate.

 ⚠️ Escopo da Gravidade - Falta de Integridade de Lógica - Falha Conceitual
 
Diferente das automações de fluxo padrão, esta suíte foca na **Validação de Regras de Negócio e Requisitos Críticas** que foram negligenciadas, resultando em 12 pontos de falha comprovados para exemplo (num total de 108 FALHAS REAIS no sistema).

Pilares da Auditoria / Análise Técnica (12 Cenários para exemplo de Alta Criticidade)
A suíte está estruturada para expor e documentar falhas nas seguintes frentes:

Integridade de Precisão Numérica: Detecção de truncamento de decimais e perda de precisão térmica (ex: 39.6°C vs 40°C), prevenindo a supressão de alertas críticos.

Consistência de Saída de Dados: Auditoria de sincronismo entre as camadas de visualização (UI) e exportação (PDF), assegurando que o reporte final seja fiel ao processamento em tela.

Validação de Limites Físicos (Boundary Conditions): Verificação de travas lógicas para parâmetros térmicos extremos (faixa 0°C - 99°C) e inconsistências de escala.

Estabilidade de Lógica de Interface: Monitoramento de corrupção de dados via componentes de controle (Manual Toggle), garantindo que a classificação de alertas (Cores/Status) permaneça íntegra sob interferência do usuário.

 🚩 Inconsistências Detectadas (Resumo)
1.  **Lógica Térmica:** Aceitação de temperaturas impossíveis (0°C e 99°C).
2.  **Conformidade de Dados:** Divergência entre dados de tela (UI) e relatórios PDF.
3.  **Segurança de Sessão:** Vazamento de contexto entre usuários concorrentes.
4.  **UX & Interface:** Corrupção de cores (Toggle) e eixos de gráfico negativos.
5.  **Performance:** Latência de 5s em notificações de emergência.

 Diferencial Técnico: Automação de Defeitos é o oposto do "Caminho Feliz", estes scripts são calibrados para identificar "Logic Mismatches". Se um teste nesta pasta falha (Red Status), ele não indica erro no script de automação, mas sim uma Falha de Consistência na Arquitetura e no Desenvolvimento  do Software analisado.
 "A qualidade não é apenas garantir que o código rode, mas assegurar que a lógica que o sustenta seja fiel à realidade e à segurança da operação." — Energy Or um produto Lux by Or 💎 de Luciana Orli.

 📊 Relatório de Evidências
 
Os resultados detalhados estão consolidados no relatório HTML autogerado:
`reports/dossie_evidencias_lux_climate.html`

 🛠️ Execução Técnica
Bash
pytest test_logic_integrity.py --html=reports/dossie_evidencias_lux_climate.html --self-contained-html


🚀 O relatório com as 12 falhas críticas pode ser visualizado aqui:
* [Visualizar Relatório de Integridade (HTML)](./reports/dossie_evidencias_lux_climate.html)

 **Nota:** Para visualizar o arquivo formatado diretamente no navegador, baixe o arquivo ou utilize um renderizador de HTML do GitHub.
