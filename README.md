# Políticas de Privacidade — hub multi-jogo (GitHub Pages)

Site estático único que serve as **Políticas de Privacidade de todos os jogos** da
Brazil Games Studio. Um só GitHub Pages para o estúdio inteiro — cada jogo novo é
só uma subpasta a mais, sem precisar criar outro repositório/Pages.

```
politica-privacidade/
  index.html          → HUB (lista os jogos e linka cada política)
  style.css           → visual compartilhado por todas as páginas
  spectrum/
    index.html        → política do SPECTRUM (Português)
    en.html           → política do SPECTRUM (Inglês)
  <proximo-jogo>/     → cada jogo futuro entra assim
    index.html
    en.html
```

Não há segredo aqui dentro — pode ser um repositório **público**.

---

## Publicar no GitHub Pages

O repositório do jogo é **privado**, e o Pages grátis só funciona em repo público.
Então crie **um** repositório público para o hub (serve todos os jogos).

### Recomendado: repo `brazil-games-studio.github.io` (URLs limpas)

Um repositório com esse nome exato vira a **raiz** do Pages da organização/usuário.

1. Crie em <https://github.com/new> um repo **público** chamado
   `brazil-games-studio.github.io`.
2. Suba o **conteúdo desta pasta** (os arquivos e as subpastas), não a pasta em si:
   `index.html`, `style.css` e a pasta `spectrum/` ficam na raiz do repo.
3. **Settings → Pages → Source:** *Deploy from a branch* · **Branch:** `main` `/(root)` → **Save**.
4. Em ~1 min o site fica no ar:

| Página | URL |
| --- | --- |
| Hub | `https://brazil-games-studio.github.io/` |
| SPECTRUM (usar na Play) | `https://brazil-games-studio.github.io/spectrum/` |

### Alternativa: repo de projeto `politicas`

Se preferir não usar o repo especial, crie um repo público `politicas`, suba o
mesmo conteúdo e ative o Pages igual. As URLs ficam com o nome do repo no meio:

- Hub: `https://brazil-games-studio.github.io/politicas/`
- SPECTRUM: `https://brazil-games-studio.github.io/politicas/spectrum/`

### Por git (linha de comando)

```powershell
# dentro desta pasta (politica-privacidade)
git init
git add .
git commit -m "Hub de politicas de privacidade da Brazil Games Studio"
git branch -M main
git remote add origin https://github.com/brazil-games-studio/brazil-games-studio.github.io.git
git push -u origin main
```
Depois ative o Pages em **Settings → Pages** (branch `main`, `/(root)`).

---

## Usar a URL na Play Console

Para o SPECTRUM, cole a URL **da subpasta do jogo** (não a do hub):
```
https://brazil-games-studio.github.io/spectrum/
```
em **Play Console → Política → Política de Privacidade** (e no formulário da ficha).

---

## Adicionar um jogo novo (no futuro)

1. Duplique a pasta `spectrum/` com o nome do novo jogo (ex.: `meujogo/`).
2. Edite `meujogo/index.html` e `meujogo/en.html`: nome do jogo, pacote, e o que
   ele coleta de verdade (ranking? anúncios? compras?).
3. No `index.html` do hub, copie o bloco `<li class="game">` do SPECTRUM e aponte
   o `href` para `meujogo/`.
4. Suba de novo (upload ou `git push`). O Pages atualiza sozinho.

> O `style.css` é compartilhado: as páginas dos jogos o referenciam como
> `../style.css` (um nível acima). O hub usa `style.css` (mesma pasta).

---

## Contato configurado

E-mail de contato nas políticas e no hub: **brazilgamesstudio@gmail.com**.
