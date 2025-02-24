# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.
n this scenario App services has been selected on the following factors:
- Costs: App services has much smaller costs compared to the VMs.
- Scalability: Current demands can be met with App services (Assumption)
  App services has the limitation such as a maximum of 14GB of memory and 4 vCPU cores per instance.
  VMs can be easily scaled: vertical or Horizontal scaling. Vertical scaling increases or decreases resources allocated to our App Service, such as the amount of vCPUs or RAM, by changing the App Service pricing tier. Horizontal scaling increases or decreases the number of Virtual Machine instances our App Service is running
   In the given scenario it is considered to be just an initial lauch and Appservices should be enough to meet the load demand.

  - Availability: App services has the high availability and VMs can be grouped to provide high availability, scalability, and redundancy. There are two options when it comes to scaling—Virtual Machine Scale Sets and Load Balancers. These will be covered in a different course

Complexity: App services are much simpler to deploy, manage vs the VMs.
This has been the biggest consideration 

### Assess app changes that would change your decision.

The biggest assumption in current decision to select App services are due to considerations that current and future load demands can be met by App services. 
If any changes to this assumtion including high volumes that required upscaling to more CPUs then the VM may be more appropriate to deploy an app afterward
