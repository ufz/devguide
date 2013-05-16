---
layout: default
title: Virtual Machines on Windows
description: A quick guide to get you started with Vagrant on Windows
categories: advanced
---

- Install Ruby 1.9.3 with its [installer](http://rubyforge.org/frs/download.php/76798/rubyinstaller-1.9.3-p392.exe)
  - Install to `C:\Ruby193`
  - During installation add ruby binaries to the path
- Install the Ruby DevKit
  - [Download it](https://github.com/downloads/oneclick/rubyinstaller/DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe)
  - Extract to `C:\Ruby193\DevKit`
  - In the terminal run:
        {% highlight ruby %}
cd C:\Ruby193\DevKit
ruby dk.rb init
ruby dk.rb review
ruby dk.rb install
{% endhighlight %}

- Download [ogs-vagrant](https://github.com/bilke/ogs-vagrant/archive/master.zip) and unzip it
- Go in to the ogs-vagrant directory and run from terminal:
    {% highlight ruby %}
gem install bundler
bundle install --path .bundle --binstubs
ruby bin\librarian-chef install
{% endhighlight %}

- Add optional configuration settings, see the [README](https://github.com/bilke/ogs-vagrant/blob/master/README.md#optional-configuration)-file
- Start the virtual machine with
    {% highlight ruby %}
vagrant up
{% endhighlight %}
