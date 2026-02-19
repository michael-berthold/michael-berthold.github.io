---
title: Agentic AI Orchestration: Can Generalists Outperform Specialists?
author: Michael Berthold
---

AI functionality is now integrated into nearly every piece of business software. Almost all vendors offer copilots that assist users with operation and routine tasks — significantly increasing productivity. A Microsoft report, for example, shows that 3 out of 4 Word users use Copilot for initial drafts, achieving an average productivity increase of 10–15 percent. And the next evolutionary stage is already on the horizon: \"agentic\" systems that consolidate data from various systems, interpret it, and increasingly prepare or even make autonomous decisions.

As a result, many software vendors are now adopting AI assistants that analyze the information and data managed within their applications — with varying degrees of intelligence. This not only makes the software itself more attractive but also creates additional revenue streams: in addition to normal software usage fees, there are now additional charges for AI usage. This means not only does software usage itself become more efficient, but the information collected across the organization can be used more creatively, moving beyond the typical predefined dashboards or manual reporting mechanisms to unlock existing data assets.

### The Challenge: Fragmentation and Data Silos

The downside of this development, however, is a flood of AI agents that operate only on limited data silos. These agents are useful only to a very limited extent because they have visibility into just a small portion of available information. For highly specialized tasks, that may be sufficient. But the real value emerges through generalist agents that can access all relevant corporate data across systems. Only then can they identify connections that span multiple platforms.

Even the now commonplace copilots will increasingly benefit from organization-wide data — if only to avoid redundancies and inform users when a colleague has already completed similar work in another context.

A proliferation of isolated assistants operating on partial data is neither efficient nor sustainable. Google’s Agent-to-Agent Framework (and to some extent Anthropic's MCP protocol) attempts to address this fragmentation by standardizing cooperation between agents. But the fundamental challenge remains: ideally, AI agents operate across systems with free access to all internal data sources — and increasingly, to information outside the organization as well, such as professional social networks, rating platforms, or simply internet search results.

The first part is easy if the company successfully implemented a global data warehouse years ago or consolidated everything within a single cloud provider. But one has to ask: do we really want to use only their AI? Or should we retain the freedom to build our own AI agent or use one from a provider whose core expertise is in AI rather than in running a data warehouse or data lake?

### Orchestration as the Key to Efficiency and Control

This \"one warehouse rules it all\" mindset is unrealistic for most companies. In reality, organizations work with many different systems and depend on free access to the data managed by those systems. But that is not in the vendors' interest — allowing external agents access means losing potential AI‑usage revenue.

Some vendors have begun restricting or even blocking external AI access altogether — a conflict that directly contradicts the needs of users who expect to freely use their own data in agentic workflows. Time will tell how much customers are willing to tolerate.

In the long run, agentic AI platforms will prevail that enable cross‑system orchestration of AI tools and agents — independent of the software used in the organization, but built on top of the underlying data sources. These platforms allow flexible agent configuration, combine information from diverse sources at multiple abstraction levels, and integrate specialized sub‑agents when needed. This ensures the solution remains technology‑ and vendor‑agnostic, which is extremely beneficial when switching systems.

For example, if the company switches to a different CRM system, it doesn’t have to rely on the built‑in AI of the new tool, nor must all existing agents be rewritten. Only a few integration tools in the orchestration layer need adjustment to reroute access from the old system to the new one.

### Compliance, User Experience, and a Look Ahead

From a compliance perspective, an overarching orchestration layer is also valuable. It logs the complete decision‑making process of an agent — from requests to tools used, including parameters and retrieved data — making audits and traceability significantly easier. For example: which request was processed how, which tools were invoked with which parameters, which information was retrieved from where.

KNIME provides a practical example with its internal AI agent “Ask KNIME Anything”, which builds on a variety of tools that aggregate information from virtually all systems. They offer comprehensive insights into customer, user, and event data as well as information about employees, finances, and documentation. Importantly, these tools do not simply provide raw database access; they combine information across systems. For instance, the \"Customer Information\" tool provides curated insights from the CRM system combined with support‑system data and event‑database records.

Instead of having a CRM‑specific agent summarize only past sales activities, the agent can contextualize them with webinar participation, content from public presentations, financial reports from recent years, and internal forum posts.

This kind of data integration could be performed by AI, but that would make its job unnecessarily complicated, and many organizations already have these integration workflows in place. A scenario in which an agent repeatedly reconstructs fragmented information from different systems and their individual AIs is highly inefficient.

In the future, this will become even more interesting as agents autonomously create and refine data‑retrieval tools over time. Through continuous user feedback, they will increasingly model (deliberately avoiding the term \"understand\") the structure and relationships within the organization.

### Long-Term Benefits and Development Potential

How can one measure the value of a centralized AI orchestration layer compared to isolated, software‑specific AI tools? As is often the case, it's not straightforward. The actual benefit becomes apparent only over time: the more systems the agent can integrate, the more helpful it becomes.

No agent will solve all company problems from day one. But with user feedback, prompts and memory improve, making agents better with each iterative refinement. Initially, specialized agents may seem more powerful because they are optimized for a specific tool. But in the medium term, an agent with access to significantly more information will surpass these specialists.

It has become widely recognized that the introduction of AI does not immediately lead to a major efficiency leap — as with any new technology, there are initial friction losses. Implementing cross‑system agents is no different.

In the future, it will be interesting to see how tool vendors try to force customers to use their built‑in AI. Some providers have already begun blocking external AI access. For cloud vendors, this is not only a product decision but also a bandwidth issue: if every customer accesses their own data manually, that's manageable. But if each customer runs their own AI infrastructure with agents retrieving larger datasets every few minutes, it quickly becomes a challenge.

It is likely that in the future part of what vendors charge us will not be due to our own use of the tool, but due to our agents accessing and working with our data. And again — this reinforces the value of a centralized orchestration layer that can optimize data access, instead of relying on the efficiency of a vendor's AI.

A good strategy today is to follow a multi‑track approach. Use built‑in vendor agents initially and simultaneously develop a cross‑system AI orchestration structure. Before long, this layer can take over most specialist tasks. Observing usage patterns will show which specialized AIs are still actually used — and as with search engines in the past, the generalist will become the go‑to agent.

Unlike humans, agents have no problem stuffing more and more into their \"heads\". They never get tired of absorbing, processing, and using new information — and above all, they never forget or overlook anything.



