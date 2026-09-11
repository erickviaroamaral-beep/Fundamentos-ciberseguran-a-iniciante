# Autenticação e Senhas

## Objetivo do estudo

Compreender os conceitos de autenticação, autorização e gerenciamento de senhas, identificando falhas comuns e boas práticas para proteger contas e sistemas.

## Como o tema foi estudado

O tema foi estudado utilizando o NotebookLM como ferramenta de apoio, com base nas fontes selecionadas para o projeto.

Foi solicitado ao NotebookLM que explicasse os conceitos de autenticação, autorização e gerenciamento de senhas de forma didática e apresentasse perguntas de compreensão sem fornecer as respostas.

Após responder às perguntas, os conceitos foram revisados para identificar quais pontos foram compreendidos corretamente e quais precisavam de maior atenção.

## Principais conceitos estudados

### Autenticação

Autenticação é o processo utilizado para verificar a identidade de uma pessoa ou entidade.

Em termos simples, a autenticação busca responder:

> "Quem é você?"

Um exemplo é o login em uma conta utilizando nome de usuário e senha.

### Autorização

Autorização determina quais recursos ou ações uma pessoa autenticada pode acessar ou realizar.

Em termos simples:

> "O que você pode acessar ou fazer?"

Uma pessoa pode estar autenticada em um sistema, mas ainda assim não possuir autorização para acessar determinadas informações ou executar determinadas ações.

### Diferença entre autenticação e autorização

| Conceito | Pergunta principal | Exemplo |
|---|---|---|
| Autenticação | Quem é você? | Fazer login com usuário e senha |
| Autorização | O que você pode fazer? | Permitir que somente administradores alterem configurações |

A autenticação vem antes da autorização: primeiro o sistema verifica a identidade e depois determina quais permissões devem ser concedidas.

## Falhas relacionadas à autenticação

Entre os problemas estudados estão:

- Senhas fracas;
- Credenciais padrão que não foram alteradas;
- Ausência ou implementação inadequada de MFA;
- Falhas no gerenciamento de sessões;
- Recuperação de contas insegura;
- Proteção inadequada das credenciais;
- Possibilidade de ataques automatizados contra mecanismos de login.

Essas falhas podem permitir que um atacante obtenha acesso indevido a contas ou sistemas.

## Ataque de força bruta

Um ataque de força bruta consiste em tentar diversas combinações de credenciais até encontrar uma combinação válida.

Quanto mais fraca for uma senha e quanto menos proteção existir no mecanismo de autenticação, maior pode ser o risco desse tipo de ataque.

## Credential Stuffing

Credential stuffing ocorre quando credenciais obtidas de um vazamento são utilizadas para tentar acessar outras contas.

Esse ataque se aproveita principalmente da reutilização de senhas.

Por exemplo:

```text
Senha vazada em um serviço
        ↓
Atacante utiliza a mesma combinação
        ↓
Testa a combinação em outros serviços
        ↓
Possível acesso à conta
