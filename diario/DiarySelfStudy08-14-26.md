# CyberStudy - 08/14/26

# Today was another day of studying with <a href="https://tryhackme.com/">**TryHackMe**</a>.

## ***Client-Server Basics***
- I started understanding how the **Client-Server Model** works. The room gives an example of a pizza delivery to explain this model, where the client is a woman called "Alice," the server is the pizzeria called "Luigi's Pizzeria," and the protocol that allows communication between the client and the server is a man called "Bob." The room explains that when the pizza is ordered, the client sends a message (**Request**) to the server requesting a type of pizza, and the server sends another message (**Response**) to the client saying whether the request is valid and confirmed. The room also explains the **ports** system, which is the identification system used for different services — for example, when Luigi's (server) offers multiple services, such as takeaway, dine-in, and delivery, each service uses a different door: door A for takeaway, door B for dine-in, and door C for delivery. For that reason, the client needs to use a different port for each service. The **DNS** concept is also explained in the room: DNS is the protocol that gives the server's address to the client, working like a GPS in real life — the client (Alice) searches for the server's URL (Luigi's Pizzeria), and DNS provides the address (called the **Internet Protocol (IP)** address) so the client can establish a connection with the server using another protocol.

- Once the Client-Server Model was understood, the room began an explanation of **Hypertext Transfer Protocol Secure (HTTPS)**, introducing the **Request Methods** with a demonstration of the **GET** method on the lab machine.
> *GET Method* — Used to retrieve a resource from a web server.

The room gives an example using a URL from THM and explains that the client doesn't need to specify the method used, since the browser already does this for the client; the server returns a response including the status code and the requested information.
- After the GET method explanation, the room introduced some exercises on the lab machine, explaining the terms *Scheme*, *Host*, *Filename*, *Address*, and *Status*, and visiting the page *"https://www.iamlearning.thm/contact"* to see the details of the Scheme and Host, finishing up the Client-Server Basics room.

## ***Virtualization Basics***

- The explanation in that room starts with a simple example: a building with 10 apartments, where the building represents a server and a single tenant lives there alone, simulating one application. In this scenario, the lone tenant needs to take care of all the building's needs alone — including water, electricity, cleaning, and security — making the work expensive, inefficient, and unnecessary for their actual needs. The room then shows another version of the same building, but now with 10 tenants living there, each with their own responsibilities, dividing the work and organizing everything with privacy, transforming a space that previously saw only 10% utilization into one operating at 100% of its total capacity. This building now has a "Building Manager," called the **Hypervisor**, the entity that allocates space, manages operations, and keeps harmony among the building's tenants.
- The index ends with this:
> The building is the physical server
> The apartments are the lab machines
> The tenants are the applications or operating systems
> And the building manager is the hypervisor (the software shown in greater detail later).

- After this, the room presents an explanation of the **Hypervisor**. Basically, the hypervisor is the core technology of virtualization and is the software that:
> Divides a physical computer into multiple virtual ones.
> Gives each lab machine its own share of CPU, memory, and storage.
> Keeps everything isolated and safe.
> Manages the lifecycle of lab machines (start, stop, pause, clone, delete).

- There are two types of hypervisor:
**Type 1**: runs directly on the physical hardware, making it fast, efficient, and ideal for servers and professional environments.
**Type 2**: runs within an existing operating system, making it easier to install and ideal for learning, testing, or small setups.
The two types are used for different use cases, such as testing malicious files, production servers, database servers, software testing, Kali Linux, and data centers.

- Continuing the explanation, the room talks about **Lab Machines** (the apartments of the building). In simple terms, a lab machine (**Virtual Machine**) is a virtual computer created by the hypervisor. It has its own virtual CPU, RAM, storage, and network, can run any operating system (Windows, Linux, etc.), and is completely isolated from other VMs. This means that if one VM breaks, the others continue to work.

- The last concept was **Containers** (the rooms inside the apartment), which are basically a lightweight, isolated environment that runs a single application and all the necessary components to support it. Containers package the application and its dependencies (libraries, tools, versions) and share the host's operating system, so they start almost instantly and remain isolated from each other — a misbehaving container doesn't affect the others — and they can run consistently on any machine, making them perfect for development, testing, and scalable deployments. The room ends this section by explaining that VMs provide the "full apartment" with maximum separation and flexibility, while containers offer lightweight "rooms" ideal for scalable, fast-deploying applications.

- The last exercise in this room was practical VM management, where I was hired to manage a system with 3 physical machines and several virtual machines. In this role, I fixed a virtual machine that had broken — restarting it was enough — and I created a new VM for the Marketing team to use, allocating 4 CPU cores, 8GB of RAM, and 100GB of storage. I solved some simple exercises that THM proposed and completed the room.

## ***Cloud Computing Fundamentals***

- This room started by talking about the evolution of the cloud over time, starting with: Physical Servers → Virtualization → Automation & Remote Management → Cloud Computing → Modern Cloud Era. After that, the room showed some characteristics of the cloud and their benefits, such as: **Scalability**, **On-demand self-service**, **Pay only for what you use**, **Security**, **High availability**, and **Global access** — attributes that make the cloud so strong and widely used today. Continuing with the types of cloud, I learned about the three types of cloud: **Public Cloud**, **Private Cloud**, and **Hybrid Cloud**, which have different uses for different environments, with Public Cloud being the most used in the world. Next, I was able to understand the *Cloud Service Models*, such as **Infrastructure as a Service (IaaS)**, **Platform as a Service (PaaS)**, and **Software as a Service (SaaS)**. Using a simple example, the room teaches these models through a renting-an-apartment analogy: **IaaS** is an *empty* apartment, **PaaS** is a *semi-furnished* apartment, and **SaaS** is a complete *hotel*.
- In the next tasks, I learned about the major cloud vendors that provide cloud services worldwide, such as Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP), among others, as well as some companies currently using the cloud, such as Netflix, Spotify, Instagram, and various online stores.
- At the end of Task 2, I had to answer some simple questions about the cloud, cloud applications, and cloud services. Starting Task 3, I began a lab in THM using a cloud interface very similar to the AWS platform to create my first cloud environment. Next, I learned some cloud terminology, such as *EC2* and *Instance Type*, and created a lab machine for my fake IaaS. Following the steps, I created two more lab machines, which were much more powerful than the first one I had created. At the end of this room, I answered some simple questions about the cloud interface by reviewing the missing steps, and finally reviewed the Cloud Key Terminology, completing the Cloud Computing Fundamentals room.

## That's all for today regarding my cybersecurity studies with TryHackMe, thanks for following along ☺️.
