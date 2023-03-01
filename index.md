---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
---
---

Welcome to My Home Page

# last_modified_at Usage

1.
``` liquid
{% last_modified_at %}
```
- {% last_modified_at %}

2.
By default, `"%d-%b-%y"` (like "04-Jan-14").

your own time format. For example:

3.
```liquid
{% last_modified_at %Y:%B:%A:%d:%S:%R %}
```
That produces
- {% last_modified_at %Y:%B:%A:%d:%S:%R %}
You can also call the method directly on a Jekyll "object," like so:

``` liquid
{{ page.last_modified_at }}
```
- {{ page.last_modified_at }}

To format time, you'll need to rely on Liquid's `date` filter:

``` liquid
{{ page.last_modified_at | date: '%Y:%B:%A:%d:%S:%R' }}
```
- {{ page.last_modified_at | date: '%Y:%B:%A:%d:%S:%R' }}


# timeago

{% assign date = '2020-04-13T10:20:00Z' %}

- Original date - {{ date }}
- With timeago filter - {{ date | timeago }}
