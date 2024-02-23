---
layout: posts
title:  "Prioritization"
tagline: "Prioritizing with competing stakeholders"
date:   2024-02-13 19:13:27 -0500
categories: article
tags: ["Product Management"]
author_profile: true
author: Leigh Stewardson
header:
 teaser: https://images.unsplash.com/photo-1516321318423-f06f85e504b3
 overlay_image: https://images.unsplash.com/photo-1516321318423-f06f85e504b3
 caption: "Photo credit: [**Unsplash: John Schnobrich*](https://unsplash.com/@johnschno)"
 description: This article covers my exploration of Machine Learning Course.
---

## Background
Working at a SaaS startup can introduce unique prioritization challenges. You typically work with a small dev team, have many features to execute, on and have many stakeholders competing for their work. There are several ways to approach prioritization, but inevitably you will run into a situation where stakeholders and their work will have equal priority and you will have to make a call. 

In this article, I present my approach to prioritization and what to do when there is a stalemate. To illustrate this, I will use the following **FIFO** (first in first out) prioritized list of features for a fake SaaS Startup in the Growth stage:

{% include feature_table.markdown%}

## Approach
Let's start with two basic prioritization techniques, MoSCoW and BRICE, to get an idea of how to prioritize when there is a clear hierarchy.

### Basic Prioritization Methods
The following frameworks help Product Managers put metrics around feature requests and cumminicate prioritization. Not only do these frame works allow PdMs to create a roadmap (when things will get done), they can help your stakehodlers understand why their work is prioritized the way it is. 

#### MoSCoW
MoSCoW, or Must, Should, Could, Wont (right now) is an easy to uderstand framework that can quickly sequence your feature requests. *For simplicity,* I will bucket the requests in the following ways (Note: there are mutlple ways to buckets and they often depend on company goals):
- **Must Do:** 
  - A feature is broken and preventing usage of the app.
  - There is a deadline that is enforced by a contract or compliance.
  - The request is preventing another team from completing their work.
- **Should Do:**
  - A feature is broken, but there is a good workaround.
  - A feature is missing and pushing users to a competitor.
- **Could Do:**
  - The exeprience can be improved, but the feature is currently working as designed.
  - A feature is at the MVP stage, has clear feedback, and is ready for an itteration.
- **Wont Do (right now):**
  - No evidence of improvement to the experience and needs to be tested.

Below is how our feature list is prioritized with **MoSCoW**:
{% include feature_table_moscow.markdown%}

So, you may be wondering why I ranked these the way I did. Below is the reasoning for my buckets:
- **Sales:** There is a clearly defined deadline, and even if there wasn't, this feature might fall into the "Should" column.
- **Service:** One might argue that this could go in the "Should" column, but I dropped it to the "Could" colum because of the ability to rely on a human interface, the Service team. Though not a great exeprience for the team, which could lead to attrition, there is little to no impact for the user. 
- **Marketing:** This one is interesting. It sounds good, but if you dig deeper, the ranking system is problematic. If you are buying a carton of milk FIFO (first in first out) works. However, if you are shopping for non-perishable items, there are other variables that influence your decisions. You will notice sites like Amazon don't just rank their products, they highlight shiping time, ratings, and savings/price (the things that would influence a decision). Additionally, they use media/advertising at the top of the page to promote brands. I put this one in "Won't (Right Now)" because I don't believe that simply putting our partners at the top of a list will achieve the goal of getting more sales for them and adding a ranking system to our data will be hard to manage and become quickly outdated. The idea needs more research.
- **Developers:** The poor development team rarely gets love in these situations. As  SaaS products grow and teams evolve, technical debt accumulates. This can lead to slow performace for the product and slower development times and poor experiences for the developers, which could lead to attrition.

MoSCow becomes more complicated when you start asking questions such as, "impact and/or experience for who?" Should a product manager only focus on exepriences for the user? Or should they also consider exepriences for the staff? Additionally, should a product manager only be concerned with getting features out, or should they also be looking at performance and business goals like promoting preferred vendor products to improve partnerships. To address these concerns, we'll next look at BRICE.

#### BRICE
BRICE (or RICE if you choose to take out the business value) is an acronym for Business Value (1-3), Reach (0-1), Impact (0-1), Confidence (0-1), Effort (1-4). The formula is simple: **(B x R x I x C)/E**. It measures the features overall importance breakes it down to units of the over all effort it takes to complete. If the overall importance/effort of feature A is 6/1 and feature be is 6/3, feature A gets done first, as it has a higher score. (Note: this formula emphasizes Busines Value and under values projects with a high Effort. In this case, a start up that wants to get impactful work out quickly, the formula makes sense. The emphasis, however, can be modified by changing the range for the value.) 

Let's look at what our ranking looks like with our new framework to think this through. To calculate this, we'll need the fake company's very simple, ranked OKRs for the year (usually this is done quarterly):

**Key Objective:** Grow user base
- **Result:** 5x customers by End of Year
- **Business Value:** 3
**Key Objective:** Improve partner profit margins
- **Result:** Increase partner product engagement by 30%
- **Business Value:** 2
**Key Objective:** Grow development team
- **Result:** Decrease atrition in by 20%
- **Business Value:** 1

With this new perspective, our ranking changes a bit:
{% include feature_table_brice.markdown %}

The BRICE (with the appropriate emphasis) seems to work. However, there is other things to consider, before we take these features in order of BRICE. 

### Tradeoffs
Good communication with your stakeholders is key to prioritization. Let's take the feaure request from the Servicing team. Their goal is to reduce the amount of time they take to service a client. Let's assume all clients call into the Service team to get advice on products and manage their billing and invoices. The team believes that integrating their CRM with financial and product data from the the SaaS product will improve their times to service a customer. But notice, the Sales feature, and the marketing feature, which are self-service, also achieve a percentage of these goals by reducing the amount of requests the Service team recieves. Developing 4 features is time consuming and the company is concerned about getting the work out quickly. 

This is where your influence and communication become crucial. Often requests can be made in isolation, without the knowledge of another team's request. The approach here may be to cut the Service feature request and revisit their needs once the other features are released.

### Prioritizing for Development
Each feature has a software development lifecycle (SDLC) that we can leverage:
- Discovery/Plan (assumption: Discovery is performed by the Product Team)
- Design
- Development/Implement (assumption: Development includes testing)
- Deploy (happens every 2 weeks)

Depending on the feature, each phase can take a different length of time. Here is the revised list (minus the Servicing request) and the length of time for each phase in the SDLC. This is where your partnership with you development team is crucial. They can provide you with high-level estimates and help you prioritize in a way which keeps the development team working efficiently.

{% include feature_table_sdlc.markdown %}

## Reults
The final prioritization looks like this:

{% include feature_table_final.markdown %}