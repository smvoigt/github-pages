# Developing GitHub Pages on Windows 10

This guide demonstrates how to create a GitHub pages site. A GitHub pages site can be used to create static web pages for documentation, blogs or tutorials

## Creating a GitHub pages repository

1. On GitHub create a new repository. Your web site will have a URL that looks like https://username.github.io/repository-name

2. On the Create a New Repository page, add a .gitignore for Jekyll. [Jekyll](https://jekyllrb.com/) is a tool that GitHub uses to convert markdown text into html web pages. ![gitignore jekyll](images\gitignore-jekyll.png)

3. Open the repository settings page: ![Repository Settings](images\repo-settings.png)

4. Make this repository a GitHub Pages project by scrolling down to the GitHub pages section and setting the source to the master branch. ![GitHub Pages source naster branch](images\repo-setting-github-pages.png)

5. Set the GitHub pages theme. ![GitHub pages theme](images\repo-setting-github-pages-theme.png)

## Clone the repository

Using GitHub Desktop or your favourite git client, clone the repository

![GitHub Desktop Clone](images\github-desktop-clone.png)

## Add a landing page

The default landing page for a GitHub Pages project is typically generated from a file named index.md - open Visual Studio Code onto the cloned repository.

Add a file called index.md and create content in markdown. Visual Studio Code comes built in with a previewer for markdown code so you can get a feel for what it will look like.

![VS Code - index.md](images\vscode-index.md.png)

You can use markdown to link to other markdown files in your repository as well to build a static website.

When you have finished, you can commit and push the changes back to GitHub. After a few moments, you should see the updated page at github.io - ![github.io](images\github-io-website.png)

* [Setup Jekyll locally](jekyll-win10.html)



