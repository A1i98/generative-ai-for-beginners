<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "f1413b349a65b4e9eda3f48807656a6d",
  "translation_date": "2025-10-11T11:42:48+00:00",
  "source_file": "00-course-setup/README.md",
  "language_code": "ta"
}
-->
# இந்த பாடத்தை தொடங்குவது

இந்த பாடத்தை நீங்கள் தொடங்குவதற்கு மிகவும் உற்சாகமாக உள்ளோம், மேலும் Generative AI மூலம் நீங்கள் உருவாக்குவதற்கு உந்துதல் பெறுவது எப்படி என்பதை பார்க்க!

உங்கள் வெற்றியை உறுதிப்படுத்த, இந்த பக்கம் அமைப்பு படிகள், தொழில்நுட்ப தேவைகள் மற்றும் உதவி தேவைப்பட்டால் எங்கு பெறுவது என்பதை விளக்குகிறது.

## அமைப்பு படிகள்

இந்த பாடத்தை தொடங்க, நீங்கள் கீழே உள்ள படிகளை முடிக்க வேண்டும்.

### 1. இந்த Repo-வை Fork செய்யவும்

[இந்த Repo-வை முழுமையாக Fork செய்யவும்](https://github.com/microsoft/generative-ai-for-beginners/fork?WT.mc_id=academic-105485-koreyst) உங்கள் சொந்த GitHub கணக்கில், இதனால் நீங்கள் எந்த கோடையும் மாற்றி சவால்களை முடிக்க முடியும். மேலும் [இந்த Repo-வை Star (🌟) செய்யவும்](https://docs.github.com/en/get-started/exploring-projects-on-github/saving-repositories-with-stars?WT.mc_id=academic-105485-koreyst), இதனால் இதை மற்றும் தொடர்புடைய Repo-களை எளிதாக கண்டுபிடிக்க முடியும்.

### 2. Codespace உருவாக்கவும்

கோடுகளை இயக்கும்போது எந்த சார்பு பிரச்சனைகளையும் தவிர்க்க, இந்த பாடத்தை [GitHub Codespaces](https://github.com/features/codespaces?WT.mc_id=academic-105485-koreyst) இல் இயக்க பரிந்துரைக்கிறோம்.

உங்கள் Fork-இல்: **Code -> Codespaces -> New on main**

![Codespace உருவாக்குவதற்கான பொத்தான்கள் காட்டும் உரையாடல்](../../../00-course-setup/images/who-will-pay.webp)

#### 2.1 ஒரு ரகசியத்தை சேர்க்கவும்

1. ⚙️ Gear ஐகான் -> Command Pallete-> Codespaces : Manage user secret -> Add a new secret.
2. Name OPENAI_API_KEY, உங்கள் key-ஐ paste செய்யவும், Save செய்யவும்.

### 3. அடுத்தது என்ன?

| நான் செய்ய விரும்புகிறேன்... | செல்ல வேண்டிய இடம்...                                                      |
|----------------------------|---------------------------------------------------------------------------|
| பாடம் 1 தொடங்க            | [`01-introduction-to-genai`](../01-introduction-to-genai/README.md)       |
| ஆஃப்லைனில் வேலை செய்ய     | [`setup-local.md`](02-setup-local.md)                                     |
| LLM Provider அமைக்க       | [`providers.md`](providers.md)                                           |
| மற்ற மாணவர்களை சந்திக்க    | [எங்கள் Discord-ஐ சேரவும்](https://aka.ms/genai-discord?WT.mc_id=academic-105485-koreyst) |

## பிரச்சனைகளை சரி செய்ய

| அறிகுறி                                   | தீர்வு                                                           |
|-------------------------------------------|-----------------------------------------------------------------|
| Container build 10 நிமிடத்திற்கு மேல் சிக்கியது | **Codespaces ➜ “Rebuild Container”**                            |
| `python: command not found`               | Terminal இணைக்கவில்லை; **+** ➜ *bash* ஐ கிளிக் செய்யவும்       |
| OpenAI-இல் இருந்து `401 Unauthorized`     | தவறான / காலாவதியான `OPENAI_API_KEY`                            |
| VS Code “Dev container mounting…” காட்டுகிறது | உலாவி tab-ஐ Refresh செய்யவும்—Codespaces சில நேரங்களில் இணைப்பை இழக்கிறது |
| Notebook kernel காணவில்லை                | Notebook menu ➜ **Kernel ▸ Select Kernel ▸ Python 3**           |

   Unix அடிப்படையிலான அமைப்புகள்:

   ```bash
   touch .env
   ```

   Windows:

   ```cmd
   echo . > .env
   ```

3. **`.env` கோப்பை திருத்தவும்**: `.env` கோப்பை ஒரு text editor (எ.கா., VS Code, Notepad++ அல்லது வேறு editor) இல் திறக்கவும். கீழே உள்ள வரியை கோப்பில் சேர்க்கவும், `your_github_token_here` ஐ உங்கள் உண்மையான GitHub token-ஆல் மாற்றவும்:

   ```env
   GITHUB_TOKEN=your_github_token_here
   ```

4. **கோப்பை சேமிக்கவும்**: மாற்றங்களை சேமித்து text editor-ஐ மூடவும்.

5. **`python-dotenv` ஐ நிறுவவும்**: `.env` கோப்பிலிருந்து உங்கள் Python பயன்பாட்டிற்கு சூழல் மாறிகளை ஏற்ற `python-dotenv` package-ஐ நிறுவ வேண்டும். இதை `pip` மூலம் நிறுவலாம்:

   ```bash
   pip install python-dotenv
   ```

6. **Python script-இல் சூழல் மாறிகளை ஏற்றவும்**: உங்கள் Python script-இல், `.env` கோப்பிலிருந்து சூழல் மாறிகளை ஏற்ற `python-dotenv` package-ஐ பயன்படுத்தவும்:

   ```python
   from dotenv import load_dotenv
   import os

   # Load environment variables from .env file
   load_dotenv()

   # Access the GITHUB_TOKEN variable
   github_token = os.getenv("GITHUB_TOKEN")

   print(github_token)
   ```

அதுவே! `.env` கோப்பை வெற்றிகரமாக உருவாக்கி, உங்கள் GitHub token-ஐ சேர்த்து, Python பயன்பாட்டில் அதை ஏற்றியுள்ளீர்கள்.

## உங்கள் கணினியில் உள்ளூர் ரீதியாக இயக்குவது எப்படி

கோடுகளை உங்கள் கணினியில் உள்ளூர் ரீதியாக இயக்க, [Python](https://www.python.org/downloads/?WT.mc_id=academic-105485-koreyst) ஏதேனும் ஒரு பதிப்பு நிறுவப்பட்டிருக்க வேண்டும்.

அதன் பிறகு Repo-வை பயன்படுத்த, அதை clone செய்ய வேண்டும்:

```shell
git clone https://github.com/microsoft/generative-ai-for-beginners
cd generative-ai-for-beginners
```

எல்லாவற்றையும் சரிபார்த்த பிறகு, நீங்கள் தொடங்கலாம்!

## விருப்ப படிகள்

### Miniconda நிறுவுதல்

[Miniconda](https://conda.io/en/latest/miniconda.html?WT.mc_id=academic-105485-koreyst) என்பது [Conda](https://docs.conda.io/en/latest?WT.mc_id=academic-105485-koreyst), Python மற்றும் சில packages-ஐ நிறுவ ஒரு lightweight installer ஆகும். Conda என்பது ஒரு package manager ஆகும், இது Python [**virtual environments**](https://docs.python.org/3/tutorial/venv.html?WT.mc_id=academic-105485-koreyst) மற்றும் packages-ஐ அமைக்கவும் மாற்றவும் எளிதாக்குகிறது. இது `pip` மூலம் கிடைக்காத packages-ஐ நிறுவுவதற்கும் உதவுகிறது.

[MiniConda installation guide](https://docs.anaconda.com/free/miniconda/#quick-command-line-install?WT.mc_id=academic-105485-koreyst) ஐ பின்பற்றி அதை அமைக்கவும்.

Miniconda நிறுவப்பட்ட பிறகு, [repository](https://github.com/microsoft/generative-ai-for-beginners/fork?WT.mc_id=academic-105485-koreyst) ஐ clone செய்ய வேண்டும் (நீங்கள் இதை இன்னும் செய்யவில்லை என்றால்).

அடுத்ததாக, ஒரு virtual environment உருவாக்க வேண்டும். Conda-ஐ பயன்படுத்தி இதை செய்ய, ஒரு புதிய environment file (_environment.yml_) உருவாக்கவும். Codespaces-ஐ பயன்படுத்தி பின்பற்றினால், இதை `.devcontainer` directory-இல் உருவாக்கவும், அதாவது `.devcontainer/environment.yml`.

உங்கள் environment file-ஐ கீழே உள்ள snippet-ஐ கொண்டு நிரப்பவும்:

```yml
name: <environment-name>
channels:
  - defaults
  - microsoft
dependencies:
  - python=<python-version>
  - openai
  - python-dotenv
  - pip
  - pip:
      - azure-ai-ml
```

Conda-ஐ பயன்படுத்தும்போது பிழைகள் ஏற்படுமானால், Microsoft AI Libraries-ஐ கீழே உள்ள கட்டளையை terminal-இல் பயன்படுத்தி கையேடு முறையில் நிறுவலாம்.

```
conda install -c microsoft azure-ai-ml
```

Environment file-ஐ dependencies-ஐ குறிப்பிடுகிறது. `<environment-name>` என்பது உங்கள் Conda environment-க்கு நீங்கள் பயன்படுத்த விரும்பும் பெயர், மற்றும் `<python-version>` என்பது நீங்கள் பயன்படுத்த விரும்பும் Python பதிப்பு, உதாரணமாக, `3` என்பது Python-இன் சமீபத்திய முக்கிய பதிப்பு.

அதன் பிறகு, உங்கள் Conda environment-ஐ கீழே உள்ள கட்டளைகளை command line/terminal-இல் இயக்கி உருவாக்கலாம்:

```bash
conda env create --name ai4beg --file .devcontainer/environment.yml # .devcontainer sub path applies to only Codespace setups
conda activate ai4beg
```

Conda-இன் [environments guide](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html?WT.mc_id=academic-105485-koreyst) ஐப் பார்க்கவும், நீங்கள் எந்தவொரு பிரச்சனையையும் சந்தித்தால்.

### Python support extension உடன் Visual Studio Code பயன்படுத்துதல்

இந்த பாடத்திற்காக [Visual Studio Code (VS Code)](https://code.visualstudio.com/?WT.mc_id=academic-105485-koreyst) editor-ஐ Python support extension-ஐ நிறுவி பயன்படுத்த பரிந்துரைக்கிறோம். இது, எனினும், ஒரு பரிந்துரை மட்டுமே, கட்டாயம் அல்ல.

> **குறிப்பு**: VS Code-இல் course repository-ஐ திறக்கும்போது, நீங்கள் project-ஐ container-இல் அமைக்க விருப்பம் உள்ளது. இது course repository-இல் உள்ள [சிறப்பு `.devcontainer`](https://code.visualstudio.com/docs/devcontainers/containers?itemName=ms-python.python&WT.mc_id=academic-105485-koreyst) directory காரணமாக.

> **குறிப்பு**: Directory-ஐ clone செய்து VS Code-இல் திறந்தவுடன், Python support extension-ஐ நிறுவ VS Code தானாகவே பரிந்துரைக்கும்.

> **குறிப்பு**: VS Code repository-ஐ container-இல் மீண்டும் திறக்க பரிந்துரைத்தால், Python-இன் உள்ளூர் நிறுவப்பட்ட பதிப்பைப் பயன்படுத்த, இந்த கோரிக்கையை நிராகரிக்கவும்.

### உலாவியில் Jupyter பயன்படுத்துதல்

[Jupyter environment](https://jupyter.org?WT.mc_id=academic-105485-koreyst) ஐ உலாவியில் நேரடியாக project-ஐ வேலை செய்ய பயன்படுத்தலாம். பாரம்பரிய Jupyter மற்றும் [Jupyter Hub](https://jupyter.org/hub?WT.mc_id=academic-105485-koreyst) auto-completion, code highlighting போன்ற வசதிகளுடன் ஒரு development environment-ஐ வழங்குகிறது.

Jupyter-ஐ உள்ளூர் ரீதியாக தொடங்க, terminal/command line-க்கு செல்லவும், course directory-க்கு navigate செய்யவும், மற்றும் கீழே உள்ள கட்டளையை இயக்கவும்:

```bash
jupyter notebook
```

அல்லது

```bash
jupyterhub
```

இது Jupyter instance-ஐ தொடங்கும், மற்றும் அதை அணுக URL command line window-இல் காட்டப்படும்.

URL-ஐ அணுகியவுடன், course outline-ஐ காணலாம் மற்றும் எந்த `*.ipynb` கோப்பிற்கும் navigate செய்யலாம். உதாரணமாக, `08-building-search-applications/python/oai-solution.ipynb`.

### Container-இல் இயக்குதல்

உங்கள் கணினியில் அல்லது Codespace-இல் அனைத்தையும் அமைப்பதற்கான மாற்றாக, [container](../../../00-course-setup/<https:/en.wikipedia.org/wiki/Containerization_(computing)?WT.mc_id=academic-105485-koreyst>) ஐ பயன்படுத்தலாம். Course repository-இல் உள்ள சிறப்பு `.devcontainer` folder VS Code-ஐ container-இல் project-ஐ அமைக்க அனுமதிக்கிறது. Codespaces-க்கு வெளியே, இது Docker-ஐ நிறுவ வேண்டும், மேலும் இது சிறிது வேலைகளை உள்ளடக்குகிறது, எனவே containers-இல் வேலை செய்ய அனுபவம் உள்ளவர்களுக்கு மட்டுமே இதை பரிந்துரைக்கிறோம்.

GitHub Codespaces-ஐ பயன்படுத்தும்போது API key-களை பாதுகாப்பாக வைத்திருக்க Codespace Secrets-ஐ பயன்படுத்துவது சிறந்த வழிகளில் ஒன்றாகும். [Codespaces secrets management](https://docs.github.com/en/codespaces/managing-your-codespaces/managing-secrets-for-your-codespaces?WT.mc_id=academic-105485-koreyst) வழிகாட்டியை பின்பற்றவும்.

## பாடங்கள் மற்றும் தொழில்நுட்ப தேவைகள்

இந்த பாடத்தில் 6 கருத்து பாடங்கள் மற்றும் 6 கோடிங் பாடங்கள் உள்ளன.

கோடிங் பாடங்களுக்கு, Azure OpenAI Service-ஐ பயன்படுத்துகிறோம். இந்த கோடுகளை இயக்க, Azure OpenAI Service-க்கு அணுகல் மற்றும் API key தேவைப்படும். [இந்த விண்ணப்பத்தை](https://azure.microsoft.com/products/ai-services/openai-service?WT.mc_id=academic-105485-koreyst) பூர்த்தி செய்து அணுகலை பெற விண்ணப்பிக்கலாம்.

உங்கள் விண்ணப்பம் செயல்படுத்தப்படும் வரை, ஒவ்வொரு கோடிங் பாடத்திலும் `README.md` கோப்பு உள்ளது, இதில் நீங்கள் கோடுகளை மற்றும் output-களை காணலாம்.

## Azure OpenAI Service-ஐ முதன்முதலாக பயன்படுத்துதல்

Azure OpenAI Service-ஐ முதன்முதலாக பயன்படுத்தினால், [Azure OpenAI Service resource-ஐ உருவாக்கி deploy செய்ய](https://learn.microsoft.com/azure/ai-services/openai/how-to/create-resource?pivots=web-portal&WT.mc_id=academic-105485-koreyst) எப்படி என்பதை விளக்கும் வழிகாட்டியை பின்பற்றவும்.

## OpenAI API-ஐ முதன்முதலாக பயன்படுத்துதல்

OpenAI API-ஐ முதன்முதலாக பயன்படுத்தினால், [Interface-ஐ உருவாக்கி பயன்படுத்த](https://platform.openai.com/docs/quickstart?context=pythont&WT.mc_id=academic-105485-koreyst) எப்படி என்பதை விளக்கும் வழிகாட்டியை பின்பற்றவும்.

## மற்ற மாணவர்களை சந்திக்க

எங்கள் அதிகாரப்பூர்வ [AI Community Discord server](https://aka.ms/genai-discord?WT.mc_id=academic-105485-koreyst) இல் மற்ற மாணவர்களை சந்திக்க channel-களை உருவாக்கியுள்ளோம். இது Generative AI-இல் மேம்பட விரும்பும் ஒரே மாதிரியான தொழில்முனைவோர், உருவாக்குநர்கள், மாணவர்கள் மற்றும் யாரும் network செய்ய சிறந்த வழியாகும்.

[![Discord channel-ஐ சேரவும்](https://dcbadge.limes.pink/api/server/ByRwuEEgH4)](https://aka.ms/genai-discord?WT.mc_id=academic-105485-koreyst)

Project குழுவும் இந்த Discord server-இல் மாணவர்களுக்கு உதவ இருக்கும்.

## பங்களிக்க

இந்த பாடம் ஒரு open-source முயற்சியாகும். மேம்படுத்த வேண்டிய பகுதிகள் அல்லது பிரச்சனைகள் உள்ளதாக நீங்கள் காண்பீர்கள் என்றால், [Pull Request](https://github.com/microsoft/generative-ai-for-beginners/pulls?WT.mc_id=academic-105485-koreyst) உருவாக்கவும் அல்லது [GitHub issue](https://github.com/microsoft/generative-ai-for-beginners/issues?WT.mc_id=academic-105485-koreyst) பதிவு செய்யவும்.

Project குழு அனைத்து பங்களிப்புகளையும் கண்காணிக்கும். Open source-க்கு பங்களிப்பது Generative AI-இல் உங்கள் தொழில்முனைவை உருவாக்க ஒரு அற்புதமான வழியாகும்.

பெரும்பாலான பங்களிப்புகள் Contributor License Agreement (CLA) உடன் ஒப்புதல் அளிக்க வேண்டும், இது நீங்கள் பங்களிப்பதற்கான உரிமையை கொண்டிருக்கிறீர்கள் மற்றும் நாங்கள் உங்கள் பங்களிப்பை பயன்படுத்த உரிமை அளிக்கிறீர்கள் என்பதை உறுதிப்படுத்துகிறது. மேலும் விவரங்களுக்கு [CLA, Contributor License Agreement website](https://cla.microsoft.com?WT.mc_id=academic-105485-koreyst) ஐ பார்வையிடவும்.

முக்கியம்: இந்த Repo-இல் உள்ள உரையை மொழிபெயர்க்கும்போது, machine translation-ஐ பயன்படுத்த வேண்டாம் என்பதை உறுதிப்படுத்தவும். மொழிபெயர்ப்புகளை சமூகத்தின் மூலம் சரிபார்ப்போம், எனவே நீங்கள் திறமையான மொழிகளில் மட்டுமே மொழிபெயர்ப்புக்கு தன்னார்வமாக முன்வரவும்.

நீங்கள் pull request-ஐ சமர்ப்பிக்கும்போது, CLA-bot தானாகவே நீங்கள் CLA-ஐ வழங்க வேண்டியதா என்பதை தீர்மானித்து PR-ஐ சரியாக அலங்கரிக்கும் (எ.கா., label, comment). Bot வழங்கும் வழிகாட்டுதல்களை பின்பற்றவும். அனைத்து Repo-களிலும் CLA-ஐ பயன்படுத்தும் போது, இதை ஒருமுறை மட்டுமே செய்ய வேண்டும்.

இந்த Project [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/?WT.mc_id=academic-105485-koreyst) ஐ ஏற்றுக்கொண்டுள்ளது. மேலும் தகவலுக்கு Code of Conduct FAQ ஐ படிக்கவும் அல்லது [Email opencode](opencode@microsoft.com) ஐ தொடர்பு கொள்ளவும்.

## தொடங்குவோம்
இப்போது நீங்கள் இந்த பாடத்தை முடிக்க தேவையான படிகளை முடித்துவிட்டீர்கள், [Generative AI மற்றும் LLMs பற்றிய அறிமுகம்](../01-introduction-to-genai/README.md?WT.mc_id=academic-105485-koreyst) மூலம் தொடங்கலாம்.

---

**அறிவிப்பு**:  
இந்த ஆவணம் [Co-op Translator](https://github.com/Azure/co-op-translator) என்ற AI மொழிபெயர்ப்பு சேவையை பயன்படுத்தி மொழிபெயர்க்கப்பட்டுள்ளது. நாங்கள் துல்லியத்திற்காக முயற்சிக்கிறோம், ஆனால் தானியங்கி மொழிபெயர்ப்புகளில் பிழைகள் அல்லது தவறுகள் இருக்கக்கூடும் என்பதை கவனத்தில் கொள்ளவும். அதன் சொந்த மொழியில் உள்ள மூல ஆவணம் அதிகாரப்பூர்வ ஆதாரமாக கருதப்பட வேண்டும். முக்கியமான தகவல்களுக்கு, தொழில்முறை மனித மொழிபெயர்ப்பு பரிந்துரைக்கப்படுகிறது. இந்த மொழிபெயர்ப்பைப் பயன்படுத்துவதால் ஏற்படும் எந்த தவறான புரிதல்களுக்கும் அல்லது தவறான விளக்கங்களுக்கும் நாங்கள் பொறுப்பல்ல.