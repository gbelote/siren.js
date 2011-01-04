siren.js
========

The goal of siren.js is to make it easy to get visibility into issues that happen
with your users that are client-side. Are IE7 users getting a JS error, thus breaking
your shopping cart? Find out with siren.js!

Get Started
-----------

To get started, simply add

    <script type="text/javascript" id="sirenjs" src="//cdn.sirenjs.com/siren.js"></script>

to the top of your page. Like:

    <!DOCTYPE html>
    <html>
      <head>
        <script type="text/javascript" id="sirenjs" src="//cdn.sirenjs.com/siren.js"></script>

        <title>Example</title>
        ......

This will start collecting JavaScript errors and send them to [sirenjs.com](javascript:).
You can configure siren.js to report to a custom server, see Configuration for details.

Configuration
-------------



