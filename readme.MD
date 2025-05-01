Wat is het project 
Wat is de huidige status
Wat dingen die bereikt zijn 
Wat moet er nog gebeuren



**SupplyLens**  
**AI-Enhanced Supply Chain Mapping System**  
*“Turning fragmented data into full-spectrum supply visibility”*

Presented by: [Your Name / Team / Organization]  
Windesheim University – Value Chain Hackers

---

## 1️⃣ **What is it?**

> “Every supply chain starts in the dark.”

- Companies face massive pressure to map ESG risks across their supply chains.  
- But most data is buried in reports, PDFs, supplier sites, and disconnected systems.
- ConflictChain turns that chaos into clarity.

**ConflictChain is an AI-powered system that**:
- Crawls unstructured sources
- Builds a supply graph from extracted entities
- Stores it in a unified graph database
- Lets you query it in plain language

> It’s like Google Maps for your supply chain — with an AI co-pilot.

---

## 2️⃣ **How does it work?**

### 🧠 Step 1: **Collect the Data**
- Use `Crawl4AI` or your own PDF/web crawler  
- Ingest ESG reports, supplier lists, trade documents  
- Extract entities: companies, products, countries

→ Output: Raw text + metadata, structured for reasoning

---

### 🧠 Step 2: **Embed and Reason**
- Feed text into an LLM (Ollama, GPT-4, LM Studio)
- Generate knowledge graph triples:  
  _EasyFiets → sources lithium from → Chinese Mining Corp_
- Use `pgvector` or `Qdrant` to store semantic embeddings
- LLM rates relationship validity and strength

→ Output: A clean, annotated map of who connects to whom — and why

---

### 🗃 Step 3: **Store and Structure**
- All data lives inside **PostgreSQL**  
  - `Apache AGE`: handles graph relationships  
  - `pgvector`: powers semantic search  
  - `JSONB`: stores rich ESG metadata

→ One database, one interface, no microservice spaghetti

---

### 🗣️ Step 4: **Query in Natural Language**
- Use **LangChain or LlamaIndex** to connect the graph to an LLM  
- User types:  
  _“Where is lithium for the electronic bike from EasyFiets coming from most likely?”_
- LLM turns that into a graph query → matches nodes and embeddings → gives a readable answer

→ Anyone can ask — no code, no SQL, just insight

---

## 3️⃣ **Are you sure?**

- 🧾 Based on **proven tools**: PostgreSQL, Apache AGE, LangChain, pgvector  
- 📊 Aligned with **EU regulation**: CSRD and CSDDD demand visibility past Tier 1  
- 🧪 Research-backed: LLM + KG approaches boost supply mapping depth by 3x (Cambridge, 2024)

**It’s open-source. Modular. Auditable.**  
And it’s the infrastructure we need to map the unmappable.

---

## 4️⃣ **Can you do it?**

Yes — and here’s how we’re planning it:

- 💻 All components containerized with Docker Compose
- 🔄 `start_services.py` orchestrates environment with profiles (CPU, GPU)
- 🔐 HAProxy or Caddy provides HTTPS + subpath routing on  
  `https://aisandbox1.ixworx.nl`
- 🧠 Stack already running in development:  
  Apache AGE + pgvector + LangChain + Supabase + n8n

**Now we’re seeking pilot partners to deploy it in the real world.**

---

## 5️⃣ **What do you want?**

We’re ready to test this in live environments.

We’re looking for:
- 🎓 **Academic partners** to stress test the system with real research data  
- 🏢 **Companies** who want supply chain transparency without the black box  
- 📈 **Investors and grantmakers** to fund the open-source build-out  
- 🌍 **NGOs and EU bodies** to help us align with real reporting needs

> ConflictChain makes visibility a utility.  
> Help us turn data chaos into clean, defensible ESG reporting.

---

## 📬 Contact

**Christiaan Verhoef**  
ConflictChain – Windesheim University  
📧 christiaan@valuechainhackers.xyz  
🌐 [https://aisandbox1.ixworx.nl](https://aisandbox1.ixworx.nl)  

---

Would you like this packaged into:
- A `.Rmd` ioslides presentation?  
- A slide-deck-style PDF/Quarto version?  
- Or a website-ready pitch layout?

Let me know how you want to present this.