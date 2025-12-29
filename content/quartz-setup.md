---
title: Quartz setup
publish: true
---


### Seperate sites based on tags
I would like to be able to publish to two different sites, from one repo, based on the frontmatter in de md files. I want the following behaviour:

publish: true => public site  
publish: false | nothing => private site 

Right now the `draft` field works fine, but the private pages are now not build into a site. 

I could probably overload the domain with logic so that guests on pangolin get sent to the public site but with my sso creds I get sent to my private site.

* [Authoring-content](https://quartz.jzhao.xyz/authoring-content)

Diagram of what I would implement, adapted from [this](https://rakshanshetty.in/blog/quartz-obsidian-multi-site-publishing) diagram:

```mermaid
flowchart TD
    A[Private git Repository] --> B{Tag-Based <br/> Filter code}
    B -->|tags: published| C[Public Quartz Repo<br/>git submodule]
    B -->|tags: private, none| D[Private Quartz Repo<br/>git submodule]
    C --> F[Quartz Build]
    D --> G[Quartz Build]
    F --> H[Public Page]
    G --> I[Private Page]

    %% Annotation for public subset
    H -.->|Regular case| J[Final Page]
    I -.->|served when allowed pangolin account accesses it| J



    style A fill:#4C566A,stroke:#5E81AC,stroke-width:2px,color:#ECEFF4
    style B fill:#5E81AC,stroke:#81A1C1,stroke-width:2px,color:#ECEFF4
    style C fill:#D08770,stroke:#BF616A,stroke-width:2px,color:#ECEFF4
    style D fill:#D08770,stroke:#BF616A,stroke-width:2px,color:#ECEFF4
    style F fill:#8B6F5F,stroke:#7C5F4F,stroke-width:2px,color:#ECEFF4
    style G fill:#8B6F5F,stroke:#7C5F4F,stroke-width:2px,color:#ECEFF4
    style H fill:#6B8E7F,stroke:#5F7F70,stroke-width:2px,color:#ECEFF4
    style I fill:#6B8E7F,stroke:#5F7F70,stroke-width:2px,color:#ECEFF4
```

I don't quite know if it is possible to set such a default behaviour in pangolin without seeing the pangolin screen. I'd like the private page to only be triggered when it detects my SSO being loaded in the cookie.  

### Redo docker container
Right now my docker container is rather hacky, based on [this](https://github.com/shommey/dockerized-quartz) repo. I think I would also like to have one docker container serve both sites.
