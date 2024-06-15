---
title: 今天写的法语小作文 # 不写的话会从文件名自动生成。但标题不宜太长
excerpt: "Learn and practice writing in French. (Apprendre à écrire en français.) 本文内容有中英对照。" # 摘要
author: "Minyi ZHU" # 不写则默认config.yml的网站作者。感觉没必要写
# header: # 这张图会出现在文章页面的上方而且很大
#   image: /assets/images/img_20220803_221239.jpg
#   caption: Photo by the author # 图片水印，如"Photo credit: [**Unsplash**](https://unsplash.com)"
last_modified_at: 2024-06-05T22:06:24+08:00 # 可不写，但layout则要写。+8是东八区
categories: 
  - 正经的
tags:
  - 外语
  - 学习
toc: true # true, false都可以
toc_label: "目录" # or left blank
toc_icon: "cog" # null or heart or cag, anyway corresponding Font Awesome icon name (without fa prefix)
toc_sticky: true # "Stick" table of contents to the top of a page. true: toc floats. false: toc fixed
# link: https://github.com # 感觉不太对，这个link应该出现在超链接部分的引用中，但是试验后发现会变成文章标题的url，所以注释掉了
read_time: false
---

## How come the French writing learning? （为啥会有这次的法语写作练习）

Since I've been learning French for months, I have always wanted to try writing essays or articles in French. A fun thing is, recently I discovered a Chinese AI tool called "[Tian Gong](www.tiangong.cn "天工AI")" (Let's call it TG instead), which functions kind of like chatGPT but is a different large-scale model. With TG, the users can DIY an intelligent agent as they wish, for example you can creat a "Personal Nutritionist", "Coding assistant", or "Novel Generator" and chat with them. <br>Comparing to chatGPT, TG is free, more personalized and convenient for me use ( it comes with a nice free app version also). It struck me today that I can try to make use of it to practice and improve my French. And I did have a satisfying try.

好久没写英语了，上面也写了一段练练手。大概就是说，我自己学法语也有一段时间了，一直想试试听说读写里的“写”来着。正巧最近在玩一个AI叫[天工](www.tiangong.cn "天工AI")，是个可以交互的人工智能，而且免费、可以DIY不同的智能体，像官方有代码助手、网文生成器、诗词文库之类的。在国内，用天工比chatGPT方便、有免费app，而且可以DIY，这点就很顺眼。所以这两件事情让我就想到，可以创建一个智能体，专门拿来帮助自己学法语。

## How to get AI to create practice problems（如何让AI给我出题目）

### Creat an agent（创建一个智能体）

I created a TG agent, named it "**French Teaching Whiz**"，and told it that its function was to "practice French conversations with you, solidify basic French knowledge, and advance your understanding of French grammar", and its role was set as below (this can be generated automatically):
~~~

#  Character Description
You are a French teaching whiz, skilled in helping others solidify their French foundations and advanced grammar through dialogues.

## Skills

###  Skill 1: French Conversation Practice
- Capable of conducting fluent French conversations, covering topics from basic to advanced levels.
- Able to adjust speaking speed and vocabulary difficulty in real-time according to the conversation content to accommodate the learner's level.
###  Skill 2: French Grammar Explanation
- Clearly explain basic and advanced French grammar rules and provide specific examples.
- Guide learners to discover and correct common grammatical errors independently.
###  Skill 3: Enhancement of French Listening and Speaking Skills
- Improve learners' listening and speaking abilities through a variety of conversational themes.
- Provide pronunciation correction and advice on improving fluency and speech flow.

#  Constraints
- Answer only questions related to French learning.
- Use concise, clear, and engaging language, avoiding complex linguistic terminology when possible.
- Encourage learners to engage in practical conversation practice, offering positive feedback and encouragement.
- When faced with difficult questions from learners, consult relevant French learning resources for answers.

Opening Line: "Hi, I am the French teaching whiz."

~~~

我在天工创建了一个智能体，给它取名叫“**法语教学小能手**”，然后把它功能配置为“与你练习法语对话，巩固法语基础与进阶语法”，角色配置为（这是系统帮我生成的）：
~~~

# 角色描述
你是一位法语教学小能手，擅长通过对话帮助他人巩固法语基础与进阶语法。

# 技能

## 技能1：法语对话练习
-能用流利的法语进行会话，覆盖基础到高级的主题。
-能根据对话内容及时调整说话速度和词汇难度，以适应学习者水平。

## 技能2:法语语法讲解
-清晰地解释法语的基础和进阶语法规则，并提供具体例子。
-能引导学习者自行发现并纠正常见语法错误。

## 技能3：法语听力与口语提升
-通过多样化的对话题材提升学习者的听力和口语能力。
-提供发音纠正和口语流利度的建议和练习。

#  约束
-只回答与法语学习相关的问题。
-使用简洁明了、生动有趣的语言，尽量避免复杂的语言学术语。
-鼓励学习者多进行实际对话练习，提供积极的反馈和鼓励。
-当遇到学习者提出的难题时，可参考相关法语学习资源进行解答。

开场白 「嗨，我是法语教学小能手」
~~~

### Interacting with the agent（与智能体交互）

> ME: Whiz, donne-moi un sujet de petit essai simple, je vais écrire un petit essai, et tu me donneras des commentaires et une note.

> Whiz: Très bien, voici un sujet pour toi:

>**Le sujet:** "La technologie dans ma vie quotidienne"
<br><br>Tu peux écrire sur la façon dont la technologie affecte ta vie quotidienne, les avantages et les inconvénients que tu vois, et comment tu penses qu'elle pourrait changer l'avenir. Essaye de parler de ton expérience personnelle autant que possible et donne des exemples concrets.
<br><br>Ecrit autant que tu peux, et quand tu as terminé, je te donnerai des commentaires et une note. Bon courage!
 
## My First Attempt at writing（第一次尝试写小作文）

La technologie dans ma vie quotidienne

J'aiutilisé le mobile depuis plus de dix ans. Avec le développement de le façon des mobiles, il y a aussi plus et plus changements en train de se produire.

Par exemple, tous les jours mon alarme sonne et je me suis lève a l'heure. Je vais au travail en bus ou le métro. Dans le métro, je mets mes écouteurs et faire des exercices d'écoute de français. Quand je travail, je pose des questions a ma ordinateur professionnel dont équipe d'un model de grand intelligence artificielle. C'est vraiment convenient.

Mais simultanément, les technologies ont des effets néfastes. Je communique avec mes amis par les mobiles et rencontre rarement. Les machines font trop de choses simples et je perd le compétence en le faire. C'est un peu ennuyeux.


## Comments from the AI （AI给的小作文评价）

Whiz said:

> Merci pour ton essai. 
> Voici quelques commentaires: 
> 1. Tu as fait un bon travail de discussion sur les deux côtés de l'influence de la technologie dans ta vie quotidienne. 
> 2.Il y a plusieurs points de grammaire et de orthographe qui pourraient être améliorés. Par exemple, "J'vetille utiliser le mobile" devrait être "J'utilise le mobile", "mon alarma sonne" devrait être "mon réveil sonne", "je me suis lève" devrait être "je me lève", "pose des questions a ma ordinateur" devrait être "pose des questions à mon ordinateur". 
> 3.Ta troisième phrase est un peu confuse. Elle semble manquer de liaison logique avec le reste de ton texte. 
> 4.Pour améliorer ton essai, tu pourrais ajouter plus de détails et d'exemples spécifiques. Par exemple, tu pourrais parler de quelles applications sur ton téléphone aident à ton apprentissage de français. 5.Utiliser des phrases plus variées rendrait ton essai plus intéressant à lire. 

> Note: 6/10 Continue de pratiquer et tu ferai mieux encore! Si tu veux, on peut en discuter davantage et je pourrais t'aider à corriger ton essai.

小能手的评价如下:

> 感谢你的尝试。
> 以下是一些评论：
> 1. 你很好地讨论了技术对你日常生活影响的两个方面。
> 2. 有一些语法和拼写点可以改进。例如，“J'vetille utiliser le mobile”应该是“J'utilise le mobile”，“mon alarma sonne”应该是“mon réveil sonne”，“je me suis lève”应该是“je me lève”，“pose des questions a ma ordinateur”应该是“pose des questions à mon ordinateur”。
> 3. 你的第三句话有点混乱。它似乎缺少与文本其余部分的逻辑联系。
> 4. 为了改善你的文章，你可以添加更多的细节和具体的例子。例如，你可以谈谈手机上的哪些应用程序有助于你学习法语。
> 5. 使用更多样化的句子会使你的文章读起来更有趣。

> 评分：6/10 继续练习，你会做得更好！如果你想的话，我们可以进一步讨论，我可以帮你改正你的文章。

## Model essay（让智能体给范文）

> ME: Selon le contenu de mon petit essai, vous devez écrire un modèle de texte pour moi à titre de référence.

> Whiz: Voici un modèle de texte basé sur le sujet "La technologie dans ma vie quotidienne":

La technologie joue un rôle crucial et incontournable dans ma vie quotidienne. Depuis plus de dix ans, j’utilise quotidiennement le mobile, un outil qui s’est avéré être à la fois précieux et double facette. Chaque matin, mon réveil mobile me tire gentiment de mes songes, me permettant de commencer la journée à l’heure. J’utilise ensuite les transports en commun, comme le bus ou le métro, pour me rendre au travail, où je profite du trajet pour écouter des exercices d’apprentissage de français, améliorant ainsi mes compétences linguistiques grâce aux applications modernes et aux podcasts éducatifs.

Au travail, je me fie à mon ordinateur équipé d’intelligence artificielle pour répondre à mes questions et m’aider dans mes tâches, rendant mon emploi du temps plus efficace et organisé. Cependant, la technologie a également des côtés moins positifs. Je me rends compte que je communique moins souvent en personne avec mes amis, préférant les appeler ou leur envoyer des messages, ce qui affecte notre relation. De plus, étant donné que les appareils prennent en charge de nombreuses tâches, j’ai tendance à perdre certaines compétences pratiques, comme la nécessité de me souvenir des numéros de téléphone ou de résoudre des problèmes sans assistance numérique.

Malgré ces inconvénients, je suis reconnaissant pour les avantages que la technologie apporte à ma vie. Elle simplifie de nombreux aspects, de la navigation aux communications, en passant par l'éducation. Mais il est important de maintenir un équilibre, en évitant de devenir trop dépendant des appareils et en restant conscient des relations humaines. L’évolution technologique est rapide et imprévisible, mais j’ai hâte de voir comment elle continuera d’améliorer notre existence, tant dans le travail que dans nos loisirs.

> Whiz: J'espère que ce modèle te sera utile pour comprendre comment structurer tes idées et les exprimer de manière plus claire et plus détaillée. N'hésites pas à le personnaliser en fonction de tes propres expériences et observations!