<div align="center">

# Letech Flow Hub — ERP Empresarial

**Sistema de gestão operacional, comercial e financeira desenvolvido para a [Letech Energia](https://letech.com.br)**

[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=white)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![Vite](https://img.shields.io/badge/Vite-Build-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev)
[![Vercel](https://img.shields.io/badge/Deploy-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com)

> Desenvolvido por **Danilo da Silva** — Administrativo / TI  
> Sistema em produção: [https://letech-flow-hub.vercel.app](https://letech-flow-hub.vercel.app)

</div>

---

## Sobre o Projeto

O **Letech Flow Hub** é um ERP completo desenvolvido do zero para digitalizar e integrar toda a operação da Letech Energia — empresa de serviços e comércio de equipamentos elétricos.

O sistema substitui processos manuais em planilhas e documentos avulsos, centralizando em uma única plataforma web:

- Gestão comercial com propostas, CRM em Kanban e pipeline de vendas
- Controle operacional com ordens de serviço, equipes multifunção e equipamentos
- Locação de equipamentos com geração automática de contratos, notas e checklists em PDF
- Gestão financeira com DRE, fluxo de caixa, aportes, reembolsos e adiantamentos
- Relatórios técnicos com geração automática de documentos Word e PDF
- Controle de frota, estoque e calibração de instrumentos
- Registro de frequência (própria e de terceirizados) e remuneração da equipe
- Apólices de seguro e certificados de segurança com alerta automático de vencimento

---

## Stack Tecnológico

| Camada | Tecnologia |
|---|---|
| Frontend | React 18 + TypeScript + Vite |
| UI | Tailwind CSS + Shadcn/UI + Radix UI |
| Backend | Supabase (PostgreSQL + Auth + Storage + Edge Functions) |
| Realtime | Supabase Realtime Subscriptions |
| Formulários | React Hook Form + Zod |
| Gráficos | Recharts |
| Documentos | jsPDF + jsPDF-AutoTable + DOCX + XLSX |
| Deploy | Vercel (CI/CD automático via GitHub) |
| Package Manager | Bun |

---

## Módulos do Sistema

### Comercial
- Cadastro e gestão de clientes com múltiplos contatos por empresa
- Propostas comerciais com 3 tipos (Serviço, Obra, Locação) e fluxo de aprovação simplificado
- Geração automática de **PDF de proposta** com logo, tabelas e formatação profissional
- **CRM em Kanban** (Negociações): múltiplos funis configuráveis por tipo de cliente, qualificação por estrelas, histórico automático de mudanças, indicador de "dias na etapa" e geração de proposta formal a partir da negociação

### Ordens de Serviço
- OS de Visita e OS Avulsa unificadas em um único fluxo, com tipo escolhido no próprio formulário
- Montagem de equipes com suporte a **múltiplas funções por pessoa** (ex: técnico que também é motorista e responsável por gastos)
- Controle de quilometragem, gastos e notas fiscais por OS — com registro de KM avulso liberado a toda a equipe de campo
- Fluxo de aprovação em dois níveis (operacional e financeiro)
- Resultado financeiro por OS: receita vs. custo vs. margem

### Locações de Equipamentos
- Controle completo do ciclo: abertura → aprovação → execução → encerramento
- Prorrogação de contratos com numeração automática (ex: 178 → 178_1)
- **Motor de geração de documentos**: Proposta, Contrato, Nota e Checklist de equipamentos gerados automaticamente em PDF a partir dos dados da locação
- Integração com financeiro: marcar pagamento cria lançamento em contas automaticamente

### Financeiro
- Contas a pagar e a receber com múltiplos bancos
- **DRE** (Demonstração de Resultado do Exercício) mensal
- Fluxo de caixa previsto com geração de **PDF executivo**
- Previsão de folha de pagamento integrada à frequência, incluindo terceirizados
- Aportes de sócios, reembolsos e adiantamentos a colaboradores e terceirizados, cada um com sua própria regra de baixa e impacto no caixa
- Pagamento parcial de terceirizados, com saldo devido e histórico de cada baixa

### Relatórios Técnicos
- **RAE** (Relatório de Execução): instrumentos, pontos de medição, fotos e geração de **DOCX** formatado
- **RTT** (Relatório Técnico de Termografia): severidades, normas ABNT/NR, aprovações
- Exportação de dados em **XLSX**

### Frota
- Cadastro e gestão de veículos com controle de KM
- Registro de abastecimento e manutenção unificado (natureza + tipo do item, com upload de comprovante)
- Movimentação de veículos com ou sem vínculo a uma OS (ex: deslocamento avulso), registrável por qualquer perfil
- Alertas de revisão por quilometragem e periodicidade

### Apólices e Documentos
- Controle de apólices de seguro (veículo, equipamento, funcionário e gerais) com vigência e arquivos anexados
- Certificados de segurança por colaborador (ASO, NR-10, NR-35, Termografia, Primeiros Socorros)
- Certificados da empresa (PCMSO, PGR e outros documentos obrigatórios)
- Notificações automáticas de vencimento

### Equipamentos e Calibração
- Cadastro de instrumentos com subtipos customizáveis
- Controle de calibração com cálculo automático da próxima data
- Scanner de QR Code para acesso rápido ao histórico do equipamento

### Estoque
- Controle de itens com entrada, saída e saldo
- Histórico de movimentações com custo unitário e total

### Frequência e RH
- Registro diário de presença por status (base, cliente, home office, falta, viagem)
- Extras automáticos: sábado, domingo, feriado, viagem com pernoite, hora extra
- Rateio de mão de obra em gastos de OS por diária
- Remuneração: cálculo de salários, diárias e extras por colaborador
- Exportação em XLSX para folha de pagamento

### Colaboradores
- Cadastro completo com dados pessoais e profissionais
- Integração entre usuários do sistema e técnicos de equipe

### Configurações
- Gestão de usuários com 7 perfis de acesso granular
- Subtipos de equipamentos customizáveis
- Fotos de capa para propostas (upload via Storage)

---

## Controle de Acesso

O sistema implementa **7 perfis** com RLS (Row Level Security) no banco de dados:

| Perfil | Acesso |
|---|---|
| Diretor | Tudo, incluindo configurações e usuários |
| Administrativo | Tudo exceto configurações de usuários |
| Gerente Operacional | Tudo exceto Financeiro/DRE |
| Comercial | Clientes, Propostas, Locações |
| Técnico | Somente suas próprias OS |
| Almoxarifado | Estoque, Frota, Equipamentos, Frequência |
| Contador | Somente Financeiro e DRE (via view específica) |

---

## Destaques Técnicos

- **Autenticação customizada** — login por matrícula via RPC no banco, não por email
- **Soft-delete em todo o sistema** — nenhum dado é apagado, sempre `ativo = false`
- **Numeração automática** — propostas, OS e locações numeradas por triggers no banco
- **Geração de documentos em tempo real** — PDF e DOCX sem dependência de servidor externo
- **Realtime** — hook `useRealtime()` com Supabase para atualização automática de listas
- **Regime de competência** — relatórios financeiros por `data_inicio`, não por data de pagamento
- **Validações robustas** — Zod schemas com formatos de placa, datas e moeda brasileira
- **Design system próprio** — paleta de cores da marca com tokens CSS customizados
- **Abatimento financeiro automático** — adiantamentos a terceirizados são consumidos em FIFO contra o saldo em aberto, sem passo manual
- **RLS granular por perfil** — políticas no Postgres que combinam autoria do registro e papel do usuário (ex: autor ou gestor podem editar)

---

## Estrutura do Projeto

```
src/
├── components/          # Componentes reutilizáveis e dialogs
│   ├── ui/              # Primitivos (Shadcn/UI)
│   ├── financeiro/      # Componentes do módulo financeiro
│   ├── os/              # Componentes de ordens de serviço
│   ├── locacoes/        # Componentes de locações
│   └── equipamentos/    # Componentes de equipamentos
├── contexts/            # AuthContext — autenticação e perfil
├── layouts/             # AppLayout + AppSidebar
├── lib/                 # Supabase client + schemas Zod
├── pages/               # Páginas por módulo
├── hooks/               # useRealtime, useNotificacoes
└── config/              # Menus e rotas
```

---

## Sobre o Desenvolvedor

**Danilo da Silva**  
Administrativo / TI — Letech Energia

Responsável pelo desenvolvimento completo deste sistema: desde a modelagem do banco de dados no Supabase, arquitetura do frontend em React + TypeScript, implementação das regras de negócio, até o deploy automatizado na Vercel.

O projeto foi construído de forma incremental, módulo a módulo, com foco em usabilidade para usuários não técnicos e robustez para operação diária de uma empresa.

---

<div align="center">

**Feito com dedicação para a Letech Energia**

</div>
