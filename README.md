# irenealegre.com

My UX Portfolio.

A [Jekyll][1] powered blog, hosted by [GitHub Pages][2] at https://irenealegre.com


## Setup

- Install [Homebrew][3]:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

- Install application:

```
brew cask install github
brew cask install atom
```

- Clone repostiry with GitHub desktop application

- Install Ruby Version Manager:

```
brew install rbenv ruby-build
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
```

- Close terminal and open it again.

- Install Ruby:

```
rbenv install 2.6.1
rbenv global 2.6.1
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
bundle exec jekyll server
```

- Go to http://127.0.0.1:4000

---

Built from scratch with lots of patience and some tea.


[1]: http://jekyllrb.com/
[2]: https://pages.github.com/
[3]: https://brew.sh/
