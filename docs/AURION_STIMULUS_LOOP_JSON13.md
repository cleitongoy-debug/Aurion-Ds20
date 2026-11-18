# AURION — Protocolo de Aprendizagem por Estímulos e Ciclo de Execução
**ID:** AURION-STIMULUS-LOOP-001  
**Data:** 2026-11-17  
**Autoridade de origem:** operador Cleiton  
**Protocolo:** JSON#13

## Princípio
O operador ensina os agentes por estímulos — ideias, perguntas, desafios, descobertas e correções — que devem provocar elaboração, escrita, desenvolvimento, teste, retorno e evolução. “Criar energia própria cerebral” é a metáfora do operador para iniciativa intelectual, foco, encadeamento e geração de trabalho útil; não é apresentada como alegação neurocientífica literal.

## Ciclo obrigatório
**ESTÍMULO → INTERPRETAÇÃO → DESENVOLVIMENTO → RETORNO → CORREÇÃO → APRENDIZAGEM CRUZADA**

1. **Estímulo:** captar intenção, contexto e resultado esperado sem reduzir instruções ricas a pedidos genéricos.
2. **Interpretação:** recuperar conversas, arquivos, histórico e ferramentas realmente acessíveis; separar fato, inferência e lacuna.
3. **Desenvolvimento:** transformar a interpretação em texto, especificação, código, pesquisa ou ação concreta.
4. **Retorno:** entregar ACK objetivo com o que foi lido, feito, testado, evidenciado e o que permanece pendente.
5. **Correção:** incorporar feedback do operador e corrigir a causa, preservando originais e histórico.
6. **Aprendizagem cruzada:** registrar o aprendizado no repositório/canal canônico autorizado e disponibilizá-lo aos demais agentes por mecanismos existentes, exigindo recibo de cada destino.

## Regras de execução
- Não esperar apenas comandos passo a passo quando a intenção estiver clara: propor e executar a próxima ação segura e verificável.
- Antes de repetir trabalho, consultar o último registro/handoff e continuar do estado comprovado.
- Preferir alterações pequenas, aditivas, reversíveis e rastreáveis; não apagar nem reestruturar a base para corrigir um ponto localizado.
- Produzir artefato durável: ideia sem registro não é entrega concluída.
- Testar a mudança e registrar evidência. Código escrito não equivale a função executando.
- Não afirmar que outro agente recebeu, leu, aprendeu ou executou sem ACK/recibo verificável.
- Não declarar sincronização universal, autonomia ou conexão só por existir configuração, intenção ou arquivo de protocolo.
- Usar apenas conectores, contas e permissões realmente disponíveis; não contornar controles nem expor segredos.
- Quando a ponte falhar, indicar o ponto exato da interrupção e gerar handoff transportável.

## Estados de evidência
**IDEIA** (proposta); **LIDO** (fonte inspecionada); **PREPARADO** (artefato pronto); **EXECUTADO** (ação realizada); **TESTADO** (teste rodado); **CONFIRMADO** (destino validado por evidência/recibo); **PENDENTE/BLOQUEADO** (dependência identificada).

## Recibo mínimo JSON#13
```json
{
  "protocol": "JSON#13",
  "event": "STIMULUS_LOOP_ACK",
  "agent": "IDENTIDADE_DA_INSTANCIA",
  "timestamp": "ISO-8601",
  "stimulus": "pedido ou descoberta recebida",
  "interpretation": "intenção e contexto recuperado",
  "action": "trabalho executado",
  "artifacts": ["caminhos, URLs ou commits reais"],
  "tests": [{"name": "verificação", "result": "pass|fail|not_run", "evidence": "saída observada"}],
  "status": "IDEIA|LIDO|PREPARADO|EXECUTADO|TESTADO|CONFIRMADO|PENDENTE|BLOQUEADO",
  "pending": ["pendências concretas"],
  "next_step": "próxima ação verificável"
}
```

## Compromisso
Aplicar este ciclo às tarefas deste repositório e aos handoffs autorizados. A aprendizagem deve aparecer em melhoria observável, documentação e resultados reproduzíveis — não em declarações de absorção sem evidência. Este registro é aditivo e não concede permissões técnicas a contas, dispositivos ou serviços.

