<div align="center">

<img src="assets/banner.svg" alt="Immigration Consultant AI Agent" width="100%"/>

<br/>

<img src="https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n"/> <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI"/> <img src="https://img.shields.io/badge/WhatsApp%20API-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp API"/> <img src="https://img.shields.io/badge/Calendly-006BFF?style=for-the-badge&logo=calendly&logoColor=white" alt="Calendly"/> <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase"/>

<br/>

<img src="https://img.shields.io/badge/n8n%20nodes-30-EA4B71?style=flat-square" alt="nodes"/>
<img src="https://img.shields.io/badge/Status-Delivered%20to%20client-success?style=flat-square" alt="status"/>
<img src="https://img.shields.io/badge/Workflow-Private%20(client%20project)-lightgrey?style=flat-square" alt="source"/>

**[Get this built for your business](https://www.fiverr.com/faizan_develope) · [Rootocloud](https://rootocloud.com) · [More projects](https://github.com/MuhammadFaizan73)**

</div>

---

## 📌 Overview

A WhatsApp assistant for an immigration consultancy. It answers questions about visas and processes, understands voice notes, registers client cases as tickets, and books consultations by fetching live Calendly slots and creating the booking inside the chat.

## ✨ What It Does

- Text and voice-note understanding (Whisper)
- Case / complaint registration → Supabase, Google Sheets and email
- Live Calendly availability shown as choices in WhatsApp
- Booking created and confirmed inside the chat
- Conversation memory and live-agent handover

## 📈 Business Impact

Prospects get answers and a booked consultation in one WhatsApp conversation, with no back-and-forth emails.

## 🔀 How It Works

The diagram below is generated directly from the production n8n workflow.

### Workflow — 30 nodes

```mermaid
flowchart TD
  n0(["📱 WhatsApp Webhook"])
  n1["✅ Respond to Webhook"]
  n2["📋 Extract Message"]
  n3["🗄️ Supabase - Load History"]
  n4["🌉 History Bridge"]
  n5{"🔀 Live Agent?"}
  n6["📝 Save User Msg Only"]
  n7["💾 Save History (Live Agent)"]
  n8{"🔀 Is Voice?"}
  n9["📥 Download Audio"]
  n10["🗣️ Whisper Transcribe"]
  n11["🔗 Merge Voice"]
  n12["🧠 Session Manager"]
  n13["🔍 Response Parser"]
  n14["💾 Supabase - Save History"]
  n15{"🔀 Register?"}
  n16{"🔀 Book Appointment?"}
  n17["📤 WhatsApp - Send Reply"]
  n18["🗄️ Supabase - Save Ticket"]
  n19["📊 Google Sheets - Save Ticket"]
  n20["📧 Format Email"]
  n21["📨 Send Company Email"]
  n22["📤 WhatsApp - Complaint Confirmed"]
  n23["📅 Fetch & Format Slots"]
  n24["💾 Save Slots State"]
  n25["📤 WhatsApp - Send Slots"]
  n26["🔗 Create & Send Booking"]
  n27["💾 Save Booking Confirmed"]
  n28["📤 WhatsApp - Send Confirmation"]
  n29{"🔀 Create Booking?"}
  n0 --> n1
  n0 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n5 --> n8
  n6 --> n7
  n8 --> n9
  n8 --> n12
  n9 --> n10
  n10 --> n11
  n11 --> n12
  n12 --> n13
  n13 --> n14
  n14 --> n15
  n15 --> n18
  n15 --> n16
  n16 --> n23
  n16 --> n29
  n18 --> n19
  n19 --> n20
  n20 --> n21
  n21 --> n22
  n23 --> n24
  n24 --> n25
  n26 --> n27
  n27 --> n28
  n29 --> n26
  n29 --> n17
```

<!-- SCREENSHOTS -->
<!-- /SCREENSHOTS -->

## 🔒 About the Workflow File

This automation was built for a client, so the n8n workflow JSON (with prompts, credentials and business logic) is kept private.
**I can build a version tailored to your business** — [contact me on Fiverr](https://www.fiverr.com/faizan_develope) or [email](mailto:faizan.developer9200@gmail.com).

## 👨‍💻 Author

**Muhammad Faizan** — Founder, [Rootocloud](https://rootocloud.com) · n8n & AI Automation Specialist (8+ years)

[![Website](https://img.shields.io/badge/rootocloud.com-0B1220?style=for-the-badge&logo=googlechrome&logoColor=white)](https://rootocloud.com)
[![Fiverr](https://img.shields.io/badge/Fiverr-1DBF73?style=for-the-badge&logo=fiverr&logoColor=white)](https://www.fiverr.com/faizan_develope)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/muhammad-faizan-b7062b7a/)

<div align="center"><sub>© Muhammad Faizan. All rights reserved.</sub></div>
