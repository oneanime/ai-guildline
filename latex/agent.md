# LaTeX Auto Build Rules

Whenever you modify main.tex:

1. Automatically compile using:

```bash
mkdir -p out
docker run --rm -v "$(pwd)":/work -w /work texlive/texlive:latest \
  xelatex -interaction=nonstopmode -file-line-error -synctex=1 \
  -output-directory=out main.tex
```

2. If compilation fails:
   - Read out/main.log
   - Identify the first error (line starting with "!")
   - Fix main.tex directly
   - Recompile

3. Stop after 3 attempts if still failing.

4. When successful, confirm: "Build successful: out/main.pdf"