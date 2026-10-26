## ⚠️ IMPORTANTE

Projeto cumulativo.

Todas as funcionalidades devem utilizar esta estrutura.

---

# SUPABASE

Criar estrutura completa para o Deliverrr.

---

## PROFILES

id

nome

email

telefone

role

Valores:

- admin
- cliente

preferred_language

receber_whatsapp

created_at

---

## ESTABLISHMENTS

id

nome_estabelecimento

cnpj

telefone

email

endereco

cep

latitude

longitude

raio_entrega_km

logo_url

created_at

---

## CUSTOMERS

id

profile_id

endereco

cep

latitude

longitude

created_at

---

## CATEGORIES

id

establishment_id

nome_pt

nome_en

descricao_pt

descricao_en

ordem

---

## PRODUCTS

id

category_id

nome_pt

nome_en

descricao_pt

descricao_en

imagem_url

preco

ativo

destaque

created_at

---

## PROMOTIONS

id

product_id

percentual_desconto

inicio

fim

---

## ORDERS

id

customer_id

establishment_id

status

Valores:

- pending
- queued
- preparing
- delivering
- completed
- cancelled

subtotal

frete

desconto

total

distancia_km

created_at

---

## ORDER_ITEMS

id

order_id

product_id

quantidade

preco_unitario

---

## WHATSAPP_LOGS

id

order_id

telefone_destino

mensagem

status_envio

created_at

---

## MÉTRICAS

Criar views automáticas:

- Pedidos por dia
- Pedidos por semana
- Pedidos por mês
- Ticket médio
- Produto mais vendido
- Produto menos vendido
- Faturamento diário
- Faturamento mensal

---

## SEGURANÇA

Implementar:

- Foreign Keys
- Índices
- RLS
- Policies
- Migrations
- Seeds

---

## SEED INICIAL

Restaurante:

Bella Napoli

Categorias:

- Entradas
- Massas
- Pizzas
- Sobremesas
- Bebidas

Inserir produtos de demonstração prontos para teste.