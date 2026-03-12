# 🎯 AI Prompt Generator (RTRI, RISEN & more)

Tato aplikace je profesionální nástroj postavený na **Streamlit** a **Groq API**, který využívá moderní metodiky (frameworky) prompt inženýringu pro tvorbu neprůstřelných systémových promptů pro AI asistenty.

Aplikace sází na dvoufázový proces **REFINE** (Evaluation & Iterative Refinement) – AI nejprve navrhne strukturu podle zvolené metodiky a následně ji kriticky zhodnotí a vylepší.

## 🚀 Hlavní funkce

*   **7 Specializovaných metodik**:
    *   **RTRI**: Metodika pro pedagogy (Role - Task - Requirements - Instructions).
    *   **RISEN**: Robustní struktura pro komplexní úkoly.
    *   **CO-STAR**: Ideální pro marketing a textovou tvorbu (Context - Objective - Style - Tone - Audience - Response).
    *   **T.A.G.**: Zaměřeno na bezpečnost a mantinely (Task - Audience - Guardrails).
    *   **T.R.A.C.E.**: Pro technické a programátorské úkoly.
    *   **R.A.S.E.**: Klasické zadání s důrazem na roli.
    *   **5S**: Srozumitelné a čisté prompty.
*   **Dvoufázová optimalizace**: Každý prompt prochází automatickou kontrolou a iterativním vylepšením.
*   **Dynamické rozhraní**: Formulář se přizpůsobuje zvolené metodice a nabízí relevantní nápovědu i příklady.
*   **Export do Markdownu**: Vygenerované prompty lze stáhnout jako soubor `.md`.

## 🛠️ Instalace a spuštění

Aplikace využívá nástroj `uv` pro správu závislostí.

1.  **Klonování repozitáře**:
    ```bash
    git clone https://github.com/MasterPumpkin/ai-agent.git
    cd ai-agent
    ```

2.  **Nastavení API klíče**:
    Vytvořte soubor `.env` v kořenovém adresáři a vložte svůj Groq API klíč:
    ```env
    GROQ_API_KEY=vase_groq_api_klic_zde
    ```

3.  **Spuštění aplikace**:
    ```bash
    uv run streamlit run main.py
    ```
    *(Pokud nemáte `uv`, můžete použít standardní `pip install -r requirements.txt` nebo `pip install streamlit groq python-dotenv`.)*

## 📖 Použité metodiky

Detailní popisy a příklady všech metodik jsou dostupné přímo v rozhraní aplikace pod sekcí **„Detailní přehled metodik“**.

## 🛡️ Zabezpečení
Aplikace nikdy neukládá vaše API klíče na žádný server. Klíč je uložen pouze lokálně ve vašem prostředí nebo v paměti sezení prohlížeče.

## 📜 Licence
Tento projekt je volně k použití (MIT License).
