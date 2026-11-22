# DukaanMitra AI (दुकानमित्र) 🏪🇮🇳

> **Empowering 60M+ Indian SMB Merchants & Kirana Stores with Sovereign AI, Gemini MCP Connectors & Zero-Fee WhatsApp Integration.**

DukaanMitra is an open-source, India-first retail intelligence system designed to digitize inventory, conversational billing, udhaar (credit khata), and GST compliance. It brings native Google Gemini Model Context Protocol (MCP) tool integration and free, self-hosted WhatsApp automation directly to Indian shopkeepers.

---

### 🌐 Official Repositories & Architecture

| Repository | Status | Key Capabilities |
|---|---|---|
| **[DukaanMitra OS](https://github.com/dukaanmitra-ai/Dukaanmitra-MitraOS)** | Public Flagship | **The Complete Monorepo** — Merchant Web POS (`apps/mitra-os-web`), Core Prisma Engine (`apps/core-engine`), Python AI Backend (`apps/ai-services`), and Docker orchestration. |
| **[dukaanmitra-mcp](https://github.com/dukaanmitra-ai/dukaanmitra-mcp)** | Public Tool | **Gemini & AI Agent Connector** — Model Context Protocol (MCP) server exposing tools for real-time inventory checks, vernacular voice bills ("Ramesh ko 2 packet aata udhaar"), and GSTR-2B compliance. |
| **[whatsapp-gateway](https://github.com/dukaanmitra-ai/whatsapp-gateway)** | Public Gateway | **Free WhatsApp Shopkeeper Gateway** — Zero Meta API charges. Self-hosted QR-pairing gateway (powered by OpenWA) on port 2785 with two-way webhooks for bill OCR, voice notes, and order alerts. |
| **[Dukaanmitra.in](https://github.com/dukaanmitra-ai/Dukaanmitra.in)** | Public Web | **Official Platform Web Presence** — Merchant landing platform, localized discovery, and onboarding. |
| **[AI-QR](https://github.com/dukaanmitra-ai/AI-QR)** | Core Utility | **Shopkeeper Dynamic UPI QR Engine** — Point-of-Sale instant billing QR with direct zero-fee settlement. |

---

### ⚡ Gemini MCP Integration at a Glance

Any autonomous AI model (Google Gemini 1.5/2.0, Claude, OpenMausBot) can connect directly to a Kirana store via MCP:

```json
{
  "mcpServers": {
    "dukaanmitra": {
      "url": "http://localhost:8001/mcp"
    }
  }
}
```

**Exposed MCP Tools:**
- `get_inventory_summary` — Stock levels, threshold warnings, and inventory valuations.
- `record_voice_transaction` — AI transcription & ledger entry from shopkeeper voice notes.
- `detect_stockout_risk` — Sales velocity-based depletion prediction.
- `validate_gst_invoice` — Deterministic CGST/SGST/IGST breakdown.
- `get_magic_insights` — Top-selling products, dead stock, and cashflow analytics.

---

### 💬 Free WhatsApp Kirana Bot (Zero-Cost OpenWA)

No per-conversation Meta WhatsApp Business API charges:
1. Run `docker compose -f apps/whatsapp-gateway/docker-compose.dev.yml up -d`.
2. Open `http://localhost:2785` and scan the QR code with WhatsApp.
3. Kirana shopkeeper receives customer orders, photo bills, and voice notes instantly!

---

*Architected & Founded by [Amit Sharma (@1nsharma)](https://github.com/1nsharma).*
