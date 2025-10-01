```bash
# =============================
#   DIOS — Dump In One Shot
# =============================
```

> ⚠️ **Disclaimer:** For educational, security research, and red team testing only.  
> Do not use this tool to exploit systems without explicit authorization.

```bash
[ Summary ]
DIOS is a proof-of-concept (PoC) payload that exports MySQL query results
into structured HTML format, making database dumps easier to read in a browser.
It leverages SQL concat with MySQL comments and hex encoding to inject HTML/CSS/JS.

[ Features ]
- Render MySQL server info (host, version, user, OS, port, datadir).
- Display user privileges and `information_schema` metadata (tables & columns).
- Outputs results styled with Bootstrap classes for a clean layout.
- Includes watermark/branding to mark the PoC source.

[ Ethics & Legal ]
- Use is allowed only if it is **legal** and **ethical** within your environment.
- The repository owner is **not responsible** for any misuse or illegal activity.
```

```bash
$ echo "Analyze responsibly. Use only in authorized labs."
```
