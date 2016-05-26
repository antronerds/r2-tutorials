# R2 Tutorials
###Project contents

This project contains the tutorials for the web based molecular biology data analysis and visualization platform R2 (http://r2platform.com). The setup of the documention in Github is according to the Cytoscape manual as done by Barry Demcak
It has tags identifying the material that goes into the user manual for each version. A tag is formatted according to semantic versioning rules (e.g., 1.1).

The outstanding issues are identified as GitHub Issues. 

While the manual sources are maintained in GitHub, the document is actually assembled, formatted, and staged by the ReadTheDocs.org site. ReadTheDocs presents online and PDF versions, and we will use both.

ReadTheDocs can present versions of the tutorials for each release, as identified by GitHub tags. For example, given a tag of 1.1, ReadTheDocs will produce a document containing the repository files as they were for R2-tutorials 1.1, and will make it available at http://r2-tutorials.readthedocs.io/en/1.1/ ReadTheDocs will make a "stable" version of the manual available at http://r2-tutorials.readthedocs.io/en/stable ... it will resolve to the latest tagged version (ignoring beta versions such as 3.4b1). The "latest" version of the manual will be available at http://r2-tutorials.readthedocs.io/en/latest, and will contain all of the latest GitHub content, irrespective of tagging.

Note that for a manual under developement, we should make "latest" non-public (configurable in ReadTheDocs) so it isn't indexed by Google.

## Editing the Manual
To edit manual text, you must first check out this repository and use a text editor on your workstation. (You can use GitHub's native Markdown editor directly, too, for small edits.) 
Another option is use the online wysiwyg editor http://dillinger.io/ It has an underwater screen and shows direct output of your actions. You'll have to create an access token though: https://github.com/joemccann/dillinger/blob/master/plugins/github/README.md

All document components are in the "docs" directory. Each chapter is contained in its own file, and the files are assembled as a complete document by naming them in the "docs/index.rst" file.

Images are stored in the "docs/_static/images" directory, organized into subdirectories by chapter.

Simple tables can be represented in Markdown, but high quality formatting requires direct HTML coding. By convention, we encode tables as HTML-tagged data, but do not specify visual attributes and layout inline. Instead, we use preset table styles contained in "docs/_static/css" for formatting -- we do not use Markdown's table formatting. Note that additional CSS files can be added, but must be accounted for in "conf.py". Note that while the tables appear in the HTML document, they do not appear in the PDF version -- we're working on this.

More documentation here: http://www.sphinx-doc.org/en/stable/templating.html#configuration-variables

Note that the GitHub file viewer displays Markdown files reasonably well. However, it only approximates the look of tables created via HTML. For an accurate view of a table, you must look at a document rendered by ReadTheDocs.

Note that a full (browsable) link to a location has the form: "http://r2-tutorials.readthedocs.io/en/stable/Introduction.html#mylink" where "http://r2-tutorials.readthedocs.io/en/stable/" is the full URL, "Introduction" is the root name of the file containing the target link, and "mylink" is a named section (e.g., <a name="mylink">System requirements</a>). A link between chapters in the document has the form [My Link](Introduction.html#mylink), and a link within the same chapter can have the form [My Link](#mylink). For intra-document references, best to use the Introduction.html#mylink form, as ReadTheDocs will append the full URL appropriate for the build (e.g., "stable", "latest", "3.3", etc).

## Rebuilding the Manual
The "latest" manual is automatically rebuilt by ReadTheDocs when the GitHub repository is updated. (This is courtesy of a WebHook that I installed per http://docs.readthedocs.org/en/latest/webhooks.html). To rebuild other versions, you'll need to be in the ReadTheDocs web site on the Build page -- there should be little/no reason to ever do this.

The rebuild can be observed by logging into the ReadTheDocs account (see devnotes google doc for credentials) and choosing the "R2-tutorials" project. To see the build log, click on the grey Builds button. You can watch the progress of the build by manually refreshing your browser window until the build status shows either Passed or Failed - a build can take anywhere from 3 minutes to 10 minutes, depending on how busy the build server is. When the build is complete, if the status shows Passed, you can view the build result by clicking on the green View Docs button. 

Note that the "stable" version of the manual is the build for the most recent release tag (e.g., "3.3") according to semantic versioning rules. This is the version that should be reference from the R2 web site. Note, too, that for testing, we can set a tag (e.g., "3.4.0") and have ReadTheDocs build from the tagged GitHub files. It will be available at http://r2-tutorials.readthedocs.io//3.4.0 ... and as we refine the document, we can use GitHub to move the tag to the appropriate latest checkin. This is useful for testing with a candidate 3.4.0 that will eventually stop being re-tagged.



## Process for Importation
The existing R2 tutorials were ported from MediaWiki to Markdown/ReadTheDocs according to a formula laid out by Kozo Nishida. The original port is contained in the "originals" directory and are not part of the current document build. The initial instructions were:

1. Export http://ogtoolbox/w/index.php/R2_Wiki_Tutorials to a xhtml format. 

2. Convert R2Tutorials.xml to R2Tutorials.md with pandoc: http://pandoc.org/installing.html
with ```pandoc -f html -t markdown -s R2Tutorials.xhtml -o R2Tutorials.md```

3. Setup Github structure according to needs for ReadTheDocs

4. Remove sporadic html tags 

5. Get all pictures used by each chapter and put them into the Images directory. These are contained in the collection.zip on 
the mediawiki server. Resolve all picture references in the text by hand. Provide two links, one to read directly in github and one for readthedocs including polaroid style css layout
<div class="noshow">
![ *Figure 1: Default multiple gene view.*](_static/images/UsingDatasets/MultipleGenesView_Default.png)
</div>
<div class="polaroid">
  <img src="_static/images/UsingDatasets/MultipleGenesView_Default.png" alt="Default multiple genes view in R2" style="width:100%">
  <div class="container">
    <p>Figure 1: Default multiple gene view</p>
  </div>
</div>

The above is unfortunately not translated into the pdf; so for now used a regex in eclipse to search and replace all instances as follows:

regex for images
(\[!\[\])(.*)(\)\*\*)(.*)(\R*)(.*)(\R*)(.*)(\*\*\])(\()(.*)(\))

replace with: 
!\[$4$6$8\]$2 "$4$6$8"\)\R\R\*\*$4$6$8\*\*

6. Separate UserManual.md per chapter manually. 
 
7. Create a new project in ReadTheDocs, a WebHook was generated automatically from GitHub to ReadTheDocs via http://docs.readthedocs.org/en/latest/webhooks.html

Note that text is processed by Sphinx, which is documented here: http://www.sphinx-doc.org/en/stable/contents.html
