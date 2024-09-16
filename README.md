# Vale Style

We have adopted Vale to improve the quality and consistency of our written content across the company. This repository contains a custom Vale package designed to enforce style guidelines and maintain clear, consistent writing. In this repository you will find all the necessary resources to integrate it into your workflow.

You can find more information about Vale here: [vale.sh](https://vale.sh/docs)

## Usage

To use this package:

* Place the files from the `usage` directory in the root of your repository 
* Replace `<package>` in the link to the Vale package with the correct name (`website` or `github`)
* Execute the respective commands as commented in the `usage/.vale.ini` file.

## Update package

To update these packages, start by updating the files in the respective directories. Once you are satisfied with the package content, create a zip archive using the following command:

```bash
export RELEASE_TAG=<tag>

rm -rf general.zip website.zip github.zip
zip -r general.zip packages/general
zip -r website.zip packages/website
zip -r github.zip packages/github

gh release upload $RELEASE_TAG general.zip website.zip github.zip --clobber
```

After obtaining the zip archive, create a GitHub Release in this repository and attach your new zip archives.

***Note:** Once you have finished, please ensure to update the release tag in `github/.vale.ini`, `website/.vale.ini` and `usage/.vale.ini` to the one you just created.*