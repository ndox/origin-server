# OpenShift Origin Manuals #

This repo contains AsciiDoc versions of the OpenShift Origin manuals. The included "index.txt" file is the home page for the complete set of OpenShift Origin documentation.

## Building the Manuals ##
The manuals themselves are .txt files written in [AsciiDoc](http://asciidoc.org/), so they are easily human-readable. However, they are intended to be published in various formats, notably HTML. 

To generate the HTML document set, first install the necessary gems:

    bundle install

Then run the "build" rake task:

    bundle exec rake build

This will create html files from the AsciiDoc files, including an index.html.

If you want to quickly clean up all of the generated HTML files, run:

    bundle exec rake clean

## Manual Authoring with LivePreview ##

For ease of authoring in AsciiDoc and checking the results in a web browser, a live preview environment has been set up using [Guard](http://guardgem.org/) and [LiveReload](http://livereload.com/).

To begin, install the LiveReload extension in your web browser (Firefox, Chrome and Safari are supported). Then build the docs following the [Building the Manuals] instructions.

Next, start the guard process:

    bundle exec guard

Now open the _html_ version of a local file that you are working with in your browser and enable the LivePreview add-on for that file.

At this point, you can begin editing the AsciiDoc version of the file in your text editor. Every time you save the AsciiDoc file, you will see output from the guard process as it detects the change and regenerates the HTML file. The LivePreview browser add-on detects the updated file and automatically reloads it into the browser.
 
## Old Manuals ##
The `archive` subdirectory contains older manuals that were written in Markdown. Over time, the contents of these files will be updated to AsciiDoc and assimilated into the documents in this directory.
