siren.js
========

The goal of siren.js is to make it easy to get visibility into issues that happen
with your users that are client-side. Are IE7 users getting a JS error, thus breaking
your shopping cart? siren.js makes it easy to know!

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

Behavior
--------

When a JavaScript error occurs or an uncaught exception is thrown, siren.js records the error,
collects information about the environment, and reports this to a server. Using the dashboard
on [sirenjs.com](sirenjs.com/about/dashboard) or by creating your own, you can see when errors
happen.

### Information Collected ###

siren.js captures the following by default:

* The error/exception object

* Page URL

Configuration
-------------

Global configuration for siren.js is done by defining a hash `sirenjs_config` before
siren.js is loaded, like so:

    <!DOCTYPE html>
    <html>
      <head>
        <script type="text/javascript">
            sirenjs_config = {
                // ... config here ...
            };
        </script>
        <script type="text/javascript" id="sirenjs" src="//cdn.sirenjs.com/siren.js"></script>

        <title>Example</title>
        ......

Options include:

* `host` - Server siren.js reports to. Default: `report.sirenjs.com`

* `error_endpoint` - URI siren.js POSTs to when reporting errors. Default: `/sirenjs/error`

* `account_token` - *Only relevant for sirenjs.com accounts.* Account token for your sirenjs.com subscription. Default `null`

Running your own reporting server
---------------------------------

While [sirenjs.com](sirenjs.com) provides a freemium reporting service for siren.js, you have the freedom and
flexibility to run your own. Here's how:

1. Edit the siren.js configuration `host` property to point towards your own server. Example:
    <script type="text/javascript">
        sirenjs_config = {
            host: "example.com"
        };
    </script>

2. Setup your server to handle POST requests to `/sirenjs/error` or configure a custom endpoint (See Configuration).

3. Serve `siren.js` from your own server. Example:
    <script type="text/javascript" id="sirenjs" src="//example.com/siren.js"></script>


