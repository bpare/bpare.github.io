---
layout: post
title:  "Research: Visualization of Controversy in Wikipedia "
date:   2018-09-9 21:15:05 +0000
image: /assets/images/wikiPic.png
---
[PROJECT GITHUB](https://github.com/bpare/wikihistory-mirror)

__**This is an ongoing project that is being updated frequently.**__

#### Summary:


The purpose of this research is to detect and visualize controversy in collaborative versioned documents. We are currently focussing on an implementation using Wikipedia articles.


When an average user views a page on Wikipedia, they see what appears to be a static document. In actuality, Wikipedia articles are dynamic collaborations with deep and intricate edit histories. These histories contain vital data about the reliability and integrity of textual information.


Our high level definition of controversy is "meaning changing rapidly". We estimate this by calculating the total semantic distance a text segment travels over a specified time. In other words, we suggest that a text segment is controversial if it has been repeatedly modified in ways that significantly changes its meaning.

We utilize latent semantic analysis and diff algorithms to create a provenance graph which models the evolution of meaning in an article. More information about this can be found [here.](https://github.com/bpare/wikihistory-mirror/blob/master/CoDeVerT)

#### Visualization Work:

It is imperative that we are able to effectively and intuitively encode and convey this information such that it is useful to an average Wikipedia user.

We propose that multiple levels of granularity are necessary for this task.
A user should be able to identify:
1. which specific word segments are controversial.
2. which general topics in an article are controversial ( indicated by article sub-sections).
3. how the level of controversy in an article changes over time.

More information about the visualization and a small live demo can be found [here.](https://github.com/bpare/wikihistory-mirror/tree/master/visualization)
