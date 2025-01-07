- https://gohugo.io/
- first hugo website
  collapsed:: true
	- hugoinaction - https://github.com/hugoinaction/
	- ![image.png](../assets/image_1736222141063_0.png)
	- hugo cli
	  collapsed:: true
		- commands
			- hugo -> to build the site (default command to build the site)
			- hugo new -> to create new things (default to create new contents pages)
			- hugo new site -> to generate a skeleton folder
			- hugo new theme -> to generate a theme
		- flags (cli parameters)
			- provide configuration to command
			- ex: hugo new site --format yaml -> changes the metadata format from the default TOML to YAML
			- yaml https://yaml.org/
			- toml https://toml.io
		- learning hugo commands is to use `--help`
			- hugo --help
			- hugo new --help
			- hugo gen man -> to generate documentation in man format like in UNIX
			- hugo gen doc -> to generate documentation in markdown
	- structure of source folder
	  collapsed:: true
		- win cli> tree /f
		- ![image.png](../assets/image_1735019980822_0.png)
		- archetypes
			- contains templates for the content files
		- content
			- we can organise the content into files and folders. hugo generates website based on the folder's structure can be overridden using metadata in each file (called `front matter`)
		- data
			- stores structured content in the form of yaml, toml, csv, json, which are made available as global variables throughout the website
		- layouts
			- overrides parts of the theme
			- customization of theme
		- themes
			- contains the code of theme
		- config
			- houses the website's configuration. this directory contains metadata shared across the website, including theme's name and any parameters that need to be passed to Hugo or to the theme to render content.
			- `config.yaml`
		- static
			- stores static content like fonts (`.woff`), pdf, zip files.
		- when building hugo-based website, here are some other files and folders you will encounter
			- assets folder
				- images, javascript, css files as unprocessed source code to be consumed globally from website.
				- hugo can resize images, bundle and minify js files and convert SCSS to CSS via Hugo pipes.
			- public folder
				- hugo command generates HTML output to be deployed and cached at the CDN
			- resource folder
				- when processing data, Hugo caches the results of heavy operations in this folder
			- go.mod and go.sum files
				- hugo modules uses these files to synchronize project dependencies
			- vendor folder
				- stores 3rd party dependencies that we can include via hugo modules
			- node_modules, package.json, package-lock.json, package.hugo.json
			- .github folder and netlify.toml files
			- api folder
	- adding a theme
	  collapsed:: true
		- multiple ways to get a theme
		  collapsed:: true
			- use hugo modules to integrate the theme
			- use git submodules to reference the theme in the themes folder
			- download and copy the theme to the themes folder
		- https://themes.gohugo.io/
		- website config file: hugo.yaml
		  collapsed:: true
			- theme: Eclectic
		- hugo server
			- hugo server (default port 1313)
			- hugo server --port 1350
			- hugo serve
			- hugo server --disableFastRender
			- hugo server --disableLiveReload
			- hugo server --noHTTPCache --disableFastRender
			- hugo server --environment
	- adding content
	  collapsed:: true
		- configuration `hugo.yaml`
			- 2 distinct parts
			  collapsed:: true
				- top-level configuration -> common across themes
				- theme-specific `params` section
			- ```hugo.yaml
			  baseURL: http://example.org/
			  languageCode: en-us
			  title: Acme Corporation
			  theme: Eclectic
			  author:
			    facebook: " https://facebook.com/example"
			    twitter: " https://twitter.com/example"
			    email: "contact@example.org"
			    name: "Acme Corporation"
			    location: New York
			    phone: (999) 999-9999
			    hours: "Mon-Fri: 9:00AM - 6:00PM, ET"
			  menu:
			    main:
			      - identifier: about
			        name: About
			        url: /about
			        weight: 100
			      - identifier: contact
			        name: Contact
			        url: /contact
			        weight: 200
			  params:
			    color: "#4f46e5"
			    copyright: "Copyright &copy; 2022 Acme Corporation.
			      All Rights Reserved."
			    footer:
			      - title: About
			        content: >
			          Acme Corporation is the world's leading
			          manufacturer of digital shapes. From squares and
			          circles to triangles and hexagons, we have it
			          all. Browse through our collection of various
			          forms with different thicknesses and line styles.
			          We shape the world. You live in it.
			      - title: Recent Blog Posts
			        recents: blog
			        recentCount: 7
			      - title: Contact Us
			        contact: true
			  ```
			- hugo supports multiple authors via a feature `taxonomies`
		- content folder > about.md, credits.md, terms.md, contact.md
		- index page has unique template `index template`. templates are HTML files but can be JSON, XML with additional template tags
		- Hugo templates can be overridden using the layout folder. layouts/index.html
		- exampleSite will be available in Hugo themes
	- continuous deployment pipeline / continuous delivery
		- https://gohugo.io/hosting-and-deployment/
		- https://app.netlify.com/signup
		- https://app.netlify.com/start
	- measuring performance and analysing website maintainability
- create a site
	- hugo new site acme-corporation --format yaml
		- hugo -> command line
		- new -> command
		- site -> sub command
		- --format yaml -> parameters to pass to the command
	- vector creation www.freepik.com