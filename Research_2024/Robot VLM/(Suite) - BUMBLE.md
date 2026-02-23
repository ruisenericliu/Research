[https://arxiv.org/abs/2410.06237](https://arxiv.org/abs/2410.06237)
 
[https://itcanthink.substack.com/p/paper-notes-building-wide-mobile](https://itcanthink.substack.com/p/paper-notes-building-wide-mobile)
 
The paper of course has it’s own lit review - [you can check that out](https://arxiv.org/pdf/2410.06237) - so I’ll just share a few thoughts. **We’re seeing a concensus on what currently deployable systems look like**:

- Large vision-language models _on their own, without action information_ capture enough semantic knowledge to come up with reactive, high-quality, long-horizon plans
- While these don’t really understand actions per se, they’re a really incredibly capable part of a _system_ which does understand those actions (shades of [LLM-Modulo](https://arxiv.org/pdf/2402.01817) in a way)
- These can be used together with skill libraries (optionally learned; often, as in this case, not!) to perform a really wide variety of tasks. If learned, you could collect targetted data to improve these skills.

Compare to [OpenVLA](https://openvla.github.io/) and its ilk; we have models which try to do _everything_ all in one architecture, which requires a lot more actual robot data (most of the papers above require essentially none!)  
As it’s a [core interest of mine](https://itcanthink.substack.com/p/what-does-the-world-representation), and extremely relevant to how to actually make a system like this work in practice, let’s look at how that memory actually works.
 \> From \<[https://itcanthink.substack.com/p/paper-notes-building-wide-mobile](https://itcanthink.substack.com/p/paper-notes-building-wide-mobile)\>   
--------------------------------------------------