# Day 1 – Route 53 Basics

## 🌐 Concepts I Learned

1. **DNS (Domain Name System)**  
   - DNS is the system that translates domain names (like google.com) into IP addresses that computers understand.
   - It acts like the internet’s phonebook.

2. **AWS Route 53**  
   - Route 53 is Amazon’s DNS service.
   - It can register domains, manage DNS records, and route internet traffic using advanced policies.
   - It is scalable, highly available, and integrated with other AWS services.

3. **Hosted Zones**  
   - A hosted zone contains DNS records for a domain.
   - **Public Hosted Zone**: Used for domains accessible on the internet.
   - **Private Hosted Zone**: Used within a private VPC network.

4. **Record Types**  
   - **A Record**: Points a domain to an IPv4 address.
   - **CNAME**: Points one domain to another domain (not an IP).
   - **Alias Record**: Similar to CNAME, but works with AWS resources like S3, ELB.
   - **NS, SOA, MX**: Other types used for nameservers, authority, and mail exchange.

5. **TTL (Time to Live)**  
   - Determines how long DNS information is cached.
   - Shorter TTL = faster updates, but more lookups.
   - Longer TTL = slower updates, but better performance.

6. **Routing Policies**  
   - **Simple**: Single static response.
   - **Weighted**: Distribute traffic between multiple resources based on weights.
   - **Latency-based**: Route to the region with lowest latency.
   - **Failover**: Use a backup if the primary is unhealthy.
   - **Geolocation**: Route users based on their physical location.

---

## Questions I Had (Now Answered)

- **What is the difference between A and Alias Records?**  
  A → IP address.  
  Alias → AWS resource like ELB/S3. Alias can’t be used outside AWS.

- **What does TTL do?**  
  It controls how long DNS results are cached before they refresh. Useful when making frequent changes.

---

## 🔁 Plan for Day 2

- Create a public hosted zone in Route 53
- Add an A record for an EC2 instance or dummy IP
- Try Weighted Routing (if possible)
- Start documenting hands-on results


