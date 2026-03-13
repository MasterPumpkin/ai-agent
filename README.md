# 🤖 AI Agent Generátor & Tester (Pro školství i praxi)

Tato aplikace je profesionální nástroj postavený na **Streamlit** a **Groq API**. Pomáhá uživatelům (zejména pedagogům) nejen navrhnout neprůstřelný systémový prompt pomocí osvědčených metodik, ale rovnou ho i **otestovat v simulovaném souboji proti umělé inteligenci v roli vynalézavého žáka**.

Aplikace sází na dvoufázový proces **REFINE** při tvorbě zadání a na pokročilý **Automated Red Teaming** při jeho testování.

## 🚀 Hlavní funkce

* **📝 Generátor promptů (7 Specializovaných metodik)**:
    * **RTRI**: Metodika pro pedagogy (Role - Task - Requirements - Instructions).
    * **RISEN**: Robustní struktura pro komplexní úkoly.
    * **CO-STAR**: Ideální pro marketing a textovou tvorbu.
    * **T.A.G.**: Zaměřeno na bezpečnost a mantinely.
    * **T.R.A.C.E.**: Pro technické a programátorské úkoly.
    * **R.A.S.E.**: Klasické zadání s důrazem na roli.
    * **5S**: Srozumitelné a čisté prompty.
* **🛡️ Automatický zátěžový test (Red Teaming)**: 
    * Možnost okamžitě otestovat vygenerovaný prompt v tříkolovém dynamickém chatu.
    * AI simuluje chování "líného a zákeřného studenta", který se snaží agenta přimět k řešení úkolů za něj nebo k vyzrazení tajných instrukcí.
* **⚖️ LLM-as-a-Judge (Nezávislý Soudce)**: Po skončení zátěžového testu zanalyzuje třetí AI model celou konverzaci a vynese objektivní verdikt (Úspěch/Selhání) včetně doporučení k opravě promptu.
* **⚙️ Volba AI modelů**: Podpora přepínání mezi modely `llama-3.3-70b-versatile` (vysoká inteligence) a `llama-3.1-8b-instant` (extrémní rychlost a úspora tokenů).
* **🔒 Automatické bezpečnostní restrikce**: Generátor do každého promptu natvrdo vkládá zákazy psaní úkolů za žáky a obranu proti jailbreakingu.
* **📊 Počítadlo tokenů**: Transparentní zobrazení spotřeby API tokenů po každé akci.

## 🛠️ Instalace a spuštění

Aplikace využívá nástroj `uv` pro správu závislostí.

1.  **Klonování repozitáře**:
    ```bash
    git clone [https://github.com/MasterPumpkin/ai-agent.git](https://github.com/MasterPumpkin/ai-agent.git)
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
    *(Pokud nemáte `uv`, můžete použít standardní `pip install streamlit groq python-dotenv` a poté `streamlit run main.py`.)*

## 📖 Jak aplikaci používat

1.  **Tvorba Promptu (Záložka 1):** Vyberte metodiku, vyplňte téma a hlavní cíl asistenta. Klikněte na vygenerování. AI váš nápad rozpracuje a následně sama zkritizuje a vylepší.
2.  **Zátěžový Test (Záložka 2):** Přejděte do druhé záložky, kde se váš čerstvý prompt automaticky zkopíroval. Spusťte "simulovaný útok" a sledujte konverzaci v reálném čase.
3.  **Nasazení:** Pokud Soudce test vyhodnotí jako "ÚSPĚCH", stáhněte si prompt (nebo jej zkopírujte) a vložte jej do své oblíbené AI platformy (např. Poe.com, Coze.com nebo Mizou.com).

## 🛡️ Zabezpečení
Aplikace nikdy neukládá vaše API klíče na žádný server. Klíč je uložen pouze lokálně ve vašem prostředí nebo v paměti aktuálního sezení prohlížeče.

## 📜 Licence
Tento projekt je volně k použití (MIT License).