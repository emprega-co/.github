# Emprega.co

Aplicativo mobile da [Emprega.co](https://empregaco.com.br), negócio de impacto social que conecta empresas a candidatos das favelas do Brasil.

## Sobre a Emprega.co

A Emprega.co está sediada em Paraisópolis (SP) e integra o Hub de Negócios do G10 Favelas. Atua com empregabilidade com propósito social, conectando empresas parceiras a pessoas em busca de trabalho e capacitação nas favelas de SP, PA, MA, PE, RJ, DF e MG.

Seus serviços incluem recrutamento e seleção, terceirização de mão de obra, capacitação profissional, apoio ao empreendedor local e indicação de profissionais autônomos.

## O projeto

Esta organização reúne o desenvolvimento do aplicativo mobile da Emprega.co, realizado como Trabalho de Conclusão de Curso do Técnico em Desenvolvimento de Sistemas do SENAI Suíço-Brasileira.

O objetivo é levar a operação da Emprega.co para o celular e cobrir toda a jornada de contratação em um único aplicativo, da publicação da vaga ao encerramento do contrato.

## Como funciona

1. O contratante, pessoa física ou jurídica, publica uma vaga.
2. O candidato encontra a vaga e se candidata.
3. O contratante analisa a candidatura e pode abrir uma conversa com o candidato a partir da aprovação.
4. Após uma etapa opcional de entrevista, o contratante envia uma proposta.
5. Quando o candidato aceita, o contrato é criado aguardando pagamento.
6. O contratante paga a taxa de colocação via Pix, e a confirmação do pagamento ativa o contrato.
7. Ao final, o contrato é encerrado e as duas partes podem se avaliar.

## Funcionalidades

**Candidato**

- Cadastro rápido e perfil profissional editável por seção
- Busca de vagas, inclusive por localização
- Candidatura e acompanhamento do status
- Resposta a propostas e acompanhamento de contratos
- Inscrição em cursos presenciais e histórico de participação

**Contratante**

- Cadastro e perfil do contratante
- Publicação, pausa e encerramento de vagas
- Análise de candidaturas e envio de propostas
- Pagamento da taxa de colocação via Pix
- Gestão de contratos, incluindo cancelamento e encerramento

**Recursos comuns**

- Mensagens em tempo real
- Notificações dentro do aplicativo
- Avaliação mútua após o contrato
- Denúncia e bloqueio de usuários
- Configurações e exclusão de conta

**Organizações parceiras e operação**

- Cadastro de cursos e turmas presenciais por ONGs parceiras
- Painel web administrativo para moderação e acompanhamento da plataforma

## Arquitetura

A solução é composta por dois repositórios:

- **Aplicativo mobile:** React Native com Expo e JavaScript, navegação com React Navigation, estado global com Zustand, requisições HTTP com Axios e mensagens em tempo real via STOMP sobre WebSocket.
- **API:** Java 21 com Spring Boot, Spring Security com autenticação JWT, Spring Data JPA, PostgreSQL 16 com migrations em Flyway e documentação OpenAPI. A API também serve o painel administrativo, renderizado com Thymeleaf.

Os pagamentos são processados por gateway externo, com confirmação por webhook. O ambiente de homologação roda no Microsoft Azure, com deploy automatizado via GitHub Actions, e o ambiente de produção está sendo implantado na AWS.

## Qualidade

- Testes de integração da API com PostgreSQL efêmero via Testcontainers
- Testes do aplicativo com o test runner nativo do Node.js
- Integração contínua com GitHub Actions
- Padronização de código com ESLint e Prettier
- Coleções Postman para validação dos contratos da API
- Fase dedicada de QA em dispositivos reais antes da publicação

## Privacidade e segurança

- Registro do aceite dos Termos de Uso e da Política de Privacidade no cadastro
- Exclusão de conta com remoção dos dados pessoais e política de retenção definida
- Motivos de cancelamento e recusa por códigos fixos, sem texto livre, em conformidade com a LGPD
- Limitação de requisições nas conexões em tempo real
- Denúncia, bloqueio e fila de moderação

## Processo de desenvolvimento

- Scrum com sprints quinzenais, gerenciadas no ClickUp
- Times divididos por jornada: contratante e plataforma (Pod A) e candidato (Pod B)
- Design de telas e Design System próprio no Figma
- Branches de trabalho (`feature/*`, `fix/*`) integradas à branch `develop` por Pull Request
- Conventional Commits

## Equipe

| Nome | Função |
| --- | --- |
| Cauê Rodrigues | Scrum Master, Product Owner e Design |
| David Lucas | Tech Lead |
| Victor Hugo | Tech Lead |
| André Dias | Desenvolvimento e Documentação |
| Heitor Perciliano | Desenvolvimento |

**Orientação:** Prof.ª Fiama Brenda Barbosa dos Santos

---

SENAI Suíço-Brasileira · Técnico em Desenvolvimento de Sistemas · 2026
