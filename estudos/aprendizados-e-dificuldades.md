# Aprendizados e Dificuldades

## Sobre este arquivo

Este documento registra os principais aprendizados, dificuldades e descobertas realizadas durante o estudo dos fundamentos de cibersegurança.

O objetivo é documentar não apenas os conceitos estudados, mas também o processo de aprendizagem e a utilização da Inteligência Artificial como ferramenta de apoio.

---

# Principais aprendizados

Durante o projeto, pude estudar diferentes conceitos fundamentais de cibersegurança e compreender que segurança não depende de apenas uma ferramenta ou técnica.

Entre os principais aprendizados estão:

- importância da proteção de informações;
- diferença entre autenticação e autorização;
- importância de senhas fortes e exclusivas;
- funcionamento e riscos do phishing;
- importância da autenticação multifator;
- riscos relacionados a componentes de terceiros;
- importância da criptografia e da proteção adequada de dados;
- riscos de Injection;
- importância de considerar segurança durante o design de sistemas;
- proteção da integridade de software e dados;
- importância de logs e alertas;
- necessidade de tratar situações excepcionais de maneira segura.

---

# Aprendizados sobre o OWASP Top 10:2025

O estudo do OWASP Top 10:2025 ajudou a compreender diferentes categorias de riscos relacionados a aplicações e sistemas.

## A01 — Broken Access Control

Aprendi que esconder uma função ou botão na interface não é suficiente para proteger um recurso.

O sistema precisa verificar no servidor se o usuário realmente possui autorização para executar determinada ação.

Também compreendi a diferença entre autenticação e autorização.

---

## A02 — Security Misconfiguration

Aprendi que configurações inadequadas podem criar vulnerabilidades mesmo quando a aplicação possui mecanismos de segurança.

Entre os exemplos estudados estão:

- credenciais padrão;
- recursos desnecessários;
- mensagens de erro detalhadas;
- configurações inadequadas;
- falta de hardening.

---

## A03 — Software Supply Chain Failures

Aprendi que uma aplicação também pode depender de componentes externos, bibliotecas, fornecedores e outras partes da cadeia de desenvolvimento.

Uma vulnerabilidade ou comprometimento em um componente externo pode afetar sistemas que dependem dele.

Também compreendi melhor os conceitos de dependências diretas e transitivas.

---

## A04 — Cryptographic Failures

Aprendi que utilizar criptografia não significa automaticamente que uma informação esteja protegida.

É necessário utilizar mecanismos adequados, proteger chaves e utilizar técnicas apropriadas para cada situação.

Também aprendi a diferenciar:

- criptografia;
- hashing;
- codificação.

Um exemplo importante foi compreender que Base64 é codificação e não criptografia.

---

## A05 — Injection

Aprendi que entradas fornecidas por usuários podem representar riscos quando são incorporadas diretamente a comandos ou consultas.

Um dos exemplos estudados foi SQL Injection.

Também compreendi a importância de:

- consultas parametrizadas;
- validação de entrada;
- separação entre dados e comandos;
- defesa em profundidade.

---

## A06 — Insecure Design

Aprendi que uma aplicação pode possuir problemas de segurança mesmo quando seu código funciona conforme planejado.

Isso pode acontecer quando uma regra de segurança não foi considerada durante o projeto.

O estudo também mostrou a importância de:

- Threat Modeling;
- Secure by Design;
- requisitos de segurança;
- regras de negócio;
- limites e controles.

---

## A07 — Authentication Failures

Aprendi que autenticação não se resume ao momento do login.

É necessário considerar também:

- senhas;
- MFA;
- recuperação de contas;
- sessões;
- tentativas automatizadas;
- credenciais comprometidas.

Também compreendi melhor ataques como Brute Force e Credential Stuffing.

---

## A08 — Software or Data Integrity Failures

Aprendi que é importante verificar a origem e a integridade de softwares e dados antes de confiar neles.

Também estudei:

- assinaturas digitais;
- hashes;
- atualizações;
- firmware;
- componentes externos;
- serialização e desserialização.

Um dos aprendizados importantes foi entender que Base64 não fornece integridade nem autenticidade.

---

## A09 — Security Logging and Alerting Failures

Aprendi que registrar eventos de segurança é importante para detectar e investigar incidentes.

Também compreendi a diferença entre:

- logging;
- alerting;
- falso positivo;
- falso negativo;
- Alert Fatigue.

Percebi que registrar somente eventos bem-sucedidos pode dificultar a identificação de determinados comportamentos suspeitos.

---

## A10 — Mishandling of Exceptional Conditions

Aprendi que uma aplicação segura precisa considerar também situações em que algo dá errado.

Entre os conceitos estudados estão:

- condições excepcionais;
- tratamento de erros;
- fail open;
- fail closed;
- rollback;
- estados inconsistentes;
- esgotamento de recursos;
- rate limiting.

Também compreendi que mensagens de erro podem revelar informações técnicas que não deveriam ser apresentadas ao usuário.

---

# Dificuldades encontradas

Durante o processo de aprendizagem, algumas dificuldades apareceram.

## Confusão entre conceitos semelhantes

No início, alguns conceitos de segurança pareciam muito próximos.

Foi necessário diferenciar, por exemplo:

```text
Autenticação ≠ Autorização

Criptografia ≠ Hashing ≠ Codificação

Logging ≠ Alerting

A03 ≠ A08

A02 ≠ A10
