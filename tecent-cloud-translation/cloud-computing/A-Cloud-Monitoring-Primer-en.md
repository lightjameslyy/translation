# A Cloud Monitoring Primer

原文作者：Angela Stringfellow

原文地址：[here](https://dzone.com/articles/a-cloud-monitoring-primer)


Cloud monitoring is the process of evaluating, monitoring, and managing cloud-based services, applications, and infrastructure. Companies utilize various application monitoring tools to monitor cloud-based applications. Here’s a look at how it works and best practices for success.

## Types of Cloud Services to Monitor

There are multiple types of cloud services to monitor. Cloud monitoring is not just about monitoring servers hosted on AWS or Azure. For enterprises, they also put a lot of importance into monitoring cloud-based services that they consume. Including things like Office 365 and others.

 

- SaaS – Services like Office 365, Salesforce and others



- PaaS – Developer friendly services like SQL databases, caching, storage and more



- IaaS – Servers hosted by cloud providers like Azure, AWS, Digital Ocean, and others



- FaaS – New serverless applications like AWS Lambda and Azure Functions



- Application hosting – Services like Azure App Services, Heroku, etc



Many of these can be monitored usually traditional application performance monitoring tools. However, [cloud monitoring has some unique requirements](https://stackify.com/cloud-monitoring-vs-server-monitoring/)  over basic server monitoring tools. 

## How It Works

The term cloud refers to a set of web-hosted applications that store and allow access to data over the Internet instead of on a computer’s hard drive.

 

- For consumers, simply using the internet to view web pages, access email accounts on services such as Gmail, and store files in Dropbox are examples of cloud computing for consumers.



- Businesses use it in many of the same ways. They also may use Software as a Service (SaaS) options to subscribe to business applications or rent server space to host proprietary applications to provide services to consumers.



Cloud monitoring works through a set of tools that supervise the servers, resources, and applications running the applications. These tools generally come from two sources:


1. **In-house tools from the cloud provider** — This is a simple option because the tools are part of the service. There is no installation, and integration is seamless.



2. **Tools from independent SaaS provider** — Although the SaaS provider may be different from the cloud service provider, that doesn’t mean the two services don’t work seamlessly. These providers also have expertise in managing performance and costs.



Cloud monitoring tools look for problems that can prevent or restrict businesses from delivering service to their customers. Generally, these tools offer data on performance, security, and customer behavior:

 


- **Cybersecurity** is a necessary part of keeping networks safe from cyber attacks. IT teams can use it to detect breaches and vulnerabilities early and secure the network before the damage gets out of hand.


- **By testing at regular intervals**, organizations can detect errors quickly and rectify them in order to mitigate any damage to performance and functionality, which improves the customer experience and, as a result, can boost sales and enhance customer retention.


- **Speed** — like functionality and user experience — is a primary driver of customer satisfaction. Speed metrics can be monitored and generate data that helps organizations optimize websites and applications.


If an organization monitors early and often, they can use the data to troubleshoot problems and implement repairs in a timely — if not instantaneous — manner.


## Benefits of Cloud Monitoring

The top benefits of leveraging cloud monitoring tools include:

 


- They already have infrastructure and configurations in place. Installation is quick and easy.


- Dedicated tools are maintained by the host. That includes hardware.


- These solutions are built for organizations of various sizes. So if cloud activity increases, the right monitoring tool can scale seamlessly.


- Subscription-based solutions can keep costs low. They do not require startup or infrastructure expenditures, and maintenance costs are spread among multiple users.


- Because the resources are not part of the organization’s servers and workstations, they don’t suffer interruptions when local problems disrupt the organization.


Many tools can be used on multiple types of devices — desktop computers, tablets, and phones. This allows organizations to monitor apps and services from any location with Internet access.


## Best Practices

Organizations need to make cloud monitoring a priority and plan for it. The plan should include questions that need to be answered and goals of implementation, such as:

 


- **Identify metrics and events** – What activity needs to be monitored? Not everything that can be measured needs to be reported. Monitor the metrics that matter to the bottom line.


- **Use one platform to report all the data** – Organizations may have their own infrastructures in addition to cloud services to monitor. They need solutions that can report data from different sources on a single platform, which allows for calculating uniform metrics and results in a comprehensive view of performance.


- **Monitor cloud service use and fees** – The ability to scale is a feature is a key feature of cloud services, but increased use can trigger increased costs. Robust monitoring solutions should track how much organization activity is on the cloud and how much it costs.


- **Monitor user experience** – Organizations need to know what users experience when using their cloud-based applications. Monitor metrics such as response times and frequency of use to get the complete picture of performance.


- **Trigger rules with data** – If activity exceeds or falls below defined thresholds, the right solution should be able to add or subtract servers to maintain efficiency and performance.


- **Separate and centralize data** – Organizations should store monitoring data separately from their apps and services, and it should be centralized for easy access for key stakeholders.


- **Try failure** – Test your tools to see what happens when there is an outage or data breach and evaluate the alert system when certain thresholds are met.


## Additional Resources and Tutorials

For more information and tips for implementation, visit the following resources:

 


- [6 Reasons Cloud Monitoring Is Different Than Server Monitoring](https://stackify.com/cloud-monitoring-vs-server-monitoring/)


- [Guide to Cloud Monitoring Tools and Best Practices](http://www.datacenterknowledge.com/archives/2014/03/21/guide-cloud-monitoring-tools-best-practices/)


- [4 Best Practices for Monitoring Cloud Infrastructure You Don’t Own](https://www.sevone.com/white-paper/4-best-practices-monitoring-cloud-infrastructure-you-dont-own)


- [Designing and Implementing Cloud Governance: Cloud, and Cloud Governance are Emerging Capabilities](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=12&cad=rja&uact=8&ved=0ahUKEwj7wOPFsvzVAhXDTCYKHSv9Boo4ChAWCEUwAQ&url=https%3A%2F%2Fwww.eiseverywhere.com%2Ffile_uploads%2F8d78b669e86b0120d704469d84fbf680_CLF_2011_Governance_Frameworks_Eric_Marks.pdf&usg=AFQjCNFHtkQ-4DNbeQejXtaYLm0sAie_Ag)


- [Continuous monitoring strategy](https://cloud.gov/docs/ops/continuous-monitoring/)


Monitoring is a must for any organization leveraging the cloud, both for security and performance, but choosing the right application performance monitoring (APM) solution can be challenging. Check out [this post](https://stackify.com/mistakes-implementing-application-performance-monitoring-solutions/) to learn about the common mistakes IT management teams make when evaluating and implementing APM solutions. Got noisy neighbors impacting your performance? Read [this article](https://stackify.com/how-to-monitor-noisy-cloud-neighbors-your-web-apps-using-stackifys-apm/) for tips on monitoring your noisy cloud neighbors and web apps with Stackify’s Retrace for APM. Finally, for some expert insights on the DevOps movement, server monitoring, and the cloud, [this interview](https://stackify.com/devops-movement-sean-hull-interview/) with Sean Hull is a must-read.
