# IT Industry Challenges 
Disseration for Rovira i Virgily University students about IT Industry. GSX is the system administration subject in the curriculum.

Goals:
- How a systems department works and different models that I have found so far and vision of the possible roles that systems specialists play in companies.
- What are the possible futures of systems specialists (DevOps, SRE, Kubernetes, etc.), and how is the world of infrastructure evolving to face different challenges. (A booming industry indeed). This direction that the market is taking is in order to overcome different challenges and adapt to new needs.
- During the talk I will try to emphasize that OpenSource has revolutionized and is revolutionizing this entire world.
- The importance of the GSX subject since it provides a good base knowledge to start a career in the world of infrastructure. For example, it is impossible to be an SRE or Kubernetes specialist without a strong knowledge of systems and networks, since this is the basis.

The speech begins introducing how the IT industry works and what are tha current challenges and solutions. Afterwards, it gets a bit techy and introduces concepts to address the challenges in the IT industry. This doc is meant to provide a brief introduction, so none of the topics are covered in depth. It is meant for students or people getting started in the IT industry.

Only two main problems will be addressed. Other challenges have been left aside due to the scope of the dissertation.

Topics:
  - 1. [System administration in the real workd](https://github.com/jangel97/k8s-for-dummies/edit/main/docs/Others/GSX_sysadmin_devops_sre/README.md#1-sysadmin-in-the-real-world)
  - 2. [Challenges faced by systems departments](https://github.com/jangel97/k8s-for-dummies/edit/main/docs/Others/GSX_sysadmin_devops_sre/README.md#2-challenges-faced-by-systems-departments)
  - 3. [Current solutions](https://github.com/jangel97/k8s-for-dummies/edit/main/docs/Others/GSX_sysadmin_devops_sre/README.md#3-current-solutions)
  - 4. [Containers, Kubernetes and Cloud](https://github.com/jangel97/k8s-for-dummies/edit/main/docs/Others/GSX_sysadmin_devops_sre/README.md#4-containers-kubernetes-and-cloud)
  - 5. [Infrastructure as code, configuration as code, and GitOps](https://github.com/jangel97/k8s-for-dummies/edit/main/docs/Others/GSX_sysadmin_devops_sre/README.md#5-infrastructure-as-code-configuration-as-code-and-gitops)
  - 6. [Work methodologies](https://github.com/jangel97/k8s-for-dummies/edit/main/docs/Others/GSX_sysadmin_devops_sre/README.md#6-work-methodologies)
  - 7. [Conclusions](https://github.com/jangel97/k8s-for-dummies/edit/main/docs/Others/GSX_sysadmin_devops_sre/README.md#7-conclusions)
  - 8. [Resources](https://github.com/jangel97/k8s-for-dummies/edit/main/docs/Others/GSX_sysadmin_devops_sre/README.md#8-resources)

# 1. Sysadmin in the real world
Systems administration is the field of work in which someone manages one or more systems, be they software, hardware, servers, or workstations. Its goal is to ensure that systems work efficiently and effectively.

There are different specialities (some examples):
- DBA
- Network sysadmin
- Security admin
- Technical support staff
- System admin
- Hardware (datacenter people)

The following lists illustrates an example of the tasks a system administrator can work:
- Daily system/software checks.
- Making data backups.
- Application of operating system updates and configuration changes.
- Installation and configuration of new hardware/software.
- Add/delete/create/modify user account information, reset passwords, etc.
- Answer technical queries.
- Responsibility for security.
- Responsibility for documenting the system configuration and architecture of the different solutions.
- Troubleshooting of any reported issues or reported issues.
- System performance tuning.
- Keep the network running. (corporate network, VPN, DNS, DHCP, etc.)

Without a resilient infrastructure, fault-tolerant, high availability, adjusted to the needs of consumers (developers), monitoring and alerts, developers' applications could not function.

The main goal of being a sysadmin is to be as lazy as possible. Not lazy in the sense that you don't work, but lazy in the sense that you make the computer do the hard, repetitive work, and you do the thinking work.

In this link you can find an example on some of the requirements to become a system administrator: https://www.linkedin.com/jobs/collections/recommended/?currentJobId=3047489497

Important technologies (traditionally):
- Linux.
- Network skills. (HTTP, TCP, udp, dns, dhcpd, sshd, IPAM, etc)
- Cloud.
- Databases.
- Containers.
- Observability.
- Continuous integration / Continuos Delivery.
- Windows (Windows AD, domain controller).

It's good to know a little about various runtimes for example the JVM, python, golang, php, etc.

Troubleshooting skill is extremely important.

We could possibly split the responsibilities of a system admin in three different groups:
1. **Operational work**. Attend customer requests, for example:
  - Create DNS records
  - System patching and reboot
  - Remove or create resources in hypervisors or cloud providers
  - Network ACL
  - Troubleshooting
2. **Engineering work**. Deliver new infrastructure offerings, for example:
  - Automate operational tasks.
  - Deliver new DNS solution
  - Implement a new technological solution.
3. **Training**. It is vital to keep up to date, there are many interesting sysadmin certs out there, for example:
  - https://www.redhat.com/es/services/training-and-certification
  - https://www.cncf.io/certification/training/
  - https://www.elastic.co/es/training/
  - https://www.cisco.com/c/en/us/training-events/training-certifications/certifications.html
  
    You have to be up to date and expand in different fields of knowledge. The more things you know, the more value it adds to you and the better you can define your path as a technician.
    Official certifications, from Red Hat, other manufacturers or CNCF.
    
# 2. Challenges faced by systems departments
## Problem 1: Systems department as bottleneck of an IT organisation

What happens, imagine there are 1000 developer teams with 10k+ VMs in an organization and systems team. The systems department  becomes a brutal bottleneck for the organization and the whole company loses agility, which is key against competitors. Also, how reliable are more than 10k systems managed by a single systems team?

Scaling up (adding technical resources) is not a scalable solution to the problem.
Scaling out horizontally and dividing the systems department is an interesting alternative. The concept of productization is interesting here. An SLA can be defined per product. In this case, a given product would be an infrastructure or automation offering.

Therefore, the market is evolving in a different direction, and as new problems appear, the sector has to adapt more and more. Agility is key for organizations, and business value depends on how reliable and compliant the systems are.

An interesting strategy to solve this problem is self-service, providing tooling and each team of developers being responsible for their own systems. The systems team now has a totally different role in this regard, and it is that now it does not manage teams but rather provides the tools to make possible the administration and access to the functionalities of each of the products. Documentation is very important here. Also automation, if you can give access to certain functionality of a product through a form is ideal. For example, a product could be managing infrastructure as code on AWS, and the workflow that enables access could be to create a repository with the base infrastructure and an automation that builds the infrastructure as code.

The idea is that the more self-service and autonomous the teams are, the less operational work, the better offering and the greater agility for the organization. Of course, it is important to help the teams if necessary to use the tooling, consultation.

## Problem 2: Gap between systems and development departments
DevOps movement was born to narrow the gap between both departments.
This movement dates back to between 2007 and 2008, when the software development and IT operations communities came together to address a pressing concern in the industry. Both parties felt that there was a fatal level of dysfunction caused by the traditional model of software development. In the model, the people who develop the code and those who implement and support it work independently, organizationally, and functionally. Additionally, developers and IT professionals (Ops) worked in siled teams with different leadership, KPIs, goals, and physical locations.

Both communities stated that there was a better way of doing things than working in silos. They started online forums and local meetings to develop a way forward. In 2009, the first DevOps event was held in Belgium to achieve greater efficiency in software development. From its humble beginnings, DevOps is a hot topic in IT today.

Challenges addressed here:

1. Overcome the development versus operations mindset
2. Faster time to market
3. Speed up time to resolution of development issues
4. Optimize productivity

Personally I like to explain the conflict between Ops and Dev with the factory metaphor:
Imagine a factory where there are two teams:
- Team A dedicated to going to work to produce at the factory.
- Team B that goes into building plants and reactors and maintaining them. If needed provides new features in the factory tools and creates new plants and tooling for team A.

It turns out that these teams do not understand each other, because neither of them is capable of understanding the needs of the other, here is a major collaboration problem. In the end, this problem ends up generating unproductiveness and loss of business value, because of a considerable lack of agility.

Possible solutions? Check out the following topics.

# 3. Current solutions
## Solution to problem I. Site Reliability Engineering
Let us suppose an organisation of thousands of development teams. Imagine if systems team is required to manage resourcses, corporate network, Storage, accesses and so on for all developer teams. It is just unfeasible.

One solution to this problem is the Site Reliability Engineering. Let's split each responsability in a product offering managed by a virtual team behind IT.

Each team should be responsible of devlivering the tooling, documentation and automation to the development teams so they can, by themselves, manage their infrastructure.

SRE is what you get when you treat operations like a software problem.
The SRE mission is to protect, deliver, and advance the software and systems behind all different environments with an ever-vigilant eye on availability, latency, performance, and capacity. In order to achieve it, all infrastructure must be managed seemengly.

Standardization and automation are two important elements of the SRE model. Site reliability engineers must always look for ways to improve and automate operational tasks.

## Solution to problem II. DevOps engineering

In order to narrow the gap between Ops and Devs the DevOps movement was born (aforementioned in previous topic).
The idea of DevOps is that if you are a company with 100 developers and you compete against one that has 10,000. The only way you can make is by being agile. This implies important changes in organizations. Among these, one of the most important changes is the idea that the systems department and the development department have to begin to understand each other.

If you remember the factory metaphor, it is similar to the ongoing situation in the IT industry. 

In the case of the IT Industry the idea of a hybrid profile is born. A profile that is capable of mediating between both teams.
In the case of software engineering, what this profile does is that the developer builds and deploys applications automatically and does not have to worry about the environment or the infrastructure. Concepts like CI/CD apply here. In the end, these new professionals build a platform where build and deploy is automatic. These new professionals know how the applications work (not at the level of a developer) as well as its requirements, and they also have the infrastructure knowledge to maintain this automatic construction and deployment platform.

Although DevOps is a cultural movement, some IT organisations call DevOps Engineer to this role, the main responsibility of which, is to narrow down the gap between Ops and Devs and speed up the delivery of applications, features and bugs.

Currently, in an organisation it is possible that system team has evolved into a SRE team and provide tooling, docs and consultation, so teams can manage infrastructure seemingly. As for DevOps engineers, it is possible that they exist either in the same Development teams or in a specific Delivery team. DevOps teams must be capable of using the SRE tooling to manage the required infrastructure for the applications to run.

These types of professionals are highly demanded because they significantly increase agility in organizations.

Currently, in some organizations the roles of devops and SRE can be a bit mixed. You may apply to a devops position and see that the requirements ask for a bit of SRE and DevOps.

You can find what are the responsabilities for a DevOps engineer or a Site Reliability Engineer in the following links:
- https://www.linkedin.com/jobs/search/?keywords=sre
- https://www.linkedin.com/jobs/search/?keywords=devops


# 4. Containers, Kubernetes and Cloud

The changes required in the IT organisations to tackle the aforementioned problems, require new technology. In this topic we will introduce new technologies vital to address both problematics.

## Containers

Linux containers are technologies that allow you to package and isolate your applications along with the entire runtime environment, that is, with all the files that they require to run. This allows you to move the application inside the container between environments (development, test, production, etc.), without losing any of its functionality.

![image](https://images.contentstack.io/v3/assets/blt300387d93dabf50e/bltb6200bc085503718/5e1f209a63d1b6503160c6d5/containers-vs-virtual-machines.jpg)

You can easily build your own containers (or containerize existing ones). It's a nice consistent way to package your apps.
https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

**Pros**
- *Less overhead*
  
  Containers require less system resources than traditional or hardware virtual machine environments because they don’t include operating system images.
- *Increased portability*

  Applications running in containers can be deployed easily to multiple different operating systems and hardware platforms.
- *More consistent operation*

  DevOps teams know applications in containers will run the same, regardless of where they are deployed.
- *Greater efficiency*

  Containers allow applications to be more rapidly deployed, patched, or scaled.
- *Better application development*

  Containers support agile and DevOps efforts to accelerate development, test, and production cycles.

**Use cases**
- *“Lift and shift” existing applications into modern cloud architectures*
  
  Some organizations use containers to migrate existing applications into more modern environments. While this practice delivers some of the basic benefits of operating system virtualization, it does not offer the full benefits of a modular, container-based application architecture.
  
  Lift and shift is a strategy for moving an application or operation from one environment to another without stopping to redesign the app or operations workflow.
  
- *Refactor existing applications for containers*
  Although refactoring is much more intensive than lift-and-shift migration, it enables the full benefits of a container environment.
- *Develop new container-native applications*
  Much like refactoring, this approach unlocks the full benefits of containers.
- *Provide better support for microservices architectures*
  Distributed applications and microservices can be more easily isolated, deployed, and scaled using individual container building blocks.
- *Provide DevOps support for continuous integration and deployment (CI/CD)*
  Container technology supports streamlined build, test, and deployment from the same container images.
- *Provide easier deployment of repetitive jobs and tasks*
  Containers are being deployed to support one or more similar processes, which often run in the background, such as ETL functions or batch jobs.
  
Containers in the end are Linux Processes. In order to provide isolation and control of resources they rely on following Kernel Linux features:
- Linux namespaces (isolation) https://en.wikipedia.org/wiki/Linux_namespaces
- cgroups v2 (control of resources) https://www.kernel.org/doc/html/latest/admin-guide/cgroup-v2.html
- chroot (file system isolation) https://btholt.github.io/complete-intro-to-containers/chroot

For now it's enough to provide a brief introducion into the container concept. If you wish to learn more about this, please, check out the following resources:
- https://podman.io/
- https://docs.podman.io/en/latest/Tutorials.html
- https://developers.redhat.com/blog/2018/08/29/intro-to-podman
- https://docs.docker.com/develop/develop-images/dockerfile_best-practices/
- https://kubernetes.io/docs/setup/production-environment/container-runtimes/#containerd
- https://kubernetes.io/docs/setup/production-environment/container-runtimes/#cri-o
- https://kubernetes.io/docs/setup/production-environment/container-runtimes/#docker
- https://kubernetes.io/docs/setup/production-environment/container-runtimes/#mcr
- https://www.aquasec.com/cloud-native-academy/container-security/container-runtime/

## Kubernetes 

## Cloud


# 5. Infrastructure as code, configuration as code, and GitOps
# 6. Work methodologies
# 7. Conclusions
# 8. Resources
