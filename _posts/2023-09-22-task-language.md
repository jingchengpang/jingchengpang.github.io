---
title: "Natural Language Instruction-following with Task-related Language Development and Translation"
date: 2023-09-22
permalink: /posts/2023/09/task-language
tags:
  - reinforcement learning
  - language development
  - instruction-following
---

This blog introduces [our work](https://arxiv.org/abs/2302.09368) that will appear in NeurIPS 2023. 
We focus on 

Abstract
======
Natural language-conditioned reinforcement learning (RL) enables agents to follow human instructions. Previous approaches generally implemented language-conditioned RL by providing the policy with human instructions in natural language (NL) and training the policy to follow instructions. In this is outside-in approach, the policy must comprehend the NL and manage the task simultaneously. However, the unbounded NL examples often bring much extra complexity for solving concrete RL tasks, which can distract policy learning from completing the task. To ease the learning burden of the policy, we investigate an inside-out scheme for natural language-conditioned RL by developing a task language (TL) that is task-related and easily understood by the policy, thus reducing the policy learning burden. Besides, we employ a translator to translate natural language into the TL, which is used in RL to achieve efficient policy training. We implement this scheme as TALAR (TAsk Language with predicAte Representation) that learns multiple predicates to model object relationships as the TL. Experiments indicate that TALAR not only better comprehends NL instructions but also leads to a better instruction-following policy that significantly improves the success rate over baselines and adapts to unseen expressions of NL instruction. Besides, the TL is also an effective sub-task abstraction compatible with hierarchical RL.



Method
======
The following figure depicts the overall framework of TALAR. There are three parts in the figure. 
(a) Overall training process: The Task Language (TL) generator develops TL
via playing a referential game with a receiver, and the translator translates natural language (NL) to TL. 
(b) Network architecture of the TL generator. 
(c) Network architecture of the translator. The number of predicate
arguments and networks can be adjusted according to the task scale.

<img src="/images/posts/task_language/framework.png" style="display: block; margin: auto;" />


Main results
======
<img src="/images/posts/task_language/main_results.png" style="display: block; margin: auto;" />



Performance
======

The following video presents the performance of different agents under a same instruction: Can you
 open the microwave door for me? The baseline method is one-hot. TALAR agent behaves more flexibly and quickly.

<table>
  <tr>
    <td>
<video id="video" controls="" preload="none" width='100%'>
<source id="mp4" src="/images/posts/task_language/baseline_micro.mp4" type="video/mp4">
</video>      
<figcaption style="text-align: center;">Baseline</figcaption>
    </td>
    <td>
<video id="video" controls="" preload="none" width='100%'>
<source id="mp4" src="/images/posts/task_language/ours_micro.mp4" type="video/mp4">
</video>   
      <figcaption style="text-align: center;">TALAR</figcaption>
    </td>
  </tr>
</table>
