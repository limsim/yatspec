# Changing where the HTML output is written to #

This can be done by setting the system property `yatspec.output.dir`.
There is a public constant on `com.googlecode.yatspec.junit.SpecRunner.OUTPUT_DIR` if you wish to do it programmatically.

If this is not set this will default to `java.io.tmpdir`.

This is only read after the test has run so can be changed in the test under execution to dynamically change the location of the output directory.