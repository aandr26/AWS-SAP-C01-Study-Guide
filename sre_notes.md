# SRE Team
In general, an SRE team is responsible for the availability, latency, performance, efficiency, change management, monitoring, emergency response, and capacity planning of their service(s).

# Postmortems
Postmortems should be written for all significant incidents, regardless of whether or not they paged; postmortems that did not trigger a page are even more valuable, as they likely point to clear monitoring gaps. 
This investigation should establish what happened in detail, find all root causes of the event, and assign actions to correct the problem or improve how it is addressed next time.

# What is our error budget?
Error budger = 1 - availability target.
A service that is 99.99% available has error budget of 0.01%
Use that error budget to your advantage, but don't overspend it.
An outage is no longer a “bad” thing—it is an expected part of the process of innovation, and an occurrence that both development and SRE teams manage rather than fear.

# Monitoring
Monitoring should never require ahuman to interpret any part of the alerting domain. Instead, software should do the interpreting, and humans should be notified only when they need to take action.
### Three kinds of valid monitoring output:
- [ ] Alerts: Human needs to take immediate action to improve situation.
- [ ] Tickets: Human actions needs to be taken but not immediately.
- [ ] Logging: No one needs to look at unless compelled to do so.

# Emergency Response
The most relevant metric in evaluating the effectiveness of emergency response is how quickly the response team can bring the system back to health—that is, the mean time to repair (**MTTR**).

When humans are necessary, Google found that thinking through and recording the best practices ahead of time in a “playbook” produces roughly a **3x** improvement in MTTR as compared to the strategy of “winging it.”

# Change Management
Best practices in this domain use automation to accomplish the following:
- [ ] Implementing progressive rollouts.

- [ ] Quickly and accurately detecting problems.

- [ ] Rolling back changes safely when problems arise.

# Capacity Planning
There’s nothing particularly special about these concepts, except that a surprising number of services and teams don’t take the steps necessary to ensure that the required capacity is in place by the time it is needed.

### Several steps are mandatory in capacity planning:

- [ ] An accurate organic demand forecast, which extends beyond the lead time required for acquiring capacity.

- [ ] An accurate incorporation of inorganic demand sources into the demand forecast.

- [ ] Regular load testing of the system to correlate raw capacity (servers, disks, and so on) to service capacity.

Because capacity is critical to availability, it naturally follows that the SRE team must be in charge of capacity planning, which means they also must be in charge of provisioning.

# Provisioning
Provisioning combines both change management and capacity planning.
Adding new capacity often involves spinning up a new instance or location, making significant modification to existing systems (configuration files, load balancers, networking), and validating that the new capacity performs and delivers correct results.

