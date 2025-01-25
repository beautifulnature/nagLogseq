- nix-os installation
	- wsl --import NixOS $env:USERPROFILE\NixOS\ .\Downloads\nixos-wsl.tar.gz
	- wsl -d NixOS
	- sudo nix-channel --update
	- sudo nixos-rebuild switch
- book
	- Nix Mastery - Reproducible Systems and Functional Package Management
		- Introduction
		- collapsed:: true
		  1. Introduction to Nix and Functional package management
			- philosophy behind Nix
			- overview of functional package management
			- benefits and improvements over traditional systems
			  collapsed:: true
				- reproducibility
				- co-existence of multiple versions
				- atomic transactions and rollbacks
				- progressive and declarative configurations
				- traditional approach
				- functional approach
				- impact and uses cases
					- software development
					- devops and system administration
					- research and data science
					- security and compliance
			- understanding the Nix Ecosystem
			- why choose nix for package management
			  collapsed:: true
				- reproducibility and consistency
				- continuous integration and deployment (CI/CD)
				- scientific research and experimentation
				- isolated and conflict-free environments
				- atomic upgrades and reliable rollbacks
				- Nix channels and Binary caches
				- sustainability and ecosystem benefits
					- NisOS
					- NisOps
					- Hydra
				- Real-World case studies and community success
					- Research institutions
					- Enterprise-level IT operations
					- open source community collaborations
		- collapsed:: true
		  2. core concepts of Nix language
			- 2.1 Nix syntax and basic types
			  collapsed:: true
				- white space and comments
				- basic types
				- operations on basic types
				- type conversion and type checking
				- error handling and debugging
				- attributes and variables
			- 2.2 functions and variables in Nix
			  collapsed:: true
				- variables in Nix
				- function definitions in Nix
				- anonymous functions
				- higer-order functions
				- default arguments and optional parameters
				- recursive functions and let-in constructs
				- combining variables and functions with let-expressions
				- scoping and closure
			- 2.3 Nix expression structure
			  collapsed:: true
				- general expression syntax
				- expression with attribute sets
				- nested attribute sets
				- modifiers and inheritance
				- Lists and Iteration
				- Working with List comprehensions
				- conditional logic
				- integration of functions and expressions
				- recursive expression structures
				- expression composition
			- 2.4 Lists and Sets in Nix
			  collapsed:: true
				- introduction to lists
				- operations on lists
				- higher-order functions on lists
				- nested lists
				- introduction to sets
				- operations on sets
				- nested sets and recursive attribute sets
				- combining lists and sets
				- practical applications in NixOS and nixpkgs
			- 2.5 conditional and recursive expressions
			  collapsed:: true
				- understanding conditional expressions
				- complex conditional logic
				- conditional expressions in attribute sets
				- introduction to recursive expressions
				- recursive attribute sets
				- applications and use cases
					- conditional package options
					- recursive inventory or data crawling
				- recursive pattern matching and processing
			- 2.6 modules and evaluations
			  collapsed:: true
				- understanding nix modules
				- defining a basic module
				- composition and inheritance of modules
				- importing modules
				- overriding and extending module options
				- nixos module system
				- evalutions in Nix
				- example of evaluation
				- lazy evaluation and purity
				- evaluation environments
				- debugging and tracing evaluations
		- collapsed:: true
		  3. setting up nix environment
			- 3.1 installing nix on your system
			- 3.2 configuring the nix environment
			- 3.3 basic nix commands
			- 3.4 setting up a nix shell
			- 3.5 integrating nix with existing workflows
			- 3.6 common installation issues and solutions
			  collapsed:: true
				- network and connectivity problems
					- solution
				- permission and file system constratints
					- solution
				- conflict with existing software and dependencies
					- solution
				- OS-specific issues - windows
					- solution for windows
				- disk space and resource limitations
					- solution
				- checksum and integrity validation errors
					- solution
				- environmental configuration anomalies
					- solution
		- collapsed:: true
		  4. understanding nix expressions
			- 4.1 what are nix expressions?
			- 4.2 syntax and structure of nix expressions
			- 4.3 attributes and attribute sets
			- 4.4 writing custom nix expressions
			- 4.5 importing and using expressions
			- 4.6 debugging nix expressions
		- collapsed:: true
		  5. nix packages and the nixpkgs repository
			- 5.1 exploring nix packages
			- 5.2 navigating the nixpkgs repository
			- 5.3 package expressions in nix
			  collapsed:: true
				- attributes and their significance
				- custom build phases
				- nix language constructs
				- function abstractions
				- extensions and overrides
				- complex dependencies and conditional builds
			- 5.4 building and modifying packages
			  collapsed:: true
				- building from source
					- defining the derivation
					  logseq.order-list-type:: number
					- executing the build
					  logseq.order-list-type:: number
					- verifying outputs
					  logseq.order-list-type:: number
				- modifying existing packages
					- overriding package attributes
					  logseq.order-list-type:: number
					- adding additional patches or build inputs
					  logseq.order-list-type:: number
					- customisation with configuration flags
					  logseq.order-list-type:: number
				- best practices in building and modifying
					- use variables for common values
					- minimize side effects
					- test changes thoroughly
					- document extensively
				- nixpkgs testing and contribution
					- create a feature branch
					  logseq.order-list-type:: number
					- use nixpkgs review tools
					  logseq.order-list-type:: number
					- collaborate with community
					  logseq.order-list-type:: number
			- 5.5 contributing to nixpkgs
			  collapsed:: true
				- understanding the contribution process
					- identify and discuss issues
					- fork and clone the repository
					- create a branch
					- make and test changes
					- run linting and review tools
					- submit a pull request
				- adhering to nixpkgs guidelines
					- ensure reproducibility
					- provide extensive documentation
					- confirm to repository standards
					- integrate test where applicable
					- maintain backward compatibility
				- engaging with the community
					- participate in discussions
					- review existing pull requests
					- attend or host meetups
				- overcoming challenges and impediments
					- continuous learning
					- seek mentorship
					- iterate and improve
			- 5.6 customizing packages with overrides
			  collapsed:: true
				- introduction to overrides
				- using overrideAttrs
				- advanced attribute overrides
					- customising build phases
					- applying patches
				- using override
				- combining overrides with overlays
				- best practices for package customistaion
					- encapsulation with function abstractions
					- separation of concerns
					- documentations and clarity
					- robust testing
					- integration with continuous integration pipelines
				- use cases highlighting customisation needs
					- environment specific builds
					- experimental feature testing
					- dependency upgrades or downgrades
					- collaborative development
		- collapsed:: true
		  6. building and installing software with nix
			- 6.1 understanding the build process
			- 6.2 writing a simple build expression
			- 6.3 managing build inputs and outputs
			- 6.4 using nix-build for software compilation
			- 6.5 installation of software via nix-store
			- 6.6 creating reproducible builds
		- collapsed:: true
		  7. managing package dependencies
			- 7.1 defining package dependencies
			- 7.2 handling dependency conflicts
			- 7.3 using overlays for customisation
			- 7.4 pinning and ensuring reproducibility
			- 7.5 advanced dependency management with nix
			- 7.6 leveraging built-in package sets
		- collapsed:: true
		  8. nixos: a linux distribution built on nix
			- 8.1 overview of nixos
			- 8.2 installing nixos
			- 8.3 system configuration with nixos
			- 8.4 service and modules in nixos
			- 8.5 upgrading and rolling back nixos
			- 8.6 community and development in nixos
		- collapsed:: true
		  9. declarative system configuration with nixos
			- 9.1 principles of declarative configuration
			- 9.2 writing a nixos configuration file
			- 9.3 managing packages and services declaratively
				- declarative package management
				- ensuring consistency and reproducibility
				- service management in nixos
				- efficiency and automation benefits
				- customising and extending packages
				- integration with user configurations
				- service dependencies and ordering
				- conclusion without closure
			- 9.4 customising nixos configuration
				- configuring environment variables
				- user interface configuration
				- hardware customisation and performance tuning
				- modularizing configuration for scalability
				- security enhancements and customisations
				- developing with nix: custom deviations
			- 9.5 deploying and scaling nixos configurations
				- shared configurations
				- remote deployment with nixops
				- scaling configurations with declarative templates
				- optimising for scalability and performance
				- integrating continuous deployment pipelines
				- disaster recovery and rollbacks
				- case studies of scaled deployments
					- web hosting services
					- data-centric applications
				- final insights on scaling with nixos
			- 9.6 using configuration modules for modularity
		- collapsed:: true
		  10. advanced nix usage and customisation
			- 10.1 deep dive into nix language features
				- higher order functions
				- lazy evaluation
				- attribute sets and advanced typing
				- modularity and function composition
				- recursive functions and fixed points
				- nix language and domain-specific constructs
			- 10.2 customising builds with hooks and patches
			- 10.3 leveraging overlays for package management
				- scenario 1: integrating new dependencies
				- scenario 2: performance enhancements
				- scenario 3: debugging and development
			- 10.4 using lib functions for simplified configurations
				- list manipulation
				- attribute set functions
				- string manipulation
				- option handling
				- predicate utilities
				- building modular configurations
				- automation in package expressions
				- case studies and implications
					- case study 1:  streamlined nixos configuration
					- case study 2: unified development environments
			- 10.5 creating and maintaining private repositories
			- 10.6 integrating nix with other development tools
			- 10.7 performance tuning and optimisation
				- simplifying expressions
				- minimising dependency chains
				- configuring parallel builds
				- analysing build performance
				- enabling and utilising binary caches
				- automated build output management
		- collapsed:: true
		  11. continuous integration and devops with nix
			- 11.1 nix in the devops lifecycle
			- 11.2 setting up nix for CI/CD pipelines
			  collapsed:: true
				- installing nix
				- integrating nix in CI/CD tools
				- using nix in jenkins
				- using nix in gitlab CI
				- using nix in github actions
				- best practices for configuration
					- stateless builds
					- caching
					- declarative configurations
					- parallelisation
				- challenges and considerations
					- learning curves
					- platform compatibility
					- security concerns
			- 11.3 building reliable dev environments
			  collapsed:: true
				- immutability
				- reporducibility
				- minimal dependency hell
				- granular version control
			- 11.4 using nix to manage environment dependencies
				- exact reproducibility
				- elimination of dependency hell
				- flexibility and compatibility
				- easy rollbacks and upgrades
				- example of managing dependencies with nix
				- advanced dependency management techniques
					- overriding dependencies
					- pinning nixpkgs
					- external dependency mangement
				- best practices for effective nix dependency management
					- consistent environment definitions
					- team-wide nix configurations
					- regularly review pinning strategies
					- automation and CI integration
					- documentation
				- challenges in dependency management with nix
					- learning curve
					- binary cache mismatches
					- cross-compatibility issues
			- 11.5 automating builds and tests with nix
				- fundamentals of nix automation
					- nix expressions
					- the nix store
					- execution sandboxing
					- writing build scripts with nix
			- 11.6 deploying applications using nix
		- collapsed:: true
		  12. reproducible builds using nix
			- 12.1 understanding reproducible builds
			- 12.2 nix's role in ensuring reproducibility
			- 12.3 creating reproducible environment configurations
				- defining environment sources with nix
				- advanced techniques for environment management
				- reproducibility in complex systems
				- nixos: beyond development into system-wide reproducibility
				- collaborative development and reproducible research
			- 12.4 managing dependencies for reproducibility
				- the functional nature of nix dependency management
				- fixed-output derivations
				- pinning dependencies with nixpkgs
				- dependency version compatibility and overrides
				- ensuring dependency integrity and security
				- conclusion on dependency management
			- 12.5 building and verifying reproducibility
			- 12.6 challenges and solutions for reproducible builds
			- 12.7 case studies of reproducible builds with nix
		- collapsed:: true
		  13. nix and containerisation
			- 13.1 basics of containerisation
			- 13.2 integrating nix with docker
			- 13.3 nix as a tool for building immutable containers
			- 13.4 managing multi-stage builds with nix
			- 13.5 container orchestration with nix
			- 13.6 nixos containers: system-wide consistency
			- 13.7 challenges and solutions in nix-based containerisation
				- challenge 1: learning curve and adoption
					- solution
				- challenge 2: complex dependency management
					- solution
				- challenge 3: build times and computational overheads
					- solution
				- challenge 4: debugging and diagnostics
					- solution
				- challenge 5: ecosystem integration
					- solution
				- challenge 6: security considerations
					- solution
		- collapsed:: true
		  14. security and isolation with nix
			- 14.1 security principles in nix
			- 14.2 package isolation and sandboxing
			- 14.3 managing dependencies securely
			- 14.4 immutable infrastructure with nixos
			- 14.5 implementing system security policies
			- 14.6 nix and trusted computing
			- 14.7 addressing security vulnerabilities
		- collapsed:: true
		  15. Troubleshooting and best practices in nix
			- 15.1 common issues and error messages
			- 15.2 debugging techniques for nix expressions
			- 15.3 effective use of nix logs
			- 15.4 versioning and compatibility practices
			- 15.5 optimisation and performance tuning
			- 15.6 maintaining and updating nix environments
			- 15.7 community and support resources
	- installation
		- nagaraju@RD-nagaraju ~ $ curl -k -L https://nixos.org/nix/install | sh
		    % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
		                                   Dload  Upload   Total   Spent    Left  Speed
		    0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
		  100  4267  100  4267    0     0   1931      0  0:00:02  0:00:02 --:--:--  1931
		  downloading Nix 2.26.1 binary tarball for x86_64-linux from 'https://releases.nixos.org/nix/nix-2.26.1/nix-2.26.1-x86_64-linux.tar.xz' to '/tmp/nix-binary-tarball-unpack.KdCMWvz4zH'...
		    % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
		                                   Dload  Upload   Total   Spent    Left  Speed
		  100 22.8M  100 22.8M    0     0  3630k      0  0:00:06  0:00:06 --:--:-- 4217k
		  Note: a multi-user installation is possible. See https://nixos.org/manual/nix/stable/installation/installing-binary.html#multi-user-installation
		  performing a single-user installation of Nix...
		  directory /nix does not exist; creating it by running 'mkdir -m 0755 /nix && chown nagaraju /nix' using sudo
		  copying Nix to /nix/store...
		- installing 'nix-2.26.1'
		  building '/nix/store/a8d3dkyxn2wzrhh6pc81myif4s72sfkm-user-environment.drv'...
		  warning: error: unable to download 'https://nixos.org/channels/nixpkgs-unstable': SSL peer certificate or SSH remote key was not OK (60) ; retrying in 254 ms
		  warning: error: unable to download 'https://nixos.org/channels/nixpkgs-unstable': SSL peer certificate or SSH remote key was not OK (60) ; retrying in 682 ms
		  warning: error: unable to download 'https://nixos.org/channels/nixpkgs-unstable': SSL peer certificate or SSH remote key was not OK (60) ; retrying in 1319 ms
		  warning: error: unable to download 'https://nixos.org/channels/nixpkgs-unstable': SSL peer certificate or SSH remote key was not OK (60) ; retrying in 2057 ms
		  error: unable to download 'https://nixos.org/channels/nixpkgs-unstable': SSL peer certificate or SSH remote key was not OK (60)
		  Fetching the nixpkgs channel failed. (Are you offline?)
		  To try again later, run "nix-channel --update nixpkgs".
		  modifying /home/nagaraju/.profile...
		  modifying /home/nagaraju/.zshenv...
		- Installation finished!  To ensure that the necessary environment variables are set, either log in again, or type
		- . /home/nagaraju/.nix-profile/etc/profile.d/nix.sh in your shell.