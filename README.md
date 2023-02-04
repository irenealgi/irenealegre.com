# irenealegre.com

My UX Portfolio.

A [Jekyll][1] powered blog, hosted by [GitHub Pages][2] at https://irenealegre.com


## Setup

- Install [Homebrew][3]:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

- Install application:

```
brew cask install github
brew cask install visual-studio-code
```

- Clone repository with GitHub desktop application

- Install Ruby Version Manager:

```
brew install asdf
asdf plugin add ruby
```

- Close terminal and open it again.

- Install Ruby:

```
asdf install ruby latest
asdf global ruby latest
```

- Go to the directory where your portfolio is.

- Install Ruby gems

```
gem install bundler
bundle install
```

## Usage

- Go to the directory where your portfolio is to run website on local

```
bundle exec jekyll server --livereload
```

The line above can be summarised by alias 'jekyll'. If the alias hasn't been created yet, use the line below to set it up. For the alias to work - if it hasn't been created yet - you will have to restart the tab so that it's updated.
```
echo 'alias jekyll="bundle exec jekyll server --livereload"' >> ~/.bash_profile
```

Therefore, to start the application just type in `jekyll`

- Go to http://127.0.0.1:4000

---

Built from scratch with lots of patience and some tea.


[1]: http://jekyllrb.com/
[2]: https://pages.github.com/
[3]: https://brew.sh/
