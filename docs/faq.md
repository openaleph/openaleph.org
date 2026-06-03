---
title: "FAQ"
# hide:
#   - toc
---

<section class="screen screen--bg-white" data-background-color="white" markdown>

# Frequently Asked Questions

## About OpenAleph

**What is OpenAleph?**

OpenAleph is an open source data search platform designed to help users explore large collections of documents, datasets, and structured data. It enables powerful full-text search, entity extraction, and relationship mapping. OpenAleph is specifically built for 'follow the money' type investigations across a variety of data sources.

**Who is behind OpenAleph?**

OpenAleph is maintained by the [Data and Research Center - DARC](https://dataresearchcenter.org/), with a focus on transparency, accessibility, and collaborative development. We welcome contributions and feedback from the community. Please refer to the  'Development and Contributions' section below for more details.

**Does OpenAleph rely on Google, Amazon or other big tech service providers?**

Not unless you want it to. OpenAleph is designed to run entirely on infrastructure you control and does not depend on any proprietary cloud services from Google, Amazon, or other major tech providers. You can deploy it on-premise or in a hosting environment of your choice, with full ownership of your data and operations. If you are interested in our managed OpenAleph services, you can [find more information here](https://openaleph.org/managed/).

**Why is OpenAleph open source?**

We believe transparency, collaboration, and accessibility are essential for building trustworthy tools for research and investigations. By keeping OpenAleph open source, we enable independent audits, foster community contributions, and ensure the platform remains free and adaptable for diverse use cases, from journalism and academic research to civil society work. If there's a feature you're missing, [get in touch](https://dataresearchcenter.org/contact/) to learn how you can sponsor its development!

**My friend from NEWSROOM XYZ found a document in OpenAleph, but I can't see it with my account – why not?**

OpenAleph is open source software that can be deployed by different organizations, each operating their own independent instance. If your colleague found a document in their organization's instance, it won't be visible to you unless that instance is public or you've been granted access. Each deployment controls its own data, user permissions, and visibility settings. They don't speak to each other (yet! See our roadmap linked below).

## Data and Usage

**What data formats can I import?**

OpenAleph supports a variety of file types, among them PDFs, Word documents, spreadsheets, emails (including PST and MBOX), and various structured formats like CSV. Since release 4.0 OpenAleph supports text extraction (and therefore full text search) for audio and video material of all kinds and languages. 

**Can I connect OpenAleph to other data sources?**

Yes. You can ingest data manually or through automated pipelines. Integration with external sources can be customized using the OpenAleph API. At DARC, the team behind OpenAleph, we run a [fleet of scrapers](https://dataresearchcenter.org/library/) that integrate with the platform. If you want to learn more about the data we're ingesting into our OpenAleph instances, please [reach out](https://dataresearchcenter.org/contact/).

**How does search and indexing work?**

Data is indexed using Elasticsearch, allowing for full-text search, entity extraction, and faceted filtering. Documents are processed with natural language tools to extract people, organizations, and other entities.

**Can I run it offline?**

In theory, yes. OpenAleph can be deployed and used entirely in an offline environment, which is useful for secure or air-gapped settings. It's main purpose, however, is to serve small teams over the internet. We take security very seriously, and there are a number of measures in place to make sure permissions are handled correctly and user authentication is secure.

## Security and Deployment

**How can I deploy OpenAleph?**

OpenAleph is meant to run on a server, it is not intended to be used on a personal computer. Installation guides and configuration instructions are available in our [documentation](https://openaleph.org/docs/).

**Can you host OpenAleph for me?**

Yes, at DARC we can set up [private OpenAleph servers](https://openaleph.org/managed/) for organizations of different sizes. Please [reach out](https://dataresearchcenter.org/contact/) to learn how we can help you.

**What data models does OpenAleph support?**

OpenAleph builds on the *FollowTheMoney&#32;*(FtM) data schema, which is specifically designed for anti-corruption investigations and used in many industry grade applications. You can learn more about FtM [here](https://followthemoney.tech/).

**Is there an API?**

Yes, OpenAleph provides a RESTful API for programmatic access to all core features, including document upload, search, and metadata queries. You can find the [API documentation here](https://redocly.github.io/redoc/?url=https://search.openaleph.org/api/2/openapi.json).

**Is OpenAleph secure for sensitive investigations?**

Yes, when properly configured. We recommend deploying OpenAleph behind a firewall with a properly configured reverse proxy, using HTTPS, setting up an intrusion detection system, and enabling role-based access control for multi-user setups. If you need help with this, [please reach out to us](https://dataresearchcenter.org/contact/).

## Development and Contribution

**Can I see the OpenAleph source code?**

Yes. OpenAleph is fully open source under the [MIT license](https://github.com/investigativedata/aleph#MIT-1-ov-file) and available on GitHub. You can inspect [the repository here](https://github.com/openaleph).

**How can I contribute?**

You can contribute by submitting issues, suggesting features, or opening pull requests. See our [contributor guide](https://github.com/openaleph/openaleph/blob/main/CONTRIBUTING.md) for details.

**What’s your roadmap?**

We share and discuss updates on upcoming features, priorities, and long-term goals in our Discourse forum. Feedback from users helps shape future development. You can view the [roadmap here](https://darc.social/t/openaleph-roadmap/25).

**Where can I report issues or bugs?**

Please use our [GitHub issue tracker](https://github.com/openaleph/openaleph/issues) to report bugs, request features, or ask technical questions.

**Are there professional support options?**

Yes, if you need enterprise-level support, integration help, or hosting services, [please get in touch](https://dataresearchcenter.org/contact/).

## OpenAleph and Aleph

**What’s the relationship between OpenAleph and the original Aleph project?**

OpenAleph is an independent fork of Aleph. While it builds on Aleph’s foundation, it is maintained separately and may evolve differently over time. Read [here](https://openaleph.org/blog/2025/03/OpenAleph-commits-to-the-commons/3510138e-16b3-4b5d-a06c-41af0aa2d517/) about the history of Aleph and OpenAleph.

**I’m already using Aleph - can I migrate to OpenAleph?**

Yes. OpenAleph maintains compatibility with most existing Aleph installations.

</section>
