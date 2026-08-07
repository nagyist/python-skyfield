
When it’s time for me to release Skyfield, I first re-run the tests with:

    ./test-code.sh
    ./test-docs.sh

Then I rebuild the docs and double-check them, making sure that new
changelog entries look good as HTML:

    make -C documentation

Then (adjusting version numbers as necessary):

    bin/build
    uv publish dist/skyfield-1.55.tar.gz dist/skyfield-1.55-py3-none-any.whl

Then:

    bin/publish-docs
