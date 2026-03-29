# Avaliação de Large Language Models Aplicados à Pecuária Leiteira

Artigo acadêmico (TCC) utilizando o template Springer Nature.

## Estrutura do Projeto

```
.
├── main.tex            # Artigo principal
├── refs.bib            # Referências bibliográficas do artigo
├── figures/            # Figuras utilizadas no artigo
├── previous-work/      # Materiais de versões anteriores do trabalho
├── template/           # Template original Springer Nature (referência)
│   ├── sn-article.tex
│   ├── sn-article.pdf
│   ├── sn-jnl.cls
│   ├── sn-bibliography.bib
│   ├── bst/
│   ├── empty.eps
│   ├── fig.eps
│   └── user-manual.pdf
├── sn-jnl.cls          # Symlink → template/sn-jnl.cls
├── bst/                # Symlink → template/bst/
└── .gitignore
```

## Compilação

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Ou com `latexmk`:

```bash
latexmk -pdf main.tex
```

## Observações

- Os arquivos `sn-jnl.cls` e `bst/` na raiz são **symlinks** para o diretório `template/`, necessários para compilação.
- Adicione suas figuras na pasta `figures/` e referencie-as no `main.tex`.
- A pasta `previous-work/` contém materiais de versões anteriores e não deve ser misturada com o artigo atual.
