# BlockBorn Wiki

The wiki for BlockBorn, built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)
and hosted free on GitHub Pages. Every push to `main` rebuilds the site in about a minute.

## Writing a page

Pages are plain Markdown files in `docs/`. The folder a file sits in is its address:
`docs/world/mystbloom.md` becomes `/world/mystbloom/`.

1. **Make the file.** On GitHub, open the `docs` folder, then **Add file > Create new file**,
   and type a name like `world/mystbloom.md` (typing `/` makes a folder).
2. **Write it.** Start with a `# Title` line, then write normally.
3. **Add it to the menu.** Open `mkdocs.yml` and add a line under `nav:`, e.g.

   ```yaml
   - World:
       - world/index.md
       - Mystbloom Dungeon: world/mystbloom.md
   ```

4. **Commit.** The site updates itself. Watch the **Actions** tab if you want to see it build.

## Cheat sheet

| You want | Write |
|---|---|
| Heading | `## Heading` (`###` for smaller) |
| Bold / italic | `**bold**`, `*italic*` |
| Link to another page | `[the eras](../progression/eras.md)` |
| Image | put it in `docs/assets/`, then `![Alt text](assets/pic.png)` (path is relative to the page) |
| Table | `\| Item \| Era \|` rows, with `\|---\|---\|` under the header |
| Tip box | `!!! tip "Title"` then the text indented 4 spaces (also `note`, `warning`, `danger`) |
| Collapsible box | `??? note "Spoiler"` then the text indented 4 spaces |
| Era label | `<span class="pill era">Era 2</span>` |
| Gold label | `<span class="pill gold">Rare</span>` |
| Star rating | `<span class="stars">★★★</span>` |
| Hidden note to self | `<!-- only you can see this -->` |
| Icon | `:material-sword:` (search icons at https://pictogrammers.com/library/mdi/) |

**Card grid** (like the home page):

```markdown
<div class="grid cards" markdown>

-   **Card title**

    ---

    Some text. [Read more](page.md)

</div>
```

## Previewing on your computer (optional)

```bash
pip install -r requirements.txt
mkdocs serve
```

Then open http://127.0.0.1:8000. The page reloads as you save.

## Changing the look

- Colours and fonts: `docs/stylesheets/extra.css` (the variables at the top match the game's UI palette).
- The home page banner: `overrides/home.html`; its tagline is in `docs/index.md`.
- The **Play on Roblox** button: `play_url` in `mkdocs.yml`.
- Logo: `docs/assets/logo.svg`.
