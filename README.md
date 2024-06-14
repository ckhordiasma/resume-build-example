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

The build.yml file has all the implementation details for how this works, but basically it searches for subfolders in `resumes` and `cover-letters` that have `.tex` files, and tries to build a PDF for each file. Then it saves the PDFs as build artifacts, and in a later step these artifacts are published as releases. 

In order to trigger a build only, you just need to do a pull request on the main branch and the pipeline will start. You can see the built pdfs in the build artifacts zip file. In order to make an automatic release, you need to create and push a tag that starts with "v". This tag will be used as the suffix for that release. You can create and push tags from the cli like so:

```
git tag "name_of_tag"
git push --tags
```
