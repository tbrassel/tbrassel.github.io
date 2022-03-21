---
layout: post
title: RShinyStockDemonstration
subtitle: A Shiny App Stock Market analysis tool 
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

I made this Shiny application as an exercise on working with the package [tidyquant](https://business-science.github.io/tidyquant/) in order to gain more experience building and deploying applications that scrape real-world web data in an unfamiliar format.

**Here is some bold text**

## Here is a secondary heading

Here's a useless table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |


How about a yummy crepe?

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

It can also be centered!

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){: .mx-auto.d-block :}

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight R linenos %}
# Download the most recent list of NASDAQ traded stocks
url = "ftp.nasdaqtrader.com/SymbolDirectory/nasdaqtraded.txt"
tmp <- tempfile()
curl_download(url=url, tmp)
tbl <- read.table(tmp, stringsAsFactors = FALSE, header = TRUE, fill = TRUE, sep = "|", quote = "")
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.
