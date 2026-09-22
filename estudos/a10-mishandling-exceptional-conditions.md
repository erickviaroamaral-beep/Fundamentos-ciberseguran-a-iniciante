# A10 — Mishandling of Exceptional Conditions

## Objetivo

Compreender o que são condições excepcionais, o que significa tratá-las de maneira inadequada e como falhas no tratamento de erros e situações inesperadas podem afetar a segurança de uma aplicação.

---

## O que são condições excepcionais?

Condições excepcionais são situações incomuns, inesperadas ou anormais que podem ocorrer durante a execução de um sistema.

Exemplos:

- dados inesperados;
- falha de conexão;
- falta de memória;
- falta de recursos;
- erro no banco de dados;
- permissões insuficientes;
- parâmetros inesperados;
- falhas em serviços externos;
- operações que não conseguem ser concluídas.

Essas situações precisam ser consideradas durante o desenvolvimento do sistema.

---

## O que significa Mishandling of Exceptional Conditions?

**Mishandling of Exceptional Conditions** significa tratar de maneira inadequada situações excepcionais ou inesperadas.

Quando uma aplicação não consegue lidar corretamente com uma condição excepcional, ela pode:

- apresentar comportamento inesperado;
- entrar em um estado inconsistente;
- revelar informações internas;
- interromper operações de maneira incorreta;
- permitir comportamentos que não deveriam ocorrer;
- consumir recursos excessivamente;
- falhar de maneira insegura.

---

## Condição esperada x condição excepcional

É importante diferenciar situações normais de situações excepcionais.

### Condição esperada

É uma situação que faz parte do funcionamento normal da aplicação.

Exemplo:

```text
Usuário informa senha incorreta
        ↓
Sistema informa:
"Usuário ou senha inválidos."
