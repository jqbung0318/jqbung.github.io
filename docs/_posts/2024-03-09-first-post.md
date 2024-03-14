---
layout: post
title:  "I have finally started tech blogging"
date:   2024-03-09 15:19:06 +0800
# categories: blog, github, jekyll
---

# I have finally started tech blogging

* Do not remove this line (it will not be displayed)
{:toc}

Finally, I have surrendered my memory capacity on remembering every stuff I had done/learnt throughout my career path or my daily life. With the COVID infections and the aging, I can feel that I am no longer recall things very well. So in order to get a chance to review my own tech life, I have decided to begin my tech blogging here. If you managed to find this post anywhere from the internet, either via SEO or my connections, congraz you are the OG viewer.

## What tech did I used for my blog?
I had deployed this blog via Github pages. Partially out of the curiosity on Static Site Generation with Github, I worked this blog with Jekyll. Despite of Jekyll not being the most popular way of starting the blogs, it works very well with markdown and liquid template. With those, writing the blog is kinda similar to how I was writing my HTML template in Django and documentation for Software Version Control (SVC).

### Why not using Notion, Google Doc?
I was initially documenting most of my tech stuff in Notion privately. The innovation of Notion is actually a pretty crazy. It has the database-like feature, 3rd party software integrations etc. With the recent AI feature, I do personally feel that piece of tech is getting out of hand, and it strive way too far for my simple use case, which just to make my notes.

Google Doc is out of question with the messy organisation and accessibility. And I am taking this opportunity to share my experience and walkthrough to anyone who are trying to find "tutorials" or "HOW-TOs".

## How can you start blogging in Github? / How can you "copy" my setup?
Actually, instead of a HOW-TO, it is more for a memo for me to record all the steps to start any github pages with Jekyll from scratch. Who knows I may be automating the progress of this into other coming frameworks of mine.

Note that this requires some level of coding experience to clone my setup.

### A. Create new repository
Create a new Github repository(repo). This Github repo must be a public repo if you are the free users. While if you are in the subscriptions of Pro, Team, Enterprise Cloud/Server, you can do this with private repo.

In the Github repository, look for "Settings". In the left side of settings page, look for the "Code and automation" section, click into "Pages". In Github Pages, you can select to deploy from which branch, as well as folders for the site.

### B. Setup Ruby
Jekyll utilises Ruby programming language for its operations. Based on your working Operating System (OS), you will have different steps to install Ruby. Here I will be mainly focus on setup with MacOS. If you are coming from different OS, you can refer to the instructions provided by [Jekyll official website here](https://jekyllrb.com/docs/installation/)
```shell
# 3. Install homebrew for custom packages.
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 4. Install chruby and latest version of Ruby
brew install chruby ruby-install xz
ruby-install ruby 3.1.3

# 5. Points the system default ruby whenever you started the terminal
# replace .zshrc with .bashrc or .config/fish/config.fish depends on your default terminal
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.3" >> ~/.zshrc # run 'chruby' to see actual version

# 6. Close the current terminal, relaunch and check for ruby version
ruby -v # <== this should gives you 3.1.3

# 7. Install jekyll and bundler
gem install jekyll; gem install bundle
```

### C. Setup local development environment
```shell
# 8. Clone the Github repository to local
git clone https://github.com/<your github username>/<your git repo>.git
cd <your git repo>

# 9. Create the folder/directory
mkdir docs

# 10. Create jekyll template pages
jekyll new --skip-bundle .
```
Jekyll by default creates the base templates for blogging. Before you can go ahead customising your blog, there're a few more stuff that we need to configure to make sure the blog is compatible for Github Pages.

In `Gemfile`:
-  comment the line `gem "jekyll", "~> 4.3.3"` (adding # in front of the line)
-  uncomment the line `gem "github-pages", group: :jekyll_plugins` (remove # in front of the line)
-  add a line `gem webrick` (as mentioned in the [Jekyll Quickstart guide](https://jekyllrb.com/docs/))
<br/><br/>

Do another `bundle update` in the terminal will do the package updates.

### D. Start your development/blogging
You are good to go! You can now start writing your own posts or get a new themes for your pages. For all the themes resource, you can look into [Jekyll Themes](https://jekyllrb.com/resources/#themes).

If you were to look for the theme that I used, you can refer to [jekyll-theme-console](https://github.com/b2a3e8/jekyll-theme-console). Simply commenting out the minima theme in `_config.yml` and add the new gem. For sure you may find there's no such theme color as mine simply because I overriding the existing theme. You can copy my `_sass` folder as the reference.


## Verdict
As you can see, this is definitely not a smooth process to start the blogging for a non technical person. With simpler approach like Wordpress, you can create your own blogs with more designs and more colorful posts.

For a not so GUI, terminal nerd, this is sufficient enough for me. Happy blogging.


## Reference
[jekyll-theme-console](https://github.com/b2a3e8/jekyll-theme-console/)
