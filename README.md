# LaTeX Resume Build Pipeline

This repo is an example repo that you can use to set up a pipeline for auto-building LaTeX resumes. You should see some releases on the left with PDF versions of the example resumes. 

The basic folder structure in this repo is as follows:

```
/
--/resumes
----/subfolder
--/cover-letters
----/subfolder
--/.github/workflows/build.yml
```

The build.yml file has all the implementation details for how this works, but basically it searches for subfolders in `resumes` and `cover-letters` that have `.tex` files, and tries to build a PDF for each file. Then it saves the PDFs as build artifacts, and in a later step these artifacts are published as releases. The PDFs will be named based on the subfolder they came from, along with a suffix identifier that shows which pipeline run the release came from. 