{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fmodern\fcharset0 Courier;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\partightenfactor0

\f0\fs26 \cf0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 ---\
layout: post\
title:  "Your Step-by-Step Guide to Creating a Free Blog with Jekyll and GitHub Pages"\
date:   2025-08-25 11:42:00 +0530\
categories: jekyll github tutorial\
---\
\
Have you ever wanted to start your own blog without the cost and complexity of traditional hosting platforms? You're in the right place. This guide will walk you through the entire process of creating a fast, secure, and completely free blog using Jekyll, a powerful static site generator, and GitHub Pages for hosting.\
\
Let's dive in!\
\
### Step 1: Getting Your System Ready\
\
Before we can start building, we need to install a few essential tools. Jekyll is built with a programming language called Ruby, so the first step is to get a modern version of Ruby running on your computer.\
\
#### For macOS Users:\
\
Setting up on a Mac is smooth with the help of Homebrew, a package manager for macOS.\
\
1.  **Install Homebrew**: If you don't have it already, open your Terminal and run this command:\
    ```bash\
    /bin/bash -c "$(curl -fsSL [https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh))"\
    ```\
2.  **Install Ruby**: Next, use Homebrew to install the latest version of Ruby.\
    ```bash\
    brew install ruby\
    ```\
3.  **Configure Your Terminal's PATH**: This is a crucial step to tell your terminal to use the new version of Ruby instead of the outdated one that comes with macOS. You'll need to add both the Ruby and Ruby Gems directories to your PATH.\
    ```bash\
    echo 'export PATH="$(brew --prefix ruby)/bin:$PATH"' >> ~/.zshrc\
    echo 'export PATH="/usr/local/lib/ruby/gems/3.4.0/bin:$PATH"' | sudo tee -a ~/.zshrc\
    ```\
    *Note: If you install a different version of Ruby, you may need to update the version number in the second command.*\
4.  **Reload Your Terminal**: For the changes to take effect, either close and reopen the terminal window or run `source ~/.zshrc`.\
5.  **Install Jekyll and Bundler**: With your environment now configured, you can install Jekyll. **Do not use `sudo` for this command.**\
    ```bash\
    gem install bundler jekyll\
    ```\
\
#### For Windows Users:\
\
The easiest way to get started on Windows is with the RubyInstaller.\
\
1.  **Install Ruby+Devkit**: Download and run the [RubyInstaller](https://rubyinstaller.org/downloads/).\
    * Choose a **Ruby+Devkit** version (e.g., 3.2.x or newer).\
    * Run the installer, making sure the **"Add Ruby executables to your PATH"** box is checked.\
    * On the final screen, run the `ridk install` step and choose the `MSYS2 and MINGW development toolchain` option.\
2.  **Verify the Installation**: Open a **new** Command Prompt window and run `ruby -v` and `gem -v`. You should see version numbers appear. If not, try restarting your computer.\
3.  **Install Jekyll and Bundler**: In the command prompt, run:\
    ```cmd\
    gem install jekyll bundler\
    ```\
\
#### For Linux (Ubuntu) Users:\
\
1.  **Install Prerequisites**:\
    ```bash\
    sudo apt-get update\
    sudo apt-get install ruby-full build-essential zlib1g-dev\
    ```\
2.  **Configure Gem Path**:\
    ```bash\
    echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc\
    echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc\
    echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc\
    source ~/.bashrc\
    ```\
3.  **Install Jekyll and Bundler**:\
    ```bash\
    gem install jekyll bundler\
    ```\
\
### Step 2: Creating Your First Jekyll Blog\
\
With the tools installed, it's time for the fun part.\
\
1.  **Create a New Site**: In your terminal, navigate to where you want to store your blog and run:\
    ```bash\
    jekyll new my-awesome-blog\
    ```\
2.  **Enter the Directory**:\
    ```bash\
    cd my-awesome-blog\
    ```\
3.  **Preview Your Blog Locally**: Run the local server to see your new blog in action.\
    ```bash\
    bundle exec jekyll serve\
    ```\
    Now, open a web browser and go to `http://localhost:4000`. You should see the default Jekyll blog!\
\
### Step 3: Setting up on GitHub\
\
Next, we'll create a free home for your blog on GitHub.\
\
1.  **Create a GitHub Account**: If you don't have one, sign up at [github.com](https://github.com).\
2.  **Create a Special Repository**:\
    * Click the "+" icon and select "New repository."\
    * The repository name has a special format: `your-username.github.io`. (e.g., if your username is `octocat`, the repo is `octocat.github.io`).\
    * Ensure the repository is **Public** and click "Create repository."\
\
### Step 4: Pushing Your Blog to GitHub\
\
Let's connect your local blog to your new GitHub repository.\
\
1.  **Initialize Git**: In your blog's folder, run:\
    ```bash\
    git init\
    ```\
2.  **Add the Remote Repository**:\
    ```bash\
    git remote add origin [https://github.com/your-username/your-username.github.io.git](https://github.com/your-username/your-username.github.io.git)\
    ```\
    *(Replace `your-username` with your actual GitHub username).*\
3.  **Add, Commit, and Push Your Files**:\
    ```bash\
    git add .\
    git commit -m "Initial commit"\
    git push -u origin main\
    ```\
After a few minutes, your blog will be live at `https://your-username.github.io`!\
\
### Step 5: Writing Your First Post\
\
1.  **Create a New Post File**: In your project's `_posts` directory, create a new file named `YYYY-MM-DD-your-post-title.md`.\
2.  **Add Content**: Open the file and add "front matter" and your content.\
    ```markdown\
    ---\
    layout: post\
    title:  "My First Blog Post!"\
    date:   2025-08-25 10:00:00 +0530\
    categories: jekyll update\
    ---\
\
    ## Hello World!\
\
    This is my first post on my new Jekyll blog. It's written in Markdown.\
    ```\
3.  **Commit and Push**: Save your file, then commit and push the changes. Your new post will appear on your live blog shortly.\
    ```bash\
    git add .\
    git commit -m "Add first blog post"\
    git push\
    ```\
\
### Step 6: Customizing Your Blog\
\
* **Configuration**: Edit the `_config.yml` file to change your blog's title, description, and more.\
* **Themes**: Give your blog a new look by installing a Jekyll theme. A great place to browse is [jekyllthemes.org](http://jekyllthemes.org/).\
\
### Step 7: Using a Custom Domain\
\
Want to use a domain like `blog.yourdomain.com`?\
\
1.  **Add a CNAME File**: In the root of your project, create a file named `CNAME` and add your full subdomain on a single line (e.g., `blog.teachmeai.in`). Commit and push this file.\
2.  **Configure Your DNS**: Log in to your domain registrar and create a new **CNAME record**.\
    * **Host**: `blog`\
    * **Value**: `your-username.github.io`\
\
### macOS Installation Troubleshooting\
\
Running into trouble during the setup? Here are fixes for the most common macOS issues.\
\
* **Error: `zsh: command not found: jekyll`**\
    This means your terminal can't find the Jekyll program. It's almost always a `PATH` issue.\
    1.  **Conda Interference**: If your prompt starts with `(base)`, your Conda environment is likely overriding your PATH. Deactivate it with `conda deactivate`.\
    2.  **Reload Shell**: Always run `source ~/.zshrc` after making changes or deactivating Conda to ensure the new PATH is loaded.\
    3.  **Verify Paths**: Make sure you've run the two `echo 'export PATH=...'` commands from Step 1 correctly.\
\
* **Error: `zsh: permission denied: /Users/yourname/.zshrc`**\
    This happens when you try to write to your `.zshrc` file. Use this command format instead:\
    ```bash\
    echo 'THE-TEXT-YOU-WANT-TO-ADD' | sudo tee -a ~/.zshrc\
    ```\
\
* **Error: `Bundler::PermissionError` during `jekyll new`**\
    This means you don't have permission to write to the folder where Ruby gems are installed. You need to take ownership of the directory.\
    ```bash\
    sudo chown -R $(whoami) /usr/local/lib/ruby/gems/3.4.0\
    ```\
    *(Remember to adjust the version number if you used a different version of Ruby).*\
\
* **Error: `Conflict: /path/to/blog exists and is not empty`**\
    This happens when a previous `jekyll new` command failed and left behind an empty folder. It's safe to remove it and try again.\
    ```bash\
    # Replace 'my-awesome-blog' with your actual folder name\
    rm -rf my-awesome-blog\
    ```\
\
### GitHub Push Troubleshooting\
\
Can't push your code to GitHub? Here are the solutions.\
\
* **Error: `src refspec main does not match any`**\
    This means your local branch isn't named `main` or you haven't made any commits.\
    1.  First, make a commit: `git add .` followed by `git commit -m "Initial commit"`.\
    2.  Then, rename your branch to match GitHub's standard: `git branch -M main`.\
    3.  Try pushing again.\
\
* **Error: `Permission to user/repo.git denied to other-user`**\
    Your Mac has saved the wrong GitHub credentials.\
    1.  Open the **Keychain Access** app.\
    2.  Search for `github.com` and delete the entry.\
    3.  Try pushing again. It will now ask for the correct username and password (or token).\
\
* **Error: `Password authentication is not supported` or `Invalid username or token`**\
    GitHub no longer accepts passwords for command-line operations. You must use a **Personal Access Token (PAT)**.\
    1.  **Generate a Token**: On GitHub, go to `Settings > Developer settings > Personal access tokens > Tokens (classic)`.\
    2.  Click **Generate new token**.\
    3.  Give it a name, set an expiration, and **check the `repo` scope**. This is essential.\
    4.  Click **Generate token** and **copy the token immediately**.\
    5.  **Use the Token**: When the terminal asks for your password, paste the PAT instead.\
\
Happy blogging!\
\
}