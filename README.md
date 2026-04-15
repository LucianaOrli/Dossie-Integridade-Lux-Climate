# 🛡️ Dossiê de Integridade: Lux-Climate (Energy Or)

Este repositório é dedicado EXCLUSIVAMENTE à documentação de falhas de lógica, inconsistências físicas e vulnerabilidades de segurança identificadas no projeto Lux-Climate.

## ⚠️ Escopo da Gravidade
Diferente das automações de fluxo padrão, esta suíte foca na **Validação de Regras de Negócio Críticas** que foram negligenciadas, resultando em 12 pontos de falha comprovados.

## 🚩 Inconsistências Detectadas (Resumo)
1.  **Lógica Térmica:** Aceitação de temperaturas impossíveis (0°C e 99°C).
2.  **Conformidade de Dados:** Divergência entre dados de tela (UI) e relatórios PDF.
3.  **Segurança de Sessão:** Vazamento de contexto entre usuários concorrentes.
4.  **UX & Interface:** Corrupção de cores (Toggle) e eixos de gráfico negativos.
5.  **Performance:** Latência de 5s em notificações de emergência.

## 📊 Relatório de Evidências
Os resultados detalhados estão consolidados no relatório HTML autogerado:
`reports/dossie_evidencias_lux_climate.html`

## 🛠️ Execução Técnica
```bash
pytest test_logic_integrity.py --html=reports/dossie_evidencias_lux_climate.html --self-contained-html
