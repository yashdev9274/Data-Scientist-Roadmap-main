## What is Docker?

<img align="centre" src="Asset\Docker img.png" height="300" alt="Why"> 



A software platform called Docker makes it simple to develop, test, and deploy applications. Software is packaged by Docker into standardized units called [`containers`]() that contain all of the necessary code, libraries, system tools, and runtime. With Docker, you can easily scale and deploy apps into any environment while being confident that your code will work.

Docker also works together with AWS to speed up the delivery of contemporary programs to the cloud. Through this partnership, developers may more easily deploy apps to Amazon ECS and AWS Fargate by using Docker Compose and Docker Desktop in conjunction with their current local workflow. To learn more, read the blog.


## What are containers?

A container is a standardised software component that wraps up code and all of its dependencies to ensure that an application will run swiftly and consistently in different computing environments. An application's code, runtime, system tools, libraries, and settings are all included in a lightweight, independent, executable package known as a "Docker container image."

In the case of Docker containers, images become containers when they are running on Docker Engine. Container images become containers at runtime. Containerized software is available for both Linux and Windows-based applications, and it will always operate the same no matter the infrastructure. Software is isolated from its environment by containers, which guarantee that it operates consistently despite variations, such as those between development and staging.


### How containers work?

Containers are made possible by process isolation and virtualization capabilities built into the Linux kernel. Similar to how a hypervisor allows multiple virtual machines (VMs) to share the CPU, memory, and other resources of a single hardware server, these capabilities—such as control groups (Cgroups) for allocating resources among processes and namespaces for restricting a process' access or visibility into other resources or areas of the system—allow multiple application components to share the resources of a single instance of the host operating system.