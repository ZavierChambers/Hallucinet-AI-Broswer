# 🌐 Hallucinet

### A browser for an internet that doesn't exist.

**Hallucinet** is an experimental, single-file browser that uses AI models to generate an entirely fictional internet on demand.

Instead of connecting you to real websites, Hallucinet creates **search results, websites, articles, forums, stores, blogs, news sites, and other pages dynamically** based on what you search for.

Every fictional website can develop its own identity, visual design, navigation, styling, and content — creating the feeling that you're exploring a parallel internet that was never actually built.

> **Search anything. Visit anywhere. The internet is invented as you explore it.**

---

## ✨ Features

### 🔎 AI-Powered Search

Search the fictional internet just like you would use a normal search engine.

Hallucinet can generate:

* Search results
* Search snippets
* Related searches
* Fictional domains
* News sites
* Forums
* Blogs
* Wikis
* Online stores
* University pages
* Personal websites
* Abandoned fan sites
* Other fictional web properties

Searches can return a variable number of results to make the experience feel less deterministic.

---

### 🖥️ Generated Websites

Clicking a result generates the website you're looking for.

Pages are written as real HTML and rendered inside the browser.

The AI can generate:

* Complete layouts
* Navigation
* Typography
* Colors
* Articles
* Product pages
* Forums
* Comments
* Images
* Videos
* Links to additional pages

The project specifically maintains **per-domain identities**, allowing pages belonging to the same fictional website to retain a consistent name, palette, navigation, footer, and overall tone.

---

## 🧬 Persistent Websites

One of Hallucinet's core ideas is that a website should feel like an actual website rather than a collection of unrelated AI generations.

The first complete page generated for a domain can establish that site's visual shell.

Later pages reuse the site's:

* Header
* Footer
* Stylesheet
* Body structure
* Navigation
* Overall visual identity

This means you can visit:

```text
example.com
example.com/about
example.com/products
example.com/forum
```

and have them feel like pages from the **same website**.

---

## 🤖 Multiple AI Providers

Hallucinet isn't locked to a single AI provider.

The browser currently supports OpenAI-compatible APIs as well as provider-specific APIs.

### Language Models

Supported configurations include:

* 🖥️ LM Studio
* 🦙 Ollama
* llama.cpp / llama-server
* OpenAI
* Anthropic / Claude
* Google Gemini
* OpenRouter
* Groq
* DeepSeek
* Mistral
* xAI / Grok
* Together AI
* Custom OpenAI-compatible endpoints

The provider system is designed around several request formats, including OpenAI-compatible `/chat/completions`, Anthropic `/messages`, and Gemini `generateContent`.

---

## 🏠 Run AI Locally

Hallucinet works especially well with local models.

### LM Studio

The default provider is:

```text
LM Studio
http://localhost:1234/v1
```

Start a model in LM Studio, enable its local server, configure browser CORS, and connect Hallucinet to it.

No cloud AI subscription is required for the core browsing experience when using a local model.

The project also supports Ollama and llama.cpp for local inference.

---

## 🎨 AI-Generated Images

Generated pages can contain images.

Hallucinet can either:

* Generate images with an AI image model
* Search real image sources
* Use offline behavior when media providers aren't configured

Image providers include configurations for services such as:

* OpenAI image generation
* Google image generation
* Image search providers
* Custom image APIs

Images are generated or resolved when the page needs them rather than requiring every page to contain pre-existing assets.

---

## 🎬 Video

Generated pages can also contain video.

Hallucinet supports both:

### Video search

Find existing videos through configured providers.

### AI video generation

Connect a compatible video-generation API and allow generated websites to contain AI-generated clips.

Videos are loaded when the user interacts with them rather than automatically loading everything immediately.

---

## 🧭 Browser Features

Hallucinet isn't just a search interface.

It includes a browser-style interface with:

* Multiple tabs
* Back / forward navigation
* Reload
* Address bar
* Bookmarks
* Browsing history
* Search
* Persistent page cache
* Site persistence
* Settings
* Connection status
* Generated-page navigation
* New-tab behavior

The browser maintains tab history and supports navigating between generated pages like a conventional browser.

---

## ⭐ Bookmarks

Pages can be bookmarked directly from the address bar.

Bookmarks are stored locally and displayed in the browser's bookmark bar.

You can:

* Add bookmarks
* Remove bookmarks
* Navigate directly to bookmarked pages
* Persist bookmarks between sessions

---

## 🕐 History

Hallucinet maintains a local browsing history of generated pages.

History supports:

* Previously visited pages
* Grouping by domain
* Returning to generated pages
* Removing individual entries
* Clearing history/cache

---

## 💾 Local Persistence

Hallucinet stores its data using browser storage.

This allows generated content and settings to survive page reloads and browser sessions.

Cached data includes things such as:

```text
Pages
Search results
Bookmarks
Site identities
Site shells
Settings
Generated media
```

The page cache keeps a limited number of recent entries to prevent unlimited storage growth.

---

## 📦 Export Your Internet

One of the more unusual features is the ability to export the fictional internet you've created.

Cached pages can be downloaded as actual:

```text
.html
```

files.

This allows you to take the generated websites outside Hallucinet and keep them as normal HTML documents.

You can also import a folder of HTML files back into Hallucinet and have them treated as visited pages.

---

## 🧩 Custom Domain Templates

Hallucinet can also use your own HTML templates for domains.

For example:

```text
templates/
├── example.com.html
├── news.example.html
└── forum.example/
    └── index.html
```

A template can provide the visual shell of a website while Hallucinet generates the content inside it.

This makes it possible to create your own persistent fictional websites rather than relying entirely on AI-generated designs.

---

## 🎛️ Generation Controls

The settings panel provides control over how the fictional internet is generated.

### Imagination

Adjust the model temperature to control how predictable or unusual generated pages are.

### Page Length

Control how many tokens the model can use when generating a page.

### Lite Mode

Designed for smaller local models.

Lite Mode uses:

* Shorter prompts
* Simpler pages
* Fewer tokens

This can make the project considerably easier to run with smaller local models.

---

## 🌍 Customize the Internet

You can define what kind of fictional internet Hallucinet should create.

For example:

```text
A parallel internet from the early 2000s.

Websites should feel slightly outdated,
personal, strange, and experimental.
Use forums, personal blogs, small businesses,
fan sites, and independent news organizations.
```

Or:

```text
A futuristic internet from 2087.

Corporations dominate the web.
Personal websites are rare.
Use holographic interfaces, virtual cities,
AI-generated news, digital marketplaces,
and fictional social networks.
```

The entire character of the generated internet can change based on this setting.

---

## 🔌 Architecture

Hallucinet is intentionally designed as a **single HTML file**.

Everything lives inside one document:

```text
index.html
```

The file contains:

```text
HTML
├── Browser interface
├── CSS
├── JavaScript
├── Application state
├── AI provider clients
├── Search generation
├── Page generation
├── Page renderer
├── Cache
├── Domain persistence
├── Site shells
├── History
├── Bookmarks
├── Settings
└── Media handling
```

The project describes itself internally as a browser whose internet is generated on demand, with the state, multi-provider model client, renderer, and fictional web contained in the same file.

---

## 🚀 Getting Started

### 1. Download the project

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/hallucinet.git
```

Or download the HTML file directly.

---

### 2. Open Hallucinet

Open:

```text
index.html
```

in a modern browser.

---

### 3. Configure an AI Provider

Open:

```text
⚙ Settings → Model
```

Choose your provider.

For local AI, you can use:

```text
LM Studio
Ollama
llama.cpp
```

For hosted AI, configure the appropriate API key.

---

### 4. Search

Enter something like:

```text
The history of the fictional city of New Avalon
```

or:

```text
best computer store in Westbridge
```

or even:

```text
forum discussing strange lights over Lake Erie
```

Hallucinet will generate an internet around the query.

---

## 🧪 Example Experience

Try searching:

```text
"best pizza in New Avalon"
```

You might discover:

```text
newavalonpizza.com
```

Then follow a link to:

```text
newavalonpizza.com/menu
```

Then:

```text
newavalonpizza.com/about
```

Then perhaps discover:

```text
newavalonpizza.com/forum
```

The goal is for these pages to feel like pieces of a larger internet rather than isolated AI responses.

---

## ⚠️ Important

Hallucinet intentionally creates fictional information.

Generated websites, companies, people, events, articles, products, and search results may **not exist in the real world**.

Do not treat generated information as factual.

The project is intended as an experiment in:

* Generative interfaces
* AI-assisted web creation
* Procedural worldbuilding
* Local AI
* Browser interfaces
* Synthetic web environments
* Human-computer interaction

---

## 🔐 API Keys & Privacy

API keys entered into the settings interface are stored in the browser's local storage and sent directly to the configured provider from the page.

If you use a cloud provider, your prompts and generated content will be sent to that provider according to its API behavior and policies.

For a more private setup, use a local provider such as:

```text
LM Studio
Ollama
llama.cpp
```

---

## 🛠️ Technologies

Hallucinet is built with standard web technologies:

* HTML5
* CSS3
* JavaScript
* Local Storage
* Fetch API
* iframe sandboxing
* AI APIs
* REST APIs

No framework is required.

No build system is required.

No package manager is required.

No backend is required for the basic browser application.

---

## 🎯 Project Goals

Hallucinet explores a simple question:

> **What happens if an AI doesn't just answer questions, but creates the internet you browse through?**

Traditional AI interfaces give you an answer.

Hallucinet tries to give you a **place to explore**.

The goal isn't simply to generate a webpage.

It's to create the illusion of an interconnected digital world where:

```text
Search → Website → Link → Website → Forum → Article → Store → Blog
```

can continue indefinitely.

---

## 🗺️ Possible Future Ideas

Some directions this project could explore:

* 🌐 Shared fictional internet worlds
* 👥 AI-generated social networks
* 💬 Persistent AI forum communities
* 🛒 Functional fictional marketplaces
* 📰 AI-generated newspapers
* 🗺️ Generated maps and locations
* 👤 Persistent fictional users
* 📧 Fictional email systems
* 🎮 Generated browser games
* 🧠 Long-term world memory
* 🕸️ Larger persistent site graphs
* 💻 More realistic browser behavior
* 🖥️ Desktop/OS environments built on top of Hallucinet

---

## 📜 License

Add your preferred license here.

For example:

```text
MIT License
```

---

## ⭐ Why Hallucinet?

The real internet is enormous because millions of people have created things that connect to other things.

Hallucinet experiments with creating that feeling artificially.

Instead of:

> "Here is an AI-generated webpage."

the idea is:

> **"Here is an internet. Go explore it."**

---

### Built with curiosity, HTML, JavaScript, and way too much imagination. 🌐✨
