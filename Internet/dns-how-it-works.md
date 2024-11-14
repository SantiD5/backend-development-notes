# DNS an how it works?
**The Domain Name System (DNS)** is the phonebook of the Internet. Humans access information online through Domain names like google.com. Web browsers interact through **Internet Protocol (IP)** addresses. DNS translates domain names to IP addresses so browsers can load the web page.
### DNS servers
- **DNS recursor**: Think of the DNS recursor as a librarian who is asked to find a specific book in a library. This server receives queries from client machines (e.g., web browsers) and then makes additional requests to fulfill the DNS query.
- **Root Nameserver**: The **root server** is the first step in translating (resolving) human-readable host names into IP addresses. It’s like an index in a library that points to different shelves of books—typically acting as a reference to other more specific locations.
- **TLD nameserver**: The top-level domain (TLD) nameserver acts like a specific book rack in the library. It’s the next step in searching for an IP address, hosting the last portion of a domain name (e.g., in google.com, the TLD is “.com”).
- **Authoritative nameserver**: This is the last stop in the DNS lookup chain. Think of it like a dictionary, where a domain name is translated into its corresponding IP address. The authoritative nameserver holds the definitive DNS records and responds with the IP address when requested.
### What’s the Difference Between an Authoritative DNS Server and a Recursive DNS Resolver?
#### Recursive DNS Resolver
A **recursive DNS resolver** is the first stop in handling DNS queries from client machines. It tracks down the necessary DNS record by making multiple requests until it reaches the authoritative nameserver for the domain. When records are cached, it can respond without needing to go through the entire process again.
#### Authoritative DNS Server
An **authoritative DNS server** directly holds DNS resource records and is responsible for resolving DNS queries. It provides the final answer to a query. Unlike recursive servers, an authoritative server doesn't need to ask other servers for DNS records—it's the ultimate source of truth for DNS data related to its domains.
### What Are the Steps in a DNS Lookup?
Typically, DNS is used to translate a domain name into an IP address. The following outlines the steps in a DNS lookup:
#### The 8 Steps in a DNS Lookup:
1. A user types ‘example.com’ into a browser, which sends the query to a recursive resolver.
2. The resolver queries a root nameserver.
3. The root nameserver responds with the address of the appropriate TLD nameserver (e.g., .com for example.com).
4. The resolver sends a request to the TLD nameserver.
5. The TLD server responds with the IP address of the domain’s nameserver (example.com).
6. The resolver sends a query to the domain’s nameserver.
7. The authoritative nameserver for example.com returns the IP address.
8. The recursive resolver sends the IP address back to the browser.
Once the IP address is obtained, the browser can then send an HTTP request to the server, and the webpage will be loaded.

### What is a DNS Resolver?

A **DNS resolver** is the first server in the DNS query process. It receives the client’s request and begins the process of querying other DNS servers to find the correct IP address for the domain. The DNS resolver plays a key role in handling DNS queries efficiently.

### Types of DNS Queries

1. **Recursive Query**: In a recursive query, the client requests the DNS resolver to respond with either the requested record or an error if the resolver can't find it.
2. **Iterative Query**: The client allows the DNS server to give the best answer it can. If the server doesn't have the record, it provides a referral to another DNS server, and the client continues querying until the request is resolved or times out.
3. **Non-recursive Query**: This occurs when the DNS server has already cached the required record or is authoritative for the record. The server can return the answer directly without further querying.

### What is DNS Caching?

**DNS caching** involves storing DNS records closer to the requesting client so future lookups can be resolved faster, reducing load times and bandwidth consumption. Cached DNS records are stored for a set period based on their **time-to-live (TTL)** value.
#### Types of DNS Caching:
- **Browser DNS Caching**: Modern browsers store DNS records locally for faster access to websites. For instance, Chrome has an internal DNS cache.
- **Operating System (OS) Level DNS Caching**: The operating system also caches DNS records before sending a query to a DNS server. If a record is found in the local cache, the resolver responds immediately without querying external servers.
Once DNS data is cached, it reduces the need to make repeated queries, thus speeding up the resolution process.