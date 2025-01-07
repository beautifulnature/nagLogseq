- https://gohugo.io/
- first hugo website
	- hugo cli
		- commands
			- hugo -> to build the site (default command to build the site)
			- hugo new -> to create new things (default to create new contents pages)
			- hugo new site -> to generate a skeleton folder
			- hugo new theme -> to generate a theme
		- flags (cli parameters)
			- provide configuration to command
			- ex: hugo new site --format yaml -> changes the metadata format from the default TOML to YAML
		- learning hugo commands is to use `--help`
			- hugo --help
			- hugo new --help
			- hugo gen man -> to generate documentation in man format like in UNIX
			- hugo gen doc -> to generate documentation in markdown
		- structure of source folder
			- win cli> tree /f
			- ![image.png](../assets/image_1735019980822_0.png)
			- archetypes
			- content
			- data
			- layouts
			- themes
			- config
			- static
			- when building hugo-based website, here are some other files and folders you will encounter
				- assets folder
				- public folder
				- resource folder
				- go.mod and go.sum files
				- vendor folder
				- node_modules, package.json, package-lock.json, package.hugo.json
				- .github folder and netlify.toml files
				- api folder
			- adding a theme
				- multiple ways to get a theme
					- use hugo modules to integrate the theme
					- use git submodules to reference the theme in the themes folder
					- download and copy the theme to the themes folder
				- https://themes.gohugo.io/
				- website config file: hugo.yaml
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
				- configuration `hugo.yaml`
					- 2 distinct parts
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
- create a site
	- hugo new site acme-corporation --format yaml
		- hugo -> command line
		- new -> command
		- site -> sub command
		- --format yaml -> parameters to pass to the command
	- vector creation www.freepik.com