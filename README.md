# Vale Style

[Vale Official Documentation](https://vale.sh/docs/)

## Usage

To use this package, simply place the files from the `usage` directory in the root of your repository and execute the respective commands as commented in the `usage/.vale.ini` file.

## Update package

To update this package, start by updating the files in the `livewyer` directory. Once you are satisfied with the package content, create a zip archive using the following command:

```
rm -rf livewyer.zip
zip -r livewyer.zip livewyer
```

After obtaining the zip archive, create a GitHub Release in this repository and attach your new zip archive.

***Note:** Once you have finished, please ensure to update the release tag in `usage/.vale.ini` to the one you just created.*