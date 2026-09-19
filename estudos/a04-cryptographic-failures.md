# A04 — Cryptographic Failures

## Objetivo

Compreender o que são falhas criptográficas, por que elas podem comprometer a confidencialidade e a proteção dos dados e quais práticas ajudam a evitar esse tipo de vulnerabilidade.

---

## O que são Cryptographic Failures?

Cryptographic Failures são falhas relacionadas ao uso inadequado, fraco ou inexistente de mecanismos criptográficos para proteger informações.

Essas falhas podem ocorrer quando:

- dados sensíveis não são protegidos adequadamente;
- algoritmos criptográficos fracos ou desatualizados são utilizados;
- informações são transmitidas sem proteção adequada;
- senhas são armazenadas de maneira insegura;
- chaves criptográficas são mal protegidas;
- mecanismos de criptografia são utilizados de forma incorreta.

O problema não está apenas em "não usar criptografia". Uma implementação incorreta ou inadequada também pode comprometer a segurança.

---

## O que a criptografia protege?

A criptografia pode ajudar a proteger principalmente a **confidencialidade** das informações.

Por exemplo:

- dados pessoais;
- senhas;
- informações financeiras;
- documentos;
- informações de autenticação;
- dados transmitidos entre sistemas.

Entretanto, é importante entender que criptografia, sozinha, não garante todos os aspectos da segurança.

A segurança da informação costuma considerar três propriedades principais:

### Confidencialidade

Garante que somente pessoas ou sistemas autorizados tenham acesso à informação.

### Integridade

Busca garantir que os dados não sejam alterados de maneira indevida.

### Disponibilidade

Busca garantir que sistemas e informações estejam disponíveis quando necessários.

---

## Dados em trânsito e dados em repouso

Os dados podem precisar de proteção em diferentes situações.

### Dados em trânsito

São informações que estão sendo transmitidas entre sistemas.

Exemplos:

- navegador → servidor;
- aplicativo → API;
- computador → serviço online.

Uma conexão protegida por TLS ajuda a proteger os dados durante a transmissão.

### Dados em repouso

São informações armazenadas em algum local.

Exemplos:

- banco de dados;
- arquivos;
- discos;
- backups;
- servidores.

Esses dados também podem precisar de mecanismos de proteção adequados.

---

## Criptografia não é a mesma coisa que hashing

Esses conceitos possuem objetivos diferentes.

### Criptografia

A criptografia permite transformar uma informação em um formato protegido e, utilizando a chave apropriada, recuperar a informação original.

De forma simplificada:

```text
Texto original
      ↓
Criptografia
      ↓
Dados protegidos
      ↓
Descriptografia
      ↓
Texto original
