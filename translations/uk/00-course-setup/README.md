<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "8693a24942b670e3cb8def77f92513f9",
  "translation_date": "2025-08-21T14:11:26+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "uk"
}
-->
# Налаштування курсу

## Вступ

У цьому уроці ми розглянемо, як запускати приклади коду цього курсу.

## Клонування або форк репозиторію

Для початку, будь ласка, склонуйте або зробіть форк репозиторію GitHub. Це створить вашу власну версію матеріалів курсу, щоб ви могли запускати, тестувати та змінювати код!

Це можна зробити, натиснувши на посилання.

Ви повинні мати власну форковану версію цього курсу за наступним посиланням:

![Forked Repo](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.uk.png)

## Запуск коду

Цей курс пропонує серію Jupyter Notebook, які ви можете запускати, щоб отримати практичний досвід створення AI-агентів.

Приклади коду використовують:

**Потрібен обліковий запис GitHub - безкоштовно**:

1) Semantic Kernel Agent Framework + GitHub Models Marketplace. Позначено як (semantic-kernel.ipynb)
2) AutoGen Framework + GitHub Models Marketplace. Позначено як (autogen.ipynb)

**Потрібна підписка Azure**:
3) Azure AI Foundry + Azure AI Agent Service. Позначено як (azureaiagent.ipynb)

Ми рекомендуємо спробувати всі три типи прикладів, щоб зрозуміти, який з них найкраще підходить для вас.

Вибір варіанту визначить, які кроки налаштування вам потрібно виконати нижче:

## Вимоги

- Python 3.12+
  - **NOTE**: Якщо у вас не встановлено Python 3.12, переконайтеся, що ви його встановили. Потім створіть віртуальне середовище (venv) за допомогою python3.12, щоб забезпечити встановлення правильних версій з файлу requirements.txt.
- Обліковий запис GitHub - для доступу до GitHub Models Marketplace
- Підписка Azure - для доступу до Azure AI Foundry
- Обліковий запис Azure AI Foundry - для доступу до Azure AI Agent Service

Ми включили файл `requirements.txt` у кореневу папку цього репозиторію, який містить усі необхідні Python-пакети для запуску прикладів коду.

Ви можете встановити їх, виконавши наступну команду в терміналі в кореневій папці репозиторію:

```bash
pip install -r requirements.txt
```
Ми рекомендуємо створити віртуальне середовище Python, щоб уникнути конфліктів і проблем.

## Налаштування VSCode
Переконайтеся, що ви використовуєте правильну версію Python у VSCode.

![image](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## Налаштування для прикладів з використанням GitHub Models 

### Крок 1: Отримання вашого GitHub Personal Access Token (PAT)

Цей курс використовує GitHub Models Marketplace, що надає безкоштовний доступ до великих мовних моделей (LLMs), які ви будете використовувати для створення AI-агентів.

Щоб використовувати GitHub Models, вам потрібно створити [GitHub Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

Це можна зробити, перейшовши до вашого облікового запису GitHub.

Будь ласка, дотримуйтесь [Принципу найменших привілеїв](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) при створенні токена. Це означає, що ви повинні надати токену лише ті дозволи, які необхідні для запуску прикладів коду цього курсу.

1. Виберіть опцію `Fine-grained tokens` на лівій стороні екрана, перейшовши до **Developer settings**.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.uk.png)

    Потім виберіть `Generate new token`.

    ![Generate Token](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.uk.png)

2. Введіть описову назву для вашого токена, яка відображає його призначення, щоб його було легко ідентифікувати пізніше.

    🔐 Рекомендація щодо тривалості токена

    Рекомендована тривалість: 30 днів. 
    Для більшої безпеки ви можете вибрати коротший період, наприклад, 7 днів 🛡️. 
    Це чудовий спосіб встановити особисту мету і завершити курс, поки ваша навчальна мотивація висока 🚀.

    ![Token Name and Expiration](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.uk.png)

3. Обмежте область дії токена вашим форком цього репозиторію.

    ![Limit scope to fork repository](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.uk.png)

4. Обмежте дозволи токена: У розділі **Permissions** натисніть вкладку **Account** і натисніть кнопку "+ Add permissions". З'явиться випадаюче меню. Будь ласка, знайдіть **Models** і поставте галочку біля нього.
    ![Add Models Permission](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.uk.png)

5. Перевірте необхідні дозволи перед створенням токена. ![Verify Permissions](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.uk.png)

6. Перед створенням токена переконайтеся, що ви готові зберегти токен у безпечному місці, наприклад, у сховищі паролів, оскільки він більше не буде показаний після створення. ![Store Token Securely](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.uk.png)

Скопіюйте ваш новий токен, який ви щойно створили. Тепер ви додасте його до вашого `.env` файлу, включеного в цей курс.

### Крок 2: Створення вашого `.env` файлу

Щоб створити `.env` файл, виконайте наступну команду в терміналі.

```bash
cp .env.example .env
```

Це скопіює приклад файлу і створить `.env` у вашій директорії, де ви заповните значення для змінних середовища.

Скопіювавши ваш токен, відкрийте `.env` файл у вашому улюбленому текстовому редакторі і вставте ваш токен у поле `GITHUB_TOKEN`.
![GitHub Token Field](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.uk.png)

Тепер ви повинні бути готові до запуску прикладів коду цього курсу.

## Налаштування для прикладів з використанням Azure AI Foundry та Azure AI Agent Service

### Крок 1: Отримання вашого Azure Project Endpoint

Виконайте кроки для створення хабу і проекту в Azure AI Foundry, описані тут: [Hub resources overview](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

Після створення проекту вам потрібно буде отримати рядок підключення для вашого проекту.

Це можна зробити, перейшовши на сторінку **Overview** вашого проекту в порталі Azure AI Foundry.

![Project Connection String](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.uk.png)

### Крок 2: Створення вашого `.env` файлу

Щоб створити `.env` файл, виконайте наступну команду в терміналі.

```bash
cp .env.example .env
```

Це скопіює приклад файлу і створить `.env` у вашій директорії, де ви заповните значення для змінних середовища.

Скопіювавши ваш токен, відкрийте `.env` файл у вашому улюбленому текстовому редакторі і вставте ваш токен у поле `PROJECT_ENDPOINT`.

### Крок 3: Увійдіть до Azure

Як найкращу практику безпеки, ми будемо використовувати [автентифікацію без ключів](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) для автентифікації в Azure OpenAI за допомогою Microsoft Entra ID.

Далі відкрийте термінал і виконайте команду `az login --use-device-code`, щоб увійти до вашого облікового запису Azure.

Після входу виберіть вашу підписку в терміналі.

## Додаткові змінні середовища - Azure Search та Azure OpenAI 

Для уроку Agentic RAG - Урок 5 - є приклади, які використовують Azure Search та Azure OpenAI.

Якщо ви хочете запустити ці приклади, вам потрібно буде додати наступні змінні середовища до вашого `.env` файлу:

### Сторінка огляду (Проект)

- `AZURE_SUBSCRIPTION_ID` - Перевірте **Project details** на сторінці **Overview** вашого проекту.

- `AZURE_AI_PROJECT_NAME` - Подивіться на верхню частину сторінки **Overview** вашого проекту.

- `AZURE_OPENAI_SERVICE` - Знайдіть це на вкладці **Included capabilities** для **Azure OpenAI Service** на сторінці **Overview**.

### Центр управління

- `AZURE_OPENAI_RESOURCE_GROUP` - Перейдіть до **Project properties** на сторінці **Overview** Центру управління.

- `GLOBAL_LLM_SERVICE` - У розділі **Connected resources** знайдіть назву підключення **Azure AI Services**. Якщо не вказано, перевірте **Azure portal** у вашій групі ресурсів для назви ресурсу AI Services.

### Сторінка моделей + кінцевих точок

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - Виберіть вашу модель для вбудовування (наприклад, `text-embedding-ada-002`) і запишіть **Deployment name** з деталей моделі.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - Виберіть вашу модель для чату (наприклад, `gpt-4o-mini`) і запишіть **Deployment name** з деталей моделі.

### Портал Azure

- `AZURE_OPENAI_ENDPOINT` - Знайдіть **Azure AI services**, натисніть на нього, потім перейдіть до **Resource Management**, **Keys and Endpoint**, прокрутіть вниз до "Azure OpenAI endpoints" і скопіюйте той, що позначений "Language APIs".

- `AZURE_OPENAI_API_KEY` - З того ж екрану скопіюйте KEY 1 або KEY 2.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - Знайдіть ваш ресурс **Azure AI Search**, натисніть на нього і перегляньте **Overview**.

- `AZURE_SEARCH_API_KEY` - Потім перейдіть до **Settings**, а потім **Keys**, щоб скопіювати первинний або вторинний адміністративний ключ.

### Зовнішня веб-сторінка

- `AZURE_OPENAI_API_VERSION` - Відвідайте сторінку [API version lifecycle](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) у розділі **Latest GA API release**.

### Налаштування автентифікації без ключів

Замість того, щоб жорстко кодувати ваші облікові дані, ми будемо використовувати підключення без ключів з Azure OpenAI. Для цього ми імпортуємо `DefaultAzureCredential` і пізніше викличемо функцію `DefaultAzureCredential`, щоб отримати облікові дані.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## Виникли труднощі?

Якщо у вас виникли проблеми з виконанням цього налаштування, приєднуйтесь до нашого.

## Наступний урок

Тепер ви готові запускати код цього курсу. Бажаємо успіхів у вивченні світу AI-агентів!

[Вступ до AI-агентів та їх використання](../01-intro-to-ai-agents/README.md)

**Відмова від відповідальності**:  
Цей документ було перекладено за допомогою сервісу автоматичного перекладу [Co-op Translator](https://github.com/Azure/co-op-translator). Хоча ми прагнемо до точності, зверніть увагу, що автоматичні переклади можуть містити помилки або неточності. Оригінальний документ мовою оригіналу слід вважати авторитетним джерелом. Для критично важливої інформації рекомендується професійний людський переклад. Ми не несемо відповідальності за будь-які непорозуміння або неправильні тлумачення, що виникли внаслідок використання цього перекладу.