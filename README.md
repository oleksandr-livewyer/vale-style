<!-- markdownlint-disable MD033 MD041 -->

![LiveWyer Banner](./.github/img/github-banner.png?raw=true)

<p align="center">
    <a href="https://livewyer.io" ><img src="https://badgen.net/badge/Website/livewyer.io" alt="LiveWyer Website badge" /></a>
    <a href="https://twitter.com/LiveWyerUK"><img src="https://badgen.net/badge/twitter/@LiveWyerUK" alt="Twitter badge" /></a>
    <a href="https://www.linkedin.com/company/livewyer"><img src="https://badgen.net/badge/LinkedIn/LiveWyer" alt="LinkedIn badge" /></a>
</p>

<h1 align="center">Vale Packages</h1>

## Overview

We have adopted Vale to improve the quality and consistency of our written content across the company. This repository contains a custom Vale package designed to enforce style guidelines and maintain clear, consistent writing. In this repository you will find all the necessary resources to integrate it into your workflow.

You can find more information about Vale here: [vale.sh](https://vale.sh/docs)

## Documentation

### Usage

To use this package:

* Place the files from the `usage` directory in the root of your repository 
* Replace `<package>` in the link to the Vale package with the correct name (`website` or `github`)
* Execute the respective commands as commented in the `usage/.vale.ini` file.

### Update package

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

## Contributing

We value your feedback and suggestions!
If you have any ideas or want to report issues, please create an [issue](https://github.com/livewyer-ops/\\repo_name\\/issues/new/choose).
Additionally, you can submit your contributions by opening a [pull request](https://github.com/livewyer-ops/\\repo_name\\/pulls).

---

Copyright © 2024 LiveWyer, Licensed under the `MIT` License; you may not use this file except in compliance with the [License](LICENSE).

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the [License](LICENSE).