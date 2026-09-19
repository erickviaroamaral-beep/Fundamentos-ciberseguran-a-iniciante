# A06 — Insecure Design

## Objetivo

Compreender o que é Insecure Design (Design Inseguro), como falhas de segurança podem surgir ainda na etapa de planejamento de um sistema e por que algumas vulnerabilidades não podem ser corrigidas apenas alterando o código.

---

## O que é Insecure Design?

**Insecure Design** ocorre quando uma aplicação ou sistema possui falhas de segurança relacionadas à própria arquitetura, aos requisitos ou à lógica definida durante o projeto.

Nesse caso, o problema pode existir antes mesmo da implementação do código.

Uma aplicação pode ter um código aparentemente bem escrito e ainda assim possuir uma falha de segurança porque determinada regra de segurança nunca foi planejada.

De forma simplificada:

```text
Requisitos
    ↓
Arquitetura e Design
    ↓
Implementação
    ↓
Aplicação
