# FBA Control — CMMS

Sistema de gestão de manutenção (Computerized Maintenance Management System) para registro, acompanhamento e controle de ordens de serviço, com gestão de usuários e autorização de acesso por perfil.

🔗 **Demo ao vivo:** https://fbacontrol.com/login

---

## Sobre o projeto

O FBA Control foi projetado com foco em disponibilidade contínua, integridade dos dados e escalabilidade. A plataforma reúne registro e acompanhamento de ordens de manutenção, gestão de usuários e um fluxo de autorização em duas etapas: novos usuários só ganham acesso após liberação explícita de um administrador.

## Funcionalidades

- Autenticação e gestão de usuários com Firebase Authentication
- Fluxo de autorização de acesso: novos usuários aguardam liberação de um Admin
- Controle de permissões por perfil de usuário
- Ordens de manutenção com operações CRUD completas
- Persistência de dados em Cloud Firestore
- Regras de segurança aplicadas no servidor
- Deploy automatizado em Firebase Hosting

## Stack

| Camada | Tecnologia |
| --- | --- |
| Front-end | React + Vite |
| Autenticação | Firebase Authentication |
| Banco de dados | Cloud Firestore (NoSQL) |
| Hospedagem | Firebase Hosting |

## Arquitetura

Aplicação SPA em React com build via Vite. O estado de autenticação é gerenciado em contexto global, e o acesso às rotas é controlado por perfil de usuário. A camada real de proteção dos dados são as regras de segurança do Firestore, combinadas ao fluxo de aprovação de novos usuários.

## Como executar localmente

1. Clone o repositório:
   `git clone https://github.com/pedroqueirozbatera-alt/fba-control.git`
2. Instale as dependências:
   `npm install`
3. Configure suas credenciais do Firebase no arquivo de configuração do projeto
4. Execute em desenvolvimento:
   `npm run dev`
<img width="1920" height="1080" alt="Captura de Tela 2026-09-11 às 00 06 44" src="https://github.com/user-attachments/assets/ce04709b-86ab-4918-9cab-dae2b8f7043b" />

## Deploy
```bash
npm run build
firebase deploy --only hosting
