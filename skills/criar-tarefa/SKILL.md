---
name: criar-tarefa
description: Cria uma ou mais tarefas no Rizhel Orbit a partir de uma descrição em linguagem natural. Use quando o usuário pedir para criar tarefa, adicionar item, registrar atividade, ou qualquer variação similar.
---

# Criar tarefa no Rizhel Orbit

Quando o usuário pedir para criar uma tarefa:

1. **Se não souber o projeto**, use `listar_projetos` para mostrar as opções e peça confirmação.
2. **Extraia do pedido**: título, descrição (opcional), prioridade (URGENTE/ALTA/MEDIA/BAIXA), data de entrega (ISO 8601).
3. **Se não houver seção ou status informados**, crie sem eles — o Orbit aplica os padrões.
4. Use `criar_tarefa` com os campos extraídos.
5. Confirme ao usuário com o título e link implícito ao workspace.

## Mapeamento de linguagem natural → prioridade

| O usuário diz | Prioridade |
|---|---|
| urgente, para ontem, crítico, bloqueando | URGENTE |
| importante, prioritário, logo | ALTA |
| normal, padrão (omissão) | MEDIA |
| quando der, sem pressa | BAIXA |

## Exemplo

Usuário: "Cria uma tarefa pra revisar o relatório financeiro até sexta"

→ `criar_tarefa({ projetoId: "<id>", titulo: "Revisar relatório financeiro", dataEntrega: "2026-06-20T23:59:00-03:00" })`
