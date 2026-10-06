# lawtern-plugins

Prywatny marketplace pluginów Lawtern dla Claude (Claude Code, claude.ai, Desktop, Cowork).

## Instalacja

**claude.ai / Desktop / Cowork:** Customize → Plugins → Add → Add marketplace → `paszkiewiczmichal/lawtern-plugins`,
potem dodaj plugin **Lawtern** i w zakładce Connectors kliknij **Connect** (logowanie do Lawtern).

**Claude Code:**

```
/plugin marketplace add paszkiewiczmichal/lawtern-plugins
/plugin install lawtern@lawtern-plugins
```

Przy pierwszym użyciu narzędzia Lawtern zaloguj się przez `/mcp` → `lawtern`.

## Struktura

```
.claude-plugin/marketplace.json     katalog pluginów (marketplace)
plugins/lawtern/
  .claude-plugin/plugin.json        manifest pluginu
  .mcp.json                         konektor MCP Lawtern (https://mcp.lawtern.com/)
  skills/                           skille jawne: router + cienkie skille wejściowe (w przygotowaniu)
```

Plugin nie ustawia `version`: użytkownicy dostają każdy commit z `main` przy aktualizacji marketplace.

## Walidacja

```
claude plugin validate .
claude plugin validate ./plugins/lawtern
```

## Licencja

Apache License 2.0 (`LICENSE`).
