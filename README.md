# 🏆 Murf AI Voice Agent Challenge: 10-Day Project Portfolio

## 🚀 The Real-Time Voice Revolution

This repository showcases the successful completion of the **Murf AI Voice Agent Challenge**, a 10-day initiative dedicated to building advanced, real-time conversational AI applications. The project suite demonstrates mastery in integrating low-latency voice infrastructure, sophisticated LLM-based reasoning, and complex state management across a variety of real-world and creative use cases.

A primary technical focus was achieving **ultra-low latency**, seamless voice-first interaction by leveraging the **Murf Falcon Text-to-Speech (TTS) API** for instant, natural-sounding audio responses.

---

## 🛠️ Core Technology Stack and Architecture

The solutions are built on a robust, modern AI pipeline, emphasizing modularity, performance, and intelligent tool-use through **Gemini's Function Calling**.

| Component | Technology | Technical Contribution |
| :--- | :--- | :--- |
| **TTS Engine** | **Murf AI Falcon API** | Achieved near-zero latency, crucial for spontaneous, fluid, real-time dialogue and dynamic voice-persona switching. |
| **Voice Platform** | **LiveKit Agents SDK** | Manages the full media pipeline (STT, VAD, LLM, TTS) and WebRTC signaling for robust, scalable voice connectivity. |
| **AI Brain** | **Google Gemini 2.5 Flash** | Powers intent recognition, dynamic tool selection, complex reasoning, and structured output generation across all 10 agents. |
| **State Management** | **Python Function Tools** | Implements all business logic (e.g., order state, inventory, qualification logic) external to the LLM, ensuring reliability and testability. |

---

## 🎯 Detailed Challenge Breakdown: 10 Days, 10 Agents

Each agent met the core challenge requirements and successfully incorporated advanced, real-world features, as proven by the respective JSON/Database persistence logs.

| Day | Agent Theme | Persona | Core Achievement & Persistence | Advanced Technical Implementation |
| :---: | :--- | :--- | :--- | :--- |
| **Day 1** | Starter Agent | General | Successfully set up the LiveKit/Murf/Gemini baseline voice pipeline. | Focus on pipeline integration and verifying the low-latency loop. |
| **Day 2** | Coffee Shop Barista | Friendly Barista ('Shadow Brews') | Implemented stateful order gathering using the `place_coffee_order` tool. Final order data saved to `day2_order_summary.json`. | Enforced a full order state (`drinkType`, `size`, `milk`, `extras`, `name`) before tool execution. |
| **Day 3** | Health & Wellness Companion | Supportive Companion ('Luna') | Designed for daily, contextual check-ins. Conversation history is managed by `get_past_checkin_summary` and `save_checkin_data` tools. | Achieved **Stateful Conversation** by reading historical data from `wellness_log.json` to inform the current session's dialogue. |
| **Day 4** | Active Recall Coach | Dynamic Tutor | Implemented the "Teach-the-Tutor" learning model with three distinct personas (Teacher, Quizmaster, Tutor). | Utilized the `set_learning_mode` tool to dynamically call `session.tts.update_options(voice=voice_id)` for **real-time persona switching** (Murf voices: Matthew, Alicia, Ken). |
| **Day 5** | SDR / Lead Capture | Sales Development Rep (Tata Neu) | Answered FAQs using an internal knowledge base and collected 7 key lead fields. Data saved to `captured_lead_data.json`. | Developed the `clean_email_input` utility function to mitigate **Speech-to-Text (ASR) transcription errors** on sensitive data like email addresses. |
| **Day 6** | Fraud Alert Agent | Professional Bank Rep | Implemented a secure verification and transaction review flow. Used stored security data (e.g., city of birth: 'surat') to verify the user ('Shadow'). | Successfully performed **database lookups and updates** (simulated JSON/SQLite) to mark the fraud case status as `confirmed_safe` or `confirmed_fraud`. |
| **Day 7** | Food & Grocery Ordering | Shopping Assistant ('Luna') | Managed dynamic `CART` contents, supported item additions, removals, and price calculations. | Achieved **Advanced Goals 1 & 2** by implementing **Mock Order Tracking** (time-based status progression via `StoreManager` class) and maintaining a persistent Order History in `orders.json`. |
| **Day 8** | Voice Game Master (RPG) | Mysterious Game Master ('Benimaru') | Created an interactive D&D-style narrative engine guided by player voice commands. | Implemented the **Advanced Goal: JSON World State**, maintaining a Python `WorldState` class to track character HP, inventory, and location, supported by tools like `roll_dice` and `save_game`. |
| **Day 9** | E-commerce Agent | Shopping Assistant ('Diablo') | Implemented a structured product browsing and ordering flow inspired by the Agentic Commerce Protocol (ACP). | Achieved **Advanced Goal: Multi-Item Cart & Checkout**, using separate `add_item_to_cart` and `checkout_cart` tools to process complex, consolidated orders. |
| **Day 10** | Voice Improv Battle Host | High-Energy Game Show Host ('Luna') | Hosted a spontaneous, multi-round improv game with varied, realistic critiques and summaries. | Demonstrated the pinnacle of low-latency performance with a **Dynamic Game State Machine** to manage unscripted dialogue flow and reaction timing. |
---

## 🔗 Project Structure and Next Steps

The project follows the standard LiveKit Agents repository structure, with individual agent solutions placed in thematic directories.

### Directories

* **`challenges/`**: Original task descriptions for all 10 days.
* **`types of agent/`**: Contains the source code (`agent.py`, `readme.md`, and data files) for each day's solution.

### Local Development

For instructions on setting up the environment, obtaining the necessary API keys (Murf, LiveKit, Gemini), and running the agents locally, please refer to the main repository `README.md` and the `backend/AGENTS.md` file.
