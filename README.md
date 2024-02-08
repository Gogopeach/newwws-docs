# Newwws Documentation

Welcome to the documentation site for Newwws.

## Installation

### Step 1: Install Homebrew

First, make sure you have Homebrew installed. If not, you can install it by running the following command in your terminal:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Step 2: Install chruby via Homebrew

Next, use Homebrew to install chruby along with other dependencies:

```bash
brew install chruby ruby-install xz
```

### Step 3: Install Ruby

After installing chruby, you can install Ruby with the following command:

```bash
ruby-install ruby 3.1.3
```

### Step 4: Configure Chruby in your Shell

Depending on your preferred shell (e.g., zsh or bash), add the following lines to your shell configuration file (usually ~/.zshrc for zsh or ~/.bash_profile for bash):

For zsh:

```bash
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.3" >> ~/.zshrc # run 'chruby' to see actual version
```

For bash:

```bash
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.bash_profile
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.bash_profile
echo "chruby ruby-3.1.3" >> ~/.bash_profile # run 'chruby' to see actual version
```

### Step 5: Install Dependencies

Now, install the necessary dependencies using RubyGems:

```bash
gem install jekyll bundler
```

### Step 6: Run the Documentation Locally

To view the documentation site locally, run the following command:

```bash
bundle exec jekyll serve
```

### Deployment

We use GitHub Actions to deploy and host the site via GitHub Pages. For deployment instructions, please refer to the .github folder.
