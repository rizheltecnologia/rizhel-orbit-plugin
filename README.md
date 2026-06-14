# Rizhel Orbit — Plugin para Claude Code

Gerencie projetos e tarefas do [Rizhel Orbit](https://orbit.rizhel.com.br) diretamente no Claude Code. Crie tarefas, liste projetos, atualize status e conclua itens sem sair do terminal.

## Instalação

```bash
claude plugin marketplace add rizheltecnologia/rizhel-orbit-plugin
claude plugin install rizhel-orbit-plugin@rizhel-orbit
```

Ao instalar pela primeira vez, o Claude Code abrirá o navegador para autenticar com sua conta Rizhel Orbit. Selecione o workspace que deseja conectar e autorize o acesso.

## Ferramentas disponíveis

| Ferramenta | O que faz |
|---|---|
| `listar_projetos` | Lista todos os projetos do workspace com seções e statuses |
| `listar_tarefas` | Lista tarefas de um projeto específico |
| `criar_tarefa` | Cria uma nova tarefa em um projeto |
| `atualizar_tarefa` | Atualiza título, descrição, prioridade, prazo ou status |
| `concluir_tarefa` | Marca uma tarefa como concluída |

## Exemplos de uso

```
# No Claude Code:
"Liste meus projetos do Orbit"
"Crie uma tarefa 'Revisar PR #42' no projeto Backend com prioridade alta"
"Marque a tarefa abc-123 como concluída"
"Quais tarefas estão em aberto no projeto Frontend?"
```

## Autenticação

Este plugin usa **OAuth 2.0**. Ao adicionar o plugin, o Claude Code inicia o fluxo de autorização automaticamente — você faz login na sua conta Rizhel Orbit e autoriza o acesso ao workspace. Nenhuma chave de API é necessária.

O token de acesso é armazenado com segurança pelo Claude Code e renovado automaticamente.

## Requisitos

- Conta ativa no [Rizhel Orbit](https://orbit.rizhel.com.br)
- Claude Code versão 1.0.0 ou superior

## Suporte

- Site: [rizhel.com.br](https://rizhel.com.br)
- Issues: [github.com/rizhel/rizhel-orbit-plugin/issues](https://github.com/rizhel/rizhel-orbit-plugin/issues)
