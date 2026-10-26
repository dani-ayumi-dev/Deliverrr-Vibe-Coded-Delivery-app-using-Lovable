<div align="right">
  <a href="prompts_ENG-US/README.en.md">🇺🇸 Switch to English</a>
</div>

# Deliverrr : Vibe Coding para um Delivery App com Lovable

## 🍕 Sobre o Projeto

**Deliverrr** é uma plataforma de delivery desenvolvida utilizando os princípios de **Vibe Coding**, com foco em proporcionar uma experiência moderna tanto para clientes quanto para donos de restaurantes.

A proposta do aplicativo é centralizar toda a operação de delivery em um único sistema, permitindo que restaurantes possuam seu próprio canal de vendas online sem depender exclusivamente de marketplaces externos.

O projeto foi concebido com os seguintes objetivos:

- Automatizar o fluxo de pedidos.
- Organizar pedidos através de um Kanban intuitivo.
- Disponibilizar métricas estratégicas para tomada de decisão.
- Permitir comunicação automática com clientes via WhatsApp.
- Disponibilizar um chatbot inteligente chamado **Elvisys** para interação com clientes e administradores.
- Possuir um cardápio digital totalmente personalizável.
- Suportar internacionalização (PT-BR e EN-US).
- Oferecer uma experiência moderna, responsiva e mobile-first.

---

## 🎯 Principais Funcionalidades

- 🤖 Elvisys (Chatbot Principal)
- 🍕 Cardápio Digital
- 🛒 Carrinho de Compras
- 📦 Gestão de Pedidos
- 📊 Dashboard Administrativo
- 📋 Kanban Operacional
- 💬 Integração WhatsApp
- ⭐ Sistema de Avaliações e Feedback
- 🌎 Internacionalização (i18n)
- 🔐 Autenticação e Controle de Acesso
- 🚚 Cálculo Automático de Frete
- 📈 Métricas e Relatórios

---

## 📁 Estrutura dos Prompts

| Prompt | Funcionalidade Definida | Diretório do Arquivo |
|----------|----------|----------|
| Prompt 1 | Elvisys (Chatbot, Login e Cadastro) | [PROMPT 1](prompts_PT-BR/prompt1_chatbot.md) |
| Prompt 2 | Cardápio Digital |[PROMPT 2](prompts_PT-BR/prompt2_menu.md) |
| Prompt 3 | Área Administrativa (Dashboard, Kanban, Elvisys Admin e Feedback) |[PROMPT 3](prompts_PT-BR/prompt3_area_adm.md)|
| Prompt 4 | Integração WhatsApp e Notificações | [PROMPT 4](prompts_PT-BR/prompt4_whatsapp_api.md) |
| Prompt 5 | Banco de Dados Supabase |[PROMPT 5](prompts_PT-BR/prompt5_supabase.md) |

---

## Business Canvas Model e Brainstorm

![BMC e Brainstorm](<Deliverr_ Mapa de Funcionalidades e Negócio.png>)
---
## 🏗️ Arquitetura Geral

```text
Cliente
   │
   ▼
Elvisys
   │
   ├── Login
   ├── Cadastro
   ├── Visitante
   └── Dono de Restaurante
            │
            ▼
        Dashboard
            │
            ├── Kanban
            ├── Cardápio
            ├── WhatsApp
            ├── Feedbacks
            └── Elvisys Admin
```

---

## 🤖 Elvisys

O Elvisys é o assistente virtual oficial do Deliverrr.

Ele atua como:

- Ponto de entrada do sistema.
- Assistente de cadastro.
- Assistente de login.
- Assistente administrativo.
- Central de alertas.
- Futuro copiloto operacional do restaurante.

### Fluxos suportados

#### 👀 Visitante

- Navega pelo cardápio.
- Consulta preços.
- Monta carrinho.
- Faz cadastro apenas no checkout.

#### 🛒 Cliente

- Login.
- Cadastro.
- Acompanhamento de pedidos.
- Recebimento de notificações via WhatsApp.
- Avaliação de pedidos.

#### 🏪 Dono de Restaurante

- Login administrativo.
- Gestão do restaurante.
- Edição do cardápio.
- Acompanhamento de métricas.
- Gestão operacional via Kanban.

---

## 📋 Kanban Operacional

Fluxo de pedidos:

```text
📥 Na fila para preparo
        │
        ▼
👨‍🍳 Em preparo
        │
        ▼
🚚 Enviado para delivery
        │
        ▼
✅ Entregue
```

Cada movimentação pode gerar notificações automáticas para o cliente via WhatsApp.

---

## ⭐ Sistema de Avaliações

Após a entrega do pedido, o cliente será convidado a avaliar sua experiência.

### Escala de avaliação

```text
0 ⭐ a 5 ⭐
```

### Informações coletadas

- Nota
- Comentário opcional
- Data da avaliação
- Pedido relacionado

### Alertas

O Elvisys notificará automaticamente o administrador quando uma avaliação de **0 estrelas** for recebida.

---

## 💬 Integração WhatsApp

Prioridade de integrações:

1. Evolution API
2. WAHA
3. Baileys

Funcionalidades:

- Notificação de status do pedido.
- Atualizações de entrega.
- Envio de pedido de feedback.
- Histórico de mensagens.
- Logs de envio.

---

## 🌎 Internacionalização

Idiomas suportados:

- 🇧🇷 Português (Brasil)
- 🇺🇸 English (United States)

A preferência de idioma é persistida no perfil do usuário.

Todo o sistema deve respeitar a configuração escolhida pelo usuário.

---

## 🗄️ Banco de Dados

Tecnologia:

```text
Supabase
```

Principais entidades:

- Profiles
- Establishments
- Customers
- Categories
- Products
- Promotions
- Orders
- Order Items
- Customer Reviews
- WhatsApp Logs
- Admin Alerts
- Chat Messages

---

## 🎨 Design System

Tecnologias:

- React
- TypeScript
- Tailwind CSS
- Supabase

Diretrizes:

- Mobile First
- Dark Mode
- Responsivo
- Componentes reutilizáveis
- UX inspirada em:
  - iFood
  - Uber Eats
  - Stripe Dashboard
  - WhatsApp

---

## 🚀 Objetivo Final

Transformar o Deliverrr em uma plataforma completa para restaurantes, reunindo:

- Gestão operacional
- Canal próprio de vendas
- Comunicaizada
- Inteligência de negócios
- Atendimento assistido por IA

Tudo centralizado em uma única experiência moderna e escalável.