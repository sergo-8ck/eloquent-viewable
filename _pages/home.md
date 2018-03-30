---
title: "Home"
permalink: /
excerpt: "Simple package for adding a page view counter to your viewable Eloquent models"
# last_modified_at: 2018-03-20T15:58:49-04:00
toc: true
---

Eloquent Viewable is a powerful, flexible and easy to use Laravel package for adding a page view counter to your Eloquent models. It's designed to be flexible and useful for various projects.

This package is not built with the intent to collect analytical data. It is made to simply store the views of a Laravel Eloquent model. You would use our trait for models like: Post, Video, Course and Hotel, but of course, you can use this package as you want.

## Features

Here are some of the main features:

* Store model views
* Get the total number (unique) views
* Get the total number (unique) views since a specific date
* Get the total number (unique) views upto a specific date
* Cache the retrieved views counts
* Queue the views before saving them in the database to prevent slow requests
