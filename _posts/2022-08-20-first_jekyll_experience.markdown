---
layout: post
title:  "My first Jekyll experience"
date:   2022-08-20 21:17:06 -0700
categories: jekyll update
---

I was following the tutorials in Github Pages to build a website. I typed in 

{% highlight shell %}
jekyll -new --skip-bundle .
{% endhighlight %}

and this gives

{% highlight shell %}
Command 'jekyll' not found, but can be installed with:

sudo apt install jekyll
{% endhighlight %}

indicating that I haven't installed jekyll.


Finally, what worked for me was:

{% highlight shell %}
bundle update sass
bundle install --path vendor/bundle --full-index
{% endhighlight %}

If I get 'permission denied' errors, I will do something like 
{% highlight shell %}
sudo chmod +w /usr/share/rubygems-integration/all/
{% endhighlight %}
or even something simpler, 
{% highlight shell %}
sudo mkdir /usr/share/rubygems-integration/all/bin
{% endhighlight %}

My main takeaway from this is that, when configuring things, follow the directions of the tutorial and do not deviate from them. Otherwise I don't know what mistake I make. 

