## Docker Notes
Docker is a container technology: A tool for creating and managing containers.

What is a Container?
- A standardized unit of software. A package of code and dependencies to run that code. (e.g. NodeJS code + the NodeJS runtime)
- The same container always yields the exact same application and execution behavior. No matter where or by whom it might be executed.
- Self contained an isolated

Support for containers is built into modern operating systems. Docker simplifies the creation and management of such containers

Why containers?
> Why would we want **independent, standardized "application packages"**?
- We often have different development & production environments
- We want to build and test in exactly (!) the same environment as we later run our app in
	+ Environment: The runtimes, languages, and frameworks you need for development
- Containerization allows different versions of a project to easily run without having to manually change, add, or drop dependencies.
- Low impact on OS, very fast, minimal disk space usage
- Sharing, re-building, and distribution is easy
- Encapsulated apps/environments instead of "whole machines"

Setting up Docker:
- go to: https://www.docker.com
- From the menu choose: 'Developers' > 'Docs'
- On that page choose 'Download and Install'
- Choose Docker Desktop for your OS *(I'm on Windows)*
- **BEFORE** downloading and installing Docker Desktop make sure you have:
	+ WSL 2 for Windows enabled
		* Hyper-V: From Start Menu search "Settings" > "Apps" > "Optional Features" > "Related Settings" > "More Windows Features"
		* Check on "Windows Hypervisor Platform"
	+ Hyper-V backend & Windows containers enabled
		* Same path into "More Windows Features"
		* Check on "Virtual Machine Platform"
	+ **NOTE**: changing these settings will require a restart of your computer.