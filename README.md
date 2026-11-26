# Valm Dex

**Not your ordinary Roblox Dex.**

Let's be honest, there are already plenty of basic Dex tools around. Instead of another basic-ass Dex like Dex REContinued or LQ Explorer, Valm Dex brings its own decompiler, Fin assistant, advanced Explorer search, AI Beautifier, plugin system, and more.

There's a lot more going on here than just looking through instances.

## Features

### Explorer
- Advanced search by name, class, full path, tags, attributes, and GUI text.
- Combine filters and save your own filter presets.
- Inspect instances, properties, attributes, and children.
- Insert objects directly from the Explorer.
- Multiple Roblox class icon styles.

### Decompiler
- Valm's native decompiler.
- Reconstruction for nested functions and complex control flow.
- Additional fallback decompiler support.
- Output for inspecting and analyzing scripts.

### Fin — Dex Helper
Fin is the built-in helper inside Valm Dex. It can answer questions and use MCP tools to inspect your game.

It can help with:
- Finding and inspecting instances.
- Checking properties, attributes, and tags.
- Searching scripts and inspecting the active script.
- Listing RemoteEvents.
- Auditing Workspace.
- Checking plugins and runtime information.
- Checking decompiler status.

Fin also supports configured AI providers. Local help functions remain available when AI isn't configured.

### AI Beautifier
- Beautify scripts using your selected AI provider.
- Configure providers, models, and endpoints.
- Adjust generation settings.
- Keep its own settings separate from the main AI configuration.
- Use shared provider credentials where configured.

### Plugin Manager
- Import and manage plugins.
- Create custom tabs and UI elements.
- Add buttons, toggles, sliders, dropdowns, textboxes, and notifications.
- Register and call plugin functions.
- Access supported Dex services and theme information.

### Themes & Class Icons
- Multiple interface themes.
- Theme-aware dropdowns and pickers.
- Different Roblox class icon sets.
- Custom plugin icons.
- Consistent styling across the interface.

---

## Plugin Security — READ THIS.

**Plugins can be DANGEROUS. Seriously. Like, seriously.**

You might be thinking:

> "But these ninjas are probably just gonna do `print("hi")` anyways and act like a useless plugin. What's the point?"

Well, GOOD QUESTION!

**Deobfuscation.**

Not every developer wants you to see what their plugin is doing. Some plugins have readable source, others are heavily obfuscated, and some load additional code from somewhere else.

That's the problem. A plugin can look completely harmless while the actual code doing the work is buried somewhere you wouldn't think to look.

A malicious plugin could potentially:
- Steal API keys or other credentials it can access.
- Collect personal information available to its environment.
- Send information to an external server.
- Download and execute additional code.
- Read or modify data exposed by the executor.
- Hide suspicious behavior behind obfuscated functions and encoded strings.

### Why deobfuscation?

Obfuscation makes code harder to read. Deobfuscation can help turn confusing code into something easier to inspect.

That's useful when checking suspicious plugins. You can look for unexpected requests, hidden payloads, credential access, and code that doesn't seem related to what the plugin claims to do.

But don't get it twisted: **deobfuscation does not automatically make a plugin safe.** Some code is generated or loaded dynamically, and a plugin can change what it executes at runtime.

### Before installing a plugin

1. Check who made it. Don't trust a random upload just because it has a nice icon.
2. Look through the source code when it's available.
3. Be suspicious of unexplained HTTP requests, remote code loading, and hidden payloads.
4. Check for unexpected access to API keys, files, clipboard contents, or other sensitive data.
5. Be careful when a plugin is heavily obfuscated and the developer refuses to explain why.
6. Check plugin updates too. A previously harmless plugin can change later.
7. Remove anything behaving suspiciously.

**And no, a plugin being listed in the Plugin Manager doesn't automatically mean it's safe.**

Only install plugins you trust. Third-party plugins may execute code with the permissions available to the environment running Valm Dex.

---

## API Keys & Privacy

**Don't worry, we've got you! Your privacy matters.**

Valm Dex uses your configured API keys to authenticate requests with the AI provider you select.

Keep your keys private. Don't put them in public plugin source, screenshots, shared scripts, or bug reports. Never give your key to a plugin developer just because their plugin asks for it.

AI requests are sent to your selected provider, so check that provider's data policies before sending sensitive information.

Don't assume that a masked key in a settings textbox means every plugin is unable to access it. Always be careful about which code you run.

---

## A Note About Security

Valm Dex is a client-side tool. It does not promise that its interface, executor activity, or scripts are invisible to a game's server-side security or exploit detection.

Different games use different detection methods. Don't treat any client-side tool as a guarantee of being undetected.
---

**Valm Dex. More than just another Dex.**
