# Bookmark Server
A demonstration of handling HTTP requests using Python.

## About
This project allows you to add short names for long URIs, and when the shortname is passed in the path of the project's URI, it redirects you to the Web page whose short name you set for the long URI.

## How to use this program?
In the "Short name" field, just mention the short name you want to give for a long URI. Then add the shortname in the path part of the URI.

For example,

- Long URI: https://www.google.com/about

- Short name: aboutgoogle

Then, type in the address bar
```
https://bookmark-server-threadless.herokuapp.com/aboutgoogle
```

It would redirect you to `https://www.google.com/about`.

## Demo
A demo of this project can be found over [here](https://bookmark-server-threadless.herokuapp.com/)

## Problem with this project
When in the "Long URI" field, you enter the bookmark server's own URI, that is, `https://bookmark-server-threadless.herokuapp.com/` here, you would find that it returns an error. That's because Python's `http.server` module can handle only one request at a time. For handling multiple requests, check out [this program](https://github.com/SDey96/bookmark-server-multithreaded).
