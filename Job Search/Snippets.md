## Kubernetes Experience

I've used Kubernetes during my time at Autocorp.ai to manage our Testing, Staging and Production environments. It was useful for the flexibility and speed of iteration it allows you to manage your entire cloud stack. 

I used it mostly in the context of AWS with their EKS service. It's incredibly convenient to provision the hardware resources available to each node as well as it's networking permissions, ingress rules and routing logic for things like load balancing. It's also useful to track live usage and metrics to see where latency is being introduced when a node is getting too much traffic or a database needs to be scaled.

We used Grafana to aggregate and view logs. 

Testing environments would be provisioned with a seeded database along with development versions of whatever the microservices were required for the feature being tested at that time. Testing clusters would not be scaled for redundancy or performance, unless a specific test called for it, only the minimal amount of resources needed. These clusters would be deleted once the feature passed and was ready to be tested in Staging.

Staging would be a longer living environment that is constantly being redeployed and mirrors Production as much as possible. It might actually have access and reach out to other 3rd party APIs but it would never interact with anything stateful that is used in Production. Like a database.

Production environments were deployed when we wanted to make a new release and deploy whatever we deemed ready from Staging. This cluster would be scaled for redundancy, performance and availability. Possibly include nodes in various regions closest to our clients for better responsiveness.

## Customer Service

At Autocorp when the product reached the point of being mature enough to be sold beyond our initial beta test group, I was tasked with building the tech support team. I enjoyed talking to our clients, empathizing with their issues, learning more about the product and how they were using it and helping the product grow by solving each issue.

The first task was to create a ticketing system so that we could be aware of the any issues or feature requests. These tickets came from the internal team (mostly sales) as well as clients by filling out a form inside the application itself. That allowed us to track them, respond to creator of the ticket ASAP, put them through triage and route them to the appropriate team for a resolution.

I would initially handle all service tickets which in most cases were issues installing our widget on their website. I created templates for common issues and extended our knowledge base/wiki so that others would have a playbook to follow and handle service tickets without my technical knowledge.

Feature requests and larger bugs would be routed to the dev team where we determined it's priority and estimated deadline for resolution which would be relayed to the creator of the ticket as soon as possible.


## Hiring Manager

I'm in the job market for software engineering role and am particularly interested in Canonical because of it's position in the open source community as well as it's remote first working policies.  
  
Would you be willing to briefly speak to me about your experience working there?  
  
I have a bit of a non traditional background and I'm trying to figure out if Canonical would be a good fit and if so, which positions should I target.



## Additional Information

I absolutely love your tech stack and it's very close to an infrastructure that I would use in my own personal projects. I've been in Web Development for 15 years as a Fullstack developer but in the past 2 years I've transitioned to Backend specialization. I love programming in Go and designing system infrastructure. I have over decade of hands on experience with AWS, have worked with relational and non-relational databases. I also strong grasp of the cloud computing ecosystem.

I really like that you start employees off with more than the mininum 2 week vacation and support remote work culture. I get so much more done than I used to at the office and also have more time to enjoy life! ff