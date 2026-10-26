# Prompt 3 — Área Administrativa (Versão Atualizada com Avaliações e Feedback)

## ⚠️ IMPORTANTE

Projeto cumulativo.

Acesso permitido apenas para administradores autenticados.

Utilizar todas as funcionalidades já existentes.

Não remover funcionalidades previamente implementadas.

Integrar-se ao:

- Elvisys
- Dashboard
- Kanban
- Cardápio
- WhatsApp 
- Banco de dados Supabase

---

# ÁREA ADMINISTRATIVA

Criar rota:

/admin

---

# SIDEBAR

Criar menu lateral fixo contendo:

📊 Dashboard

📋 Kanban

🍕 Editar Cardápio

🤖 Elvisys

    Chats do WhatsApp (para que o dono do estabelecimento consiga conversar com o cliente diretamente caso seja necessário)

⚙️ Configurações

🚪 Sair

---

# DASHBOARD

Exibir métricas em tempo real.

## CARDS PRINCIPAIS

- Pedidos Hoje
- Pedidos Semana
- Pedidos Mês
- Faturamento
- Ticket Médio
- Produto Mais Vendido
- Produto Menos Vendido
- Tempo Médio de Preparo

---

## AVALIAÇÃO DOS CLIENTES

Adicionar uma seção exclusiva para experiência do cliente.

Métricas:

⭐ Avaliação Média Geral

⭐ Quantidade Total de Avaliações

⭐ Distribuição de Avaliações

Exemplo:

⭐ 5 estrelas → 45%

⭐ 4 estrelas → 30%

⭐ 3 estrelas → 15%

⭐ 2 estrelas → 7%

⭐ 1 estrela → 2%

⭐ 0 estrelas → 1%

---

## GRÁFICOS

Adicionar gráficos:

- Evolução da avaliação média ao longo do tempo
- Avaliações por dia
- Avaliações por semana
- Correlação entre avaliações e volume de pedidos

---

# FEEDBACK DOS CLIENTES

Criar painel específico chamado:

📝 Feedback dos Clientes

Exibir:

- Nome do cliente
- Nota atribuída (0 a 5)
- Comentário
- Data e hora da avaliação
- Pedido relacionado

Permitir filtros por:

- Período
- Nota
- Cliente

Permitir busca textual nos comentários.

---

# ALERTAS DE SATISFAÇÃO

Adicionar widget de alertas.

Situações monitoradas:

- Nota média abaixo de 3 estrelas
- Aumento de avaliações negativas
- Comentários contendo reclamações frequentes

Exibir alertas visuais no Dashboard.

---

# ELVISYS (MODO ADMINISTRADOR)

Criar uma área exclusiva do Elvisys dentro do painel administrativo.

O Elvisys deverá utilizar os dados do sistema para responder perguntas como:

- Qual meu produto mais vendido?
- Qual meu produto menos vendido?
- Qual meu ticket médio?
- Quantos pedidos recebi hoje?
- Qual meu faturamento do mês?
- Quantos pedidos estão em preparo?
- Como está minha avaliação média?
- Quantas avaliações negativas recebi hoje?
- Quais clientes deixaram avaliações negativas?

Responder utilizando dados reais do banco.

Utilizar linguagem simples, amigável e objetiva.

---

# ALERTA AUTOMÁTICO DO ELVISYS

Toda vez que um cliente avaliar o restaurante com:

⭐ 0 estrelas

o Elvisys deve gerar automaticamente uma notificação para o administrador.

Exemplo:

🚨 Atenção! O cliente "Maria" avaliou o restaurante com 0 estrelas.

Comentário:

"A entrega demorou muito."

Pedido:

#1042

Data:

25/10/2026 20:43

Recomendo verificar este caso para evitar perda de clientes.

---

# KANBAN

Visual semelhante ao Trello.

Colunas:

📥 Na fila para preparo

👨‍🍳 Em preparo

🚚 Enviado para delivery

✅ Entregue

Implementar drag and drop.

---

## CARD DO PEDIDO

Exibir:

- Número do pedido
- Cliente
- Itens
- Valor
- Horário
- Tempo decorrido

---

# EDITAR CARDÁPIO

Permitir:

- Criar categorias
- Editar categorias
- Excluir categorias
- Criar produtos
- Editar produtos
- Excluir produtos
- Gerenciar promoções
- Alterar preços
- Alterar imagens
- Alterar banner
- Alterar logo
- Alterar tema visual

---

# SOLICITAÇÃO DE FEEDBACK AO CLIENTE

Quando um pedido for marcado como:

✅ Entregue

Enviar automaticamente um pedido de avaliação.

---

## PT-BR

"Como foi sua experiência com {nome do restaurante}?"

"Dê uma nota de 0 a 5 estrelas."

"Adicione um comentário (opcional)."

---

## EN-US

"How was your experience with {restaurant name}?"

"Give a rating from 0 to 5 stars."

"Add a comment (optional)."

---

# FORMULÁRIO DE FEEDBACK

Campos:

⭐ Avaliação

Valores permitidos:

0
1
2
3
4
5

📝 Comentário

Campo opcional.

Botão:

✅ Enviar Avaliação

---

# REGRAS DE NEGÓCIO

Ao salvar o feedback:

- Atualizar média geral do restaurante.
- Atualizar gráficos de satisfação.
- Atualizar indicadores do Dashboard.
- Registrar comentário no banco de dados.
- Disponibilizar feedback para consulta administrativa.

Se a avaliação for:

⭐ 0 estrelas

então:

- Criar alerta prioritário para o administrador.
- Exibir alerta no Dashboard.
- Exibir alerta na área do Elvisys.
- Registrar ocorrência para acompanhamento posterior.

---

# EXPORTAÇÃO

Permitir exportação das avaliações e comentários:

- PDF
- CSV
- XLSX

Os relatórios devem conter:

- Cliente
- Nota
- Comentário
- Data
- Pedido relacionado

Respeitar o idioma selecionado pelo administrador.