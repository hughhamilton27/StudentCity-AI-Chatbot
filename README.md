# StudentCity: AI Support Chatbot Prototype

A clickable prototype of a customer-support chatbot for StudentCity, a spring-break travel company. It was a collaborative project.

The goal was to show how an AI assistant could answer common student questions and send anything it can't handle to a human, with every hand-off logged in the CRM.

**Note:** this is a prototype. The conversation follows a scripted flow written to simulate what a Claude + HubSpot integration would do. It doesn't call a live AI model or a real HubSpot account.

## What it does

- **Chat assistant ("Sunny").** A chat window opens from the page and walks the user through support topics.
- **Topic routing from free text.** Typed messages are matched on keywords ("flight", "refund", "passport", "roommate", and others) and sent to the right flow: booking status, flight details, hotel and roommates, travel documents, changes and cancellations, destination info, or a human representative.
- **Rich replies.** Booking and flight questions return formatted cards, not just text.
- **Human hand-off.** The "Speak to a representative" option appears only after the user has gone through one topic, so simple questions get answered first.
- **CRM lead capture (simulated).** When a user asks for a person, the bot collects their details and shows the HubSpot contact record that would be created.
- **Typing indicator and delays** make the conversation feel natural.

## Tech

Plain HTML, CSS, and JavaScript in a single file. The conversation logic is a set of handler functions (`handleUserInput`, `handleTopic`, `captureHubSpotLead`, and so on).

## What a production version would need

- Replace the keyword matching with an LLM call (for example the Claude API), using the booking data as context
- Connect the hand-off to the HubSpot API to create real contacts and tickets
- Pull booking and flight details from the company's actual booking system

## Run it

Open `index.html` in a browser.
