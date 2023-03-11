## Docker Notes
Docker is a container technology: A tool for creating and managing containers.

### Setting up Docker:
- **BEFORE** downloading and installing Docker Desktop make sure you have:
	+ WSL 2 for Windows enabled
		* Hyper-V: From Start Menu search "Settings" > "Apps" > "Optional Features" > "Related Settings" > "More Windows Features"
		* Check on "Windows Hypervisor Platform"
	+ Hyper-V backend & Windows containers enabled
		* Same path into "More Windows Features"
		* Check on "Virtual Machine Platform"
	+ **NOTE**: changing these settings will require a restart of your computer.
- go to: https://www.docker.com
- From the menu choose: 'Developers' > 'Docs'
- On that page choose 'Download and Install'
- Choose Docker Desktop for your OS *(I'm on Windows)*


### What is a Container?
- A standardized unit of software. A package of code and dependencies to run that code. (e.g. NodeJS code + the NodeJS runtime)
- The same container always yields the exact same application and execution behavior. No matter where or by whom it might be executed.
- Self contained an isolated

Support for containers is built into modern operating systems. Docker simplifies the creation and management of such containers

#### Why containers?
> Why would we want **independent, standardized "application packages"**?
- We often have different development & production environments
- We want to build and test in exactly (!) the same environment as we later run our app in
	+ Environment: The runtimes, languages, and frameworks you need for development
- Containerization allows different versions of a project to easily run without having to manually change, add, or drop dependencies.
- Low impact on OS, very fast, minimal disk space usage
- Sharing, re-building, and distribution is easy
- Encapsulated apps/environments instead of "whole machines"
> Containerization is a form of virtualization. Virtualization aims to run multiple OS instances on a single server, whereas containerization runs a single OS instance, with multiple user spaces to isolate processes from one another.

### Virtual Machines vs Docker Contrainers
> Why not Virtual Machines? (Machines running on our machines with Virtual OS's)  

With Virtual Machines (VMs) we have our host operating system (Windows, Linux, etc.), and on top of that we install a virtual machine. So, a computer  inside of a computer, to say. This VM has its own Operating System (OS) which runs inside of that virtual Machine (ex. Linux). Then inside this VM, we can then install extra tools. Whatever we want. Because it's just another machine. We can install all libraries, dependencies, and tools that we need. We can also move our source code onto this VM. Since this is an encapsulated VM with everything our program needs, we have the same result with Docker/Containers. We have an encapsulated environment where everything is locked in. Then we can have multiple environments for different projects or we could share our VM configuration to ensure that we are all working on the same environment.  

> Virtual Machine Breakdown:
>- Your operating system
>	+ Virtual OS
>		+ Libraries, Dependencies, Tools,
>		+ App/Source Code
##### This is a solution
However we face a few issues:  
- The Virtual OS 
- And in general the overhead associate with multiple Virtual OS's. 

Each VM is like a standalone computer/machine running on top of our machines. Multiple such machines wastes a lot of space and resources. Each time we have to set up a new virtual OS it eats memory, CPU, and space on our hard drive. This becomes a problem as your app scales and you have more and more VMs on your system.  
You may have Linux as your OS for the VM, yet it's installed separately in every VM, wastes a lot of space. In addition other tools installed in each VM which your application doesn't need directly yet are set up as a default.
##### Pros of VMs
- Seperated Environments
- Environment-specific configurations are possible
- Environment configurations can be shared and reproduced reliably
##### Cons of VMs
- Redundant duplication, waste of space
- Performance can be slow, boot times can be long
- Reproducing on another computer/server is possible but may still be tricky 

You still have to set up the virtual machine on every system where you want it. And then configure it in the exact same way. There is no single config file you can necessarily share. So if you want to deploy your application from Development to Production you also have to ensure that you configure your Production Machine the same as your VM. Alternatively you run the VM on the Production Machine, but this is a performance waste not ideal for production. It solves the problem, but not in a perfect way. Here's where Docker and Containers come in. Containers is the key concept and Docker is the defacto standard tool for creating and managing them.
### How do Containers solve this problem?
#### Docker helps you Build and Manage "Containers"
With containers we still have our host OS, but we don't install multiple virtual machines, instead we utilize built-in container support that our OS has, and then we run a tool called the Docker Engine on top of that. Based on that engine on our system, we can spin up containers. These contain our code, the tools, runtimes, libraries, but they don't contain a bloated operating system, extra tools. Perhaps they have a small OS layer in the container.
#### Highly Configurable and Sharable
You can configure and describe them with a configuration file, and then share that file with others so that they can recreate the container. Or you can also build the container into an image, and then share that image with others to ensure that everyone is able to launch that same container, which you have on your system, on their systems.
#### Summarize: Containers vs VMs
Docker Containers  
- Low impact on OS, very fast, minimal disk space usage
- Sharing, re-building and distribution is easy
- Encapsulate apps/environments instead of "whole machines"
Virtual Machines  
- Bigger impact on OS, slower, higher disk space usage
- Sharing, rebuilding, distribution, can be challenging
- Encapsulate "whole machines" instead of just apps/environments
