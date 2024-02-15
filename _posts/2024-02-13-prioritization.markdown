---
layout: post
title:  "Prioritization"
tagline: "Prioritizing with competing stakeholders"
date:   2024-02-13 19:13:27 -0500

category: article
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

In this article, I present my approach to prioritization and what to do when there is a stalemate. To illustrate this, I will use the following list of features for a fake SaaS Startup:

{%- assign features = site.data.prioritize -%}
<table>
    <thead>
        <td>Org Team</td>
        <td>Fetaure</td>
        <td>Goal</td>
        <td>Deadline</td>
    </thead>
    <tbody>

        {% for feature in features%}
        <tr>
            <td>
                {{feature.org}}
            </td>
            <td>
                {{feature.feature}}
            </td>
            <td>
                {{feature.goal}}
            </td>
            <td>
                {{feature.deadline}}
            </td>
        
        </tr>
        {%endfor%}
    </tbody>
</table>

## Approach


### Basic Prioritization Methods


### Competing Stakeholders and Features
There are several ways you can manage competing OKRs and organizational teams. You can prioritize in the following ways:

- **Linear:** Have the competing stakeholders rank and then complete features end-to-end and then move on to the next.
    - Benefit: Keeps the development team focused.
    - Drawback: Some teams have to wait a long time to get their work done, and teams that are not client facing, like the developer team, keep getting pushed back.
- **Ratios:** Split your teams into smaller pods, working on multiple team features. You can do a 50/50 split or a 30/70 split depending whether you want to put more emphasis on one feature.
    - Benefit: Engages more stakeholders
    - Drawback: The work get's done slower
- **Pivots:** Split the year and work on OKR's sequetially, pivoting to the next after MVP is complete.
    - Benefit: This can work well with early startups, 
    - Drawback: Sacrificing quarterly progress on one OKR. You must make sure you can address multiple OKRs in a year.

## Reults

