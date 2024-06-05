# Screaming Frog SEO Spider exportables

> A list of all the export options available in Screaming Frog SEO Spider. 


## Using this repository
This repository contains info on all the export options available in Screaming Frog SEO Spider.
The files are organised by the different verions of Screaming Frog, as each version has differet export options.

A full list of the command-line options can be found in the [Screaming Frog documentation](https://www.screamingfrog.co.uk/seo-spider/user-guide/general/#commandlineoptions).

```
.
├── 20.1
│   ├── bulk-export.txt
│   ├── export-tabs.txt
│   └── save-report.txt
├── 20.2
│   ├── bulk-export.txt
│   ├── export-tabs.txt
│   └── save-report.txt
└── ...
```

The options should be supplied in a comma separated list to Screaming Frog. 
The options are case sensitive.

```bash
--export-tabs "tab:filter,..."
--bulk-export "submenu:export,..."
--save-report "submenu:export,..."
```

## Example: 
To find out what export options are available in version 20.1, you can look at the files in the [20.1](./20.1/) directory.

```bash
screamingfrogseospider --headless --crawl https://example.com/ \
--save-crawl --output-folder /path/to/output/folder/ \
--export-tabs "Internal:All,External:All" \
--bulk-export "Queued URLs,Links:All Inlinks" \
--save-report "Segments Overview,Redirects:All Redirects"
```