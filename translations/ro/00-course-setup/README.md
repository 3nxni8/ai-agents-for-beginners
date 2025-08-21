<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "8693a24942b670e3cb8def77f92513f9",
  "translation_date": "2025-08-21T13:52:52+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "ro"
}
-->
# Configurarea Cursului

## Introducere

Această lecție va acoperi modul de rulare a exemplelor de cod din acest curs.

## Clonează sau Fork-uiește acest Repositoriu

Pentru a începe, te rugăm să clonezi sau să fork-uiești Repositoriul GitHub. Acest lucru îți va crea propria versiune a materialului cursului, astfel încât să poți rula, testa și ajusta codul!

Acest lucru poate fi realizat făcând clic pe linkul către

Ar trebui să ai acum propria versiune fork-uită a acestui curs la următorul link:

![Forked Repo](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.ro.png)

## Rularea Codului

Acest curs oferă o serie de Jupyter Notebooks pe care le poți rula pentru a obține experiență practică în construirea Agenților AI.

Exemplele de cod utilizează fie:

**Necesită Cont GitHub - Gratuit**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Etichetat ca (semantic-kernel.ipynb)  
2) AutoGen Framework + GitHub Models Marketplace. Etichetat ca (autogen.ipynb)  

**Necesită Abonament Azure**:  
3) Azure AI Foundry + Azure AI Agent Service. Etichetat ca (azureaiagent.ipynb)  

Te încurajăm să încerci toate cele trei tipuri de exemple pentru a vedea care funcționează cel mai bine pentru tine.

Indiferent de opțiunea aleasă, aceasta va determina pașii de configurare pe care trebuie să îi urmezi mai jos:

## Cerințe

- Python 3.12+  
  - **NOTĂ**: Dacă nu ai instalat Python 3.12, asigură-te că îl instalezi. Apoi creează-ți mediul virtual folosind python3.12 pentru a te asigura că versiunile corecte sunt instalate din fișierul requirements.txt.  
- Un Cont GitHub - Pentru acces la GitHub Models Marketplace  
- Abonament Azure - Pentru acces la Azure AI Foundry  
- Cont Azure AI Foundry - Pentru acces la Azure AI Agent Service  

Am inclus un fișier `requirements.txt` în rădăcina acestui repositoriu care conține toate pachetele Python necesare pentru a rula exemplele de cod.

Le poți instala rulând următoarea comandă în terminalul tău, în rădăcina repositoriului:

```bash
pip install -r requirements.txt
```  
Recomandăm crearea unui mediu virtual Python pentru a evita conflictele și problemele.

## Configurarea VSCode  
Asigură-te că folosești versiunea corectă de Python în VSCode.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Configurare pentru Exemple folosind Modele GitHub  

### Pasul 1: Recuperează-ți Token-ul Personal de Acces GitHub (PAT)

Acest curs utilizează GitHub Models Marketplace, oferind acces gratuit la Modele de Limbaj de Mari Dimensiuni (LLMs) pe care le vei folosi pentru a construi Agenți AI.

Pentru a utiliza Modelele GitHub, va trebui să creezi un [Token Personal de Acces GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Acest lucru poate fi realizat accesând contul tău GitHub.

Te rugăm să urmezi [Principiul Privilegiului Minim](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) atunci când creezi token-ul. Aceasta înseamnă că ar trebui să oferi token-ului doar permisiunile necesare pentru a rula exemplele de cod din acest curs.

1. Selectează opțiunea `Fine-grained tokens` din partea stângă a ecranului, navigând la **Developer settings**  
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.ro.png)

   Apoi selectează `Generate new token`.

   ![Generate Token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.ro.png)

2. Introdu un nume descriptiv pentru token care să reflecte scopul său, astfel încât să fie ușor de identificat mai târziu.

    🔐 Recomandare pentru Durata Token-ului  

    Durată recomandată: 30 de zile  
    Pentru o securitate mai mare, poți opta pentru o perioadă mai scurtă—cum ar fi 7 zile 🛡️  
    Este o modalitate excelentă de a-ți seta un obiectiv personal și de a finaliza cursul în timp ce ești motivat să înveți 🚀.

    ![Token Name and Expiration](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.ro.png)

3. Limitează domeniul de aplicare al token-ului la fork-ul acestui repositoriu.

    ![Limit scope to fork repository](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.ro.png)

4. Restricționează permisiunile token-ului: Sub **Permissions**, dă clic pe fila **Account** și apasă butonul "+ Add permissions". Va apărea un meniu derulant. Caută **Models** și bifează caseta pentru aceasta.  
    ![Add Models Permission](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.ro.png)

5. Verifică permisiunile necesare înainte de a genera token-ul. ![Verify Permissions](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.ro.png)

6. Înainte de a genera token-ul, asigură-te că ești pregătit să stochezi token-ul într-un loc sigur, cum ar fi un manager de parole, deoarece nu va mai fi afișat după ce îl creezi. ![Store Token Securely](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.ro.png)

Copiază noul token pe care tocmai l-ai creat. Acum îl vei adăuga în fișierul `.env` inclus în acest curs.

### Pasul 2: Creează Fișierul `.env`

Pentru a crea fișierul `.env`, rulează următoarea comandă în terminalul tău.

```bash
cp .env.example .env
```

Aceasta va copia fișierul exemplu și va crea un `.env` în directorul tău, unde vei completa valorile pentru variabilele de mediu.

Cu token-ul copiat, deschide fișierul `.env` în editorul tău de text preferat și lipește token-ul în câmpul `GITHUB_TOKEN`.  
![GitHub Token Field](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.ro.png)

Acum ar trebui să poți rula exemplele de cod din acest curs.

## Configurare pentru Exemple folosind Azure AI Foundry și Azure AI Agent Service

### Pasul 1: Recuperează Endpoint-ul Proiectului Azure

Urmează pașii pentru a crea un hub și un proiect în Azure AI Foundry, găsiți aici: [Hub resources overview](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

După ce ai creat proiectul, va trebui să recuperezi șirul de conexiune pentru proiectul tău.

Acest lucru poate fi realizat accesând pagina **Overview** a proiectului tău în portalul Azure AI Foundry.

![Project Connection String](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.ro.png)

### Pasul 2: Creează Fișierul `.env`

Pentru a crea fișierul `.env`, rulează următoarea comandă în terminalul tău.

```bash
cp .env.example .env
```

Aceasta va copia fișierul exemplu și va crea un `.env` în directorul tău, unde vei completa valorile pentru variabilele de mediu.

Cu token-ul copiat, deschide fișierul `.env` în editorul tău de text preferat și lipește token-ul în câmpul `PROJECT_ENDPOINT`.

### Pasul 3: Autentificare în Azure

Ca o bună practică de securitate, vom folosi [autentificarea fără cheie](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) pentru a ne autentifica în Azure OpenAI cu Microsoft Entra ID.

Apoi, deschide un terminal și rulează `az login --use-device-code` pentru a te autentifica în contul tău Azure.

După ce te-ai autentificat, selectează abonamentul tău în terminal.

## Variabile de Mediu Suplimentare - Azure Search și Azure OpenAI

Pentru Lecția Agentic RAG - Lecția 5 - există exemple care utilizează Azure Search și Azure OpenAI.

Dacă dorești să rulezi aceste exemple, va trebui să adaugi următoarele variabile de mediu în fișierul tău `.env`:

### Pagina Overview (Proiect)

- `AZURE_SUBSCRIPTION_ID` - Verifică **Project details** pe pagina **Overview** a proiectului tău.

- `AZURE_AI_PROJECT_NAME` - Uită-te în partea de sus a paginii **Overview** pentru proiectul tău.

- `AZURE_OPENAI_SERVICE` - Găsește acest lucru în fila **Included capabilities** pentru **Azure OpenAI Service** pe pagina **Overview**.

### Management Center

- `AZURE_OPENAI_RESOURCE_GROUP` - Mergi la **Project properties** pe pagina **Overview** a **Management Center**.

- `GLOBAL_LLM_SERVICE` - Sub **Connected resources**, găsește numele conexiunii **Azure AI Services**. Dacă nu este listat, verifică **Azure portal** sub grupul tău de resurse pentru numele resursei AI Services.

### Pagina Models + Endpoints

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Selectează modelul tău de embedding (de exemplu, `text-embedding-ada-002`) și notează **Deployment name** din detaliile modelului.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Selectează modelul tău de chat (de exemplu, `gpt-4o-mini`) și notează **Deployment name** din detaliile modelului.

### Portalul Azure

- `AZURE_OPENAI_ENDPOINT` - Caută **Azure AI services**, dă clic pe acesta, apoi mergi la **Resource Management**, **Keys and Endpoint**, derulează în jos la "Azure OpenAI endpoints" și copiază-l pe cel care spune "Language APIs".

- `AZURE_OPENAI_API_KEY` - Din același ecran, copiază KEY 1 sau KEY 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Găsește resursa ta **Azure AI Search**, dă clic pe ea și vezi **Overview**.

- `AZURE_SEARCH_API_KEY` - Apoi mergi la **Settings** și apoi **Keys** pentru a copia cheia de administrator primară sau secundară.

### Pagină Externă

- `AZURE_OPENAI_API_VERSION` - Vizitează pagina [API version lifecycle](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) sub **Latest GA API release**.

### Configurare autentificare fără cheie

În loc să codificăm credențialele, vom folosi o conexiune fără cheie cu Azure OpenAI. Pentru a face acest lucru, vom importa `DefaultAzureCredential` și mai târziu vom apela funcția `DefaultAzureCredential` pentru a obține credențialul.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Probleme?

Dacă întâmpini probleme în rularea acestei configurări, intră pe

## Lecția Următoare

Acum ești pregătit să rulezi codul pentru acest curs. Îți dorim succes în explorarea lumii Agenților AI!

[Introducere în Agenții AI și Cazuri de Utilizare](../01-intro-to-ai-agents/README.md)

**Declinarea responsabilității**:  
Acest document a fost tradus utilizând serviciul de traducere AI [Co-op Translator](https://github.com/Azure/co-op-translator). Deși depunem eforturi pentru a asigura acuratețea, vă rugăm să rețineți că traducerile automate pot conține erori sau inexactități. Documentul original în limba sa nativă ar trebui considerat sursa autoritară. Pentru informații critice, se recomandă traducerea umană realizată de profesioniști. Nu ne asumăm răspunderea pentru eventualele neînțelegeri sau interpretări greșite care pot apărea din utilizarea acestei traduceri.