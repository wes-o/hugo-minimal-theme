# hugo-minimal-theme

A minimal theme for Hugo framework.

## Get up to speed with Hugo  

**Starting from scratch:**  

*The official Hugo docs recommend creating a `~/Hugo/Sites` directory.*  
*For consistency, the worked example uses that format. However, you may create your `/Sites` directory wherever you choose.  
(Did I hear, using a Linux Virtual Machine with Docker?* [TODO](#at)  

The following software should be installed on your machine, as a pre-requisite.  

- [Git](https://git-scm.com/downloads) for version control and workflow management.  
- [Hugo](https://gohugo.io/getting-started/installing/) for your static-site.  

As quoted from the official Hugo Docs:  
> Hugo is written in [Go](https://golang.org/) with support for multiple platforms.  
The latest release can be found at [Hugo Releases](https://github.com/gohugoio/hugo/releases).

To begin, open a new bash terminal.

---

**Create a new site with Git version control:**

```bash
hugo new site ~/Hugo/Sites/<insert-a-new-site-name>
cd ~/Hugo/Sites/example && ls -l
git init
```

**Generate the base HTML:**

```bash
hugo --verbose
```

> You now have a base directory for your Hugo development.  

## Usage

Installed as a git submodule:

```bash
git submodule add https://github.com/wes-o/hugo-minimal-theme.git themes/hugo-minimal-theme
git submodule init
git submodule update
```

## Configuration

In the main Hugo site directory, edit the `config.toml` file as shown:

```bash
# Add theme to the config.toml file
$ echo -e '\n theme = "hugo-minimal-theme" \n MetaDataFormat = "toml" ' >> config.toml
```

Start the hugo server and ping it for a response:

```bash
hugo server --gc
```

## Theme Content

TODO

```bash
```

### Develop locally on `exampleSite`

**As a submodule in your main Hugo site:**

*See [Usage](#usage) instructions above for pre-requisite steps.*

```bash
# Set to update from the remote repository
git submodule update --remote themes/hugo-minimal-theme
```

**Navigate to [themes/hugo-minimal-theme/exampleSite]:**

*A sample `config.toml` is located in this directory.*

**Copy to your main Hugo site, then edit with your own information:**

```bash
# In the main Hugo site directory level
cp themes/hugo-minimal-theme/exampleSite/config.toml .
```

```bash
# Start the Hugo server from sub-level directory
hugo server --themesDir ../..
```

Happy Hu-GO-ing! :coffee:

## License

Code released under the [MIT](https://github.com/wes-o/hugo-minimal-theme/blob/master/LICENSE) license.

---

Wes Oler Copyright &copy; 2020
Created and maintained by [Wes Oler](https://github.com/wes-o) from *[Listen Dinle](https://github.com/Listen-Dinle)*.
