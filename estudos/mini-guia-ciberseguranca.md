# Mini-Guia de Cibersegurança para Iniciantes

## Introdução

A cibersegurança é o conjunto de práticas, processos e medidas utilizadas para proteger sistemas, aplicações, dispositivos, redes e informações contra ameaças digitais.

Para quem está começando a estudar a área, é importante compreender não apenas as ferramentas utilizadas, mas também os conceitos fundamentais, os tipos de ameaças e as formas de prevenção.

Este mini-guia reúne os principais conceitos estudados durante o projeto **Fundamentos de Cibersegurança para Iniciantes**.

---

## 1. Princípios básicos de segurança

Um dos conceitos fundamentais da cibersegurança é a proteção das informações.

Entre os principais objetivos de segurança estão:

- **Confidencialidade:** impedir que informações sejam acessadas por pessoas não autorizadas.
- **Integridade:** garantir que informações e sistemas não sejam alterados de forma indevida.
- **Disponibilidade:** garantir que sistemas e informações estejam disponíveis quando necessários.

Esses princípios ajudam a compreender diferentes tipos de riscos e medidas de proteção.

---

## 2. Phishing

Phishing é uma técnica de engenharia social utilizada para tentar enganar uma pessoa e fazê-la realizar alguma ação, como:

- clicar em um link;
- abrir um arquivo;
- fornecer informações;
- informar credenciais;
- realizar uma transferência ou pagamento.

Mensagens de phishing podem utilizar elementos como:

- urgência;
- medo;
- consequências negativas;
- falsa autoridade;
- confiança;
- imitação de pessoas ou organizações conhecidas.

### Como se proteger

Antes de clicar ou fornecer informações:

1. Verifique quem enviou a mensagem.
2. Observe o endereço do remetente.
3. Desconfie de mensagens que criam urgência excessiva.
4. Verifique cuidadosamente os links.
5. Evite fornecer credenciais por meio de links recebidos inesperadamente.
6. Confirme solicitações importantes por outro canal.

---

## 3. Autenticação e autorização

Embora estejam relacionadas, autenticação e autorização são conceitos diferentes.

### Autenticação

É o processo de verificar **quem é o usuário**.

Exemplos:

- senha;
- aplicativo autenticador;
- chave de segurança;
- biometria.

### Autorização

Determina **o que o usuário pode fazer** depois de sua identidade ser verificada.

Por exemplo:

Um usuário pode estar autenticado em um sistema, mas não possuir autorização para acessar informações administrativas.

---

## 4. Senhas e autenticação

Boas práticas relacionadas a senhas incluem:

- utilizar senhas fortes e difíceis de adivinhar;
- evitar reutilizar a mesma senha em diferentes serviços;
- utilizar um gerenciador de senhas quando apropriado;
- utilizar autenticação multifator;
- evitar senhas previsíveis ou baseadas em informações pessoais.

Também é importante compreender que alterações periódicas de senha, quando aplicadas sem necessidade, podem incentivar usuários a criar variações previsíveis de senhas.

---

# 5. OWASP Top 10:2025

O OWASP Top 10:2025 apresenta dez categorias de riscos importantes relacionados à segurança de aplicações.

Durante este projeto, todas as dez categorias foram estudadas.

---

## A01 - Broken Access Control

Refere-se a falhas na aplicação das regras que determinam quais recursos ou ações cada usuário pode acessar.

Um usuário autenticado não deve automaticamente possuir acesso a todos os recursos do sistema.

### Exemplo

Um usuário comum consegue acessar uma página administrativa apenas alterando uma informação na URL.

### Proteções

- aplicar autorização no servidor;
- negar acesso por padrão;
- verificar permissões em cada recurso sensível;
- evitar confiar apenas em controles existentes na interface.

---

## A02 - Security Misconfiguration

Está relacionada a configurações inseguras ou inadequadas em sistemas, servidores, aplicações e ambientes.

Exemplos:

- credenciais padrão;
- recursos desnecessários habilitados;
- mensagens de erro excessivamente detalhadas;
- configurações inseguras;
- ausência de mecanismos de segurança.

### Proteções

- aplicar configurações seguras;
- remover recursos desnecessários;
- alterar credenciais padrão;
- realizar hardening;
- revisar configurações regularmente;
- manter ambientes adequadamente configurados.

---

## A03 - Software Supply Chain Failures

Relaciona-se aos riscos presentes na cadeia de fornecimento de software.

Uma aplicação pode depender de:

- bibliotecas;
- pacotes;
- componentes externos;
- fornecedores;
- ferramentas de desenvolvimento;
- processos de atualização.

Um componente comprometido pode se tornar um caminho para atingir sistemas que dependem dele.

### Proteções

- conhecer as dependências utilizadas;
- acompanhar versões e vulnerabilidades;
- utilizar fontes confiáveis;
- proteger pipelines de desenvolvimento e distribuição;
- utilizar SBOM quando apropriado;
- verificar componentes e atualizações.

---

## A04 - Cryptographic Failures

Relaciona-se ao uso inadequado, fraco ou inexistente de mecanismos criptográficos quando eles são necessários.

Pode envolver:

- ausência de criptografia;
- algoritmos inadequados;
- armazenamento inseguro de informações;
- proteção inadequada de dados em trânsito ou em repouso.

### Conceitos importantes

**Criptografia** pode ser utilizada para proteger a confidencialidade dos dados.

**Hashing** é utilizado para produzir uma representação derivada dos dados e possui aplicações diferentes da criptografia.

Para armazenamento de senhas, devem ser utilizados mecanismos apropriados de proteção de senhas, incluindo técnicas como hashing adaptativo e uso de salt.

---

## A05 - Injection

Injection ocorre quando dados fornecidos pelo usuário são interpretados de forma indevida como parte de comandos ou consultas.

Um exemplo conhecido é a **SQL Injection**, na qual uma entrada manipulada pode alterar a lógica de uma consulta ao banco de dados.

### Proteções

- utilizar consultas parametrizadas;
- evitar a concatenação insegura de entradas em comandos;
- aplicar validação adequada;
- utilizar mecanismos seguros de acesso a dados.

A validação de entrada pode ajudar, mas não deve ser considerada a única proteção.

---

## A06 - Insecure Design

Relaciona-se a falhas de segurança presentes no próprio projeto ou arquitetura de um sistema.

Nesse caso, o problema pode existir antes mesmo da implementação do código.

### Exemplo

Um sistema permite que um usuário utilize repetidamente um cupom que deveria ser utilizado apenas uma vez porque essa regra de negócio nunca foi definida ou implementada corretamente.

### Proteções

- definir requisitos de segurança;
- realizar análise de ameaças;
- utilizar threat modeling;
- considerar cenários de abuso;
- projetar mecanismos de segurança antes da implementação.

---

## A07 - Authentication Failures

Relaciona-se a falhas nos mecanismos utilizados para autenticar usuários e gerenciar sessões.

Exemplos:

- senhas fracas;
- credenciais padrão;
- ausência de MFA;
- recuperação de conta insegura;
- gerenciamento inadequado de sessões;
- proteção inadequada contra ataques de autenticação.

### Ataques relacionados

- brute force;
- credential stuffing;
- reutilização de senhas;
- roubo de credenciais;
- phishing.

### Proteções

- utilizar MFA;
- proteger adequadamente as senhas;
- remover credenciais padrão;
- utilizar mecanismos contra tentativas abusivas;
- proteger sessões;
- evitar mensagens que permitam descobrir se uma conta existe.

---

## A08 - Software or Data Integrity Failures

Relaciona-se à falta de verificação adequada da integridade e autenticidade de software ou dados.

Um sistema pode apresentar riscos quando aceita software, atualizações ou dados sem verificar sua origem ou integridade.

### Exemplos

- atualização sem assinatura ou verificação adequada;
- utilização de componentes de origem desconhecida;
- dados manipulados sendo aceitos pelo sistema;
- desserialização insegura.

### Proteções

- verificar a origem dos componentes;
- utilizar mecanismos de assinatura e integridade;
- utilizar fontes confiáveis;
- proteger dados importantes;
- evitar confiar em dados externos sem validação adequada.

---

## A09 - Security Logging and Alerting Failures

Relaciona-se à ausência ou insuficiência de registros e alertas de segurança.

Sem logs adequados, pode ser difícil:

- identificar ataques;
- investigar incidentes;
- compreender o que aconteceu;
- detectar comportamentos suspeitos.

### Problemas comuns

- registrar apenas eventos de sucesso;
- não registrar tentativas de ataque;
- permitir alterações ou exclusões indevidas nos logs;
- gerar excesso de falsos positivos;
- não possuir alertas para eventos relevantes.

### Proteções

- registrar eventos importantes;
- proteger os registros;
- monitorar atividades suspeitas;
- configurar alertas;
- revisar os registros durante investigações.

---

## A10 - Mishandling of Exceptional Conditions

Relaciona-se ao tratamento inadequado de situações excepcionais ou inesperadas durante a execução de um sistema.

Exemplos:

- erros de banco de dados;
- falta de recursos;
- falhas de rede;
- parâmetros inesperados;
- problemas de permissões;
- falhas durante transações.

Um tratamento inadequado pode fazer o sistema:

- entrar em estado inconsistente;
- expor informações internas;
- falhar de forma insegura;
- permitir acesso indevido;
- sofrer indisponibilidade.

### Proteções

- tratar exceções adequadamente;
- utilizar fail closed quando apropriado;
- realizar rollback de operações quando necessário;
- evitar expor informações técnicas aos usuários;
- registrar detalhes internamente;
- testar situações excepcionais.

---

# 6. Boas práticas gerais

Algumas práticas podem ajudar a reduzir riscos no dia a dia:

### Para usuários

- utilizar senhas fortes;
- evitar reutilização de senhas;
- ativar MFA;
- manter sistemas atualizados;
- desconfiar de mensagens inesperadas;
- verificar links e remetentes;
- evitar instalar programas de fontes desconhecidas.

### Para aplicações e sistemas

- aplicar controle de acesso;
- proteger informações sensíveis;
- manter configurações seguras;
- controlar dependências;
- validar entradas;
- registrar eventos importantes;
- monitorar atividades suspeitas;
- tratar erros de forma segura;
- testar cenários inesperados.

---

# 7. Como pensar sobre segurança

Cibersegurança não depende apenas de uma ferramenta.

Uma abordagem de segurança envolve considerar:

1. **O que precisa ser protegido?**
2. **Quem deveria ter acesso?**
3. **Quais ameaças podem existir?**
4. **O que poderia acontecer se uma proteção falhar?**
5. **Como o sistema detectaria um problema?**
6. **Como o sistema responderia a um incidente?**
7. **Como evitar que o problema aconteça novamente?**

Esse tipo de raciocínio ajuda a desenvolver uma visão mais ampla sobre segurança.

---

# 8. O papel da inteligência artificial no aprendizado

Durante este projeto, ferramentas de inteligência artificial foram utilizadas como apoio ao aprendizado.

O NotebookLM foi utilizado para:

- organizar as fontes;
- explicar conceitos;
- criar perguntas;
- revisar conhecimentos;
- comparar informações;
- verificar a origem de determinadas afirmações.

A IA foi utilizada como **ferramenta de apoio**, enquanto as fontes foram utilizadas para validar as informações.

Uma prática importante aprendida durante o projeto foi verificar a origem de uma informação antes de tratá-la como uma recomendação ou requisito oficial.

---

# 9. Checklist básico de segurança

### Conta e autenticação

- [ ] Utilizo senhas fortes.
- [ ] Evito reutilizar senhas.
- [ ] Utilizo MFA quando disponível.
- [ ] Não compartilho minhas credenciais.

### Phishing

- [ ] Verifico o remetente.
- [ ] Analiso links antes de acessá-los.
- [ ] Desconfio de mensagens inesperadas.
- [ ] Não tomo decisões importantes apenas por pressão ou urgência.

### Sistemas

- [ ] Mantenho sistemas atualizados.
- [ ] Evito programas de fontes desconhecidas.
- [ ] Utilizo configurações seguras.
- [ ] Removo recursos desnecessários quando apropriado.

### Aplicações

- [ ] Controlo permissões e acessos.
- [ ] Protejo informações sensíveis.
- [ ] Valido entradas.
- [ ] Protejo dependências.
- [ ] Registro eventos importantes.
- [ ] Trato erros e exceções de forma segura.

---

# Conclusão

O estudo dos fundamentos de cibersegurança e do OWASP Top 10:2025 mostrou que a segurança deve ser considerada desde o planejamento de um sistema até sua utilização, manutenção e monitoramento.

Os riscos estudados possuem características diferentes, mas podem estar relacionados.

Por isso, uma boa abordagem de segurança envolve prevenção, controle de acesso, proteção de dados, desenvolvimento seguro, monitoramento, tratamento adequado de erros e capacidade de resposta.

Este mini-guia representa uma síntese dos principais conhecimentos desenvolvidos durante o projeto **Fundamentos de Cibersegurança para Iniciantes**.
