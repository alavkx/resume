# Alec Lavoie — UI Engineer

## Usage
To generate a PDF from this LaTeX code, navigate to this folder in a terminal and run:

    xelatex resume.tex

## [Installation instructions]
```bash
brew cask install basictex
echo "export PATH="/usr/local/texlive/2016basic/bin/x86_64-darwin:$PATH" >> ~/.bash_profile
sudo tlmgr update --self
sudo tlmgr install texliveonfly
```
