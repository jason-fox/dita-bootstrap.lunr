# DITA Bootstrap Lunr Search

<a href="https://www.dita-ot.org"><img src="https://www.dita-ot.org/images/dita-ot-logo.svg" align="right" height="55"></a>

_DITA Bootstrap Lunr Search_ is a [DITA Open Toolkit plug-in](https://www.dita-ot.org/plugins) that extends the [DITA Bootstrap](https://infotexture.github.io/dita-bootstrap/) HTML output with a [Lunr.js](https://lunrjs.com/) search function.

<!-- MarkdownTOC levels="2,3" -->

- [Installation](#installation)
  - [Installing DITA-OT](#installing-dita-ot)
  - [Installing the Plug-in](#installing-the-plug-in)
  - [Installing Node.js](#installing-nodejs)
- [Usage](#usage)
  - [Parameter Reference](#parameter-reference)
- [License](#license)

<!-- /MarkdownTOC -->

## Installation

The _DITA Bootstrap Lunr Search_ plug-in has been tested with [DITA-OT 4.x](http://www.dita-ot.org/download). Use the latest version for best results.

### Installing DITA-OT

1.  Download the latest distribution package from the project website at
    [dita-ot.org/download](https://www.dita-ot.org/download).
2.  Extract the contents of the package to the directory where you want to install DITA-OT.
3.  **Optional**: Add the absolute path for the `bin` directory to the _PATH_ system variable.

    This defines the necessary environment variable to run the `dita` command from the command line.

See the [DITA-OT documentation](https://www.dita-ot.org/4.0/topics/installing-client.html) for detailed installation instructions.

### Installing the Plug-in

- Run the plug-in installation commands:

```console
dita install https://github.com/jason-fox/fox.jason.extend.css/archive/master.zip
dita install https://github.com/infotexture/dita-bootstrap/archive/master.zip
dita install https://github.com/infotexture/dita-bootstrap.lunr/archive/master.zip
```

### Installing Node.js

<a href="https://nodejs.org/"><img src="https://nodejs.org/static/images/logos/nodejs-new-pantone-black.svg" align="right" width="70" height="70" align="right" width="55" height="55"></a>

The _DITA Bootstrap Lunr Search_ plug-in uses the [Node.js](https://nodejs.org/) JavaScript runtime to generate the Lunr.js search index. Node.js must therefore be present for the index to be generated successfully.

To download and install a copy, follow the instructions for your operating system on the [download page](https://nodejs.org/en/download/).

## Usage

#### Adding Lunr Search to HTML Bootstrap output

To run, use the `html5-bootstrap` transformation and add the `args.hdr` parameter.

```console
PATH_TO_DITA_OT/bin/dita -f html5-bootstrap -o out -i PATH_TO_DITAMAP \
  --args.hdr=path/to/your-header.xml
```

A sample header file with a search box is provided with the plug-in: [includes/bs-navbar-lunr.hdr.xml](./includes/bs-navbar-lunr.hdr.xml).

### Parameter Reference

- `offline.mode` - enables Lunr search to work in conjunction with DITA Bootstrap [offline mode](https://infotexture.github.io/dita-bootstrap/offline.html) - this requires an additional plugin to be installed.

## License

[Apache 2.0](LICENSE) © 2023 Jason Fox

The Program includes the following additional software components which were obtained under license:

- lunr.js - https://github.com/olivernn/lunr.js - **MIT license**
- lunr-languages - https://github.com/MihaiValentin/lunr-languages - **Mozilla Public license**
