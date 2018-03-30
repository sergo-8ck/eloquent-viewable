---
title: "Introduction"
permalink: /docs/introduction/
excerpt: "How to quickly install and setup Minimal Mistakes for use with GitHub Pages."
last_modified_at: 2018-03-20T15:58:49-04:00
toc: true
---

Eloquent Viewable is a Laravel >= 5.5 package that can associate views with Eloquent models.

Here are some quick code examples:

```php
// First get a Viewable Post
$post = Post::find(1);

// Store a new view in the database
$post->addView();
```

```php
$post->getViews();
$post->getViewsSince(Carbon::parse('2007-05-21 12:23:00'));
$post->getViewsUpto(Carbon::parse('2013-05-21 00:00:00'));
$post->getViewsBetween(Carbon::parse('2014-00-00 00:00:00'), Carbon::parse('2016-00-00 00:00:00'));
```

It can also return the nuber unique views!

```php
$post->getUniqueViews();
$post->getUniqueViewsSince(Carbon::parse('2007-05-21 12:23:00'));
$post->getUniqueViewsUpto(Carbon::parse('2013-05-21 00:00:00'));
$post->getUniqueViewsBetween(Carbon::parse('2014-00-00 00:00:00'), Carbon::parse('2016-00-00 00:00:00'));
```

Retrieving the number of views in the past `days`, `weeks`, `months` or `years` is also available!

```php
$post->getViewsOfPastDays(3);
$post->getViewsOfPastWeeks(2);
$post->getViewsOfPastMonths(6);
$post->getViewsOfPastYears(5);
```

Retrieving the number of views in the past `seconds`, `minutes`, `hours`, `days`, `weeks`, `months` or `years` from now is also available!

```php
$post->getViewsOfSubSeconds(30);
$post->getViewsOfSubMinutes(2);
$post->getViewsOfSubHours(6);
$post->getViewsOfSubDays(5);
$post->getViewsOfSubWeeks(5);
$post->getViewsOfSubMonths(5);
$post->getViewsOfSubYears(5);
```

Need to order your viewable models? Use this simple scope:

```php
$posts = Post::orderByViewsCount(); // default: descending

$posts = Post::orderByViewsCount('asc'); // ascending
```

---
