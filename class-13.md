# Reading 13 - Local Storage

## Overview
- Three dealbreaking downsides of cookies:
  1. Cookies are included with every HTTP request, slowing down your web app by transmitting the same data over and over again
  1. Sending data unencrypted over the internet
  1. Cooies are limited to about 4KB of data, enough to slow things down but not enough to be useful
- What we really want:
  - A lot of storage space
  - On the client
  - Persists beyond a page refresh
  - Isn't transmitted over the server

## Local storage hacks before HTML5
- ```userData``` allows web pages to store up to 64 KB of data per domain 
- Flash feature, Local Shared Objects, allows Flash objects to store up to 100KB of data per domain
- Google launched Gears in 2007, open source browser plugin aimed at providing additional capabilities in browsers. Gears provides an API to an embedded SQL database inside SQLite. After obtaining permission from the user, Gears can store unlimited amounts of data per domain in SQL database tables
- By 2009, dojox.storage could auto-detect Adobe Flash, Gears, Adobe AIR
- All of these specific to a single browser or reliant on a third-party plugin

## HTML5 Storage
- HTML5 Storage can be referred to as web storage, certain browser vendors also refer to it as "local storage" or "DOM storage"
- HTML5 Storage is a way to web pages to store named key/value pairs locally, within the client web browser
- Like cookies, the data persists even after you navigate away from the web site, close your browser tab, exit your browser
- Unlike cookies, the data is never transmitted to the remote web server
- In JS code, you access HTML5 storage through the ```localStorage``` object on the global window object

## Using HTML5 storage
- Based on key/value pairs
- You store data based on a named key, then you can retrieve that data with the same key. Named key is a string
- The data can be any type supported by JS (strings, Boolean, integers, floats) but the data is stored as a string
- May need to use ```parseInt()``` or ```parseFloat()```
- You can treat the localStorage object as an associative array

## Tracking changes to the HTML5 Storage Area
- To keep track of when the storage area changes, you can trap the ```storage``` event
- The ```storage``` event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something

## Limitations in current browsers
- Each origin gets 5MB by default
- If you exceed your storage quota, "QUOTA_EXCEEDED_ERR" is the exception that will get thrown

[<==Back>](README.md)