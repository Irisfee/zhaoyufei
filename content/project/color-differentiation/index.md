---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Efficient way of the brain for resolving similar memory interference"
summary: "An fMRI study with MVPA and SEM analysis that reveal how our brains actively reduce interference caused by similarity between memories to achieve for better memory performance."
tags: 
- fMRI
- MVPA
- Python
- R
categories: []
date: 2021-02-21T15:10:03-08:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: "Center"
  preview_only: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: Paper
  url: media/publications/papers/JN2021.pdf
  icon_pack: fas
  icon: file-pdf
# - name: Code
#   url: https://github.com/Irisfee/roistats/
#   icon_pack: fab
#   icon: github

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

The paper is published on Journal of Neuroscience: https://www.jneurosci.org/content/41/13/3014.full#sec-27

## Background

Given the vast number of memories that humans store, overlap between memories is inevitable. The similarity between memories could cause confusion when trying to retrieve a certain piece of memory. For example, one student in your stats class is called Mario, while another student in your algorithm class is called Wario. These two guys not only have look similar but also tend to dress in a similar style. You may accidentally call Mario, Wario. However, after several weeks of classes, you can definitely tell Mario and Wario apart because your brain develop some strategies to mange the competition in memory. 

Evidence from recent neuroimaging studies hints at the idea that memory representations are distorted as an adaptive response to interference. Namely, several studies have found that, when similar events are encoded into memory, this triggers a targeted exaggeration of differences in patterns of activity. Yet, a critical limitation of these studies is that the feature dimensions along which memories move are underspecified. That is, do changes in neural representations correspond to changes in the information content of memories?

Here, we tested whether interference between highly similar memories triggers adaptive distortions in memory representations and corresponding behavioral expressions of memories. Our motivating theoretical perspective was that subtle differences between similar memories are prioritized and exaggerated to reduce the potential for interference.

![Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled.png](Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled.png)

## Controlled experiment design

In order to answer the question, we used color as the memory feature to probe since that color is 1. continuous and 2. can be reported by participants.

Specially, we used a 2-day procedure in which participants received extensive behavioral training on face-object associations on day 1 and then returned on day 2 for additional behavioral training, followed by an fMRI session, and finally a behavioral color memory test. A critical feature of our design is that we held color similarity between pairmates constant (24 degrees apart), but we included a **competitive** and **noncompetitive condition**. In the competitive condition, pairmate images corresponded to the same object category (e.g., two beanbags of slightly different colors). In the noncompetitive condition, pairmates corresponded to distinct object categories (e.g., a pillow and a ball of slightly different colors). Thus, in both conditions, the pairmates were 24 degrees apart in color space; but, for the competitive condition, color was the only feature dimension on which the pairmates differed.

![Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%201.png](Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%201.png)

![Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%202.png](Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%202.png)

## Result

### Behavioral performance analysis

As for the result, first we found that participants exaggerated the color difference between the two similar objects for only for the competitive condition, not for the non-competitive condition. Moreover, the greater memory exaggeration was associated with lower memory interference (indicated by the better associative memory performance). See figures below.

![Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%203.png](Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%203.png)

### Neural imaging data (fMRI) analysis

**Image Data processing**

After pass the fMRI through the basic preprocessing pipeline, we smoothed the data with a 1.7 mm FWHM Gaussian kernel and high pass filtered at 0.01 Hz to increase signal-to-noise-ratio (**SNR**). We modeled data with “least-squares separate” method. With this method, each item was estimated in a separate GLM as a separate regressor while all remaining items were modeled together with another regressor. The six movement parameters and framewise displacement were included in each GLM as confound regressors. This resulted in t maps that were used for the multivariate pattern analysis (**MVPA**).

![Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%204.png](Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%204.png)

**Neural representation of color information during recall**

As predicted, the greater relevance of color information in the competitive condition resulted in stronger representation of color information during recall, despite the fact that participants had not been explicitly oriented to color information in any way by this point of the experiment (the critical behavioral test of color memory occurred after fMRI scanning).

![Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%205.png](Adaptive%20Memory%20Distortions%20Are%20Predicted%20by%20Featu%20ef556ea14bc84d6ab287f06f059abe81/Untitled%205.png)

**Neural measures of pairmate similarity predict color memory bias**

Moreover, we found only for the competitive condition, the more dissimilar vIPS activity patterns were when recalling pairmates, the greater the color memory repulsion effect for those pairmates. A mediation analysis performed at the level of individual pairmates also revealed that the relationship between vIPS dissimilarity and associative memory accuracy was significantly mediated by signed color memory distance, consistent with the interpretation that vIPS dissimilarity reflected the degree of color memory repulsion, which in turn was associated with better associative memory accuracy (lower interference).

## Conclusion

Here, we show that competition between similar memories triggers biases in their neural representations and corresponding behavioral expressions. Specifically, we demonstrate that subtle, diagnostic differences between events were exaggerated in long-term memory and that this exaggeration reduced interference. Critically, these behavioral expressions of memory distortion were predicted by adaptive, feature-specific changes to memory representations in parietal cortex.


{{< tweet 1363911724060000258 >}}

