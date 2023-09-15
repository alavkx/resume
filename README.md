# Alec Lavoie — UI Engineer

## Usage

To generate a PDF from this LaTeX code, navigate to this folder in a terminal and run:

```bash
sudo texliveonfly -c xelatex resume.tex
```

## [Installation instructions]

```bash
brew install --cask basictex
echo "export PATH=/usr/local/texlive/2016basic/bin/x86_64-darwin:$PATH" >> ~/.zsh_profile
sudo tlmgr update --self
sudo tlmgr install texliveonfly
```

## Debugging

### env: python: No such file or directory

You may be on a new mac which does not come with python or python2 installed. You can symlink the python3 executable to the expected python directory to make this work with no additional install.

```bash
sudo mkdir -p /usr/local/bin # Thankfully, `/usr/local/bin` is already in the path
sudo ln -s /usr/bin/python3 /usr/local/bin/python
# Running now will return `xcode-select: Failed to locate 'python', requesting installation of command line developer tools.`
# To avoid that, you also need to symlink for xcode-select
sudo ln -s /Library/Developer/CommandLineTools/usr/bin/python3 /Library/Developer/CommandLineTools/usr/bin/python
```

Re-run `sudo texliveonfly -c xelatex resume.tex` and you may be in luck.
