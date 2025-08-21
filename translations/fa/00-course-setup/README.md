<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "8693a24942b670e3cb8def77f92513f9",
  "translation_date": "2025-08-21T12:16:20+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "fa"
}
-->
# راه‌اندازی دوره

## مقدمه

در این درس، نحوه اجرای نمونه کدهای این دوره را بررسی خواهیم کرد.

## کلون یا فورک کردن این مخزن

برای شروع، لطفاً این مخزن GitHub را کلون یا فورک کنید. این کار نسخه‌ای از محتوای دوره را برای شما ایجاد می‌کند تا بتوانید کدها را اجرا، آزمایش و تغییر دهید!

این کار با کلیک روی لینک زیر انجام می‌شود:

![مخزن فورک‌شده](../../../translated_images/forked-repo.33f27ca1901baa6a5e13ec3eb1f0ddd3a44d936d91cc8cfb19bfdb9688bd2c3d.fa.png)

## اجرای کد

این دوره مجموعه‌ای از نوت‌بوک‌های Jupyter ارائه می‌دهد که می‌توانید با استفاده از آن‌ها تجربه عملی در ساخت عوامل هوش مصنوعی کسب کنید.

نمونه کدها از یکی از موارد زیر استفاده می‌کنند:

**نیازمند حساب GitHub - رایگان**:

1) چارچوب Semantic Kernel Agent + بازار مدل‌های GitHub. با برچسب (semantic-kernel.ipynb)
2) چارچوب AutoGen + بازار مدل‌های GitHub. با برچسب (autogen.ipynb)

**نیازمند اشتراک Azure**:
3) Azure AI Foundry + سرویس Azure AI Agent. با برچسب (azureaiagent.ipynb)

ما شما را تشویق می‌کنیم که هر سه نوع مثال را امتحان کنید تا ببینید کدام یک برای شما بهتر عمل می‌کند.

هر گزینه‌ای که انتخاب کنید، تعیین می‌کند که کدام مراحل راه‌اندازی را باید در ادامه دنبال کنید:

## پیش‌نیازها

- پایتون 3.12+
  - **توجه**: اگر پایتون 3.12 نصب نشده است، مطمئن شوید که آن را نصب کنید. سپس محیط مجازی خود را با استفاده از python3.12 ایجاد کنید تا نسخه‌های صحیح از فایل requirements.txt نصب شوند.
- حساب GitHub - برای دسترسی به بازار مدل‌های GitHub
- اشتراک Azure - برای دسترسی به Azure AI Foundry
- حساب Azure AI Foundry - برای دسترسی به سرویس Azure AI Agent

ما یک فایل `requirements.txt` در ریشه این مخزن قرار داده‌ایم که شامل تمام بسته‌های پایتون مورد نیاز برای اجرای نمونه کدها است.

می‌توانید آن‌ها را با اجرای دستور زیر در ترمینال در ریشه مخزن نصب کنید:

```bash
pip install -r requirements.txt
```

ما توصیه می‌کنیم یک محیط مجازی پایتون ایجاد کنید تا از هرگونه تداخل و مشکل جلوگیری شود.

## راه‌اندازی VSCode

مطمئن شوید که از نسخه صحیح پایتون در VSCode استفاده می‌کنید.

![تصویر](https://github.com/user-attachments/assets/a85e776c-2edb-4331-ae5b-6bfdfb98ee0e)

## راه‌اندازی برای نمونه‌ها با استفاده از مدل‌های GitHub

### مرحله 1: دریافت توکن دسترسی شخصی (PAT) GitHub

این دوره از بازار مدل‌های GitHub استفاده می‌کند که دسترسی رایگان به مدل‌های زبان بزرگ (LLM) را فراهم می‌کند که شما از آن‌ها برای ساخت عوامل هوش مصنوعی استفاده خواهید کرد.

برای استفاده از مدل‌های GitHub، باید یک [توکن دسترسی شخصی GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) ایجاد کنید.

این کار با رفتن به حساب کاربری GitHub شما انجام می‌شود.

لطفاً هنگام ایجاد توکن، [اصل حداقل امتیاز](https://docs.github.com/en/get-started/learning-to-code/storing-your-secrets-safely) را رعایت کنید. این بدان معناست که باید فقط مجوزهای مورد نیاز برای اجرای نمونه کدهای این دوره را به توکن بدهید.

1. گزینه `Fine-grained tokens` را در سمت چپ صفحه خود با رفتن به **تنظیمات توسعه‌دهنده** انتخاب کنید.
   ![](../../../translated_images/profile_developer_settings.410a859fe749c755c859d414294c5908e307222b2c61819c3203bbeed4470e25.fa.png)

   سپس گزینه `Generate new token` را انتخاب کنید.

   ![ایجاد توکن](../../../translated_images/fga_new_token.1c1a234afe202ab37483944a291ee80c1868e1e78082fd6bd4180fea5d5a15b4.fa.png)

2. یک نام توصیفی برای توکن خود وارد کنید که هدف آن را منعکس کند و شناسایی آن را در آینده آسان کند.

    🔐 **توصیه برای مدت زمان توکن**

    مدت زمان پیشنهادی: 30 روز  
    برای امنیت بیشتر، می‌توانید مدت زمان کوتاه‌تری مانند 7 روز انتخاب کنید 🛡️  
    این یک روش عالی برای تعیین هدف شخصی و تکمیل دوره در حالی است که انگیزه یادگیری شما بالا است 🚀.

    ![نام و تاریخ انقضای توکن](../../../translated_images/token-name-expiry-date.a095fb0de63868640a4c82d6b1bbc92b482930a663917a5983a3c7cd1ef86b77.fa.png)

3. دامنه توکن را به فورک این مخزن محدود کنید.

    ![محدود کردن دامنه به مخزن فورک‌شده](../../../translated_images/token_repository_limit.924ade5e11d9d8bb6cd21293987e4579dea860e2ba66d607fb46e49524d53644.fa.png)

4. مجوزهای توکن را محدود کنید: در بخش **Permissions**، روی تب **Account** کلیک کنید و دکمه "+ Add permissions" را بزنید. یک منوی کشویی ظاهر می‌شود. لطفاً **Models** را جستجو کرده و تیک آن را بزنید.
    ![افزودن مجوز مدل‌ها](../../../translated_images/add_models_permissions.c0c44ed8b40fc143dc87792da9097d715b7de938354e8f771d65416ecc7816b8.fa.png)

5. قبل از ایجاد توکن، مجوزهای مورد نیاز را بررسی کنید. ![بررسی مجوزها](../../../translated_images/verify_permissions.06bd9e43987a8b219f171bbcf519e45ababae35b844f5e9757e10afcb619b936.fa.png)

6. قبل از ایجاد توکن، مطمئن شوید که آماده هستید تا توکن را در مکانی امن مانند یک مدیر رمز عبور ذخیره کنید، زیرا پس از ایجاد دیگر نمایش داده نمی‌شود. ![ذخیره امن توکن](../../../translated_images/store_token_securely.08ee2274c6ad6caf3482f1cd1bad7ca3fdca1ce737bc485bfa6499c84297c789.fa.png)

توکن جدیدی که ایجاد کرده‌اید را کپی کنید. اکنون باید این توکن را به فایل `.env` موجود در این دوره اضافه کنید.

### مرحله 2: ایجاد فایل `.env`

برای ایجاد فایل `.env` دستور زیر را در ترمینال اجرا کنید:

```bash
cp .env.example .env
```

این دستور فایل نمونه را کپی کرده و یک `.env` در دایرکتوری شما ایجاد می‌کند که در آن مقادیر متغیرهای محیطی را پر می‌کنید.

با کپی کردن توکن خود، فایل `.env` را در ویرایشگر متن مورد علاقه خود باز کنید و توکن خود را در فیلد `GITHUB_TOKEN` جای‌گذاری کنید.
![فیلد توکن GitHub](../../../translated_images/github_token_field.20491ed3224b5f4ab24d10ced7a68c4aba2948fe8999cfc8675edaa16f5e5681.fa.png)

اکنون باید بتوانید نمونه کدهای این دوره را اجرا کنید.

## راه‌اندازی برای نمونه‌ها با استفاده از Azure AI Foundry و Azure AI Agent Service

### مرحله 1: دریافت نقطه پایانی پروژه Azure

مراحل ایجاد یک هاب و پروژه در Azure AI Foundry را از اینجا دنبال کنید: [بررسی اجمالی منابع هاب](https://learn.microsoft.com/en-us/azure/ai-foundry/concepts/ai-resources)

پس از ایجاد پروژه، باید رشته اتصال پروژه خود را دریافت کنید.

این کار با رفتن به صفحه **Overview** پروژه در پورتال Azure AI Foundry انجام می‌شود.

![رشته اتصال پروژه](../../../translated_images/project-endpoint.8cf04c9975bbfbf18f6447a599550edb052e52264fb7124d04a12e6175e330a5.fa.png)

### مرحله 2: ایجاد فایل `.env`

برای ایجاد فایل `.env` دستور زیر را در ترمینال اجرا کنید:

```bash
cp .env.example .env
```

این دستور فایل نمونه را کپی کرده و یک `.env` در دایرکتوری شما ایجاد می‌کند که در آن مقادیر متغیرهای محیطی را پر می‌کنید.

با کپی کردن توکن خود، فایل `.env` را در ویرایشگر متن مورد علاقه خود باز کنید و توکن خود را در فیلد `PROJECT_ENDPOINT` جای‌گذاری کنید.

### مرحله 3: ورود به Azure

به عنوان یک بهترین روش امنیتی، از [احراز هویت بدون کلید](https://learn.microsoft.com/azure/developer/ai/keyless-connections?tabs=csharp%2Cazure-cli?WT.mc_id=academic-105485-koreyst) برای احراز هویت به Azure OpenAI با Microsoft Entra ID استفاده خواهیم کرد.

سپس یک ترمینال باز کنید و دستور `az login --use-device-code` را برای ورود به حساب Azure خود اجرا کنید.

پس از ورود، اشتراک خود را در ترمینال انتخاب کنید.

## متغیرهای محیطی اضافی - Azure Search و Azure OpenAI

برای درس Agentic RAG - درس 5 - نمونه‌هایی وجود دارند که از Azure Search و Azure OpenAI استفاده می‌کنند.

اگر می‌خواهید این نمونه‌ها را اجرا کنید، باید متغیرهای محیطی زیر را به فایل `.env` خود اضافه کنید:

### صفحه Overview (پروژه)

- `AZURE_SUBSCRIPTION_ID` - جزئیات پروژه را در صفحه **Overview** پروژه بررسی کنید.

- `AZURE_AI_PROJECT_NAME` - به بالای صفحه **Overview** پروژه نگاه کنید.

- `AZURE_OPENAI_SERVICE` - این مورد را در تب **Included capabilities** برای **Azure OpenAI Service** در صفحه **Overview** پیدا کنید.

### مرکز مدیریت

- `AZURE_OPENAI_RESOURCE_GROUP` - به **Project properties** در صفحه **Overview** مرکز مدیریت بروید.

- `GLOBAL_LLM_SERVICE` - در بخش **Connected resources**، نام اتصال **Azure AI Services** را پیدا کنید. اگر لیست نشده است، در **پورتال Azure** زیر گروه منابع خود، نام منبع AI Services را بررسی کنید.

### صفحه Models + Endpoints

- `AZURE_OPENAI_EMBEDDING_DEPLOYMENT_NAME` - مدل embedding خود را انتخاب کنید (مثلاً `text-embedding-ada-002`) و **نام استقرار** را از جزئیات مدل یادداشت کنید.

- `AZURE_OPENAI_CHAT_DEPLOYMENT_NAME` - مدل چت خود را انتخاب کنید (مثلاً `gpt-4o-mini`) و **نام استقرار** را از جزئیات مدل یادداشت کنید.

### پورتال Azure

- `AZURE_OPENAI_ENDPOINT` - به دنبال **Azure AI services** بگردید، روی آن کلیک کنید، سپس به **Resource Management**، **Keys and Endpoint** بروید، به پایین اسکرول کنید تا "Azure OpenAI endpoints" را پیدا کنید و آن را کپی کنید.

- `AZURE_OPENAI_API_KEY` - از همان صفحه، کلید 1 یا کلید 2 را کپی کنید.

- `AZURE_SEARCH_SERVICE_ENDPOINT` - منبع **Azure AI Search** خود را پیدا کنید، روی آن کلیک کنید و به **Overview** بروید.

- `AZURE_SEARCH_API_KEY` - سپس به **Settings** و سپس **Keys** بروید تا کلید اصلی یا ثانویه مدیر را کپی کنید.

### صفحه خارجی

- `AZURE_OPENAI_API_VERSION` - به صفحه [چرخه عمر نسخه API](https://learn.microsoft.com/en-us/azure/ai-services/openai/api-version-deprecation#latest-ga-api-release) در بخش **آخرین نسخه GA API** مراجعه کنید.

### راه‌اندازی احراز هویت بدون کلید

به جای کدنویسی سخت‌افزاری اعتبارنامه‌ها، از اتصال بدون کلید با Azure OpenAI استفاده خواهیم کرد. برای این کار، `DefaultAzureCredential` را وارد کرده و بعداً تابع `DefaultAzureCredential` را برای دریافت اعتبارنامه فراخوانی می‌کنیم.

```python
from azure.identity import DefaultAzureCredential, InteractiveBrowserCredential
```

## جایی گیر کرده‌اید؟

اگر در اجرای این راه‌اندازی مشکلی دارید، به ... 

## درس بعدی

اکنون آماده هستید تا کدهای این دوره را اجرا کنید. از یادگیری درباره دنیای عوامل هوش مصنوعی لذت ببرید!

[مقدمه‌ای بر عوامل هوش مصنوعی و موارد استفاده از آن‌ها](../01-intro-to-ai-agents/README.md)

**سلب مسئولیت**:  
این سند با استفاده از سرویس ترجمه هوش مصنوعی [Co-op Translator](https://github.com/Azure/co-op-translator) ترجمه شده است. در حالی که ما برای دقت تلاش می‌کنیم، لطفاً توجه داشته باشید که ترجمه‌های خودکار ممکن است شامل خطاها یا نادقتی‌ها باشند. سند اصلی به زبان اصلی آن باید به عنوان منبع معتبر در نظر گرفته شود. برای اطلاعات حساس، ترجمه حرفه‌ای انسانی توصیه می‌شود. ما هیچ مسئولیتی در قبال سوءتفاهم‌ها یا تفسیرهای نادرست ناشی از استفاده از این ترجمه نداریم.