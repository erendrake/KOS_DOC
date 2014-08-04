Editing Docs
============

This page contains information for people who wish to contibute to the kOS documentation.
If you want to edit the docs you need to know how they're generated, and where to make
your edits.

### What files do I edit?

Do not edit the HTML files directly.  They are autogenerated from a simplified Markdown language.
**The source files you need to edit end in filename extension ".md".**  They are the markdown
files. They are under the source/ directory of the Master branch.  Do NOT edit the gh-pages
branch - it contains the autogenerated HTML output, rather than the source files.

### What does it use?

The documentation is originally written in a Markdown language and processed by a tool called MiddleMan that
generates the HTML docs from the Markdown docs.  You can install and run MiddleMan yourself if you like, and
instructions for how to do this are further down this page.

### What branch do I edit?

This is where it gets messy.  MiddleMan has GIT integration and automatically hardcodes the use
of certain predefined GIT branch names.  Unfortunately this GIT itegration decides the branch names for
you and you can't edit in different branches very easily.

Therefore in KOS_DOC we will use full FORKS for some of the things that most of the time Git uses
branches for.

**KSP-KOS/KOS_DOC** fork will be used for documentation that refers to released kOS features.

**KSP-KOS/KOS_DOC_DEV** fork will be used for documentation that refers to pre-released or not-yet-released kOS features.

The normal path for updates should be to make your own private fork of KOS_DOC_DEV, form pull requests from
there, which then get pulled back into KSP-KOS/KOS_DOC_DEV and then from there move to KSP-KOS/KOS_DOC wehn
a full release of kOS is made.

### Okay, so how do I make an edit?

The markdown files are contained in master branch, under source/

[The syntax of the markdown system used here is documented separately on this page](markdown_syntax.md).

**The easy way: (aka. "editing blind")**:  Edit the .md file you want to change, check it in, and make a pull request.
The person merging it into the repository will manually check that the edits form correct syntax that renders into correctly.
For small edits this method is acceptable.  **Con:** You don't get to see the rendered final result and the person who does
the merging in may have to make corrections if the format doesn't work.  **Pro:** You don't need to install the entire
MiddleMan system on your own local computer this way.

**The hard way: (aka. "preview the results")**:  If you want to be able to see the HTML rendered results of your edits
before you check them in, then you need to install the entire Markdown system on your own computer first,
to be able to locally run the HTML generator on your .md files.  This is more appropriate if you will be doing a large
number of edits, or writing an entirely new page.
