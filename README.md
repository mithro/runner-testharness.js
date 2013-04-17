Runner for testharness.js
=====================

A Selenium+Python based test runner for testharness.js based test suites.


Features
=====================

Current set of features:
 * Spawns a local HTTP server to serve the tests and capture the results.
 * Uses selenium to fire up a browser and run the tests.
 * Downloads the needed Python packages automagically if needed.
 * Downloads the needed driver support binaries if needed.
 * Supports Chrome, Firefox and PhantomJS.
 * Supports the subunit protocol for output (can be use with testrepository).
 * Support for running a virtual display if needed.
 * Supports using a remote Selenium grid such as Sauce Lab's grid.


Things coming
 * Should support IE under windows.
 * Support Android/IPhone.
 * Support for specifying Chrome/Firefox binary.


Usage
=====================

Basic usage:

 ./run-tests.py -b PhantomJS

Advanced usage:

```
usage: run-tests.py [-h] -b {Firefox,Chrome,Ie,PhantomJS,Remote} [-x] [-d]
                    [-a] [-v] [-u] [--remote-executor REMOTE_EXECUTOR]
                    [--remote-caps REMOTE_CAPS] [-s] [--subunit] [--list]
                    [--load-list LOAD_LIST]

optional arguments:
  -h, --help            show this help message and exit
  -b {Firefox,Chrome,Ie,PhantomJS,Remote}, --browser {Firefox,Chrome,Ie,PhantomJS,Remote}
                        Which WebDriver to use.
  -x, --virtual         Use a virtual screen system such as Xvfb, Xephyr or
                        Xvnc.
  -d, --dontexit        At end of testing, don't exit.
  -a, --auto-install    Auto install any dependencies.
  -v, --verbose         Output more information.
  -u, --upload          Upload images to picture sharing site
                        (http://postimage.org/), only really useful for
                        testbots.
  --remote-executor REMOTE_EXECUTOR
                        Location of the Remote executor.
  --remote-caps REMOTE_CAPS
                        Location of capabilities to request on Remote
                        executor.
  -s, --sauce           Use the SauceLab's Selenium farm rather then locally
                        starting selenium. SAUCE_USERNAME and SAUCE_ACCESS_KEY
                        must be set in environment.
  --subunit             Output raw subunit binary data.
  --list                List tests which are avalible.
  --load-list LOAD_LIST
                        List of tests to run.
```

Related Projects
=====================

testharness.js - https://github.com/mithro/runner-testharness.js.git

