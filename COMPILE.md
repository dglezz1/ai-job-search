# Compiling the CV

## First-time setup (already done)

```bash
# Install TinyTeX (user-level, no sudo)
curl -fsSL https://yihui.org/tinytex/install-bin-unix.sh | sh /tmp/tinytex-install-bin-unix.sh /tmp --no-path
export PATH="$PATH:$HOME/Library/TinyTeX/bin/universal-darwin"

# Install required LaTeX packages
tlmgr install moderncv fontawesome5 fontawesome6 academicons import luatexbase pgf titlesec textpos xltxtra xunicode cite realscripts needspace
```

PATH is now in your `~/.zshrc` automatically.

## Compile the master CV

```bash
cd ~/Developer/ai-job-search/cv
lualatex -interaction=nonstopmode -halt-on-error main_david.tex
lualatex -interaction=nonstopmode -halt-on-error main_david.tex  # run twice for refs
open main_david.pdf
```

## Compile a tailored CV (per role)

1. Copy `main_david.tex` to `main_david_<role>_<company>.tex`
2. Edit the profile statement + reorder competencies + adjust bullet emphasis
3. Compile with lualatex

## Compile a cover letter

```bash
cd ~/Developer/ai-job-search/cover_letters
# Edit cover_<company>.tex with recipient + body
xelatex cover_<company>.tex
```

(Cover letters need xelatex, not lualatex — they use fontspec.)
