# Advanced JSON Studio

[![Version](https://img.shields.io/visual-studio-marketplace/v/GodwinJoseph.advanced-json-studio)](https://marketplace.visualstudio.com/items?itemName=GodwinJoseph.advanced-json-studio)

> ### 🎉 Launch Offer — 50% Off Pro for the First 500 Users
>
> To celebrate the Advanced JSOn Studio launch, the first **500 users** get **50% off** a Pro licence. Use the code below at checkout:
>
> Coupon code: **`XBKF1XMP`**
>
> 👉 **[Get Pro licence →](https://buy.polar.sh/polar_cl_Do1F4RavuKMBISTKelilfqp5MvGXhueNFoRjn2C5TY8)**
>
> _Limited to the first 500 — offer ends once the cap is reached._

---

> 🧡 More of an IntelliJ fan? Check out the repository here → [IntelliJ Repo](https://github.com/godwinjk/Json_Parser)
---

# Advanced JSON Studio v1.0.4

**The Intelligent JSON Workspace for VS Code**

**Advanced JSON Studio** is a complete engineering environment built right into your VS Code sidebar. Designed to handle everything from massive API responses to broken configuration files — it's the last JSON tool you'll ever need.

<kbd>Parse</kbd> <kbd>Pretty-Print</kbd> <kbd>Tree-View</kbd> <kbd>Graph-View</kbd> <kbd>Minify</kbd> <kbd>Sort-Keys</kbd>
<kbd>YAML</kbd> <kbd>XML</kbd> <kbd>TOML</kbd> <kbd>Properties</kbd> <kbd>CBOR</kbd> <kbd>BSON</kbd>
<kbd>Flatten</kbd> <kbd>Unflatten</kbd> <kbd>Base64</kbd> <kbd>CSV-Table</kbd>
<kbd>Schema-Inference</kbd> <kbd>Schema-Validator</kbd> <kbd>JSONPath</kbd> <kbd>JMESPath</kbd>
<kbd>JWT-Decode</kbd> <kbd>JWT-Verify</kbd> <kbd>Diff</kbd> <kbd>HTTP-Client</kbd>
<kbd>Dummy-JSON</kbd> <kbd>Code-Gen</kbd> <kbd>Session-Tabs</kbd> <kbd>Persistence</kbd>
<kbd>Open-In-Editor</kbd> <kbd>Right-Click-Generate</kbd> <kbd>Save-File</kbd>
<kbd>GraphQL-Format</kbd> <kbd>GraphQL-to-JSON</kbd>

---

## 🚀 Features

### 🧠 Intelligent Parsing & Repair

- **Parse any format** — paste JSON, JSON5, YAML, XML, TOML, Properties, JWT, CBOR, BSON, or Base64-encoded JSON and the parser detects it automatically
- **Auto-repair** — malformed JSON is repaired automatically using built-in heuristics (missing quotes, trailing commas, unquoted keys, and more)
- **Format detection** — the detected format is shown as a badge in the toolbar
- **⚡ Repaired badge** — a visible indicator appears when the input was automatically repaired
- **Ctrl+Enter** to parse, or click the **Parse** button

### 🎨 View Tab

- **Pretty Print** — clean, indented JSON with full syntax highlighting (keys, strings, numbers, booleans, null, punctuation)
- **Tree View** — collapsible/expandable tree navigation for complex nested structures
- **Graph View** — visual node-graph of your JSON structure; pan and zoom to explore large datasets

### 🔄 Convert Tab

- **Minify** — collapse JSON to a single line
- **YAML** — convert JSON to YAML with syntax highlighting
- **XML** — convert JSON to XML
- **TOML** — convert JSON to TOML (arrays of objects use correct `[[table]]` syntax)
- **Properties** — convert JSON to `.properties` key-value format
- **CBOR** — convert JSON to CBOR binary (hex dump)
- **BSON** — convert JSON to BSON binary (hex dump)
- **Flatten** — expand nested JSON into dot-notation flat key–value pairs (e.g. `user.address.city`)
- **Unflatten** — rebuild a nested JSON object from flat dot-notation keys
- **Base64 Encode** — encode the current JSON to a Base64 string
- **CSV Table** — convert JSON arrays to a sortable, scrollable table view

### 🔍 Analyze Tab

- **JSON Schema** — infer a JSON Schema from your JSON structure automatically
- **Schema Validator** — validate your JSON against a JSON Schema; errors shown with path and message
- **Query (JSONPath / JMESPath)** — query your JSON with either expression language; inline help with syntax reference and examples
- **JWT** — decode JWT tokens (header, payload, signature); verify HMAC (HS256/384/512) signatures with a secret key

### 🛠️ Tool Buttons

- **Diff** — compare two JSON documents side-by-side; added/removed lines highlighted in green/red with a change summary
- **HTTP Client** — full HTTP client with GET, POST, PUT, PATCH, DELETE; custom headers; request body; cURL command parser
- **Dummy JSON** — generate realistic fake JSON for testing; choose object or array, property count, nesting depth, and array size
- **Code Gen** — generate typed models from JSON in 12 languages locally (TypeScript, JavaScript, Python, Kotlin, Swift, Go, Rust, C#, Java, C++, Dart, JSON Schema); save directly to your project

### ⚡ Toolbar Actions

- **📌 Pin** — pin the current input so it is restored exactly on next open
- **Clear** — wipe input and output
- **Copy** — copy the active output tab's content to clipboard
- **⇅ Sort** — sort all JSON keys alphabetically (recursive)
- **⧉ Open** — open the full Advanced JSON Studio panel in an editor column for more screen space
- **💾 Save** — save the current output to a file
- **⚙ Settings** — manage your Pro licence; activate, deactivate, or get a new licence

### 🗂️ Session Tabs (up to 10)

- Create up to **10 independent sessions** — each tab has its own input, parse results, active output tab, and sort state
- **Double-click** a tab label to rename it inline
- **× close** button on each tab; the last tab is protected from closing
- All sessions are **automatically saved and restored** across VS Code restarts — your work is never lost
- The active session and all tab labels are preserved across restarts

### 💾 Input Persistence

- Every time you parse, your input is **automatically saved** to local storage
- Use the **📌 Pin** button to explicitly save the current input for the next session
- On next open, your input is restored and automatically re-parsed

### ◈ GraphQL Studio

Sessions now support a dedicated **GraphQL mode** alongside JSON. When you create a tab, you can switch it to GraphQL mode to get a purpose-built workspace:

- **Format** — parse and pretty-print any GraphQL SDL or query document (powered by the official `graphql` parser)
- **Convert to JSON** — convert a GraphQL SDL / query to its JSON AST representation; output is sent directly to the main JSON parser
- The GQL toolbar uses the GraphQL logo badge and a **Format** primary button (replaces Parse) for discoverability

### 🖱️ Right-Click: Generate Code in Folder

- **Right-click any folder** in the VS Code Explorer → **"Generate Code from JSON"**
- Opens a dedicated panel with a **syntax-highlighted JSON editor**, language selector, and type name field
- **📂 Load File** button loads a JSON file from disk directly into the editor
- **⇌ Format** button pretty-prints the JSON in-place
- Click **⚡ Generate & Save** — the generated file (e.g. `User.ts`, `Order.py`) is written directly into the right-clicked folder
- Supports all 12 languages; file extension is set automatically

### 🔗 Parse Selection from Editor

- Select any JSON text in any editor file → right-click → **"Parse Selection in Advanced JSON Studio"**
- The selected text is sent directly to the parser and focused in the sidebar

---

> ## Important: Advanced JSON Studio uses a Freemium Model
>
> Advanced JSON Studio is a professional-grade tool built and maintained by a solo developer. To keep it actively maintained, fast, and full of features, it uses a freemium model.
>
> #### What is Free?
> The essentials are always free:
> - Core JSON parsing, pretty-printing, and validation
> - Tree view navigation
> - Basic format detection and repair
>
> #### What is Pro?
> Advanced and specialised features require a Pro licence:
> - Format conversions (YAML, XML, TOML, Properties, CBOR, BSON, Flatten, Base64, CSV)
> - Query engine (JSONPath / JMESPath)
> - JWT decode and verify
> - JSON Diff, HTTP Client, Dummy JSON Generator
> - Schema inference and Schema Validator
> - Local code generation (12 languages)
> - Save output to file
>
> #### A Generous Daily Allowance
> Every Pro feature includes a **daily free usage limit** — you can try every feature every day without a licence. Access is gently limited once the daily threshold is met, not hard-blocked.
>
> 👉 **[Get a Pro licence →](https://buy.polar.sh/polar_cl_Do1F4RavuKMBISTKelilfqp5MvGXhueNFoRjn2C5TY8)**
>
> _— Godwin_

---

## 🔒 Pro Licence

Activate your Pro licence from the **⚙ Settings** panel (gear icon in the toolbar):

1. Click **⚙** in the top-right of the toolbar
2. Paste your licence key into the input field
3. Click **Activate**

Your licence is validated against Polar.sh and the key is stored securely in your OS keychain. Once activated, all Pro features are immediately unlocked with no daily limits.

👉 **[Get a Pro licence →](https://buy.polar.sh/polar_cl_Do1F4RavuKMBISTKelilfqp5MvGXhueNFoRjn2C5TY8)**

To deactivate (e.g. to move to a new machine), click **Deactivate** in the Settings panel. This removes the key from your keychain immediately.

---

## 🔒 Privacy — Your Data Never Leaves Your Machine

**Advanced JSON Studio is built privacy-first. No JSON data is ever sent to any server.**

| What happens | Where it runs |
|---|---|
| JSON parsing, formatting, repair | 100% local — your machine only |
| Format conversions (YAML, XML, TOML, CBOR, BSON…) | 100% local |
| Query (JSONPath / JMESPath) | 100% local |
| JWT decode | 100% local |
| Schema inference and validation | 100% local |
| Flatten / Unflatten / Base64 / CSV | 100% local |
| Code generation (all 12 languages) | 100% local — powered by [quicktype-core](https://github.com/glideapps/quicktype) |
| Input persistence (saved across sessions) | Stored in VS Code's local `globalState` — never synced |
| HTTP Client requests | Sent directly from your machine to the URL you specify — no proxy |
| **Licence key validation** | The licence key is sent to [Polar.sh](https://polar.sh) for validation only — **no JSON data is ever included** |

### How your licence key is stored
Your licence key is stored exclusively in your **operating system's secure keychain** (macOS Keychain, Windows Credential Manager, Linux Secret Service). It is never written to a plain text file, never logged, and never included in any telemetry.

---

## 📦 Installation

**From VS Code Marketplace:**

1. Open VS Code Or Any Fork of it
2. Press `Ctrl+Shift+X` to open Extensions
3. Search for **"Advanced JSON Studio"**
4. Click **Install**

**From VSIX (manual):**

1. Download the latest `.vsix` from the [Releases page](https://github.com/godwinjk/advanced_json_studio_vscode/releases/latest)
2. Open VS Code → Extensions (`Ctrl+Shift+X`)
3. Click `···` → **Install from VSIX…**
4. Select the downloaded file

**Compatible editors:**

Advanced JSON Studio is compatible with VS Code **1.80.0 and above**, including popular forks:
- [Cursor](https://cursor.sh)
- [Windsurf](https://windsurf.com)
- [Kiro](https://kiro.dev)
- [Positron](https://github.com/posit-dev/positron)

---

## 🖥️ Usage

Once installed, click the **Advanced JSON Studio icon** in the Activity Bar (left sidebar) to open the panel.

**Quick start:**

1. Paste any JSON (or YAML, XML, TOML, JWT…) into the input area
2. Press **Ctrl+Enter** or click **Parse**
3. Switch output tabs using the **View**, **Convert**, **Analyze** dropdowns or the tool buttons below

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl+Enter` / `Cmd+Enter` | Parse the current input |
| Right-click selection in editor | Parse Selection in Advanced JSON Studio |
| Right-click folder in Explorer | Generate Code from JSON |

---

## 🆓 Free vs Pro

| Feature | Free | Pro |
|---|---|---|
| JSON parsing & pretty-print | ✅ Unlimited | ✅ Unlimited |
| Tree view | ✅ Unlimited | ✅ Unlimited |
| Auto-repair | ✅ Unlimited | ✅ Unlimited |
| Format detection | ✅ Unlimited | ✅ Unlimited |
| Session tabs (up to 10) | ✅ Unlimited | ✅ Unlimited |
| Input persistence | ✅ Unlimited | ✅ Unlimited |
| YAML / XML / TOML / Properties | Limited | ✅ Unlimited |
| CBOR / BSON | Limited | ✅ Unlimited |
| Flatten / Unflatten | Limited | ✅ Unlimited |
| Base64 Encode/Decode | Limited | ✅ Unlimited |
| CSV Table | Limited | ✅ Unlimited |
| Schema Inference | Limited | ✅ Unlimited |
| Schema Validator | Limited | ✅ Unlimited |
| Query (JSONPath / JMESPath) | Limited | ✅ Unlimited |
| JWT Decode & Verify | Limited | ✅ Unlimited |
| JSON Diff | Limited | ✅ Unlimited |
| HTTP Client | Limited | ✅ Unlimited |
| Dummy JSON Generator | Limited | ✅ Unlimited |
| Code Generation (12 languages) | Limited | ✅ Unlimited |
| Save output to file | Limited | ✅ Unlimited |
| GraphQL Format | ✅ Unlimited | ✅ Unlimited |
| GraphQL Convert to JSON | Limited | ✅ Unlimited |

---

## 🆕 Changelog

### v1.0.3

- **GraphQL Studio** — sessions now support a dedicated GraphQL mode alongside JSON; switch any tab to GQL mode to get a purpose-built workspace
- **GQL Format** — parse and pretty-print any GraphQL SDL or query document using the official `graphql` library
- **GQL Convert to JSON** — convert a GraphQL SDL / query to its JSON AST representation; the output can be sent straight to the JSON parser
- **Session tab scrolling** — the session tab bar now wraps in a scrollable container so many open tabs stay reachable without overflowing the sidebar
- **Toolbar icon refresh** — toolbar action buttons now use compact Unicode symbols (✕ Clear, ⎘ Copy, ⇅ Sort, ⧉ Open) for a cleaner look at narrow widths

### v1.0.2

- **Floating Save** — the save action now floats over the output area and appears only for downloadable tabs (Pretty, Minify, YAML, XML, TOML, CBOR, BSON, CSV, Schema, Code Gen, etc.)
- **Open in Editor — focused layout** — opening the panel in the editor column now hides the session tab bar and the Pin / Open / Settings buttons; you get a full-size view without the UI that only belongs in the sidebar
- **Pin Input — visual toggle** — the 📌 Pin button now highlights when active, restores its pinned state on reopen, and clicking it again unpins
- **Tooltips — smarter positioning** — custom tooltips are now anchored to the hovered element and clamp to the viewport, so they stay fully visible even in a narrow VS Code sidebar
- **Clear & Session switch** — clearing the input or switching session tabs now reliably wipes every output panel; a session with unparsed input is now re-parsed on switch so stale data from another session can never leak in
- **HTTP Client — risk warning** — sending to `localhost` / private IPs / `.local` / `.internal` hosts now shows an inline warning banner with Proceed / Cancel and a "don't warn again this session" option
- **Security — ReDoS hardening** — JSON syntax highlighter rewritten as a linear O(n) tokenizer; the previous regex could backtrack on crafted input

### v1.0.1

- **Graph — Open in Editor** — graph now opens as a real VS Code editor tab with full pan, zoom, drag, arrowhead edges, and node tooltips
- **Graph — arrowhead edges & tooltips** — edges now draw with directional arrowheads; hovering a node shows key, type, and value in a tooltip
- **Settings — three-tab panel** — Settings is now split into General, Privacy, and License tabs
- **Settings — indent size** — configurable indent size (2 / 4 / 8 spaces) in General tab, persisted across restarts
- **Analytics** — anonymous usage analytics (opt-out toggle in Privacy tab); no JSON data ever sent
- **HTTP Client** — "→ Use as Input" button sends response body to the main parser
- **HTTP Client** — input bar no longer disappears after a response loads (layout fix)
- **JWT** — invalid tokens now show "This is not a valid JWT token." instead of attempting to decode
- **Session tabs** — active tab selection now correctly restored after VS Code restart
- **Tooltips** — every toolbar button, dropdown item, and action button now shows a custom tooltip on hover
- **Code Gen** — fully local via quicktype-core (no network call)

### v1.0.0

- Initial VS Code release
- Full parity with the IntelliJ Advanced JSON Studio feature set
- **Session Tabs** — up to 10 independent sessions with full persistence across restarts
- **Local Code Generation** — all 12 languages powered by [quicktype-core](https://github.com/glideapps/quicktype) — no network required
- **Right-click Generate Code** — context menu on any folder opens a syntax-highlighted JSON editor panel; generated file written directly into the folder
- **Input persistence** — auto-saved on every parse; restored on next open
- **⚙ Settings panel** — slide-in licence management with Activate / Deactivate
- **OS Keychain storage** — licence key stored in macOS Keychain / Windows Credential Manager / Linux Secret Service
- **Compatible with VS Code 1.80+** including Cursor, Windsurf, Kiro, and Positron

---

## ❤️ Support

If Advanced JSON Studio saves you time, consider supporting its development:

[☕ Support on Ko-fi](https://ko-fi.com/S6S0176OVQ)

[![](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/godwinj)

Every contribution — large or small — directly funds bug fixes, new features, and long-term maintenance. Thank you. ❤️

---

## 📬 Feedback & Issues

Found a bug or have a feature request?  
👉 [Open an issue on GitHub](https://github.com/godwinjk/advanced_json_studio_vscode/issues)
