# Setting up Jekyll on Windows 10

There is no offically supported [Jekyll](https://jekyllrb.com/) distribution on Windows. 

This guide will use the Windows Subsystem for Linux (WSL) to install a Linux distribution on Windows 10 and then use that to install all the tools needed for Jekyll. 

> This needs a recent version of Windows 10 - at least 1809. You can check the Windows 10 version by holding the Windows Key ***&#8862;*** + ***R***, and then typing ***winver*** \<Enter>

## Install WSL

1. Open a PowerShell window as Administrator and run:
```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

2. Restart the computer when prompted

>Original instructions [here](https://docs.microsoft.com/en-us/windows/wsl/install-win10
)

## Install Ubuntu

Open the Windows 10 Microsoft Store and search for and install Ubuntu ![Ubuntu-App](images\ms-store-ubuntu.png)

## Install Jekyll

1. Open a Ubuntu terminal and install the ruby development environment

```bash
sudo apt-get install ruby ruby-dev build-essential gcc g++ make zlib1g-dev
```

2. Install Jekyll

```bash
gem install jekyll bundler
```

3. Run the Jekyll server on your markdown

* change to the github pages working directory
```bash
cd /mnt/c/projects/github-pages/
```

# Run Jekyll

```bash
bundle exec jekyll serve
```

If it is working you should see something like:
```
  Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

Navigate to [127.0.0.1:4000](http://127.0.0.1:4000) with a browser: ![localhost jekyll](images\localhost-jekyll.png)

# Troubleshooting

if an error like this appears:
>```
>Could not locate Gemfile or .bundle/ directory
>```
>Then a ***Gemfile*** needs to be created in the root directory with the following contents
>```ruby
>source 'https://rubygems.org'
>gem 'github-pages', group: :jekyll_plugins
>```

If an error like this appears:
>```
>Could not find gem 'github-pages' in any of the gem sources listed in your Gemfile.
>Run `bundle install` to install missing gems.
>```
>Run 'bundle install' to download and install the additional files needed for github pages.
>```bash
>bundle install
>```


Original instructions are [here](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll)

[Back](index.html)
