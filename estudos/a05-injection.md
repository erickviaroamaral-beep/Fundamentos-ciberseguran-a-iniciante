# A05 — Injection

## Objetivo

Compreender o que são ataques de injeção, como eles podem acontecer e quais práticas ajudam a reduzir esse tipo de vulnerabilidade.

---

## O que é Injection?

**Injection (Injeção)** acontece quando uma aplicação recebe dados de uma fonte externa e esses dados acabam sendo interpretados como parte de um comando ou consulta.

Em vez de o sistema tratar a entrada apenas como informação, ela pode acabar sendo interpretada como uma instrução.

De forma simplificada:

```text
Entrada do usuário
        ↓
Aplicação
        ↓
Interpretação inadequada
        ↓
Comando ou consulta manipulada
