# Sistem_runner

## Descrição

O Sistema Runner é um projeto acadêmico da disciplina de Implementação e Integração de Software (2026-01). Seu objetivo é facilitar a execução de aplicações Java por meio de uma interface de linha de comando (CLI), abstraindo detalhes técnicos como configuração do ambiente, execução de arquivos `.jar` e gerenciamento de componentes auxiliares.

O sistema tem como foco principal permitir que o usuário utilize o assinador e o simulador de forma simples, sem precisar conhecer comandos Java ou detalhes internos da infraestrutura.

## Objetivo geral

Facilitar o acesso à funcionalidade de execução de aplicações Java via linha de comandos.

## Componentes do sistema

- **CLI**  
  Interface principal usada pelo usuário no terminal.

- **Assinador**  
  Aplicação Java responsável por simular operações de criação e validação de assinatura digital, com foco em validação de parâmetros.

- **Simulador**  
  Componente externo que poderá ser iniciado, parado e monitorado pelo CLI.

- **Gerenciamento de ambiente**  
  Parte responsável por verificar ou provisionar o JDK necessário para execução das aplicações Java.

## Fluxos principais

### Criação de assinatura
Usuário → CLI → Assinador → CLI → Usuário

### Validação de assinatura
Usuário → CLI → Assinador → CLI → Usuário

### Gerenciamento do simulador
Usuário → CLI → Simulador → CLI → Usuário

## Escopo inicial do projeto

Nesta fase inicial, o foco será construir uma primeira versão funcional com o menor recorte possível, priorizando entendimento da arquitetura e validação do fluxo principal.

## MVP da primeira iteração

A primeira iteração terá como objetivo:

- criar um CLI básico
- aceitar um comando de criação de assinatura
- invocar localmente a aplicação Java do assinador
- exibir o resultado da operação ao usuário

## Fora do MVP inicial

Os itens abaixo não farão parte da primeira iteração:

- comunicação via HTTP
- gerenciamento do simulador
- download automático de JDK
- distribuição multiplataforma
- pipeline de CI/CD
- assinatura de artefatos com Cosign

## Estrutura inicial do repositório

```text
sistema-runner/
├─ docs/
├─ cli/
├─ assinador/
├─ tests/
└─ README.md
