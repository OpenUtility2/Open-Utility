# OpenUtility

> **Fast tools. Private by default. Built for the web.**

OpenUtility is a browser-first collection of developer, web, data, and utility tools designed to make everyday tasks faster without unnecessary accounts, installs, or complicated workflows.

The project is built as a lightweight static web platform with a consistent interface across tools, shareable tool URLs, documentation, Tool Chains, and an offline/PWA foundation.

## ✨ Why OpenUtility?

OpenUtility focuses on four principles:

- **⚡ Fast** — launch a tool and get to work quickly.
- **🔒 Private by default** — supported tools process ordinary input locally in the browser where possible.
- **🧩 Consistent** — tools share the same discovery, layout, input/output, and sharing experience.
- **🌐 Open** — the website is publicly available and its source is maintained on GitHub.

## 🛠️ What is included?

### Tool collection

OpenUtility provides a growing collection of browser-based utilities, including developer and data-processing tools.

Tools are available directly under:

```text
/tools/<tool>.html
```

The platform also provides a dedicated tool experience:

```text
/tool.html?tool=<tool-id>
```

This gives each tool a shareable entry point while keeping the actual utility isolated inside its own page.

### 🔗 Shareable tool URLs

Every tool can be opened through a direct URL, making it easy to bookmark, share, or link to a specific utility.

Example:

```text
https://openutility.info.gf/tool.html?tool=json-formatter
```

### 🔗 Tool Chains

Tool Chains allow compatible utilities to be connected into repeatable workflows instead of manually moving data between separate pages.

A typical workflow can look like:

```text
Input → Format → Transform → Encode / Convert → Output
```

### 📚 Developer Reference

OpenUtility includes a dedicated documentation experience covering the tool collection, workflows, links, privacy considerations, and offline behavior.

- `/docs/` — documentation entry point
- `/docs.html` — documentation page

### 📱 PWA & offline foundation

The website includes a Progressive Web App foundation with a manifest and offline page. Supported browser-side functionality can continue to work without sending ordinary tool input to a server.

Offline availability depends on browser caching and the individual tool's implementation.

### 🌐 Website pages

```text
/
├── index.html        Homepage and tool discovery
├── tool.html         Tool detail experience
├── docs.html         Developer documentation
├── about.html        About OpenUtility
├── discord.html      Community information
├── open-source.html  Open-source project information
├── privacy.html      Privacy information
├── terms.html        Terms information
├── offline.html      Offline fallback
└── 404.html          Custom not-found page
```

## 🏗️ Project structure

OpenUtility is intentionally lightweight and can be served as a static website.

```text
Open-Utility/
├── assets/           Shared visual and website assets
├── docs/             Documentation entry point
├── tools/            Individual browser-based utilities
├── index.html        Main homepage
├── tool.html         Tool detail / launcher experience
├── docs.html         Documentation
├── about.html        About page
├── discord.html      Discord/community page
├── open-source.html  Open-source page
├── privacy.html      Privacy page
├── terms.html        Terms page
├── offline.html      Offline fallback
├── 404.html          Custom 404 page
├── manifest.json     PWA manifest
├── maintenance.json  Maintenance configuration
└── CNAME             Custom domain configuration
```

## 🚀 Run locally

OpenUtility does not require a large application stack to develop.

### 1. Clone the repository

```bash
git clone https://github.com/OpenUtility2/Open-Utility.git
cd Open-Utility
```

### 2. Start a static server

For example, with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

A local HTTP server is recommended over opening files directly with `file://`, especially when testing PWA, fetch, module, or browser-storage behavior.

## ➕ Adding a new tool

Tools are designed to be self-contained browser pages.

A typical tool should:

1. Live inside `tools/`.
2. Have a clear, descriptive filename.
3. Work correctly on mobile and desktop.
4. Keep input and output easy to understand.
5. Avoid unnecessary network requests.
6. Never expose secrets or sensitive input in shareable URLs.
7. Match the existing OpenUtility visual language.
8. Be usable without an account whenever technically possible.
9. Be added to the tool discovery/index configuration used by the site.
10. Include accessible labels, buttons, and meaningful error states.

## 🔒 Privacy

Privacy is a core part of the OpenUtility design.

Where technically possible, ordinary tool processing happens in the browser instead of being uploaded to a remote server. However, **not every tool necessarily has identical processing behavior**.

Before using a tool with sensitive information:

- Review the implementation.
- Check the site's Privacy page.
- Avoid putting secrets into URLs.
- Avoid sharing generated URLs containing sensitive data.

See [`privacy.html`](./privacy.html) for the project's current privacy information.

## 📦 Deployment

OpenUtility is suitable for static hosting and can be deployed through services such as:

- GitHub Pages
- Cloudflare Pages
- Netlify
- Vercel static hosting
- Any standard web server

The repository contains a `CNAME` file for custom-domain deployments.

## 🔄 Maintenance mode

The project includes `maintenance.json` so the website can provide a controlled maintenance experience without requiring a full backend application.

When changing maintenance behavior, test both normal and maintenance states before deployment.

## 🤝 Contributing

Contributions and ideas are welcome.

Before submitting changes:

- Keep the project lightweight.
- Follow the existing HTML/CSS/JavaScript conventions.
- Test on mobile and desktop layouts.
- Test keyboard interaction where applicable.
- Avoid unnecessary dependencies.
- Keep browser-side processing browser-side when practical.
- Do not commit API keys, passwords, tokens, or private data.
- Test direct tool URLs and the main tool-discovery flow.
- Update documentation when introducing a new user-facing feature.

### Reporting a bug

When reporting an issue, include:

- The page or tool affected
- Browser and device
- Steps to reproduce
- Expected behavior
- Actual behavior
- Console errors, if relevant

## 🗺️ Project direction

OpenUtility is evolving toward a more complete utility platform with an emphasis on:

- Better tool discovery
- More powerful Tool Chains
- Improved input/output experiences
- Stronger offline support
- Better accessibility
- Consistent tool interfaces
- More developer documentation
- A distinctive OpenUtility visual identity

## 🌐 OpenUtility ecosystem

| Project | Purpose |
|---|---|
| `openutility` | Main OpenUtility website/platform |
| `openutility-bot` | Official Discord bot |
| `openutility-dashboard` | Web dashboard for Discord server management |
| `openutility-api` | Dashboard/backend API |
| `mctools` | Minecraft tools platform |
| `speedcheck` | Internet/network speed testing project |

## 🔗 Links

- **Website:** https://openutility.info.gf
- **Documentation:** https://openutility.info.gf/docs/
- **GitHub:** https://github.com/OpenUtility2
- **Discord:** https://discord.gg/ufvQ4Ghtpu

## 📄 License

See the repository's license and individual project files for the applicable licensing terms.

---

**OpenUtility** — simple utilities for developers, creators, and everyday web workflows.