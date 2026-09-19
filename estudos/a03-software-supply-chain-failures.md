# A03 - Software Supply Chain Failures

## Objetivo do estudo

Compreender os riscos relacionados à cadeia de suprimentos de software, incluindo dependências externas, fornecedores, bibliotecas, repositórios e processos utilizados para desenvolver, distribuir e atualizar sistemas.

## Como o tema foi estudado

A categoria A03 foi estudada utilizando o NotebookLM como ferramenta de apoio, com base nas fontes relacionadas ao OWASP Top 10:2025 disponíveis no projeto.

O estudo buscou compreender como componentes externos podem introduzir riscos mesmo quando o código desenvolvido pela própria equipe não apresenta uma vulnerabilidade conhecida.

Também foram analisadas as diferenças entre vulnerabilidades no código próprio, vulnerabilidades em dependências e comprometimentos na cadeia de fornecimento.

## O que é uma cadeia de suprimentos de software?

A cadeia de suprimentos de software é formada pelo conjunto de pessoas, processos, ferramentas, componentes e infraestrutura utilizados para criar, testar, distribuir e atualizar software.

Uma aplicação moderna normalmente não é composta apenas pelo código escrito pela própria equipe.

Ela pode utilizar:

- Bibliotecas externas;
- Frameworks;
- Pacotes de terceiros;
- Dependências diretas;
- Dependências transitivas;
- Repositórios;
- Ferramentas de desenvolvimento;
- Sistemas de integração e entrega contínua;
- Fornecedores de software.

Isso significa que um problema em um componente externo pode afetar uma aplicação que, por si só, não possuía aquela vulnerabilidade em seu próprio código.

## Dependências de software

Uma dependência é um componente externo utilizado por uma aplicação.

Por exemplo:

```text
Aplicação
   ↓
Biblioteca A
   ↓
Biblioteca B
