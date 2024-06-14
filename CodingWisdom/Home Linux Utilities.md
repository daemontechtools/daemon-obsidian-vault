# Prebuild Binaries

- Create small always running server to listen
- ACTUALLY create a github action that builds the packages for void and hosts them in the repo. Then we can tell XBPS to look at that repo using `etc/xbps.d`
- 

Daemon Package Manager

- Bootstrap
	- Download all needed repositories
	- run binary bootstrap
	- install other packages into srcpkgs
- Update Repos
	- Pull latest versions
	- Update shlibs
	- Update srcpkgs
- Update Packages
	- Update Repos
	- Find installed packages that are out of date
		- xbps-query -m
	- Call pkg on package name
	- Call sudo xbps-install
- List all installed XBPS src packages
- List all avaialable xbps-src packagest

### Handle Custom Packages

- Create my own repo with custom packages
	- replicate abyss-packages


### Apps to include

- 1Password
- VS Code
- Discord
- Obsidian
- 