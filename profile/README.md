# Emprega.co

Aplicativo mobile da [Emprega.co](https://empregaco.com.br), negócio de impacto social que conecta empresas a candidatos das favelas do Brasil.

## Sobre a Emprega.co

A Emprega.co está sediada em Paraisópolis (SP) e integra o Hub de Negócios do G10 Favelas. Atua com empregabilidade com propósito social, conectando empresas parceiras a pessoas em busca de trabalho e capacitação nas favelas de SP, PA, MA, PE, RJ, DF e MG.

Seus serviços incluem recrutamento e seleção, terceirização de mão de obra, capacitação profissional, apoio ao empreendedor local e indicação de profissionais autônomos.

## O projeto

Esta organização reúne o desenvolvimento do aplicativo mobile da Emprega.co, realizado como Trabalho de Conclusão de Curso do Técnico em Desenvolvimento de Sistemas do SENAI Suíço-Brasileira.

O objetivo é levar a operação da Emprega.co para o celular e cobrir toda a jornada de contratação dentro de um único aplicativo: da publicação da vaga ao encerramento do contrato.

## Como funciona

1. O contratante cadastra a empresa e publica uma vaga.
2. O candidato encontra a vaga, inclusive por proximidade via CEP, e se candidata.
3. O contratante analisa as candidaturas e envia uma proposta.
4. O candidato aceita ou recusa a proposta.
5. Com o aceite, o contrato é formalizado e a taxa do serviço é paga via Pix.
6. Contratante e candidato conversam pelo aplicativo durante o contrato.
7. Ao final, o contrato é encerrado e as duas partes se avaliam.

## Funcionalidades

**Candidato**

- Cadastro rápido e perfil profissional editável por seção
- Busca de vagas com filtro por CEP
- Candidatura e acompanhamento do status
- Recebimento e resposta de propostas
- Acompanhamento de contratos
- Treinamentos com inscrição, histórico e conclusão

**Contratante**

- Cadastro e perfil da empresa
- Publicação e gestão de vagas
- Análise de candidaturas e envio de propostas
- Gestão de contratos, incluindo cancelamento e encerramento
- Pagamento da taxa do serviço via Pix

**Recursos comuns**

- Mensagens em tempo real
- Notificações dentro do aplicativo
- Avaliações entre contratante e candidato
- Denúncia e bloqueio de usuários
- Configurações e exclusão de conta

**Administração**

- Painel administrativo para a equipe da Emprega.co acompanhar a operação da plataforma

## Arquitetura

A solução é composta por três partes:

- **Aplicativo mobile:** React Native com Expo e TypeScript, com navegação via React Navigation, estado global com Zustand e comunicação com a API via Axios.
- **API:** serviço REST com WebSocket para mensagens em tempo real, sobre banco de dados PostgreSQL.
- **Painel administrativo:** interface web de gestão da plataforma.

Os ambientes são separados entre homologação, no Microsoft Azure, e produção, na AWS. Os pagamentos são processados pelo Mercado Pago, e a publicação nas lojas é feita via Expo para App Store e Google Play.

## Privacidade e segurança

- Registro do aceite dos Termos de Uso e da Política de Privacidade no cadastro
- Exclusão de conta com anonimização dos dados pessoais
- Limitação de requisições nas conexões em tempo real
- Mecanismos de denúncia e bloqueio entre usuários

## Processo de desenvolvimento

- Scrum com sprints quinzenais, gerenciadas no ClickUp
- Times divididos por jornada: contratante e plataforma (Pod A) e candidato (Pod B)
- Design de telas e Design System próprio no Figma
- Git Flow simplificado (`main`, `develop`, `feature/*`, `bugfix/*`, `hotfix/*`)
- Conventional Commits
- Fase dedicada de QA e testes em dispositivos reais antes da publicação

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
