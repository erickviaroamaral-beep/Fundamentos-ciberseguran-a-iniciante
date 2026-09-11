# A02 - Security Misconfiguration

## Objetivo do estudo

Compreender o conceito de Security Misconfiguration (Configuração Incorreta de Segurança), identificando configurações inseguras que podem aumentar a exposição de sistemas, aplicações e informações.

## Como o tema foi estudado

A categoria A02 foi estudada utilizando o NotebookLM como ferramenta de apoio, com base nas fontes relacionadas ao OWASP Top 10:2025 disponíveis no projeto.

O conteúdo foi apresentado de forma didática, com exemplos práticos, formas de prevenção e comparação com outras categorias que podem causar confusão.

Durante a revisão, foi dada atenção especial aos riscos relacionados a configurações padrão, recursos desnecessários, mensagens de erro detalhadas e diferenças entre ambientes.

## O que é Security Misconfiguration?

Security Misconfiguration ocorre quando um sistema, aplicação ou ambiente possui configurações de segurança inadequadas, inseguras ou incompletas.

O problema pode acontecer em diferentes partes de um ambiente, incluindo:

- Aplicações;
- Servidores;
- Bancos de dados;
- Sistemas operacionais;
- Serviços;
- Componentes de infraestrutura.

Uma aplicação pode possuir um código aparentemente seguro e ainda assim apresentar riscos caso sua configuração de segurança esteja inadequada.

## Exemplos de configurações inseguras

Entre os exemplos estudados estão:

- Credenciais padrão que não foram alteradas;
- Recursos ou serviços desnecessários habilitados;
- Funcionalidades de segurança desativadas;
- Mensagens de erro excessivamente detalhadas;
- Configurações diferentes entre ambientes;
- Diretórios ou arquivos expostos sem necessidade;
- Aplicações de exemplo ou funcionalidades desnecessárias disponíveis em produção.

## Credenciais padrão

Sistemas e aplicações podem possuir credenciais padrão fornecidas pelo fabricante ou pelo próprio software.

Se essas credenciais não forem alteradas, um atacante pode tentar utilizá-las para obter acesso.

Por exemplo:

```text
Sistema instalado
      ↓
Usuário e senha padrão permanecem ativos
      ↓
Atacante conhece as credenciais
      ↓
Tenta acessar o sistema
