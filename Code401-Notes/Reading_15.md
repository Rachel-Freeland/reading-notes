# Serverless Computing

## Reading

* [What is Serverless Computing?](https://www.ibm.com/cloud/learn/serverless)

### Additional Resources

* [venv - Creation of Virtual Environments](https://docs.python.org/3/library/venv.html)
  * Provides support for creating lightweight "virtual environments".
* [Vercel - Get Started](https://vercel.com/docs/get-started)
  * A platform for frontend frameworks and static sites
* [http.server](https://pymotw.com/3/http.server/index.html)
  * Uses classes from socketserver (used for creating network servers) to create base classes for making HTTp servers.
* [Requests](https://docs.python-requests.org/en/latest/)
  * Allows you to send HTTP/1.1 requests extremely easily.
* [Python & APIs](https://realpython.com/python-api/)

### Videos
* [What is Serverless?](https://www.youtube.com/watch?v=vxJobGtqKVM)

#### Bookmark & Review
* [Serverless Functions](https://vercel.com/docs/concepts/functions/serverless-functions)
* [Effective Python Environment](https://realpython.com/effective-python-environment/)

-----------------------------------------------------------------------

Serverless computing is a cloud computing execution model that:
1. Automatically provisions the computing resources required to run application code on demand, or in response to an event
2. Automatically scales those resources up or down in response to increased or decreased demand
3. Automatically scales resources to zero when the application stops running

Pros:
* Enables dev teams to focus on writing code
* Serverless customers pay for execution only. The meter starts when the request is made and ends when it is finished.
* Serverless is a polyglot environment means you can code in any language
* Simplifies deployment
* Can be faster and more cost-effective
* Provides near-total visibility into the system and user times

Cons:
* Stable or predictable workloads do not seem to take advantage of the cost-savings as much as spiky workloads
* Cold starts - for applications where latency is not an issue this is not a problem but, for certain environments this
delay is unacceptable
* Monitoring and debugging complexity is exacerbated by serverless computing
* Vendor lock-in