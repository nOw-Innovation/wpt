dpub-aria: Tests for the DPUB-ARIA Recommendations
==================================================

The [DPUB ARIA Recommendation](https://www.w3.org/TR/dpub-aria-1.0)
define extensions to HTML4/5 for support of extended semantics.  These
semantics make it easier for Assistive Technologies to interpret and
present content to users with varying physical and cognitive abilities.

The purpose of these tests is to help ensure that user agents support the
requirements of the Recommendation.

The general approach for this testing is to enable both manual and automated
testing, with a preference for automation.


Running Tests
-------------

In order to run these tests in an automated fashion, you will need to have a
special Assistive Technology Test Adapter (ATTA) for the platform under test.  We will
provide a list of these for popular platforms here as they are made available.

The ATTA will monitor the window under test via the platforms Accessibility
Layer, forwarding information about the Accessibility Tree to the running test
so that it can evaluate support for the various features under test.

The workflow for running these tests is something like:

1. Start up the ATTA for the platform under test.
2. Start up the test driver window and select the dpub -aria tests to be run
   (e.g., the DPUB ARIA 1.0 tests) - click "Start"
3. A window pops up that shows a test - the description of which tells the
   tester what is being tested.  In an automated test, the test with proceed
   without user intervention.  In a manual test, some user input may be required
   in order to stimulate the test.
4. The test runs.  Success or failure is determined and reported to the test
   driver window, which then cycles to the next test in the sequence.
5. Repeat steps 2-4 until done.
6. Download the JSON format report of test results, which can then be visually
   inspected, reported on using various tools, or passed on to W3C for
   evaluation and collection in the Implementation Report via github.

**Remember that while these tests are written to help exercise implementations,
their other (important) purpose is to increase confidence that there are
interoperable implementations.** So, implementers are the audience, but these
tests are not meant to be a comprehensive collection of tests for a client that
might implement the Recommendation.


Capturing and Reporting Results
-------------------------------

As tests are run against implementations, if the results of testing are
submitted to [test-results](https://github.com/w3c/test-results/) then they will
be automatically included in documents generated by
[wptreport](https://www.github.com/w3c/wptreport). The same tool can be used
locally to view reports about recorded results.


Writing Tests
-------------

If you are interested in writing tests for this environment, see the
associated [CONTRIBUTING](CONTRIBUTING.md) document.
