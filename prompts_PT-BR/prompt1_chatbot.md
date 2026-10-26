## ⚠️ IMPORTANTE

Este projeto é cumulativo.

Considere todas as funcionalidades, estruturas, componentes, regras de negócio, integrações e configurações criadas anteriormente.

Não substituir funcionalidades existentes.

Apenas adicionar e integrar novas funcionalidades.

Manter:

- Tailwind CSS
- Supabase
- Internacionalização (PT-BR e EN-US)
- Mobile First
- Dark Mode
- Validações existentes

---

# ELVISYS

Crie o Elvisys, assistente virtual oficial do Deliverrr.

O Elvisys será a primeira interface apresentada ao usuário e será responsável por autenticação, cadastro e direcionamento de navegação.

Inspirar-se em:

- ChatGPT
- Intercom
- Drift
- WhatsApp

Design:

- Conversacional
- Moderno
- Mobile First
- Dark Mode
- Tailwind CSS

---

## INTERNACIONALIZAÇÃO

Idiomas:

- PT-BR
- EN-US

Toda a interface deve responder ao idioma selecionado.

O idioma deve ser persistido no perfil do usuário.

---

## MENSAGEM INICIAL

PT-BR:

"Olá 👋 Eu sou o Elvisys, assistente virtual do Deliverrr."

"Como posso ajudar você hoje?"

EN-US:

"Hello 👋 I'm Elvisys, Deliverrr's virtual assistant."

"How can I help you today?"

---

## BOTÕES DE AÇÃO PRINCIPAL

Exibir três botões:

🛒 Sou Cliente

👀 Sou Visitante (Só queria ver o menu e preços)

🏪 Sou Dono de Restaurante

---

## FLUXO VISITANTE

Mensagem:

"Fique à vontade para explorar nosso cardápio 😋"

Ações:

- Direcionar para /cardapio
- Não exigir login
- Permitir visualizar produtos
- Permitir montar carrinho

Ao finalizar o pedido:

Solicitar login ou cadastro.

---

## FLUXO CLIENTE

Perguntar:

"Como você gostaria de ser chamado?"

Depois:

"Você já possui cadastro no Deliverrr?"

Botões:

✅ Já sou cadastrado

✨ Criar minha conta

---

## LOGIN DO CLIENTE

Solicitar:

Telefone

Formato obrigatório:

+55 11 99999-9999

Solicitar:

Senha 

Regras:

- Mínimo 8 caracteres
- 1 letra maiúscula
- 1 letra minúscula
- 1 número
- 1 caractere especial

Caracteres especiais:

# @ $ % & * !

Essa página precisa apresentar uma opção de "Esqueci minha senha"
Após autenticação:

Redirecionar para:

/cardapio

---

## CADASTRO DO CLIENTE

Solicitar:

- Nome
- Telefone WhatsApp
- Endereço
- CEP
- Senha

Validação:

Telefone obrigatório.

Formato:

+55 11 99999-9999

Exibir pergunta:

"Deseja receber atualizações do pedido via WhatsApp?"

Opções:

✅ Sim, claro

❌ Não, obrigado

Exibir checklist visual para senha.

Mostrar botão:

🔒 Segurança e Privacidade

Abrir modal contendo:

- LGPD
- Proteção de dados
- Criptografia de senha

Após cadastro:

Redirecionar para:

/cardapio

---

## FLUXO DONO DE RESTAURANTE

Mensagem:

"Bem-vindo ao Deliverrr para Restaurantes 🍕"

Pergunta:

"Você já possui acesso administrativo?"

Botões:

✅ Fazer Login

🚀 Criar Restaurante

---

## LOGIN ADMINISTRATIVO

Solicitar:

- Email
- Senha

Após autenticação:

/admin

---

## CADASTRO DE RESTAURANTE

Solicitar:

- Nome Completo
- Nome do Estabelecimento
- CNPJ
- Telefone
- Endereço
- CEP
- Raio de Entrega
- Email
- Senha

Raio de entrega:

- 5 km
- 10 km
- 15 km
- 20 km

Após cadastro:

Criar:

- Perfil Administrador
- Estabelecimento
- Dashboard (inicialmente vazio)
- Kanban (inicialmente vazio)
- Cardápio Inicial (inicialmente vazio)

Redirecionar para:

/admin