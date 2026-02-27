# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

## My aanalysis of VS vs WebApp
### VM IAAS (Infrastructure as a Service)

- Costs: you basically pay based on teh sive of CPU/RAM whiel running, Typically the cost is fixed untless you add more VM's
In short the cost is predictable ,but there are hidden costs for VM management, licensing, and admin to help with setup and secuirty.

- Scalability: very flexible / customizeable, but requires mroe hands on approack to add VM Scaling, load balancing and health probes.

- Availability: this depends on your need / architecture.  A single VM => single point of failure, Multiple VM's more redundancy, but more complex and overhead to manage and maintain

- Workflow: Traditional server workflows, more flexibility but requires more hands on attention & maintenance.  This is more fit for Legacy ASpps, Lift and shit migrations, aor custom runtimes.

### Azure Web App Service - PAAS (Platform as a Service)

- Costs: Requires an App Subscription / service plan (shared compute); often cheaper for small to medium we apps. No OS or VM managemnt tool so maintenance / overhead costs are minimal.  In short generally more cost-effective for web workloads beacause instrastucture is shared and managed.

- Scalability: Scaling can be built via a mnaual or automated scaling based on CPU, memor, requests, or scheduled.  Scalisn is fast and transparent in the app.  No need to design infrastructure patterns.

- Availability: Built in with the Web App.  The host handles failures and OS maintenance, and typically has load balancing, OS patching, and platform updates.  Owner mainly controols number of instances.  This means high reliability by default with much less effort.

Workflows: Typically are Developer friendly such as GitHub Actions; Azure DevOps; or container support.  Built in aspects for secuirty such as App Settings and secrets, CI/CD, and deployments.  Web Apps are desing toe feel more modern, have ability for API's and Microserices.  This mean sdevelopers can focus more on code rather than server maintenance.

### my conclusion & decion for deployment route:
On a personal note, I have stood up multiple VM's in my career for various needs, but I have never created a WebApp or used Flask, so I am going to take this opportunity to grow my skills and try something new.

WebApps are more developer friendly and less reliant on older skill sets of server maintenance.  For a small POC / MVP it would be easier to create documentation / support information to pass on for internal Architecture review, so the app can be built faster, possibly cheaper, and ulitmately an increased value to the End User / Customer.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

- The key here would be more long term / scope change.  If the ask was for more storage or processing power such as using AI to analyze images, this would requirem mroe compute power than what would come standard with WebApp so spinnup up VM's may be more cost effective and more performant.
