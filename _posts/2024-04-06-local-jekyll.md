---
layout: post
title: Jekyll
---

საიტის ლოკალში დასაწერად საჭიროა Jekyll-ის ლოკალურად ინსტალაცია.

## Jekyll-ის ინსტალაცია

ჩემი ოპერაციული სისტემა არის Linux-ი, კერძოდ Manjaro-Sway, ამიტომ ინსტრუცქციაც ჩემს სისტემას ეხება

Jekyll-ი დაწერილია Ruby-ზე, ამიტომ გვჭირდება მისი ინსტალაცია:

```
sudo pacman -Syu Ruby
```
შემდეგ საჭირო პაკეტებიც:

```
sudo pacman -S base-devel libffi libyaml openssl zlib
```

შემდეგ შესაბამისი gem-ები, გვჭირება Jekyll და Bundler:

```
gem install jekyll bundler
```

შემდეგ გვჭიდება path-ები Ruby-სთვის(მე მაქვს zsh):

```
echo 'export GEM_HOME="$(ruby -e "puts Gem.user_dir")"' >> ~/.zshrc
```
ცალცალკე მოვიყვან იმისავის, რომ კოპირება იყოს უფრო მოხერხბული:

```
echo 'export PATH="$PATH:$GEM_HOME/bin"' >> ~/.zshrc

```

ყველაფერ ამას წავაკითხებთ:

```
source ~/.zshrc
```

ესაა სულ, ამის მერე უკვე პროექტის დირექტორიაში:

```
bundle install
```

საბოლოოდ:

```
bundle exec jekyll serve
```

თუ ეს ბრძანება დასრულდა შეცდომით, სავარაუდოდ რომელიმე gem-ს ვერ პოულობს და მათი ინსტალაცია უნდა მივუთითოთ ლოკალში, ეს ხდება `Gemfile`-ში მითითებით. ჩემს შემთხვევაში ეს ორი პაკეტია:

```
gem "webrick", "~> 1.7"
gem "json", "~> 2.5.1"
```

შეცდომის შეტყობინებაში გაიგებთ, რომელ პაკეტს ვერ პოულობს და იმ პაკეტს მიუტითებთ ლეკალში და გაამეორებთ მაღლითა ორ ბრძანებას:

```
bundle install
bundle exec jekyll serve
```
