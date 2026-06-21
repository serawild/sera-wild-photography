# Sera Wild Photography

Statische Website für [sera-wild-test.com](https://sera-wild-test.com), gehostet über GitHub Pages.

## Inhalt

| Datei | Beschreibung |
|---|---|
| `index.html` | Einstiegsseite |
| `CNAME` | Custom-Domain-Konfiguration für GitHub Pages |

## Manuelle Schritte zum Go-Live

### 1. GitHub Pages aktivieren

1. Repository-Einstellungen öffnen → **Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / `/ (root)` → **Save**

GitHub generiert daraufhin eine `github.io`-URL und liest die `CNAME`-Datei automatisch ein.

### 2. DNS konfigurieren

Beim Domain-Registrar folgende DNS-Einträge setzen:

**Für Apex-Domain (`sera-wild-test.com`)** — vier A-Records:

```
@ A 185.199.108.153
@ A 185.199.109.153
@ A 185.199.110.153
@ A 185.199.111.153
```

**Optional: www-Subdomain** — ein CNAME-Record:

```
www CNAME serawild.github.io.
```

> DNS-Änderungen können bis zu 48 Stunden brauchen, bis sie weltweit sichtbar sind.

### 3. HTTPS aktivieren (nach DNS-Propagation)

Repository-Einstellungen → **Pages** → Haken bei **Enforce HTTPS** setzen.
