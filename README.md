<div align="center">
  <img src="/img/logo.jpg" alt="Logo" width="400">
</div>

# TransAgents: Multi-Agent for Translating Ultra-Long Literary Texts

<div align="center">
<img src="https://img.shields.io/badge/License-CC%20BY%204.0-green.svg" alt="License">
<img src="https://img.shields.io/github/stars/minghao-wu/transagents?color=yellow" alt="Stars">
<img src="https://img.shields.io/github/issues/minghao-wu/transagents?color=red" alt="Issues">

<!-- **Authors:** -->

**_¹ [Minghao Wu](https://minghao-wu.github.io/), ³ [Jiahao Xu](https://www.linkedin.com/in/jiahao-xu-539623187) ² [Yulin Yuan](https://fah.um.edu.mo/yulin-yuan), ¹ [Gholamreza Haffari](https://users.monash.edu.au/~gholamrh), ³ [Longyue Wang<sup>*</sup>](http://www.longyuewang.com/)_**

<!-- **Affiliations:** -->

_¹ Monash University, ² University of Macau, ³ Tencent AI Lab_

📝 [**Paper**](https://arxiv.org/abs/2405.11804) :technologist: [**Demo**](http://www.transagents.ai) 🗂️ [**Data**](/outputs) 📽️ [**Video**](https://www.youtube.com/watch?v=lB-gPHax4ow)

_<sup>*</sup>Longyue Wang is the corresponding author: [vinnlywang@tencent.com](mailto:{vinnlywang@tencent.com)_
</div>


We introduce a novel multi-agent framework based on large language models (LLMs) for literary translation, implemented as a company called TransAgents, which mirrors traditional translation publication process by leveraging the collective capabilities of multiple agents, to address the intricate demands of translating literary works. 

<!-- <iframe width="560" height="315" src="https://youtu.be/lB-gPHax4ow" title="TransAgents Demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->

<!-- [![IMAGE ALT TEXT](http://img.youtube.com/vi/lB-gPHax4ow/0.jpg)](http://www.youtube.com/watch?v=lB-gPHax4ow "Video Title") -->


<!-- <video src="/img/TransAgents_demo.mp4" width="320" height="240" controls></video> -->

<!-- <video width="320" height="240" controls>
  <source src="/img/TransAgents_demo.mp4" type="video/mp4">
</video> -->

<!-- <p align="center"> <img src="/img/TransAgents_demo.mp4" width="700px"> </p> -->

## News 🤩🤩🤩

- \[27/06/2024\] 🚀🚀🚀 **TransAgents Demo Video** is ready!
- \[27/06/2024\] 🚀🚀🚀 **TransAgents Demo System** is released at http://www.transagents.ai !
- \[12/06/2024\] 🚀🚀🚀 The translation outputs given by **TransAgents**, **reference**, and **gpt-4-1106-preview** are released!
- \[25/05/2024\] 🚀🚀🚀 **Stay tuned for updates!** We will release data and demo.

## Video

https://github.com/minghao-wu/transagents/assets/5949882/ebb175f0-5a57-46a7-a252-5b94f3079de7


## Translation Outputs

You can find the translation outputs provided by **TransAgents**, **reference**, and **gpt-4-1106-preview** in the [outputs](https://github.com/minghao-wu/transagents/tree/master/outputs) folder.

```
outputs
├── TransAgents
├── gpt-4-1106-preview
├── reference
└── source
```
* **TransAgents**: Our multi-agent translation system.
* **gpt-4-1106-preview**: Translations generated by `gpt-4-1106-preview` on a chapter-by-chapter basis.
* **reference**: Translations provided by professional human translators, referred to as `Reference 1` in our paper.


## Case Study

In this section, we present a few case studies on cultural adaptation, global consistency, and content omission, highlighting our approach's strengths and weaknesses. We also incorporate insights from interviews with two experienced professional translators.

### Cultural Adaptation

In Chinese, job titles are typically placed before a person's name, whereas in English, they usually come after.

|                    | Content                                                                                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Original Text      | 罗德抬起头来，正好看见一个中年男子推门走进来，他穿着冒险者的皮甲，一头鲜红的长发随意的向后梳理着， 看见罗德，男子微微一笑。 “你好，先生，我是星月佣兵团的团长，卡特。”                                                                                                                         |
| Reference 1        | Rhode looked up and saw a middle-aged man pushing the door open. He wore an adventurer's leather armor and casually combed back his long red hair. The man smiled when he saw Rhode.  **"Hello, sir. I am the Guild Leader of the Star Moon Mercenaries, Carter."**                            |
| gpt-4-1106-preview | Rhode looked up and saw a middle-aged man entering through the door. He was dressed in an adventurer's leather armor, with a head of bright red hair casually combed back. Seeing Rhode, the man smiled slightly.  **"Hello, sir, I am the leader of the Star Moon Mercenary Group, Carter."** |
| TransAgents        | Rhode looked up to see a middle-aged man entering. The man was dressed in the leather armor typical of adventurers, his fiery red hair casually swept back. Spotting Rhode, the man offered a modest smile.  **"Hello, sir. I am Carter, the leader of the Star Moon Mercenary Corps."**       |

### Global Consistency

|                    | Content                                                                                                                                           |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Original Text      | 第1906章 不思量，自难忘（十二）[OMITTED] 第1907章 不思量，自难忘（十三）[OMITTED]                                                                 |
| Reference 1        | Chapter 1906: Unforgettable Memories (12) [OMITTED] Chapter 1907: Unforgettable Memories (13) [OMITTED]                                           |
| gpt-4-1106-preview | Chapter 1906: **It's Hard to Forget Without Thinking (Twelve)** [OMITTED] **Chapter 1907: Without Intention, Unforgettable (Thirteen)** [OMITTED] |
| TransAgents        | Chapter 1906: Without Intention, Unforgettable (Twelve) [OMITTED] Chapter 1907: Without Intention, Unforgettable (Thirteen) [OMITTED]             |
### Content Omission

Both **gpt-4-1106-preview** and **TransAgents** exhibit significant issues with content omission.

|                    | Content                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Original Text      | 她招来女仆带叶琛和程安雅下去洗漱，小奶包虽然很想跟着去， 不过他还是留在这里，白夜作势就要揍人了，小奶包赶紧拉着他的袖子。 “白夜，你能有办法救我爹地妈咪吗？”小孩子的眼睛很亮，如两颗黑葡萄镶嵌在白嫩的脸上，充满了期盼，仿佛白夜一摇头，他眸中的亮光就会黯淡了。杰森一把揪起小奶包抱在怀里，豪气万千， “宝贝儿，你放心，小白死人都能救，别说活生生的人了，你担心个屁，有空过来给我轰了黑手党的防护。”“刚是谁质疑白夜的医术的？”黑杰克对此表示疑惑， 杰森一掌过去，他敏捷闪开。小奶包被大高个子抱着，异常的纠结，踢了踢杰森，“放我下来。”“老子也想要这么个儿子，宁宁，你来当我儿子吧？老子垂涎你很久了。”杰森湛蓝色的眸迸发出澎湃的光芒，活似小奶包就是一块肥肉。众人，“......”白夜微笑说道，“杰森，你中文再让你妈教教，别老说长官不会用词语，你也好不到哪儿去。”“我和长官不是一个级别的好吧？”杰森很不满意有人把他和长官联系在一起，所谓官寇不一家，这是原则问题。小奶包挣扎一下，杰森放他下来，小奶包问道：“白夜......”“宁宁，等我给他们做过检查才能确定，你先别着急。”白夜说道，揉揉小奶包的头， “我保证会尽全力。”                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Reference 1        | She called a maid to take Ye Chen and Cheng Anya downstairs to freshen up. Little Cutie really wanted to go with them, but he stayed behind as Bai Ye seemed ready to start fighting someone, so Little Cutie quickly grabbed his sleeve. "Bai Ye, can you save my Mommy and Daddy?" The child's eyes were bright, like two black grapes embedded in his fair face, full of expectation. It seemed that if Bai Ye shook his head, the light in his eyes would dim. Jason grabbed Little Cutie and hugged him fiercely, feeling quite confident. "Darling, don't worry. Little Bai can save even the dead, not to mention living people. Stop worrying about them and come help me take down the Mafia's line of defense when you have time." "Who was questioning Bai Ye's medical skills just now?" Black Jack expressed doubt about this. Jason threw a punch at him, but he agilely dodged it. Being carried by the tall man, Little Cutie felt extremely conflicted and kicked Jason. "Put me down." "I also want a son like you. Ningning, will you be my son? I've been coveting you for a long time." Jason's azure eyes burst with enthusiasm as if Little Cutie was a rare piece of jewelry. Everyone was speechless.... Bai Ye smiled and said, "Jason, let your mother help you improve your Chinese. Don't always complain that the commander doesn't know how to use words. You're not much better." "I'm not on the same level as the commander, okay?" Jason was very dissatisfied that someone had compared him to the commander. It was a matter of principle that officials and bandits were not on the same side. Little Cutie struggled a little, and Jason put him down. Little Cutie asked, "Bai Ye...." "Ningning, don't worry. I'll check them up before making a conclusion." Bai Ye said, rubbing the head of Little Cutie, "I promise I will do my best." |
| gpt-4-1106-preview | She summoned the maids to take Ye Chen and Cheng Anya to wash up. Xiao Nai Bao wanted to follow, but he stayed here, as Bai Ye looked like he was about to beat someone up, so Xiao Nai Bao quickly grabbed his sleeve. Bai Ye, can you save my daddy and mommy? Xiao Nai Bao's eyes were bright, like two black grapes embedded in his tender face, full of hope, as if the light in his eyes would dim if Bai Ye shook his head. Jason grabbed Xiao Nai Bao and hugged him, full of pride, "Baby, don't worry, Xiao Bai can even save the dead, let alone the living. Stop worrying about nothing, come help me bombard the mafia's defenses when you're free." Who was questioning Bai Ye's medical skills just now? Black Jack expressed doubt, and with a palm strike, Jason swiftly dodged. Xiao Nai Bao struggled a bit, and Jason put him down. Xiao Nai Bao asked, "Bai Ye..." Ningning, wait until I've examined them before I can be sure, don't be anxious, Bai Ye said, ruffling Xiao Nai Bao's head, "I promise to do my best."                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| TransAgents        | At her behest, maids ushered Ye Chen and Cheng An Ya away for a bath. Xiao Naibao, torn between following and staying, ultimately remained as Bai Ye appeared poised for a scuffle. Tugging at Bai Ye's sleeve, Xiao Naibao looked up at him with hopeful eyes. "Bai Ye, is there a way to cure my daddy and mommy?" "Ning Ning, let me conduct a thorough examination first. Stay calm," Bai Ye soothed, patting the boy's head. "I'll do everything in my power."                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

### Comments from Professional Translators

|              | Comments                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Translator A | TransAgents's translation style is similar to that of a novel, with sophisticated wording and personal flair. Despite some omissions, it makes the text more concise and effectively conveys the original text's mood and meaning. Reference 1 and gpt-4-1106-preview's translations are more conventional, adhering strictly to the original text word for word. However, gpt-4-1106-preview's translation is more grammatically precise than Reference 1's, and its wording is slightly better, making its translation aesthetically superior to Reference 1's but still not reaching the literary expressiveness of TransAgents. From their translation habits, TransAgents appears to have a solid foundation in English, Reference 1 seems to rely on machine translation, and gpt-4-1106-preview behaves like a standard, rule-abiding translator. |
| Translator B | TransAgents's translation breaks away from the constraints of the original language, using the language freely with ample additions and expansions, and the choice of vocabulary also demonstrates a deeper understanding of the language. Reference 1 remains faithful to the original text, translating directly and succinctly without adding personal interpretations. gpt-4-1106-preview's translation style is similar to Reference 1's, both strictly adhering to the original without much personal interpretation or embellishment. Overall, TransAgents's translation shows the greatest depth and sophistication, followed by Reference 1, while gpt-4-1106-preview performs most ordinarily among the three.                                                                                                                                                                                              |

## Citation

```bibtex
@article{wu2024perhaps,
  title={(Perhaps) Beyond Human Translation: Harnessing Multi-Agent Collaboration for Translating Ultra-Long Literary Texts},
  author={Wu, Minghao and Yuan, Yulin and Haffari, Gholamreza and Wang, Longyue},
  journal={arXiv preprint arXiv:2405.11804},
  year={2024}
}
```