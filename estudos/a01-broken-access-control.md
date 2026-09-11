# A01 - Broken Access Control

## Objetivo do estudo

Compreender o conceito de Broken Access Control (Controle de Acesso Quebrado), identificando como falhas de autorização podem permitir que usuários acessem recursos ou executem ações que não deveriam estar disponíveis para eles.

## Como o tema foi estudado

A categoria A01 foi estudada utilizando o NotebookLM como ferramenta de apoio, com base nas fontes relacionadas ao OWASP Top 10:2025 disponíveis no projeto.

O conteúdo foi apresentado de forma didática, com exemplos práticos, comparação com conceitos semelhantes e perguntas de compreensão.

Durante a revisão, foi dada atenção especial à diferença entre autenticação e autorização e à importância de realizar o controle de acesso no lado do servidor.

## O que é Broken Access Control?

Broken Access Control ocorre quando uma aplicação não aplica corretamente as regras que determinam quais recursos ou ações cada usuário pode acessar.

Em outras palavras, o sistema pode permitir que um usuário realize uma ação que deveria estar restrita a outro usuário ou a um perfil com mais privilégios.

O problema está relacionado principalmente à **autorização**.

### Autenticação x autorização

É importante diferenciar os dois conceitos:

- **Autenticação:** verifica quem é o usuário.
- **Autorização:** determina o que esse usuário pode acessar ou fazer.

Um usuário pode estar corretamente autenticado e, mesmo assim, conseguir acessar um recurso para o qual não possui autorização.

## Exemplo simples

Imagine um sistema que possui:

```text
Usuário comum
      ↓
Acessa sua própria conta
