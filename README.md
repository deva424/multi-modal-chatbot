#  Multi-Modal Gemini Chatbot

A professional-grade, multi-modal conversational AI built with Streamlit and Google Gemini 3. This chatbot seamlessly integrates visual understanding and high-fidelity image generation (Nano Banana 2) into a single interface.

##  Problem Statement
In the current landscape of AI tools, users often find themselves switching between different platforms to perform diverse tasks: one for textual reasoning, another for visual analysis (OCR/Object Detection), and a third for image generation (DALL-E/Midjourney). This fragmentation leads to:
- **Disrupted Workflow:** Constant context-switching between tabs and apps.
- **Data Silos:** Difficulty in using the context of a generated image for a follow-up conversation.
- **Efficiency Loss:** The lack of an "interleaved" system that understands images and text as a single unified input.

##  Methodology
This project implements a **Unified Multi-Modal Architecture** using the Google GenAI ecosystem:
1.  **Input Layer:** A Streamlit-based reactive UI that captures user text and binary image data.
2.  **Processing Engine (Gemini 3 Flash):** Utilizes a single transformer architecture that treats images and text as tokens of equal priority, allowing for nuanced visual reasoning.
3.  **Specialized Generation (Nano Banana 2):** When the system detects a "generation intent" (via keyword or logic), it routes the prompt to the `gemini-3.1-flash-image-preview` model to create high-resolution visuals.
4.  **Tunnelling & Deployment:** Leveraging **Cloudflare Tunnels** to expose local Streamlit instances securely to the web, bypassing traditional firewall and NAT constraints.

##  Requirements
### API & Cloud
- **Google Gemini API Key:** (Gemini 3 access via Google AI Studio)
- **Cloudflare Account:** For `cloudflared` tunnelling.

### Libraries
- `google-genai`: The primary SDK for Gemini 3.
- `streamlit`: Web interface and state management.
- `Pillow (PIL)`: Image processing and formatting.
- `python-dotenv`: Environment variable management.

##  Professional Implementation
To run this in a professional environment:
1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/your-username/gemini-multimodal-bot.git
    cd gemini-multimodal-bot
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Environment Setup:** Create a `.env` file and add: `GOOGLE_API_KEY=your_key_here`
4.  **Execution:** ```bash
    streamlit run app.py
    ```

---
*Developed for the 2026 AI Ecosystem using Gemini 3 and Cloudflare.*
