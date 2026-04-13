# Claude Skills

Kolekce custom skillů pro Claude Code a Claude.ai.

## Struktura

```text
├── skill-name/
│   ├── SKILL.md
│   └── ...pomocné soubory
├── another-skill/
│   ├── SKILL.md
│   └── ...
```

## Instalace pro Claude Code

### Konkrétní skill do projektu

```bash
cp -r claude-skills/skill-name .claude/skills/
```

### Globální instalace (pro všechny projekty)

```bash
cp -r claude-skills/skill-name ~/.claude/skills/
```

## Použití v Claude Code

Spusťte `claude` a v konverzaci aktivujte skill pomocí lomítka například pro skill `tech-doc`:

```text
> /tech-doc
```

Claude načte instrukce ze skillu `tech-doc` a bude je následovat. Například `/tech-doc` přidá instrukce pro vytváření technické dokumentace ke kódu — stačí pak popsat co chcete zdokumentovat.

## Instalace pro Claude.ai

1. Na [claude.ai](https://claude.ai) jděte do **Customize → Skills**
2. Nahrajte buď:
   - **ZIP soubor** (pro skill s více soubory)
   - **SKILL.md** přímo (pro jednoduchý skill bez dalších souborů)

```bash
# zabalení skillu do ZIPu
cd claude-skills
zip -r skill-name.zip skill-name/
```

## OpenCode

[OpenCode](https://github.com/anomalyco/opencode) automaticky detekuje nainstalované Claude skilly z `.claude/skills/` a `~/.claude/skills/`. Díky tomu lze skilly používat i s jinými modely (GPT, Gemini, atd.) bez jakékoliv další konfigurace.

## Použití s dalšími modely

Skilly jsou v základu jen markdown soubory s instrukcemi — fungují s jakýmkoliv LLM. Dvě možnosti:

- **System prompt** — vložte obsah `SKILL.md` jako system prompt do nástroje, který používáte
- **Manuálně v chatu** — řekněte modelu ať si přečte soubor: `Přečti si ./skill-name/SKILL.md a řiď se tím`
