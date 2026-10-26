## ⚠️ IMPORTANT

This project is cumulative.

Consider all features, structures, components, business rules, integrations, and configurations created in previous generations.

Do not replace existing functionality.

Only add and integrate new features.

Maintain:

- Tailwind CSS
- Supabase
- Internationalization (PT-BR and EN-US)
- Mobile First
- Dark Mode
- Existing validations

---

# ELVISYS

Create Elvisys, the official virtual assistant of Deliverrr.

Elvisys will be the first interface presented to users and will be responsible for authentication, registration, and navigation routing.

Take inspiration from:

- ChatGPT
- Intercom
- Drift
- WhatsApp

Design:

- Conversational
- Modern
- Mobile First
- Dark Mode
- Tailwind CSS

---

## INTERNATIONALIZATION

Supported languages:

- PT-BR
- EN-US

The entire interface must adapt to the selected language.

The selected language must be persisted in the user's profile.

---

## INITIAL MESSAGE

PT-BR:

"Olá 👋 Eu sou o Elvisys, assistente virtual do Deliverrr."

"Como posso ajudar você hoje?"

EN-US:

"Hello 👋 I'm Elvisys, Deliverrr's virtual assistant."

"How can I help you today?"

---

## PRIMARY ACTION BUTTONS

Display three buttons:

🛒 I Am a Customer

👀 I Am a Visitor (I just want to browse the menu and prices)

🏪 I Am a Restaurant Owner

---

## VISITOR FLOW

Message:

"Feel free to explore our menu 😋"

Actions:

- Redirect to /menu
- Do not require login
- Allow users to browse products
- Allow users to build a cart

When the user proceeds to checkout:

Require login or registration.

---

## CUSTOMER FLOW

Ask:

"How would you like to be addressed?"

Then:

"Do you already have a Deliverrr account?"

Buttons:

✅ I Already Have an Account

✨ Create My Account

---

## CUSTOMER LOGIN

Request:

Phone Number

Required format:

+55 11 99999-9999

Then request:

Password

Requirements:

- Minimum 8 characters
- 1 uppercase letter
- 1 lowercase letter
- 1 number
- 1 special character

Accepted special characters:

# @ $ % & * !

This page must include a:

"Forgot Password?" option

After successful authentication:

Redirect to:

/menu

---

## CUSTOMER SIGN-UP

Request:

- Name
- WhatsApp Number
- Address
- ZIP Code
- Password

Validation:

Phone number is required.

Format:

+55 11 99999-9999

Display the question:

"Would you like to receive order status updates via WhatsApp?"

Options:

✅ Yes, of course

❌ No, thanks

Display a real-time password validation checklist.

Show button:

🔒 Security & Privacy

Open a modal containing:

- LGPD Compliance Information
- Data Protection Policy
- Password Encryption Information

After registration:

Redirect to:

/menu

---

## RESTAURANT OWNER FLOW

Message:

"Welcome to Deliverrr for Restaurants 🍕"

Question:

"Do you already have administrative access?"

Buttons:

✅ Log In

🚀 Create Restaurant

---

## ADMIN LOGIN

Request:

- Email
- Password

After successful authentication:

/admin

---

## RESTAURANT REGISTRATION

Request:

- Full Name
- Restaurant Name
- CNPJ
- Phone Number
- Address
- ZIP Code
- Delivery Radius
- Email
- Password

Delivery radius options:

- 5 km
- 10 km
- 15 km
- 20 km

After registration:

Create:

- Administrator Profile
- Restaurant
- Dashboard (initially empty)
- Kanban Board (initially empty)
- Menu (initially empty)

Redirect to:

/admin