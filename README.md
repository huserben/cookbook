# Cookbook

This project is using [xcookybooky](https://ctan.org/pkg/xcookybooky?lang=en) to create a nicely looking cookbook using LaTeX.

The repo contains a github action workflow that creates the pdf and publishes it to a *gh-pages* branch. This then is made available publicly under [https://huserben.github.io/cookbook/](https://huserben.github.io/cookbook)

# Build Locally
In order to build and use the sources locally, do the following:

1. Install TextLive (https://www.tug.org/texlive/acquire-netinstall.html)
2. Add Tex Live bin folder to path (e.g. D:\texlive\2021\bin\win32)  
  2.1 Pro tip: Run "kpsewhich --var-value TEXMFLOCAL" to find your local directory
3. Get emerald font from https://ctan.org/pkg/emerald?lang=en  
  3.1 Extract the font and tex directory to the local text live install (e.g. D:\texlive\texmf-local)
4. Install font (as described here https://www.tug.org/fonts/fontinstall.html)  
  4.1 Run the commands from the font map directory (e.g. D:\texlive\texmf-local\fonts\map\dvips):
  ```
    mktexlsr
    updmap-sys --force --enable Map=emerald.map
    mktexlsr
  ```
5. After this start TeXStudio and try to compile and show the cookbook. You should be all set now!
