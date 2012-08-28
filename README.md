jstd-phantomjs
==============

Run JSTestDriver tests with the PhantomJS headless Webkit-based browser.

This script is best used in a continuous integration server as PhantomJS will start (and
stop) every time JSTestDriver is run. For rapid local development feedback you
can instead just start a browser manually and leave it running between
JSTestDriver invocations.

I use version 1.3.3d of JSTestDriver with version 1.6.1 of PhantomJS.
JSTestDriver versions prior to 1.3.3 didn't allow arguments to be supplied
in the browser command line flag (http://code.google.com/p/js-test-driver/wiki/CommandLineFlags).

This is the full command line:

    $ java -jar JsTestDriver-1.3.3d.jar --captureConsole true --config jsTestDriver.conf --port 9876 --tests all --verbose true --browser 'phantomjs;phantomjs-jstd-bridge.js' --testOutput target/jstd-reports

Download links:

* JSTestDriver 1.3.3d: http://js-test-driver.googlecode.com/files/JsTestDriver-1.3.3d.jar
* PhantomJS: http://code.google.com/p/phantomjs/downloads/list

