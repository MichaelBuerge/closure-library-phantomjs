Closure Library TAP - a TAP Output Producer Plugin for Google Closure Library Unittest.
================================

DESCRIPTION
---------------------------------------
Closure Library TAP is a simple plugin for [Google Closure Library](http://code.google.com/closure/library/index.html) to produce [TAP](http://testanything.org/) output, to run tests on command-line.
Closure Library TAP runs under headless browsers like [phantomjs](http://code.google.com/p/phantomjs/) and of cource, runs under real browser too.


USAGE
---------------------------------------

1. Create deps.js, see [Using DepsWriter](http://code.google.com/intl/ja/closure/library/docs/depswriter.html).
2. Just read closurelibrary-tap.js in your HTML test.


RUNNING EXAMPLES
---------------------------------------

### Prepare

    $ git clone git@github.com:waka/js-closurelibrary-unittest-tap.git
    $ cd js-closurelibrary-unittest-tap
    $ git submodule update --init

### To run sample test script with PhantomJS

    # assume you have built and installed phantomjs
    # And you will type the following command to create deps.js
    $ python vendor/google-closure-library/closure/bin/build/depswriter.py --output_file=deps.js --root_with_prefix="sample ../../../../sample"
    $ cd ./sample
    # Run all test scripts
    $ phantomjs run_test.js test/all_tests.html
    # If you run single test script
    $ phantomjs run_test.js test/ui/textarea_test.html
