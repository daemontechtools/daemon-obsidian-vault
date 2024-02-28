
# Project Outline

Online application for creating, viewing and submitting quotes for the SMART platform.

# Repositories

### Smart Estimate

- Main Blazor Application
- Uses the server hosting model
- Consumes other libraries listed below
- Hosted with Azure App Service

### DataAccess

Generic State Management logic for handling Model Stores and APIs.

### RazorUI

Reusable Blazor UI Components.

### SMARTWebOrderApi

Uses the `SMARTOnlineOrderEntry` client to manage CRUD with the SMART Database.
## Actions

- [ ] Grant access to Repos
	- [ ] SmartEstimate
	- [ ] SmartWebOrderApi
	- [ ] daemon-dotnet
- [ ] Access to Azure 
	- [ ] App Service
	- [ ] Azure Artifact

# Areas of Focus

## Build Pipeline

### Environments

I would like to take a look at how to properly use Variables and Secrets. I don't think a Staging environment is necessary. 

#### Variables

Currently I don't have a reliable way of setting environment variables or secrets locally. 
The only local environment variable I've needed so far is `TAILWINDCSS_PATH` and it's set as a `PropertyGroup` entry in `.csproj`. Remotely it's set inside `.github/workflows/production_deploy.yml`.

You should be able to set environment variables in `launchSettings.json` but I found it unreliable when using the CLI commands.

#### Secrets

I know there's a mechanism for storing secrets in locally with `.NET` but I haven't used it yet.

### Tailwind

- Run `tailwind --watch` with `dotnet watch`
- Review my current setup for handling scoped CSS in Razor components.
- Why are some breakpoints ignored?
- Create CSS Bundle
	- App Css
	- RCL Css

## General Questions

