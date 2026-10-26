## ⚠️ IMPORTANT

This project is cumulative.

Integrate with:

- Orders
- Kanban
- Dashboard
- Elvisys

---

# WHATSAPP

Implement automatic communication through WhatsApp.

Priority order:

1. Evolution API
2. WAHA
3. Baileys

Use a free solution whenever possible.

---

## CONFIGURATION

Display:

- QR Code
- Connection Status
- Connected Phone Number
- Last Synchronization

---

## AUTOMATIC NOTIFICATIONS

Trigger notifications whenever an order status changes in the Kanban board.

---

## WAITING FOR PREPARATION → PREPARING

PT-BR

"🍕 Seu pedido já está sendo preparado."

EN-US

"🍕 Your order is being prepared."

---

## PREPARING → OUT FOR DELIVERY

PT-BR

"🚚 Seu pedido saiu para entrega."

"Tempo estimado: X minutos"

EN-US

"🚚 Your order is out for delivery."

"Estimated delivery time: X minutes"

---

## OUT FOR DELIVERY → DELIVERED

PT-BR

"✅ Pedido entregue. Obrigado por comprar conosco."

EN-US

"✅ Order delivered. Thank you for your purchase."

---

## REQUEST CUSTOMER FEEDBACK

After an order is marked as:

✅ Delivered

Automatically send a customer feedback request.

### PT-BR

"Como foi sua experiência com {restaurant name}?"

"Dê uma nota de 0 a 5 estrelas."

"Adicione um comentário (opcional)."

### EN-US

"How was your experience with {restaurant name}?"

"Give a rating from 0 to 5 stars."

"Add a comment (optional)."

---

## CUSTOMER FEEDBACK PROCESSING

When a customer submits feedback:

- Save the rating (0 to 5 stars).
- Save the optional comment.
- Associate the feedback with the corresponding order.
- Associate the feedback with the restaurant.
- Send the feedback data to the Administrator Dashboard.
- Update customer satisfaction metrics in real time.
- Update the restaurant's average rating.

---

## DASHBOARD INTEGRATION

The Administrator Dashboard must display:

- Average Rating
- Total Reviews
- Rating Distribution
- Customer Feedback History
- Negative Reviews
- Positive Reviews

Feedback received via WhatsApp must appear automatically in the Dashboard.

---

## AUTOMATIC ALERTS

If a customer submits:

⭐ 0 Stars

Automatically notify the restaurant owner through Elvisys.

Example:

🚨 Warning!

Customer "{customer_name}" rated the restaurant with 0 stars.

Comment:

"{customer_comment}"

Order:

#{order_number}

Recommended action:

Please contact this customer as soon as possible to better understand the issue and improve customer satisfaction.

---

## RULES

- Always use the customer's selected language.
- Save delivery and message logs.
- Implement automatic retry mechanisms in case of failure.
- Store message delivery status.
- Store message timestamps.
- Store feedback submission timestamps.

---

## DELIVERY STATUS

Display the delivery status in real time.

Possible statuses:

- Order Received
- Waiting for Preparation
- Preparing
- Ready for Delivery
- Out for Delivery
- Delivered
- Cancelled

Both customers and restaurant owners must be able to track the current delivery status in real time.