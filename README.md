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

* `host` - Defines the server siren.js reports to. _default: `report.sirenjs.com`_

* `error_endpoint` - Defines the URI siren.js POSTs to when reporting errors. _default: `/sirenjs/error`_

