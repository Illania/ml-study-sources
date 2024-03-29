  Reinforcement Learning combines a control problem with statistical estimation: the system dynamics are not known to the agent but can be learned through experience.


  * [**applications**](#applications)
  * [**overview**](#overview)
  * [**deep reinforcement learning**](#deep-reinforcement-learning)
  * [**problems**](#problems)
  * [**exploration and intrinsic motivation**](#exploration-and-intrinsic-motivation)
  * [**bandits**](#bandits)
  * [**contextual bandits**](#contextual-bandits)
  * [**model-based methods**](#model-based-methods)
  * [**value-based methods**](#value-based-methods)
  * [**policy-based methods**](#policy-based-methods)
  * [**interesting papers**](#interesting-papers)
    - [**applications**](#interesting-papers---applications)
    - [**exploration and intrinsic motivation**](#interesting-papers---exploration-and-intrinsic-motivation)
    - [**hierarchical reinforcement learning**](#interesting-papers---hierarchical-reinforcement-learning)
    - [**model-based methods**](#interesting-papers---model-based-methods)
    - [**value-based methods**](#interesting-papers---value-based-methods)
    - [**policy-based methods**](#interesting-papers---policy-based-methods)
    - [**behavioral cloning**](#interesting-papers---behavioral-cloning)
    - [**inverse reinforcement learning**](#interesting-papers---inverse-reinforcement-learning)



---
### applications

  - [**industry**](#applications---industry)
  - [**games**](#applications---games)
  - [**robotics**](#applications---robotics)



---
### applications - industry

  [recommender system](https://nytimes.com/interactive/2019/06/08/technology/youtube-radical.html) at YouTube ([**paper**](#top-k-off-policy-correction-for-a-reinforce-recommender-system-chen-beutel-covington-jain-belletti-chi) by Chen et al. `summary`)

  [personalized web services](http://thenewstack.io/reinforcement-learning-ready-real-world/) at Microsoft ([Personalizer](https://azure.microsoft.com/en-us/services/cognitive-services/personalizer) service [**paper**](#making-contextual-decisions-with-low-technical-debt-agarwal-et-al) `summary`)  
  ["Personalized Web Services"](http://incompleteideas.net/book/the-book-2nd.html) chapter of book by Richard Sutton and Andrew Barto  

  [datacenter cooling](https://deepmind.com/blog/safety-first-ai-autonomous-data-centre-cooling-and-industrial-control/) at Google ([paper](https://papers.nips.cc/paper/7638-data-center-cooling-using-model-predictive-control.pdf) by Lazic et al., [patent](http://freepatentsonline.com/y2018/0204116.html))

  [stratospheric balloons](https://medium.com/loon-for-all/drifting-efficiently-through-the-stratosphere-using-deep-reinforcement-learning-c38723ee2e90) at Google ([paper](https://nature.com/articles/s41586-020-2939-8) by Bellemare et al., [overview](https://youtu.be/F-6sc88xPuA?t=25m55s) `video`)

  [artwork personalization](https://medium.com/netflix-techblog/artwork-personalization-c589f074ad76) at Netflix

----

  ["Reinforcement Learning Applications"](https://arxiv.org/abs/1908.06973) by Yuxi Li `paper` ([post](https://medium.com/@yuxili/rl-applications-73ef685c07eb))

  [**other applications**](https://yadi.sk/d/tiaE7sdi3WEhDS)

----

  ["Reinforcement Learning in Industry"](http://videolectures.net/deeplearning2017_le_roux_recommendation_system/) by Nicolas Le Roux `video`

  ["Why Tool AIs Want to Be Agent AIs"](http://gwern.net/Tool%20AI) by Gwern Branwen



---
### applications - games

  ["Success Stories of Deep RL"](https://youtube.com/watch?v=N8_gVrIPLQM) by David Silver `video`  
  ["Classic Games Case Study"](https://youtube.com/watch?v=ld28AU7DDB4) by David Silver `video`  
  ["AI for Classic Games"](http://youtube.com/watch?v=kZ_AUmFcZtk) by David Silver `video`  
  ["From TD(λ) to AlphaGo: Games, Neural Nets, Reinforcement Learning and Rollouts"](http://techtalks.tv/talks/on-td-learning-and-links-with-deeprl-in-atari-and-alphago/63031/) by Gerry Tesauro `video`  
  ["Fifty Years of RL in Games"](http://videolectures.net/icml09_tesauro_itfyrlg) by Gerry Tesauro `video`  

  ["A 'Brief' History of Game AI Up To AlphaGo"](http://andreykurenkov.com/writing/a-brief-history-of-game-ai/) by Andrey Kurenkov

----
  - *StarCraft 2*

	[AlphaStar overview](https://deepmind.com/blog/article/AlphaStar-Grandmaster-level-in-StarCraft-II-using-multi-agent-reinforcement-learning)

	[**"Grandmaster Level in StarCraft II using Multi-agent Reinforcement Learning"**](#grandmaster-level-in-starcraft-ii-using-multi-agent-reinforcement-learning-vinyals-et-al) by Vinyals et al. `paper` `summary` *(AlphaStar)*  
	["StarCraft II Unplugged: Large Scale Offline Reinforcement Learning"](https://openreview.net/forum?id=Np8Pumfoty) by Mathieu et al. `paper`  

	[overview](https://youtu.be/-fdexQBpRas?t=29m26s) by Oriol Vinyals `video`  
	[overview](https://slideslive.com/38922724/grandmaster-level-in-starcraft-ii-using-multiagent-reinforcement-learning) by Oriol Vinyals `video`  
	[overview](https://youtu.be/3UdH3lPF7nE) by Oriol Vinyals `video`  
	[overview](https://slideslive.com/38916905/alphastar-mastering-the-game-of-starcraft-ii) by David Silver `video`  
	[overview](https://youtu.be/mzjGNo9Tz4g?t=10m53s) by David Silver `video`  

	[AlphaStar discussion](https://youtu.be/Kedt2or9xlo) with Oriol Vinyals `video`  
	[AlphaStar discussion](https://reddit.com/r/MachineLearning/comments/ajgzoc/we_are_oriol_vinyals_and_david_silver_from) with Oriol Vinyals and David Silver  

	[AlphaStar vs Serral](https://youtube.com/playlist?list=PLojXIrB9Xau29fR-ZSdbFllI-ZCuH6urt) games `video`  
	[AlphaStar vs Battle.net players](https://deepmind.com/research/open-source/alphastar-resources) games ([overviews](https://youtube.com/playlist?list=PLtFBLTxDxWOSrWZ8krQt6eDNXTpG67Xpf) `video`)  
	[AlphaStar vs pro players](https://youtube.com/watch?v=cUTMhmVh1qs) games `video` ([highlights](https://youtube.com/watch?v=zgIFoepzhIo) by MaNa `video`, [highlights](https://youtube.com/watch?v=_YWmU-E2WFc) by Artosis `video`)  

----
  - *Dota 2*  

	[OpenAI Five](https://openai.com/projects/five)

	[OpenAI Five training](https://openai.com/blog/how-to-train-your-openai-five)  
	[OpenAI Five overview](https://blog.openai.com/openai-five-benchmark-results)  
	[OpenAI Five architecture](https://s3-us-west-2.amazonaws.com/openai-assets/dota_benchmark_results/network_diagram_08_06_2018.pdf)  
	[OpenAI Five reward function](https://gist.github.com/dfarhi/66ec9d760ae0c49a5c492c9fae93984a)  

	["Dota 2 with Large Scale Deep Reinforcement Learning"](https://cdn.openai.com/dota-2.pdf) by Berner et al. `paper` *(OpenAI Five)*

	[OpenAI Five overview](https://slideslive.com/38922722/contributed-talk-playing-dota-2-with-large-scale-deep-reinforcement-learning) by Jie Tang and Filip Wolski `video`  
	[OpenAI Five overview](https://youtu.be/w3ues-NayAs?t=2m26s) by Ilya Sutskever `video`  
	[OpenAI Five overview](https://youtu.be/N8_gVrIPLQM?t=1h3m41s) by David Silver `video`  
	[OpenAI Five overview](https://youtube.com/watch?v=0eO2TSVVP1Y) by Xander Steenbrugge `video`  

	[OpenAI Five discussion](https://twitch.tv/videos/293517383?t=4h41m56s) with OpenAI team `video`  
	[OpenAI Five discussion](https://reddit.com/r/DotA2/comments/bf49yk/hello_were_the_dev_team_behind_openai_five_we) with OpenAI team  

	[OpenAI Five vs top players](https://youtube.com/playlist?list=PLOXw6I10VTv-ZFZV4fMqKMfNQmwmkcr0w) games `video`  
	[OpenAI Five vs ainodehna team](https://arena.openai.com/#/results) games ([highlights](https://cybersport.ru/dota-2/interviews/glavnoe-protiv-botov-otdat-im-udobnykh-dlya-nas-geroev-komanda-kotoraya-trizhdy-pobedila-openai-raskryla-svoyu-taktiku) `in russian`)  

----
  - *Poker*  

	[Libratus](https://en.wikipedia.org/wiki/Libratus)

	[Libratus overview](https://int8.io/counterfactual-regret-minimization-for-poker-ai/#Libratus_8211_DeepStack8217s_main_rival_from_Carnegie_Mellon_University) by Kamil Czarnogorski  
	[Libratus overview](https://thegradient.pub/libratus-poker) by Jiren Zhu  
	[Pluribus overview](https://ai.facebook.com/blog/pluribus-first-ai-to-beat-pros-in-6-player-poker)  

	["Superhuman AI for Heads-up No-limit Poker: Libratus Beats Top Professionals"](http://science.sciencemag.org/content/early/2017/12/15/science.aao1733.full) by Brown and Sandholm `paper` *(Libratus)*  
	["Safe and Nested Subgame Solving for Imperfect-Information Games"](https://arxiv.org/abs/1705.02955) by Brown and Sandholm `paper` *(Libratus)* ([overview](https://vimeo.com/248533943#t=53s) `video`)  
	["Depth-Limited Solving for Imperfect-Information Games"](https://arxiv.org/abs/1805.08195) by Brown et al. `paper` ([overview](https://youtube.com/watch?v=S4-g3dPT2gY) `video`)  
	["Superhuman AI for Multiplayer Poker"](https://science.sciencemag.org/content/365/6456/885) by Brown and Sandholm `paper` ([overview](https://youtube.com/watch?v=JuvN4mi861k) `video`) *(Pluribus)*  
	[**"Deep Counterfactual Regret Minimization"**](#deep-counterfactual-regret-minimization-brown-lerer-gross-sandholm) by Brown et al. `paper` `summary` *(Deep CFR)*  
	[**"Combining Deep Reinforcement Learning and Search for Imperfect-Information Games"**](#combining-deep-reinforcement-learning-and-search-for-imperfect-information-games-brown-et-al) by Brown et al. `paper` `summary` *(ReBeL)*  

	[Libratus overview](https://youtube.com/watch?v=EhvH4jdF-ko) by Tuomas Sandholm `video`  
	[Libratus overview](https://youtube.com/watch?v=xrWulRY_t1o) by Tuomas Sandholm `video`  
	[Libratus overview](http://videolectures.net/aaai2017_bowling_sandholm_poker/#t=1350) by Tuomas Sandholm `video`  
	[Libratus overview](https://youtube.com/watch?v=McV4a6umbAY) by Noam Brown `video`  
	[Libratus overview](https://youtube.com/watch?v=2dX0lwaQRX0) by Noam Brown `video`  
	[Libratus overview](https://youtube.com/watch?v=UTogLB99JKQ) by Noam Brown `video`  
	[Pluribus overview](https://youtube.com/watch?v=JuvN4mi861k) by Noam Brown `video`  

	["New Results for Solving Imperfect-Information Games"](https://vimeo.com/313942390) by Tuomas Sandholm `video`  
	["Safe and Nested Subgame Solving for Imperfect-Information Games"](https://vimeo.com/248533943#t=53s) by Noam Brown `video`  
	["Reduced Space and Faster Convergence in Imperfect-Information Games via Pruning"](https://vimeo.com/238229930) by Noam Brown `video`  
	["The State of Techniques for Solving Large Imperfect-Information Games"](https://youtube.com/watch?v=Gz026reyVwc) by Tuomas Sandholm `video`  
	["The State of Techniques for Solving Large Imperfect-Information Games, Including Poker"](https://youtube.com/watch?v=QgCxCeoW5JI) by Tuomas Sandholm `video`  

	[Libratus discussion](https://youtube.com/watch?v=b7bStIQovcY) with Tuomas Sandholm `video`  
	[Libratus discussion](https://youtube.com/watch?v=ZlPPp_xokd4) with Tuomas Sandholm `audio`  
	[Libratus discussion](https://youtube.com/watch?v=wKey6eKccYM) with Noam Brown `audio`  
	[Libratus discussion](https://reddit.com/r/MachineLearning/comments/7jn12v/ama_we_are_noam_brown_and_professor_tuomas) with Noam Brown and Tuomas Sandholm  

	[Pluribus discussion](https://reddit.com/r/MachineLearning/comments/ceece3/ama_we_are_noam_brown_and_tuomas_sandholm) with Noam Brown and Tuomas Sandholm  
	[Pluribus discussion](https://news.ycombinator.com/item?id=20415379) with Noam Brown  

	[Libratus vs top players](https://youtube.com/watch?v=crgmYTMfrSc) games highlights `video`  
	[Pluribus vs top players](https://youtube.com/playlist?list=PLm7RXNGNZs2V6en-KZx5dTV_BP-Ejem3q) games `video`  

----
  - *Poker*  

	[DeepStack](http://deepstack.ai)

	[DeepStack overview](https://int8.io/counterfactual-regret-minimization-for-poker-ai/#DeepStack_8211_Neural_Network_based_AI_playing_Heads_Up_No-Limit_Texas_Hold8217em) by Kamil Czarnogorski  
	[DeepStack overview](https://www.depthfirstlearning.com/2018/DeepStack) by Cinjon Resnick  

	[DeepStack "Science" magazine](http://science.sciencemag.org/content/early/2017/03/01/science.aam6960) `paper`  
	[**"DeepStack: Expert-Level Artificial Intelligence in No-Limit Poker"**](#deepstack-expert-level-artificial-intelligence-in-no-limit-poker-moravcik-et-al) by Moravcik et al. `paper` `summary` *(DeepStack)*  

	[DeepStack overview](https://vimeo.com/248532904) by Michael Bowling `video`  
	[DeepStack overview](https://youtu.be/02xIkHowQOk?t=11m45s) by Michael Bowling `video`  
	[DeepStack overview](https://youtube.com/watch?v=qndXrHcV1sM) by Michael Bowling `video`  
	[DeepStack overview](http://videolectures.net/aaai2017_bowling_sandholm_poker/#t=177) by Michael Bowling `video`  

	[discussion](http://thinkingpoker.net/2017/03/episode-208-michael-bowling-of-cprg/) with Michael Bowling  
	[discussion](http://thinkingpoker.net/2017/04/episode-210-michael-johanson-and-dustin-morrill/) with Michael Johanson and Dustin Morrill  
	[discussion](http://thinkingpoker.net/2017/08/episode-225-taking-the-variance-out-of-poker/) with Michael Bowling and Dustin Morrill  

	[DeepStack vs pro players](https://youtube.com/playlist?list=PLX7NnbJAq7PlA2XpynViLOigzWtmr6QVZ) games `video`

----
  - *Go*  

	[AlphaGo](https://en.wikipedia.org/wiki/AlphaGo)

	["Mastering the Game of Go"](http://incompleteideas.net/book/the-book-2nd.html) chapter of book by Richard Sutton and Andrew Barto

	[AlphaGo Zero overview](http://www.depthfirstlearning.com/2018/AlphaGoZero)

	[**"Mastering Atari, Go, Chess and Shogi by Planning with a Learned Model"**](#mastering-atari-go-chess-and-shogi-by-planning-with-a-learned-model-schrittwieser-et-al) by Schrittwieser et al. `paper` `summary` *(MuZero)*  
	[**"Mastering the Game of Go without Human Knowledge"**](#mastering-the-game-of-go-without-human-knowledge-silver-et-al) by Silver et al. `paper` `summary` *(AlphaGo Zero)*  
	[**"Mastering the Game of Go with Deep Neural Networks and Tree Search"**](#mastering-the-game-of-go-with-deep-neural-networks-and-tree-search-silver-et-al) by Silver et al. `paper` `summary` *(AlphaGo)*  
	["Sample-Based Learning and Search with Permanent and Transient Memories"](https://researchgate.net/publication/221346457_Sample-based_learning_and_search_with_permanent_and_transient_memories) by Silver et al. ([overview](http://videolectures.net/icml08_silver_sbl) `video`) *(Dyna-2)*  
	["Combining Online and Offline Knowledge in UCT"](https://researchgate.net/publication/29651027_Combining_Online_and_Offline_Knowledge_in_UCT) by Gelly and Silver `paper` ([overview](https://youtube.com/watch?v=Bm7zah_LrmE) `video`) *(MoGo)*  

	[AlphaGo, AlphaGo Zero, MuZero overview](https://youtube.com/playlist?list=PLnn6VZp3hqNsrsp_Bg-bEfzzhJ3SuEZE9) `video`

	[AlphaGo Zero overview](https://vimeo.com/252184928/#t=711) by David Silver `video`  
	[AlphaGo Zero overview](https://youtu.be/DXNqYSNvnjA?t=16m41s) by Demis Hassabis `video`  

	[AlphaGo overview](https://youtu.be/i3lEG6aRGm8?t=16m) by Demis Hassabis `video`  
	[AlphaGo overview](https://youtu.be/4D5yGiYe8p4) by David Silver `video`  
	[AlphaGo overview](https://youtu.be/LX8Knl0g0LE?t=4m41s) by Aja Huang `video`  

	"Google AlphaGo is a historical tour of AI ideas: 70s (Alpha-Beta), 80s/90s (RL & self-play), 00's (Monte-Carlo), 10's (deep neural networks)."  
	[history of ideas](http://youtube.com/watch?v=UMm0XaCFTJQ) by Richard Sutton, Czaba Szepesvari, Michael Bowling, Ryan Hayward, Martin Muller `video`  

	[AlphaGo documentary](https://youtube.com/watch?v=WXuK6gekU1Y) `video`

	[AlphaGo vs Lee Sedol](https://youtube.com/playlist?list=PLqYmG7hTraZDEaLdPx7GJ284kuE2xcFXu) games `video`  
	[AlphaGo Master vs pros](https://youtube.com/playlist?list=PLqpN3-2FP-kI21lBD8R7Q9mwXQG_2sYnD) games `video`  
	[AlphaGo Master vs Ke Jie](https://youtube.com/playlist?list=PLqYmG7hTraZDEaLdPx7GJ284kuE2xcFXu) games `video`  
	[AlphaGo Zero vs Master](https://youtube.com/playlist?list=PLqpN3-2FP-kLKm8sqTWUBShLEzJ9LeHok) games `video`  

----
  - *Chess*  

	["Vector Quantized Models for Planning"](https://arxiv.org/abs/2106.04615) by Ozair et al. `paper`  
	[**"Mastering Atari, Go, Chess and Shogi by Planning with a Learned Model"**](#mastering-atari-go-chess-and-shogi-by-planning-with-a-learned-model-schrittwieser-et-al) by Schrittwieser et al. `paper` `summary` *(MuZero)*  
	[**"Mastering Chess and Shogi by Self-Play with a General Reinforcement Learning Algorithm"**](#mastering-chess-and-shogi-by-self-play-with-a-general-reinforcement-learning-algorithm-silver-et-al) by Silver et al. `paper` `summary` *(AlphaZero)*  
	[**"Giraffe: Using Deep Reinforcement Learning to Play Chess"**](#giraffe-using-deep-reinforcement-learning-to-play-chess-lai) by Lai `paper` `summary` *(Giraffe)*  
	[**"Bootstrapping from Game Tree Search"**](#bootstrapping-from-game-tree-search-veness-silver-uther-blair) by Veness et al. `paper` `summary` *(TreeStrap)*  
	["KnightCap: A Chess Program that Learns by Combining TD(lambda) with Game-tree Search"](https://arxiv.org/abs/cs/9901002) by Baxter et al. `paper` *(KnightCap)*  

	[AlphaZero, MuZero overview](https://youtube.com/playlist?list=PLnn6VZp3hqNsrsp_Bg-bEfzzhJ3SuEZE9) `video`

	[AlphaZero overview](https://vimeo.com/252184928#t=1468) by David Silver `video`  
	[AlphaZero overview](https://youtu.be/N8_gVrIPLQM?t=47m9s) by David Silver `video`  
	[AlphaZero overview](https://youtube.com/watch?v=mzjGNo9Tz4g) by David Silver `video`  
	[AlphaZero overview](https://youtu.be/3N9phq_yZP0?t=12m43s) by Demis Hassabis `video`  
	[AlphaZero overview](https://youtu.be/DXNqYSNvnjA?t=21m24s) by Demis Hassabis `video`  

	[AlphaZero vs Stockfish](https://youtube.com/playlist?list=UUkK8M0dMhAX8JinU-6aD7xA) games `video`  
	[AlphaZero vs Stockfish](https://youtube.com/playlist?list=PLDnx7w_xuguFDbrYDxxvPH-aoQkEX0rHv) games `video`  
	[AlphaZero vs Stockfish](https://youtube.com/playlist?list=PLDnx7w_xuguHIxbL7akaYgEvV4spwYkmn) games `video`  
	[AlphaZero vs Stockfish](https://youtube.com/playlist?list=PL-qLOQ-OEls607FPLAsPZ6De4f1W3ZF-I) games `video`  

	["Game Changer: AlphaZero's Groundbreaking Chess Strategies and the Promise of AI"](https://amazon.com/Game-Changer-AlphaZeros-Groundbreaking-Strategies/dp/9056918184) by Matthew Sadler and Natasha Regan `book` ([overview](https://youtube.com/watch?v=HgZYIDslnAI) `video`, [games](https://youtube.com/playlist?list=UUkK8M0dMhAX8JinU-6aD7xA) `video`)

	[Leela Chess Zero](https://youtube.com/playlist?list=PLDnx7w_xuguH7UO4bNGo56w94NXAef6YH) games `video` ([overview](https://en.wikipedia.org/wiki/Leela_Chess_Zero))

----
  - *Quake III Arena*

	[FTW agent overview](https://deepmind.com/blog/capture-the-flag-science)

	[**"Human-level Performance in First-person Multiplayer Games with Population-based Deep Reinforcement Learning"**](#human-level-performance-in-first-person-multiplayer-games-with-population-based-deep-reinforcement-learning-jaderberg-et-al) by Jaderberg et al. `paper` `summary` *(FTW)*

	[overview](https://youtu.be/N8_gVrIPLQM?t=1h10m) by David Silver `video`

	[FTW agents vs FTW agents](https://youtube.com/watch?v=NXkD77ioGi0) games `video`  
	[FTW agents vs human players](https://youtube.com/watch?v=dltN4MxV1RI) games `video`  

----
  - *Doom*  

	[**"Learning to Act by Predicting the Future"**](#learning-to-act-by-predicting-the-future-dosovitskiy-koltun) by Dosovitskiy and Koltun `paper` `summary` *(IntelAct)*

	[IntelAct agent demo](https://youtube.com/watch?v=947bSUtuSQ0) `video`  
	[ViZDoom competition](https://youtube.com/channel/UC8UghzsxS5uEFUEbvcAWwlQ/videos) games `video`  

----
  - *Atari*  

	["Human-level Video Game Play"](http://incompleteideas.net/book/the-book-2nd.html) chapter of book by Richard Sutton and Andrew Barto

	[**"Mastering Atari, Go, Chess and Shogi by Planning with a Learned Model"**](#mastering-atari-go-chess-and-shogi-by-planning-with-a-learned-model-schrittwieser-et-al) by Schrittwieser et al. `paper` `summary` *(MuZero)*  
	[**"Playing Atari with Deep Reinforcement Learning"**](#playing-atari-with-deep-reinforcement-learning-mnih-kavukcuoglu-silver-graves-antonoglou-wierstra-riedmiller) by Mnih et al. `paper` `summary` *(DQN)*  

	[demo](http://youtube.com/watch?v=EfGD2qveGdQ) `video`

----
  - *Jeopardy!*  

	["Watson’s Daily-Double Wagering"](http://incompleteideas.net/book/the-book-2nd.html) chapter of book by Richard Sutton and Andrew Barto

	["Simulation, Learning and Optimization Techniques in Watson's Game Strategies"](https://researchgate.net/publication/260624027_Simulation_learning_and_optimization_techniques_in_Watson%27s_game_strategies) by Tesauro et al. `paper`  
	["Analysis of Watson's Strategies for Playing Jeopardy!"](https://arxiv.org/abs/1402.0571) by Tesauro et al. `paper`  

	["How Watson Learns Superhuman Jeopardy! Strategies"](https://youtube.com/watch?v=7rIf2Njye5k) by Gerry Tesauro `video`

	[**IBM Watson**](https://github.com/brylevkirill/notes/blob/master/Knowledge%20Representation%20and%20Reasoning.md#machine-reading-projects---ibm-watson) project `summary`

	[IBM Watson vs top players](https://archive.org/details/Jeopardy.2011.02.The.IBM.Challenge) match `video`

----
  - *Backgammon*  

	[TD-Gammon](http://scholarpedia.org/article/User:Gerald_Tesauro/Proposed/Td-gammon)

	["TD-Gammon"](http://incompleteideas.net/book/the-book-2nd.html) chapter of book by Richard Sutton and Andrew Barto

	["Temporal Difference Learning and TD-Gammon"](https://cling.csd.uwo.ca/cs346a/extra/tdgammon.pdf) by Tesauro et al. `paper` *(TD-Gammon)*  
	["On-line Policy Improvement using Monte-Carlo Search"](https://papers.nips.cc/paper/1302-on-line-policy-improvement-using-monte-carlo-search.pdf) by Tesauro et al. `paper` *(TD-Gammon)*  

	[TD-Gammon overview](http://techtalks.tv/talks/on-td-learning-and-links-with-deeprl-in-atari-and-alphago/63031/) by Gerry Tesauro `video`  
	[TD-Gammon overview](http://videolectures.net/icml09_tesauro_itfyrlg/#t=784) by Gerry Tesauro `video`  
	[TD-Gammon overview](https://youtu.be/ld28AU7DDB4?t=42m7s) by David Silver `video`  
	[TD-Gammon overview](https://youtu.be/kZ_AUmFcZtk?t=42m29s) by David Silver `video`  
	[TD-Gammon overview](https://youtu.be/N8_gVrIPLQM?t=7m32s) by David Silver `video`  



---
### applications - robotics

  [course](https://people.eecs.berkeley.edu/~pabbeel/cs287-fa19) by Pieter Abbeel `video`

  [overview](https://youtube.com/watch?v=T57lx_adnH0) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=DoDUpLhvWQk) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=DoDUpLhvWQk) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=sXQlQg7Hax8) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=U1dD8UALTu0) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=b97H5uz8xkI) by Sergey Levine `video`  
  [overview](http://www.fields.utoronto.ca/video-archive/2019/10/2509-21418) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=jAPJeJK18mw) by Sergey Levine `video`  
  [overview](https://livestream.com/newyorkacademyofsciences/ml2018-2/videos/171320389) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=lYU5nq0dAQQ) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=eKaYnXQUb2g) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=jtjW5Pye_44) by Sergey Levine `video`  
  [overview](http://videolectures.net/iclr2016_levine_deep_learning) by Sergey Levine `video`  

  [overview](https://youtube.com/watch?v=l9pwlXXsi7Q) by Pieter Abbeel `video`  
  [overview](https://youtube.com/watch?v=WGza-jN4CZs) by Pieter Abbeel `video`  
  [overview](https://slideslive.com/38915873/deep-learning-for-robotics) by Pieter Abbeel `video`  
  [overview](https://facebook.com/nipsfoundation/videos/1554594181298482) by Pieter Abbeel `video`  
  [overview](https://youtube.com/watch?v=TERCdog1ddE) by Pieter Abbeel `video`  

  ["Is (Deep) Reinforcement Learning Barking Up The Wrong Tree?"](https://youtube.com/watch?v=2GW7ozcUCFE) by Chris Atkeson `video`  
  ["What Should Be Learned?"](https://youtu.be/WRsxoVB8Yng?t=7h7m15s) by Chris Atkeson `video`  

  ["Sampling and Exploration for Control of Physical Systems"](https://facebook.com/icml.imls/videos/2265408103721327?t=591) by Emo Todorov `video` *(critique of MDP framework)*

----
  - *grasping*

	[QT-Opt](https://ai.googleblog.com/2018/06/scalable-deep-reinforcement-learning.html)

	[**"QT-Opt: Scalable Deep Reinforcement Learning for Vision-Based Robotic Manipulation"**](#qt-opt-scalable-deep-reinforcement-learning-for-vision-based-robotic-manipulation-kalashnikov-et-al) by Kalashnikov et al. `paper` `summary`

	[QT-Opt overview](https://youtu.be/U1dD8UALTu0?t=16m25s) by Sergey Levine `video`  
	[QT-Opt overview](http://www.fields.utoronto.ca/video-archive/2019/10/2509-21418) (19:54) by Sergey Levine `video`  
	[QT-Opt overview](https://video.ethz.ch/events/2018/corl/c7111aff-c968-43cd-ad0f-b42ddcccbf62.html) by Dmitry Kalashnikov `video`  

	[QT-Opt demo](https://youtube.com/watch?v=z-2q1eMAwps)

----
  - *in-hand manipulation*

	[OpenAI Rubik's Cube](https://openai.com/blog/solving-rubiks-cube)  
	[OpenAI Dactyl](https://openai.com/blog/learning-dexterity)  

	["Solving Rubik's Cube with a Robot Hand"](https://arxiv.org/abs/1910.07113) by OpenAI et al. `paper` ([overview](https://youtube.com/watch?v=2AqGocPOOG4) `video`)  
	[**"Learning Dexterous In-Hand Manipulation"**](#learning-dexterous-in-hand-manipulation-openai-et-al) by OpenAI et al. `paper` `summary` *(OpenAI Dactyl)*  

	[OpenAI Rubik's Cube overview](https://slideslive.com/38922026/deep-reinforcement-learning-2?t=5081) by Jerry Tworek `video`  
	[OpenAI Dactyl overview](https://youtu.be/WRsxoVB8Yng?t=57m55s) by Wojciech Zaremba `video`  
	[OpenAI Dactyl overview](https://youtu.be/w3ues-NayAs?t=16m26s) by Ilya Sutskever `video`  

	[OpenAI Dactyl discussion](https://facebook.com/icml.imls/videos/2265408103721327?t=1200) with Emo Todorov `video`

	[OpenAI Rubik's Cube demo](https://youtube.com/playlist?list=PLOXw6I10VTv9HODt7TFEL72K3Q6C4itG6) `video`  
	[OpenAI Dactyl demo](https://youtube.com/watch?v=jwSbzNHGflM) `video`  
	[OpenAI Dactyl demo](https://youtube.com/watch?v=DKe8FumoD4E) `video`  

----
  - *bipedal robots*

	["Reinforcement Learning for Robust Parameterized Locomotion Control of Bipedal Robots"](https://arxiv.org/abs/2103.14295) by Li et al. `paper`

	[demo](https://youtube.com/watch?v=goxCjGPQH7U) `video`

  - *legged robots*

	[ANYmal](https://anybotics.com/anymal-legged-robot)

	["Learning Agile and Dynamic Motor Skills for Legged Robots"](https://arxiv.org/abs/1901.08652) by Hwangbo et al. `paper`

	[demos](https://youtube.com/playlist?list=UUHjP785620I8LFjSxf_CJCw) `video`  
	[demos](https://youtube.com/playlist?list=PL22adRtGDGxeGQ5RVGS5Knh4Le5NsHEby) `video`  



---
### overview

  [definition](https://youtube.com/watch?v=kl_G95uKTHw&t=1h9m30s) by Sergey Levine `video`

----

  introduction by Kevin Frans:  
  - [basics](http://kvfrans.com/reinforcement-learning-basics/)  
  - [Markov processes](http://kvfrans.com/markov-processes-in-reinforcement-learning/)  
  - [planning](http://kvfrans.com/planning-policy-evaluation-policy-iteration-value-iteration/)  
  - [model-free methods](http://kvfrans.com/model-free-prediction-and-control/)  
  - [policy gradient methods](http://kvfrans.com/the-policy-gradient/)  
  - [model-based methods](http://kvfrans.com/making-use-of-the-model/)  

  introduction by Lilian Weng:
  - ["A Long Peak"](https://lilianweng.github.io/lil-log/2018/02/19/a-long-peek-into-reinforcement-learning.html)

  introduction by Benjamin Recht:  
  - ["Make It Happen"](http://argmin.net/2018/01/29/taxonomy/)  
  - ["Total Control"](http://argmin.net/2018/02/01/control-tour/)  

  introduction by Shakir Mohamed:  
  - ["Learning in Brains and Machines: Temporal Differences"](http://blog.shakirm.com/2016/02/learning-in-brains-and-machines-1/)  
  - ["Synergistic and Modular Action"](http://blog.shakirm.com/2016/07/learning-in-brains-and-machines-3-synergistic-and-modular-action/)  

----

  [overview](https://youtube.com/watch?v=2pWv7GOvuf0) by David Silver `video`  
  [overview](https://yadi.sk/i/bMo0qa-x3DoqkS) by Fedor Ratnikov `video` `in russian`  

----

  [Reinforcement Learning Summer School 2019](http://youtube.com/playlist?list=PLKlhhkvvU8-aXmPQZNYG_e-2nTd0tJE8v) `video`  
  [Reinforcement Learning Summer School 2018](http://videolectures.net/DLRLsummerschool2018_toronto/) `video`  
  [Reinforcement Learning Summer School 2017](http://videolectures.net/deeplearning2017_montreal/) `video`  

----

  [course](https://youtube.com/playlist?list=PLqYmG7hTraZDM-OYHWgPebj2MfCFzFObQ) by David Silver `video`  *(basic)*  
  [course](https://udacity.com/course/reinforcement-learning--ud600) by Michael Littman `video`  *(basic)*  
  [course](https://youtube.com/playlist?list=PLoROMvodv4rOSOPzutgyCTapiGlY2Nd8u) by Emma Brunskill `video`  *(basic)*  
  [course](https://youtube.com/playlist?list=PLnn6VZp3hqNvRrdnMOVtgV64F_O-61C1D) by Connor Shorten `video`  *(basic)*  

  [course](http://rail.eecs.berkeley.edu/deeprlcourse) from UC Berkeley ([videos](https://youtube.com/playlist?list=PL_iWQOsE6TfURIIhCrlt-wj9ByIVpbfGc)) `2020`  *(advanced)*  
  [course](http://rail.eecs.berkeley.edu/deeprlcourse/resources#prev-off) from UC Berkeley ([videos](https://youtube.com/playlist?list=PLkFD6_40KJIwhWJpGazJ9VSj9CFMkb79A)) `2019`  *(advanced)*  
  [course](https://youtube.com/playlist?list=PLqYmG7hTraZDVH599EItlEWsUOsJbAodm) from DeepMind `video` `2021`  *(advanced)*  
  [course](https://youtube.com/playlist?list=PLqYmG7hTraZDNJre23vqCGIVpfZ_K2RZs) from DeepMind `video` `2018`  *(advanced)*  
  [course](https://youtube.com/playlist?list=PLkFD6_40KJIznC9CDbVTjAF2oyt8_VAe3) by Sergey Levine, John Schulman and Chelsea Finn `video`  *(advanced)*  
  [course](https://github.com/yandexdataschool/Practical_RL/) from Yandex and HSE `video` `in russian`  *(advanced)*  
  [course](https://deeppavlov.ai/rl_course_2020) from MIPT and Yandex ([videos](https://youtube.com/playlist?list=PLt1IfGj6-_-eXjZDFBfnAhAJmCyX227ir)) `in russian` `2020`  *(advanced)*  
  [course](https://youtube.com/playlist?list=PLwdBkWbW0oHEUmY07a0G5jabP_fWfGQet) by Sergey Nikolenko `video` `in russian`  *(advanced)*  

----

  [tutorial](https://youtube.com/watch?v=Fsh1qMTg1xI) by Richard Sutton `video` ([write-up](https://goo.gl/PxHMLK))  
  [tutorial](https://youtube.com/watch?v=fIKkhoI1kF4) by Emma Brunskill `video`  

----

  ["Reinforcement Learning: An Introduction"](http://incompleteideas.net/book/the-book-2nd.html) book by Richard Sutton and Andrew Barto (second edition) ([code](https://github.com/ShangtongZhang/reinforcement-learning-an-introduction))  
  ["Reinforcement Learning: An Introduction"](http://incompleteideas.net/book/the-book-1st.html) book by Richard Sutton and Andrew Barto (first edition)  
  ["Algorithms for Reinforcement Learning"](http://www.ualberta.ca/~szepesva/papers/RLAlgsInMDPs.pdf) book by Csaba Szepesvari  
  ["Reinforcement Learning and Optimal Control"](http://web.mit.edu/dimitrib/www/RLbook.html) book by Dimitri Bertsekas  
  ["Bandit Algorithms"](http://downloads.tor-lattimore.com/banditbook/book.pdf) book by Tor Lattimore and Csaba Szepesvari  

----

  [course notes](https://web.stanford.edu/class/msande338/lecture_notes.html) by Ben Van Roy  
  [course slides](http://incompleteideas.net/sutton/609%20dropbox/slides%20(pdf%20and%20keynote)) by Richard Sutton  

  [exercises and solutions](https://github.com/ShangtongZhang/reinforcement-learning-an-introduction) by Shangtong Zhang  
  [exercises and solutions](https://github.com/dennybritz/reinforcement-learning) by Denny Britz  
  [exercises and solutions](https://github.com/yandexdataschool/Practical_RL/) from Yandex and HSE  

----

  [RL Weekly](https://endtoend.ai/rl-weekly) newsletter



---
### deep reinforcement learning

  "Reinforcement Learning is a general-purpose framework for decision-making:  
   - Is for an agent with the capacity to act  
   - Each action influences the agent's future state  
   - Success is measured by a scalar reward signal  
   - Goal: select actions to maximize future reward"  

  "Deep Learning is a general-purpose framework for representation learning:  
   - Given an objective  
   - Learn representation that is required to achieve objective  
   - Directly from raw inputs  
   - Using minimal domain knowledge"  

  *(David Silver)*

  - Reinforcement Learning gives a learning objective  
  - Deep Learning gives a learning mechanism  

  ["Success Stories of Deep RL"](https://youtube.com/watch?v=N8_gVrIPLQM) by David Silver `video`

----

  ["Spinning Up in Deep RL"](https://spinningup.openai.com) from OpenAI

  ["An Introduction to Deep Reinforcement Learning"](https://arxiv.org/abs/1811.12560) by François-Lavet et al. `paper`  
  ["A Brief Survey of Deep Reinforcement Learning"](https://arxiv.org/abs/1708.05866) by Arulkumaran et al. `paper`  

  ["Deep Reinforcement Learning: An Overview"](https://arxiv.org/abs/1810.06339) by Yuxi Li `book`  
  ["Deep Reinforcement Learning Hands-On"](https://amazon.com/gp/product/1788834240) by Maxim Lapan `book`  

----

  [course](http://rail.eecs.berkeley.edu/deeprlcourse) by Sergey Levine ([videos](https://youtube.com/playlist?list=PLkFD6_40KJIwhWJpGazJ9VSj9CFMkb79A))  
  [course](https://youtube.com/playlist?list=PLqYmG7hTraZDNJre23vqCGIVpfZ_K2RZs) from DeepMind `video`  
  [course](https://youtube.com/playlist?list=PLkFD6_40KJIznC9CDbVTjAF2oyt8_VAe3) by Sergey Levine, John Schulman and Chelsea Finn `video`  
  [course](https://github.com/yandexdataschool/Practical_RL/) from Yandex and HSE `video` `in russian`  

----

  ["Spinning Up in Deep RL"](https://youtube.com/watch?v=fdY7dt3ijgY) workshop by OpenAI `video`  
  [Deep RL Bootcamp](https://sites.google.com/view/deep-rl-bootcamp/lectures) workshop at Berkeley `video`  

  ["The Nuts and Bolts of Deep RL Research"](https://youtube.com/watch?v=8EcdaCk9KaQ) by John Schulman `video`
	([slides](http://rll.berkeley.edu/deeprlcourse/docs/nuts-and-bolts.pdf),
	[write-up](https://github.com/williamFalcon/DeepRLHacks))

----

  ["Challenges of Real-World Reinforcement Learning"](https://arxiv.org/abs/1904.12901) by Dulac-Arnold et al.  
  ["A Real World Reinforcement Learning Research Program"](http://hunch.net/?p=9828091) by John Langford  
  ["Pervasive Simulator Misuse with Reinforcement Learning"](http://hunch.net/?p=8825714) by John Langford  
  ["Expressivity, Trainability, and Generalization in Machine Learning"](http://blog.evjang.com/2017/11/exp-train-gen.html) by Eric Jang  
  ["On “Solving” Montezuma’s Revenge"](https://medium.com/@awjuliani/on-solving-montezumas-revenge-2146d83f0bc3) by Arthur Juliani  
  ["Deep Reinforcement Learning Doesn't Work Yet"](https://www.alexirpan.com/2018/02/14/rl-hard.html) by Alex Irpan  
  ["Reinforcement Learning Never Worked, and 'Deep' Only Helped a Bit"](https://himanshusahni.github.io/2018/02/23/reinforcement-learning-never-worked.html) by Himanshu Sahni  



---
### problems

  1. Training off-line from the fixed logs of an external behavior policy.  
  2. Learning on the real system from limited samples.  
  3. High-dimensional continuous state and action spaces.  
  4. Safety constraints that should never or at least rarely be violated.  
  5. Tasks that may be partially observable, non-stationary or stochastic.  
  6. Reward functions that are unspecified, multi-objective, or risk-sensitive.  
  7. System operators who desire explainable policies and actions.  
  8. Inference that must happen in real-time at the control frequency of the system.  
  9. Large and/or unknown delays in the system actuators, sensors, or rewards.  

  ["Challenges of Real-World Reinforcement Learning"](https://arxiv.org/abs/1904.12901) by Dulac-Arnold et al.

----

  components of algorithms  ([overview](https://youtube.com/watch?v=_UVYhuATS9E&t=2m44s) by Sergey Levine `video`):   
  - generate samples / run the policy  
  - fit a model / estimate the return  
  - improve the policy  

  classifications of methods  ([overview](http://incompleteideas.net/sutton/book/ebook/node105.html) by Sutton and Barto):  
  - prediction vs control  
  - MDPs vs bandits  
  - model-based vs value-based vs policy-based  
  - on-policy vs off-policy  
  - bootstrapping vs Monte Carlo  


----
#### theory

  ["Theory of Reinforcement Learning"](http://videolectures.net/deeplearning2017_szepesvari_theory_of_rl) by Csaba Szepesvari `video`  
  ["Is a Good Representation Sufficient for Sample Efficient Reinforcement Learning"](https://youtu.be/b9I1VYEd82c?t=2h30m) by Sham Kakade `video`  

  [course](http://nanjiang.cs.illinois.edu/cs598) by Nan Jiang

----

  ["Reinforcement Learning: Theory and Algorithms"](https://rltheorybook.github.io) by Agarwal, Jiang, Kakade `book`


----
#### reinforcement learning vs supervised learning

  [differences](https://youtube.com/watch?v=2pWv7GOvuf0&t=9m37s) `video` (by David Silver):  
  - there is no supervisor, only a reward signal  
  - feedback is delayed, not instantaneous  
  - time really matters (sequential, not i.i.d. data)  
  - agent's actions affect subsequent data it receives  

  [differences](https://youtube.com/watch?v=8jQIKgTzQd4&t=50m28s) `video` (by John Schulman):  
  - no full access to analytic representation of loss function being optimized - value has to be queried by interaction with environment  
  - interacting with stateful environment (unknown, nonlinear, stochastic, arbitrarily complex) - next input depends on previous actions  

  [differences](http://videolectures.net/deeplearning2017_szepesvari_theory_of_rl/#t=2026) `video` (by Csaba Szepesvari)

----

  ["Expressivity, Trainability, and Generalization in Machine Learning"](http://blog.evjang.com/2017/11/exp-train-gen.html) by Eric Jang


----
#### model-based vs value-based vs policy-based methods

  [**model-based methods**](#model-based-methods):  
  - build prediction model for next state and reward after action  
  - space complexity asymptotically less than space required to store MDP  
  - define objective function measuring goodness of model (e.g. number of bits to reconstruct next state)  
  - plan using model (e.g. by lookahead)  
  - allows reasoning about task-independent aspects of environment  
  - allows for transfer learning across domains and faster learning  

  [**value-based methods**](#value-based-methods):  
  - estimate the optimal value function Q*(s,a) (expected total reward from state s and action a under policy π)  
  - this is the maximum value achievable under any policy  

  [**policy-based methods**](#policy-based-methods):  
  - search directly for the optimal policy (behaviour function selecting actions given states) achieving maximum expected reward  
  - often simpler to represent and learn good policies than good state value or action value functions (such as for robot grasping an object)  
  - state value function doesn't prescribe actions (dynamics model becomes necessary)  
  - action value function requires to solve maximization problem over actions (challenge for continuous / high-dimensional action spaces)  
  - focus on discriminating between several actions instead of estimating values for every state-action  
  - true objectives of expected cost is optimized (vs a surrogate like Bellman error)  
  - suboptimal values does not necessarily give suboptimal actions in every state (but optimal values do)  
  - easier generalization to continuous action spaces  

  [overview](http://youtube.com/watch?v=P_agNaSrVhc) by Michael Littman `video`  


----
#### forms of supervision

  - scalar rewards (online vs [**offline/batch learning**](#offline-reinforcement-learning), on-policy vs [**off-policy learning**](#off-policy-reinforcement-learning))
  - demonstrated behavior ([**imitation learning**](#imitation-learning), [**inverse reinforcement learning**](#inverse-reinforcement-learning))
  - self-supervision ([**unsupervised learning**](#unsupervised-reinforcement-learning))
  - auxiliary objectives ([**exploration and intrinsic motivation**](#exploration-and-intrinsic-motivation), learning task-relevant problems)

  [overview](https://youtu.be/hKeSPnvNNJ8?t=4m2s) by Sergey Levine `video`

  ["Utilities"](https://youtube.com/watch?v=yA6wXERug70) by Pieter Abbeel `video`  
  ["Rethinking State Action and Reward in Reinforcement Learning"](https://youtube.com/watch?v=MhIP1SOqlS8) by Satinder Singh `video`  


----
#### offline reinforcement learning

  Offline/batch reinforcement learning offers a mechanism for learning offline from a fixed dataset without restrictions on the quality of the data.

  ["Decisions from Data: How Offline Reinforcement Learning Will Change How We Use Machine Learning"](https://medium.com/@sergey.levine/decisions-from-data-how-offline-reinforcement-learning-will-change-how-we-use-ml-24d98cb069b0) by Sergey Levine

  [introduction](https://youtube.com/watch?v=tW-BNW1ApN8) by Sergey Levine `video`

  tutorial by Sergey Levine and Aviral Kumar [1](https://youtube.com/watch?v=9tMLmjVq6bA), [2](https://youtube.com/watch?v=536a-CvHUZ8) `video`  
  tutorial by Emma Brunskill [1](https://youtube.com/watch?v=MEK8lTaiUvQ), [2](https://youtube.com/watch?v=JZ2opp8Wy4A) `video`  

  ["Offline Reinforcement Learning"](https://youtube.com/watch?v=qgZPZREor5I) by Sergey Levine `video`  
  ["Offline RL: Challenges, Algorithms, and Benchmarks"](https://youtube.com/watch?v=IUAePhU0E7Y) by Sergey Levine `video`  
  ["The Sub-basement of RL"](https://youtube.com/watch?v=373_zVWceqA) by Dale Schuurmans `video`  

  ["Offline Reinforcement Learning: Tutorial, Review,and Perspectives on Open Problems"](https://arxiv.org/abs/2005.01643) by Levine et al. `paper`  
  ["RL Unplugged: Benchmarks for Offline Reinforcement Learning"](https://arxiv.org/abs/2006.13888) by Gulcehre et al. `paper`  
  ["Batch Reinforcement Learning"](http://tgabel.de/cms/fileadmin/user_upload/documents/Lange_Gabel_EtAl_RL-Book-12.pdf) by Lange et al. `paper`  


----
#### off-policy reinforcement learning

  Updates to a statistic of a dynamical process are said to be off-policy if their distribution does not match the dynamics of the process, particularly if the mismatch is due to the way actions are chosen. The prototypical example is learning of value function for one policy, the target policy, using data obtained while following another policy, the behavior policy.

  [overview](https://youtube.com/watch?v=xuY1xIxFx5I) by Doina Precup `video`  
  [overview](http://videolectures.net/DLRLsummerschool2018_white_policy_learning) by Martha White `video`  
  [overview](http://videolectures.net/deeplearning2017_thomas_safe_rl/#t=1821) by Philip Thomas `video`  


----
#### imitation learning

  - learn agent's behavior in environment with unknown cost function via imitation of another agent's behavior
  - use expert's demonstrations to alleviate difficulties with exploration, credit assignment and reward design

  ["Supervised Learning of Behaviors: Deep Learning, Dynamical Systems, and Behavior Cloning"](https://youtube.com/watch?v=kl_G95uKTHw) by Sergey Levine `video`  
  ["Learning Policies by Imitating Optimal Control"](https://youtube.com/watch?v=o0Ebur3aNMo) by Sergey Levine `video`  
  ["Advanced Topics in Imitation Learning and Safety"](https://youtube.com/watch?v=UClw47acYnw) by Chelsea Finn `video`  

  [overview](https://facebook.com/icml.imls/videos/428362527678268) by Yisong Yue and Hoang Le `video`  
  [overview](http://videolectures.net/DLRLsummerschool2018_daume_imitation_learning) by Hal Daume `video`  
  [overview](https://youtube.com/watch?v=0DkPUecLLpI) by Fedor Ratnikov `video` `in russian`  
  [overview](https://youtube.com/watch?v=OiS7uT7OusY) by Artem Tsypin `video` `in russian`  

  ["An Invitation to Imitation"](http://ri.cmu.edu/pub_files/2015/3/InvitationToImitation_3_1415.pdf) by Andrew Bagnell  
  ["Imitation Learning"](http://ciml.info) chapter by Hal Daume  

  ["Global Overview of Imitation Learning"](https://arxiv.org/abs/1801.06503) by Attia and Dayan `paper`  
  ["Imitation Learning: A Survey of Learning Methods"](https://researchgate.net/publication/312591539_Imitation_Learning_A_Survey_of_Learning_Methods) by Hussein et al. `paper`  

  [**interesting papers**](#interesting-papers---imitation-learning)


----
#### inverse reinforcement learning

  - infer underlying reward structure guiding agent’s behavior based on observations and model of environment  
  - learn reward structure for modelling purposes or for imitation of another agent's behavior (apprenticeship)  

  [overview](http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/) (part 2, 20:40) by Pieter Abbeel `video`  
  [overview](https://youtube.com/watch?v=d9DlQSJQAoI) by Chelsea Finn `video`  
  [overview](https://youtube.com/watch?v=J2blDuU3X1I) by Chelsea Finn `video`  
  [overview](https://youtu.be/0DkPUecLLpI?t=17m32s) by Fedor Ratnikov `video` `in russian`  

  [tutorial](https://thinkingwires.com/posts/2018-02-13-irl-tutorial-1.html) by Johannes Heidecke

  ["Apprenticeship Learning and Reinforcement Learning with Application to Robotic Control"](http://ai.stanford.edu/~pabbeel/thesis/thesis.pdf) by Pieter Abbeel `paper`  
  ["Maximum Entropy Inverse Reinforcement Learning"](https://aaai.org/Papers/AAAI/2008/AAAI08-227.pdf) by Ziebart et al. `paper`  

  [**interesting papers**](#interesting-papers---inverse-reinforcement-learning)


----
#### unsupervised reinforcement learning

  ["Unsupervised Reinforcement Learning"](https://youtube.com/watch?v=4vK6X9Jrncs) by Sergey Levine `video`  
  ["Representation Learning for Reinforcement Learning"](https://youtube.com/watch?v=YqvhDPd1UEw) by Pieter Abbeel `video`  


----
  [**exploration and intrinsic motivation**](#exploration-and-intrinsic-motivation)


----
#### multi-agent reinforcement learning

  - compete, cooperate, communicate  
  - louse individual reward in order to get a high joint reward  
  - achieve global goals from local actions  

  [overview](http://youtube.com/watch?v=CvL-KV3IBcM) by Thore Graepel `video`  
  [overview](http://youtube.com/watch?v=p_n5fF8apiE) by Michael Bowling `video`  
  [overview](http://videolectures.net/DLRLsummerschool2018_bowling_multi_agent_RL) by Michael Bowling `video`  
  [overview](http://youtube.com/watch?v=9qPhrEYIRF4) by Jakob Foerster `video`  
  [overview](http://youtube.com/watch?v=hGEz4Aumd1U) by Arsenii Ashukha `video`  
  [overview](http://youtube.com/watch?v=0OSvoYbWs9o) by Sergei Sviridov `video` `in russian`  

  [tutorial](http://karltuyls.net/wp-content/uploads/2020/06/MA-DM-ICML-ACAI.pdf) by Balduzzi, Graepel, Hughes, Jaderberg, Omidshafiei, Perolat, Tuyls `slides` `2019`  
  [tutorial](http://mlanctot.info/files/papers/Lanctot_MARL_RLSS2019_Lille.pdf) by Marc Lanctot `slides` `2019`  

  [overview](http://youtube.com/watch?v=MEUdtwQev9A) of multi-agent systems by James Wright `video`  
  [overview](http://youtube.com/watch?v=T8G5y_t9bME) of social dilemmas by Dmitry Ivanov `video` `in russian`  

  ["Autocurricula and the Emergence of Innovation from Social Interaction: A Manifesto for Multi-Agent Intelligence Research"](https://arxiv.org/abs/1903.00742) by Leibo, Hughes, Lanctot, Graepel `paper`  
  ["A Survey and Critique of Multiagent Deep Reinforcement Learning"](https://arxiv.org/abs/1810.05587) by Hernandez-Leal, Kartal, Taylor `paper`  

  [**recent interesting papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---multi-agent)


----
#### safe reinforcement learning

  [overview](http://videolectures.net/DLRLsummerschool2018_ghavamzadeh_safety_in_RL) by Mohammad Ghavamzadeh `video`  
  [overview](http://videolectures.net/deeplearning2017_thomas_safe_rl) by Philip Thomas `video`  


----
#### hierarchical reinforcement learning
 
  - simplify dimensionality of the action spaces over which we need to reason  
  - enable quick planning and execution of low-level actions (such as robot movements)  
  - provide a simple mechanism that connects plans and intentions to commands at the level of execution  
  - support rapid learning and generalisation (that humans are capable of)  

  ["The Promise of Hierarchical Reinforcement Learning"](https://thegradient.pub/the-promise-of-hierarchical-reinforcement-learning/) by Yannis Flet-Berliac  
  ["Learning in Brains and Machines: Synergistic and Modular Action"](http://blog.shakirm.com/2016/07/learning-in-brains-and-machines-3-synergistic-and-modular-action/) by Shakir Mohamed  

  [overview](https://youtube.com/watch?v=vixOKrjmu6A) by Andre Barreto `video`  
  [overview](https://youtube.com/watch?v=sdBE3P6xL7E) by Petr Kuderov `video` `in russian`  

  *Options framework:*  
	[overview](https://youtube.com/watch?v=e8b0yC6COJ8) by Doina Precup `video`  
	[overview](http://videolectures.net/DLRLsummerschool2018_precup_temporal_abstraction) by Doina Precup `video`  
	[overview](https://youtube.com/watch?v=GntIVgNKkCI) by Doina Precup `video`  
	[overview](http://videolectures.net/deeplearning2016_precup_advanced_lr) by Doina Precup `video`  

  *Feudal framework:*  
	[overview](https://vimeo.com/249557775) by David Silver `video`  

  [Hierarchical RL](http://sites.google.com/view/hrlnips2017) workshop `video`  
  [Abstraction in RL](http://rlabstraction2016.wixsite.com/icml) workshop `video`  

  [**interesting papers**](#interesting-papers---hierarchical-reinforcement-learning)



---
### exploration and intrinsic motivation

  "Reinforcement Learning is the problem of learning to control an unknown system. Like the control setting, an agent should take actions to maximize its cumulative rewards through time. Like the inference problem, the agent is initially uncertain of the system dynamics, but can learn through the transitions it observes. This leads to a fundamental trade-off: the agent may be able to improve its understanding through exploring poorly-understood states and actions, but it may be able to attain higher immediate reward through exploiting its existing knowledge."

  *exploration-exploitation tradeoff:*  
  When should the agent try out perceived non-optimal actions in order to explore the environment and potentially improve the model, and when should it exploit the optimal action in order to make useful progress on the task?

----

  [overview](http://youtube.com/watch?v=aJI_9SoBDaQ) by Andrew Barto `video`  
  [overview](http://youtu.be/DSYzHPW26Ig?t=1h58m29s) by Alex Graves `video`  
  [overview](http://youtube.com/watch?v=sGuiWX07sKw) by David Silver `video`  
  [overview](http://youtube.com/watch?v=SfCa1HQMkuw) by John Schulman `video`  
  [overview](http://youtube.com/watch?v=eM6IBYVqXEA) by Hado van Hasselt `video`  
  [overview](http://youtu.be/fIKkhoI1kF4?t=19m23s) by Emma Brunskill `video`  
  [overview](http://youtube.com/watch?v=GlTYGmVUTbM) by Ian Osband `video`  
  [overview](http://facebook.com/icml.imls/videos/2265408103721327?t=4118) by Pieter Abbeel `video`  
  [overview](http://youtube.com/watch?v=qvxgsxQFHgQ) by Sergey Ivanov `video` `in russian`  
  [overview](http://youtube.com/watch?v=EMv1AVLOnto) by Oleg Svidchenko `video` `in russian`  
  [overview](http://youtube.com/watch?v=WCE9hhPbCmc) by Maxim Kretov `video` `in russian`  

  ["Comparing Intrinsic Motivations in a Unified Framework"](https://slideslive.com/38909803/tutorial-on-comparing-intrinsic-motivations-in-a-unified-framework) by Martin Biehl `video`

----

  [**interesting papers**](#interesting-papers---exploration-and-intrinsic-motivation)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  

----

  exploration:
  - [**bandits**](#bandits)
  - [**contextual bandits**](#contextual-bandits)
  - [**bayesian exploration**](#exploration-and-intrinsic-motivation---bayesian-exploration)
  - [**auxiliary tasks**](#exploration-and-intrinsic-motivation---auxiliary-tasks)

----

  intrinsic motivation:
  - [**information theoretic and distributional models**](#exploration-and-intrinsic-motivation---information-theoretic-and-distributional-models)
    - **uncertainty motivation (novelty)**
    - **information gain motivation (bayesian surprise)**
    - **empowerment motivation**
  - [**predictive models**](#exploration-and-intrinsic-motivation---predictive-models)
    - **predictive novelty motivation (prediction error)**
    - **learning progress motivation (prediction gain)**
    - **predictive familiarity motivation (homeostasis)**
  - [**competence-based models**](#exploration-and-intrinsic-motivation---competence-based-models)
    - **incompetence motivation**
    - **competence progress motivation (automated curriculum learning)**

  ["How Can We Define Intrinsic Motivation"](http://pyoudeyer.com/epirob08OudeyerKaplan.pdf) by Oudeyer and Kaplan `paper`


----
#### exploration and intrinsic motivation - bayesian exploration

  [overview](https://youtu.be/sGuiWX07sKw?t=57m28s) by David Silver `video`  
  [overview](https://slideslive.com/38922727/bayesadaptive-deep-reinforcement-learning-via-metalearning) by Shimon Whiteson `video` *(lack of good methods for real exploration as opposed to simulated exploration)*  

----

  [**bayesian reinforcement learning**](#bayesian-reinforcement-learning) *(papers)*

----

  [**"Learning to Optimize via Posterior Sampling"**](#learning-to-optimize-via-posterior-sampling-russo-van-roy) by Russo and van Roy `paper` `summary`  
  [**"Why is Posterior Sampling Better than Optimism for Reinforcement Learning?"**](#why-is-posterior-sampling-better-than-optimism-for-reinforcement-learning-osband-van-roy) by Osband and van Roy `paper` `summary`  
  [**"A Tutorial on Thompson Sampling"**](#a-tutorial-on-thompson-sampling-russo-van-roy-kazerouni-osband-wen) by Russo et al. `paper` `summary`  
  [**"Deep Exploration via Bootstrapped DQN"**](#deep-exploration-via-bootstrapped-dqn-osband-blundell-pritzel-van-roy) by Osband et al. `paper` `summary`  
  [**"Deep Exploration via Randomized Value Functions"**](#deep-exploration-via-randomized-value-functions-osband-russo-wen-van-roy) by Osband et al. `paper` `summary`  
  ["Randomized Prior Functions for Deep Reinforcement Learning"](https://arxiv.org/abs/1806.03335) by Osband et al. `paper`  
  [**"Dropout as a Bayesian Approximation: Representing Model Uncertainty in Deep Learning"**](https://github.com/brylevkirill/notes/blob/master/Deep%20Learning.md#dropout-as-a-bayesian-approximation-representing-model-uncertainty-in-deep-learning-gal-ghahramani) by Gal et al. `paper` `summary`  
  [**"Weight Uncertainty in Neural Networks"**](#weight-uncertainty-in-neural-networks-blundell-cornebise-kavukcuoglu-wierstra) by Blundell et al. `paper` `summary`  
  [**"BBQ-Networks: Efficient Exploration in Deep Reinforcement Learning for Task-Oriented Dialogue Systems"**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#bbq-networks-efficient-exploration-in-deep-reinforcement-learning-for-task-oriented-dialogue-systems-lipton-li-gao-li-ahmed-deng) by Lipton et al. `paper` `summary`  
  [**"Noisy Networks for Exploration"**](#noisy-networks-for-exploration-fortunato-et-al) by Fortunato et al. `paper` `summary`  

----

  [**interesting papers**](#interesting-papers---exploration-and-intrinsic-motivation---bayesian-exploration)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  

----

>	"Bayesian reinforcement learning provides approach to optimal exploration during learning and beyond. Prior information about the problem is represented in parametric form, and Bayesian inference is used to incorporate any new information about the model. Thus the exploration-exploitation problem can be handled as an explicit sequential decision problem, where the agent seeks to maximize future expected return with respect to its current uncertainty on the model. The decision-making process is significantly more complex since it involves reasoning about all possible models and courses of action."

>	"The optimal Bayesian policy chooses actions based not only on how they will affect the next state of the system, but also based on how they will affect the next belief state; and, since a better knowledge of the MDP will typically lead to greater future reward, the Bayesian policy will very naturally trade off between exploring the system to gain more knowledge, and exploiting its current knowledge of the system. Unfortunately, while the Bayesian approach provides a very elegant solution to the exploration/exploitation problem, it is typically not possible to compute the Bayesian policy exactly."

>	"Since the dimension of the belief state grows polynomially in the number of states and actions, computing the Bayesian value function using value iteration or other methods is typically not tractable. One exception, where the Bayesian approach is tractable, is the domain of a k-armed bandit (i.e., an MDP with one state and k actions, where the rewards are unknown). In this case, the Bayesian approach leads to the well-known Gittins indices. However, the approach does not scale analytically to multi-state MDPs. This has lead to numerous methods that approximate the Bayesian exploration policy."


----
#### exploration and intrinsic motivation - auxiliary tasks

  [**"Hindsight Experience Replay"**](#hindsight-experience-replay-andrychowicz-et-al) by Andrychowicz et al. `paper` `summary`  
  [**"Reinforcement Learning with Unsupervised Auxiliary Tasks"**](#reinforcement-learning-with-unsupervised-auxiliary-tasks-jaderberg-mnih-czarnecki-schaul-leibo-silver-kavukcuoglu) by Jaderberg et al. `paper` `summary`  
  ["Loss is Its Own Reward: Self-Supervision for Reinforcement Learning"](https://arxiv.org/abs/1612.07307) by Shelhamer et al. `paper`  
  ["Feature Control as Intrinsic Motivation for Hierarchical Reinforcement Learning"](https://arxiv.org/abs/1705.06769) by Dilokthanakul et al. `paper`  

  [**interesting papers**](#interesting-papers---exploration-and-intrinsic-motivation---auxiliary-tasks)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  


----
#### exploration and intrinsic motivation - information theoretic and distributional models

>	"This approach is based on the use of representations, built by an agent, that estimate the distributions of probabilities of observing certain events ek in particular contexts, defined as mathematical configurations in the sensorimotor flow. There are several types of such events, but the probabilities that are measured are typically either the probability of observing a certain state SMk in the sensorimotor flow, denoted P(SMk), or the probability of observing particular transitions between states, such as P(SMk(t), SMl(t+1)), or the probability of observing a particular state after having observed a given state P(SMk(t+1) | SMl(t)). Here, the states SMk can either be direct numerical prototypes or complete regions within the sensorimotor space (and it may involve a mechanism for discretizing the space). We will consider all these eventualities possible and just use the general notation P(ek). We will assume that the agent possesses a mechanism that allows it to build internally, and as it experiences the world, an estimation of the probability distribution of events across the whole space E of possible events (but the space of possible events is not predefined and should also be discovered by the agent, so typically this is an initially empty space that grows with experience)."


  - **uncertainty motivation (novelty)**

	> "The tendency to be intrinsically attracted by novelty has often been used as an example in the literature on intrinsic motivation. A straightforward manner to computationally implement it is to build a system that, for every event ek that is actually observed, will generate a reward r(ek) inversely proportional to its probability of observation: r(ek, t) = C·(1 − P(ek, t)), where C is a constant."

	find rare inputs under a density model

	[**"Action-Conditional Video Prediction using Deep Networks in Atari Games"**](#action-conditional-video-prediction-using-deep-networks-in-atari-games-oh-guo-lee-lewis-singh) by Oh et al. `paper` `summary`  
	[**"Unifying Count-Based Exploration and Intrinsic Motivation"**](#unifying-count-based-exploration-and-intrinsic-motivation-bellemare-srinivasan-ostrovski-schaul-saxton-munos) by Bellemare et al. `paper` `summary`  
	[**"Count-Based Exploration with Neural Density Models"**](#count-based-exploration-with-neural-density-models-ostrovski-bellemare-van-den-oord-munos) by Ostrovski et al. `paper` `summary`  
	[**"\#Exploration: A Study of Count-Based Exploration for Deep Reinforcement Learning"**](#exploration-a-study-of-count-based-exploration-for-deep-reinforcement-learning-tang-et-al) by Tang et al. `paper` `summary`  
	[**"EX2: Exploration with Exemplar Models for Deep Reinforcement Learning"**](#ex2-exploration-with-exemplar-models-for-deep-reinforcement-learning-fu-co-reyes-levine) by Fu et al. `paper` `summary`  
	[**"Episodic Curiosity through Reachability"**](#episodic-curiosity-through-reachability-savinov-et-al) by Savinov et al. `paper` `summary`  

	[**interesting papers**](#interesting-papers---exploration-and-intrinsic-motivation---information-theoretic-and-distributional-models---uncertainty-motivation)  
	[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  


  - **information gain motivation (bayesian surprise)**

	> "It has been proposed in psychology and education that humans have a natural propensity to learn and assimilate. In information theoretic terms, this notion of assimilation or of “pleasure of learning” can be modeled by the decrease of uncertainty in the knowledge about the world that the agent possesses after an event ek has happened: r(ek, t) = C·(H(E, t) − H(E, t+1)), where H is entropy."

	minimize entropy of belief over environment dynamics ~ maximize KL divergence between posterior (after seeing observation) and prior (before seeing observation)

	[overview](https://youtu.be/DSYzHPW26Ig?t=2h1m40s) by Alex Graves `video`

	["Reinforcement Driven Information Acquisition In Non-Deterministic Environments"](https://researchgate.net/publication/277286220_Reinforcement_Driven_Information_Acquisition_In_Non-Deterministic_Environments) by Storck, Hochreiter, Schmidhuber `paper`  
	[**"Universal Knowledge-Seeking Agents for Stochastic Environments"**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#universal-knowledge-seeking-agents-for-stochastic-environments-orseau-lattimore-hutter) by Orseau et al. `paper` `summary` ([**Knowledge-Seeking Agent**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#universal-artificial-intelligence---knowledge-seeking-agent) theory by Hutter and Orseau)  
	[**"Curiosity Driven Reinforcement Learning for Motion Planning on Humanoids"**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#curiosity-driven-reinforcement-learning-for-motion-planning-on-humanoids-frank-leitner-stollenga-forster-schmidhuber) by Frank et al. `paper` `summary`  
	[**"VIME: Variational Information Maximizing Exploration"**](#vime-variational-information-maximizing-exploration-houthooft-chen-duan-schulman-turck-abbeel) by Houthooft et al. `paper` `summary`  
	[**"Planning to Be Surprised: Optimal Bayesian Exploration in Dynamic Environments"**](#planning-to-be-surprised-optimal-bayesian-exploration-in-dynamic-environments-sun-gomez-schmidhuber) by Sun et al. `paper` `summary`  
	[**"Model-Based Active Exploration"**](#model-based-active-exploration-shyam-jaskowski-gomez) by Shyam et al. `paper` `summary`  

	[**interesting papers**](#interesting-papers---exploration-and-intrinsic-motivation---information-theoretic-and-distributional-models---information-gain-motivation)  
	[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  


  - **empowerment motivation**

	> "A reward measure that pushes an agent to produce sequences of actions that can transfer a maximal amount of information to its sensors through the environment. It is defined as the channel capacity from the sequence of actions At, At+1, ..., At+n−1 to the perceptions St+n after an arbitrary number of timesteps: r(At, At+1, ..., At+n−1 →  St+n) = max {p(a)} I(At, At+1, ..., At+n−1, St+n), where p(a) is the probability distribution function of the action sequences a=(at, at+1, ..., at+n−1) and I is mutual information."

	maximally influence sensory inputs ~ maximize channel capacity or mutual information between actions and future states, i.e. information contained in a about s' or information that can be "injected" into s' by a, to encourage agent to occupy states from which it can reach most states within its planning horizon and to control its future as much as possible

	[overview](https://youtu.be/DSYzHPW26Ig?t=2h9m23s) by Alex Graves `video`

	[**"Empowerment - An Introduction"**](#an-introduction-salge-glackin-polani---empowerment) by Salge et al. `paper` `summary`  
	[**"Variational Information Maximisation for Intrinsically Motivated Reinforcement Learning"**](#variational-information-maximisation-for-intrinsically-motivated-reinforcement-learning-mohamed-rezende) by Mohamed and Rezende `paper` `summary`  
	[**"Variational Intrinsic Control"**](#variational-intrinsic-control-gregor-rezende-wierstra) by Gregor et al. `paper` `summary`  

	[**interesting-papers**](#interesting-papers---exploration-and-intrinsic-motivation---information-theoretic-and-distributional-models---empowerment)  
	[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  


----
#### exploration and intrinsic motivation - predictive models

>	"Often, knowledge and expectations in agent are not represented by complete probability distributions, but rather based on the use of predictors such as neural networks that make direct predictions about future events. These predictors, denoted Π, are typically used to predict some properties Prk or sensorimotor states SMk that will happen in the future (close or far) given the current sensorimotor context SM(t) and possibly the past sensorimotor context. We will denote all properties and states under the generic notation ek. We will also use the notation SM(→ t) to denote a structure which encodes the current sensorimotor context and possibly the past contexts. Thus, a general prediction of a system will be denoted: Π(SM(→ t)) = ek^(t+1). We then define Er(t) as the error of this prediction, being the distance between the predicted event ek^(t+1) and the event that actually happens ek(t+1): Er(t) = ‖ ek^(t+1) − ek(t+1) ‖."


  - **predictive novelty motivation (prediction error)**

	> "Interesting situations are those for which the prediction errors are highest: r(SM(→ t)) = C·Er(t), where C is a constant."

	choose action to maximize prediction error in observation - predict in latent space in order to avoid noise addiction

	[overview](https://youtu.be/DSYzHPW26Ig?t=1h59m37s) by Alex Graves `video`

	[**"Learning to Play with Intrinsically-Motivated Self-Aware Agents"**](#learning-to-play-with-intrinsically-motivated-self-aware-agents-haber-et-al) by Haber et al. `paper` `summary`  
	[**"Large-Scale Study of Curiosity-Driven Learning"**](#large-scale-study-of-curiosity-driven-learning-burda-edwards-pathak-storkey-darrell-efros) by Burda et al. `paper` `summary`  
	[**"Curiosity-driven Exploration by Self-supervised Prediction"**](#curiosity-driven-exploration-by-self-supervised-prediction-pathak-agrawal-efros-darrell) by Pathak et al. `paper` `summary`  
	[**"Exploration by Random Network Distillation"**](#exploration-by-random-network-distillation-burda-edwards-storkey-klimov) by Burda et al. `paper` `summary`  
	[**"Self-Supervised Exploration via Disagreement"**](#self-supervised-exploration-via-disagreement-pathak-et-al) by Pathak et al. `paper` `summary`  

	[**interesting papers**](#interesting-papers---exploration-and-intrinsic-motivation---predictive-models---predictive-novelty-motivation)  
	[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  


  - **learning progress motivation (prediction gain)**

	> "Several researchers have proposed another manner to model optimal incongruity which avoids the problem of setting a threshold, and is related to the information gain measurement described in the information theoretic section above. It consists in modeling intrinsic motivation with a system that generates rewards when predictions improve over time. Thus, the system will try to maximize prediction progress, i.e. the decrease of prediction errors, i.e. effectively reward knowledge acquisition per se. This corresponds to the concept of epistemic curiosity proposed by (Berlyne, 1965). A first computational formalization was proposed by (Schmidhuber, 1991). It consists in measuring the difference in prediction error of the predictor Π, about the same sensorimotor context SM(→ t), between the first prediction and a second prediction made just after the predictor has been updated with a learning rule: r(SM→ t) = Er(t) − E'r(t), where E'r(t) = ‖ Π'(SM(→ t)) − ek(t+1) ‖ with Π' being the updated predictor after the learning update due to the prediction Π(SM(→ t)) and the perception of the actual consequence ek(t+1)."

	maximize change in prediction error before and after seeing an observation - prediction gain approximates information gain

	[overview](https://youtu.be/DSYzHPW26Ig?t=2h2m39s) by Alex Graves `video`

	["A Possibility for Implementing Curiosity and Boredom in Model-Building Neural Controllers"](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.957) by Schmidhuber `paper` ([**Artificial Curiosity and Creativity**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#artificial-curiosity-and-creativity) theory by Schmidhuber)  
	["Adaptive Confidence and Adaptive Curiosity"](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.34.5686) by Schmidhuber `paper` ([**Artificial Curiosity and Creativity**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#artificial-curiosity-and-creativity) theory by Schmidhuber)  
	["Curious Model-building Control Systems"](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.2597) by Schmidhuber `paper` ([**Artificial Curiosity and Creativity**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#artificial-curiosity-and-creativity) theory by Schmidhuber)  
	["What's Interesting?"](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#whats-interesting-schmidhuber) by Schmidhuber `paper` `summary` ([**Artificial Curiosity and Creativity**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#artificial-curiosity-and-creativity) theory by Schmidhuber)  
	["Intrinsic Motivation Systems for Autonomous Mental Development"](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.107.666) by Oudeyer et al. `paper`  
	["Exploration in Model-based Reinforcement Learning by Empirically Estimating Learning Progress"](https://papers.nips.cc/paper/4642-exploration-in-model-based-reinforcement-learning-by-empirically-estimating-learning-progress) by Lopes et al. `paper`  
	[**"Automated Curriculum Learning for Neural Networks"**](#automated-curriculum-learning-for-neural-networks-graves-bellemare-menick-munos-kavukcuoglu) by Graves et al. `paper` `summary`  
	["Adapting Behaviour for Learning Progress"](https://arxiv.org/abs/1912.06910) by Schaul et al. `paper`  

	[**interesting papers**](#interesting-papers---exploration-and-intrinsic-motivation---predictive-models---learning-progress-motivation)  
	[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  


  - **predictive familiarity motivation (homeostasis)**

	> "In the psychology literature, intrinsic motivations refer generally to mechanisms that push organisms to explore their environment. Yet, there are direct variants of previous computational systems that are both simple and correspond intuitively to existing forms of human motivation. For example, a slight mathematical variation of predictive novelty motivation would model a motivation to search for situation which are very predictable, and thus familiar: r(SM(→ t)) = C/Er(t), where C is a constant. It would actually be sound to consider this kind of motivation as intrinsic, in spite of the fact that it will typically not push an organism to explore its environment."

	[**"SMiRL: Surprise Minimizing RL in Dynamic Environments"**](#smirl-surprise-minimizing-rl-in-dynamic-environments-berseth-et-al) by Berseth et al. `paper` `summary`  
	["Information Theoretically Aided Reinforcement Learning for Embodied Agents"](https://arxiv.org/abs/1605.09735) by Montufar et al. `paper`  


----
#### exploration and intrinsic motivation - competence-based models

>	"A third major computational approach to intrinsic motivation is based on measures of competence that an agent has for achieving self-determined results or goals. Central here is the concept of “challenge”, with associated measures of difficulty as well as measures of actual performance. A “challenge” or “goal” here will be any sensorimotor configuration SMk, or any set {Pk} of properties of a sensorimotor configuration, that an agent sets by itself and that it tries to achieve through action. It is the properties of the achievement process, rather than the “meaning” of the particular goal being achieved, that will determine the level of interestingness of the associated activity. While prediction mechanisms or probability models, as used in previous sections, can be used in the goal-reaching architecture, they are not mandatory (for example, one can implement systems that try to achieve self-generated goals through Q-learning and never explicitly make predictions of future sensorimotor contexts). Furthermore, while in some cases, certain competence-based and knowledge-based models of intrinsic motivation might be somewhat similar, they may often produce very different behaviors. Indeed, the capacity to predict what happens in a situation can be sometimes only loosely coupled to the capacity to modify a situation in order to achieve a given self-determined goal. After a certain amount of time, bounded for example by a timeout Tg, a motivation module compares the goal that was initially set and the current situation to assess to what extent it was reached, i.e. measure the competence of the agent on goal gk at time tg: la(gk, tg) = ‖ gk^(tg) − gk(tg)) ‖. The “interestingness”, and thus reward value, of the goal gk is then derived from this competence measure."


  - **competence progress motivation (automated curriculum learning)**

	> "Maximizing incompetence does not model very well the psychological models of optimal challenge and “flow” proposed by (Csikszentmihalyi, 1991). Flow refers to the state of pleasure related to activities for which difficulty is optimal: neither too easy nor too difficult. As difficulty of a goal can be modeled by the (mean) performance in achieving this goal, a possible manner to model flow would be to introduce two thresholds defining the zone of optimal difficulty. Yet, the use of thresholds can be rather fragile, require hand tuning and possibly complex adaptive mechanism to update these thresholds during the robot’s lifetime. Another approach can be taken, which avoids the use of thresholds. It consists in defining the interestingness of a challenge as the competence progress that is experienced as the robot repeatedly tries to achieve it. So, a challenge for which a robot is bad initially but for which it is rapidly becoming good will be highly rewarding. Thus, a first manner to implement flow motivation would be: r(SM(→ t), gk, tg) = C·(la(gk, tg−θ) − la(gk, tg)) corresponding to the difference between the current performance for task gk and the performance corresponding to the last time gk was tried, at a time denoted tg−θ."

	[**"Driven by Compression Progress: A Simple Principle Explains Essential Aspects of Subjective Beauty, Novelty, Surprise, Interestingness, Attention, Curiosity, Creativity, Art, Science, Music, Jokes"**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#driven-by-compression-progress-a-simple-principle-explains-essential-aspects-of-subjective-beauty-novelty-surprise-interestingness-attention-curiosity-creativity-art-science-music-jokes-schmidhuber) by Schmidhuber `paper` `summary` ([**Artificial Curiosity and Creativity**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#artificial-curiosity-and-creativity) theory by Schmidhuber) ([overview](https://youtu.be/DSYzHPW26Ig?t=2h7m22s) by Alex Graves `video`) *(maximizing compression progress)*  
	[**"PowerPlay: Training an Increasingly General Problem Solver by Continually Searching for the Simplest Still Unsolvable Problem"**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#powerplay-training-an-increasingly-general-problem-solver-by-continually-searching-for-the-simplest-still-unsolvable-problem-schmidhuber) by Schmidhuber `paper` `summary`  
	[**"Automated Curriculum Learning for Neural Networks"**](#automated-curriculum-learning-for-neural-networks-graves-bellemare-menick-munos-kavukcuoglu) by Graves et al. `paper` `summary` *(maximizing prediction gain / complexity gain)*  
	[**"Automatic Goal Generation for Reinforcement Learning Agents"**](#automatic-goal-generation-for-reinforcement-learning-agents-held-geng-florensa-abbeel) by Held et al. `paper` `summary` *(optimally difficult goals)*  
	["Automatic Curriculum Learning For Deep RL: A Short Survey"](https://arxiv.org/abs/2003.04664) by Portelas et al. `paper`  

	[**interesting papers**](#interesting-papers---exploration-and-intrinsic-motivation---competence-based-models---maximizing-competence-motivation)  
	[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  



---
### bandits

  reinforcement learning problem with single state

----

  [overview](http://youtu.be/sGuiWX07sKw?t=11m46s) by David Silver `video`  
  [overview](http://youtube.com/watch?v=eJ3wZ14RRBQ) by Csaba Szepesvari `video`  
  [overview](http://youtu.be/fIKkhoI1kF4?t=19m23s) by Emma Brunskill `video`  
  [overview](http://videolectures.net/DLRLsummerschool2018_lattimore_bandits) by Tor Lattimore `video`  
  [overview](https://youtube.com/watch?v=M6DNMESf5Xk) by Nicolo Cesa-Bianchi `video`  
  [overview](https://youtu.be/e1sAltJhG3k?t=40m52s) by Sergey Nikolenko `video` `in russian`  

  tutorial by Csaba Szepesvari
	([part 1](https://youtube.com/watch?v=VVcLnAoU9Gw),
	[part 2](https://youtube.com/watch?v=cknukHreMdI),
	[part 3](https://youtube.com/watch?v=ruIO79C2IQc)) `video`

  tutorial by Nicolo Cesa-Bianci
	([part 1](https://youtube.com/watch?v=zjLah88ukko),
	[part 2](https://youtube.com/watch?v=YuuUvAJh40o)) `video`

----

  [overview](http://banditalgs.com/2016/09/04/bandits-a-new-beginning/) by Csaba Szepesvari

  ["Efficient Experimentation and the Multi-Armed Bandit"](http://iosband.github.io/2015/07/19/Efficient-experimentation-and-multi-armed-bandits.html) by Ian Osband  
  ["Optimism in the Face of Uncertainty: the UCB1 Algorithm"](http://jeremykun.com/2013/10/28/optimism-in-the-face-of-uncertainty-the-ucb1-algorithm/) by Jeremy Kun  
  ["Adversarial Bandits and the Exp3 Algorithm"](http://jeremykun.com/2013/11/08/adversarial-bandits-and-the-exp3-algorithm/) by Jeremy Kun  

  [example implementation](http://jeremykun.com/2013/12/09/bandits-and-stocks/) by Jeremy Kun

----

  course by Csaba Szepesvari and Tor Lattimore:  
	["Bandits: A new beginning"](http://banditalgs.com/2016/09/04/bandits-a-new-beginning/)  
	["Finite-armed stochastic bandits: Warming up"](http://banditalgs.com/2016/09/04/stochastic-bandits-warm-up/)  
	["First steps: Explore-then-Commit"](http://banditalgs.com/2016/09/14/first-steps-explore-then-commit/)  
	["The Upper Confidence Bound (UCB) Algorithm"](http://banditalgs.com/2016/09/18/the-upper-confidence-bound-algorithm/)  
	["Optimality concepts and information theory"](http://banditalgs.com/2016/09/22/optimality-concepts-and-information-theory/)  
	["More information theory and minimax lower bounds"](http://banditalgs.com/2016/09/28/more-information-theory-and-minimax-lower-bounds/)  
	["Instance dependent lower bounds"](http://banditalgs.com/2016/09/30/instance-dependent-lower-bounds/)  
	["Adversarial bandits"](http://banditalgs.com/2016/10/01/adversarial-bandits/)  
	["High probability lower bounds"](http://banditalgs.com/2016/10/14/high-probability-lower-bounds/)  
	["Contextual bandits, prediction with expert advice and Exp4"](http://banditalgs.com/2016/10/14/exp4/)  
	["Stochastic Linear Bandits and UCB"](http://banditalgs.com/2016/10/19/stochastic-linear-bandits/)  
	["Ellipsoidal confidence sets for least-squares estimators"](http://banditalgs.com/2016/10/20/lower-bounds-for-stochastic-linear-bandits/)  
	["Sparse linear bandits"](http://banditalgs.com/2016/11/13/ellipsoidal-confidence-bounds-for-least-squares-estimators/)  
	["Lower bounds for stochastic linear bandits"](http://banditalgs.com/2016/11/21/sparse-stochastic-linear-bandits/)  
	["Adversarial linear bandits"](http://banditalgs.com/2016/11/24/adversarial-linear-bandits/)  
	["Adversarial linear bandits and the curious case of linear bandits on the unit ball"](http://banditalgs.com/2016/11/25/adversarial-linear-bandits-and-the-curious-case-of-the-unit-ball/)  

  course by Sebastien Bubeck
	([part 1](https://blogs.princeton.edu/imabandit/2016/05/11/bandit-theory-part-i/),
	[part 2](https://blogs.princeton.edu/imabandit/2016/05/13/bandit-theory-part-ii/))

----

  ["Bandit Algorithms"](http://downloads.tor-lattimore.com/banditbook/book.pdf) book by Tor Lattimore and Csaba Szepesvari  
  ["Introduction to Multi-Armed Bandits"](http://slivkins.com/work/MAB-book.pdf) book by Aleksandrs Slivkins  

----

  "Bandit feedback means we only observe the feedback δ(x,y) for the specific y that was predicted, but not for any other possible (counterfactual) predictions Y\{y} unlike in supervised learning. The feedback is just a number, called the loss δ: X × Y → R. Smaller numbers are desirable. In general, the loss is the (noisy) realization of a stochastic random variable. The expected loss - called risk - of a hypothesis R(h) is R(h) = Ex∼Pr(X) Ey∼h(x) [δ(x,y)] = Eh [δ(x,y)]. The aim of learning is to find a hypothesis h∈ H that has minimum risk."

  "Most interactive systems (e.g. search engines, recommender systems, ad platforms) record large quantities of log data which contain valuable information about the system’s performance and user experience. For example, the logs of an ad-placement system record which ad was presented in a given context and whether the user clicked on it. While these logs contain information that should inform the design of future systems, the log entries do not provide supervised training data in the conventional sense. This prevents us from directly employing supervised learning algorithms to improve these systems. In particular, each entry only provides bandit feedback since the loss/reward is only observed for the particular action chosen by the system (e.g. the presented ad) but not for all the other actions the system could have taken. Moreover, the log entries are biased since actions that are systematically favored by the system will by over-represented in the logs. Learning from historical logs data can be formalized as batch learning from logged bandit feedback. Unlike the well-studied problem of online learning from bandit feedback, this setting does not require the learner to have interactive control over the system. Learning in such a setting is closely related to the problem of off-policy evaluation in reinforcement learning - we would like to know how well a new system (policy) would perform if it had been used in the past. This motivates the use of counterfactual estimators. Following an approach analogous to Empirical Risk Minimization, it was shown that such estimators can be used to design learning algorithms for batch learning from logged bandit feedback. Batch learning from logged bandit feedback is an instance of causal inference."

  "Supervised learning is essentially observational: some data has been collected and subsequently algorithms are run on it. Online supervised learning doesn't necessarily work this way, but mostly online techniques have been used for computational reasons after data collection. In contrast, counterfactual learning is very difficult do to observationally. Diverse fields such as economics, political science, and epidemiology all attempt to make counterfactual conclusions using observational data, essentially because this is the only data available (at an affordable cost). When testing a new medicine, however, the standard is to run a controlled experiment, because with control over the data collection more complicated conclusions can be made with higher confidence. Analogously, reinforcement learning is best done “in the loop”, with the algorithm controlling the collection of data which is used for learning."

----

  "The UCB family of algorithms use the problem structure to derive tight optimistic upper bounds. While these algorithms are simple and have been used in various applications with success, they lack the ability to incorporate structured prior information such as arm dependency or different reward policies without requiring complex and difficult re-analysis of the upper bounds. Bayes-UCB is a Bayesian index policy that improves on UCB in Bayesian bandits by taking advantage of the prior distribution.

  Thompson sampling works by choosing an arm based on its probability of being the best arm. The method draws a sample from the decision maker’s current belief distribution for each arm and then chooses the arm that yielded the highest sample. The performance of Thompson sampling has been proved to be near optimal, and it is simple and efficient to implement. Thompson sampling can easily be adapted to a wide range of problem structures and prior distributions. For example, one can reject sets of samples that contradict contextual information. However, the simplicity of the method makes it also difficult to improve its performance.

  Gittins indices exploit the weak dependence between actions to compute the optimal action in time that is linear in the number of arms. Gittins indices, however, are guaranteed to be optimal only for the basic multi-armed bandit problem, require a discounted infinite-horizon objective, and provably cannot be extended to most interesting and practical problems which involve correlations between arms or an additional context."

  ["Multi Armed Bandits and Exploration Strategies"](http://sudeepraja.github.io/Bandits/)



---
### contextual bandits

  reinforcement learning problem with next state not depending on earlier actions

----

  [overview](https://youtu.be/sGuiWX07sKw?t=1h29m7s) by David Silver `video`  
  [overview](https://youtube.com/watch?v=A6wNJ4-MpIg) by Alekh Agarwal and John Langford `video`  
  [overview](https://vimeo.com/240429210) by John Langford and Alekh Agarwal `video`  
  [overview](https://youtu.be/zr6H4kR8vTg) by John Langford `video`  
  [overview](https://youtu.be/GXjc-tomqpo) by Dale Schuurmans `video`  
  [overview](https://youtu.be/IWuMb0A09po) by Dale Schuurmans `video`  
  [overview](https://youtu.be/N5x48g2sp8M) by Robert Schapire `video`  

----

  ["Contextual Bandits"](http://hunch.net/?p=298) by John Langford  
  ["Counterfactual Reasoning and Learning from Logged Data"](http://timvieira.github.io/blog/post/2016/12/19/counterfactual-reasoning-and-learning-from-logged-data/) by Tim Vieira  

----

  ["A Contextual-Bandit Approach to Personalized News Article Recommendation"](https://arxiv.org/abs/1003.0146) by Li, Chu, Langford, Schapire `paper` ([overview](https://coursera.org/lecture/fundamentals-of-reinforcement-learning/jonathan-langford-contextual-bandits-for-real-world-reinforcement-learning-GkDVA) by John Langford `video`, [overview](https://youtu.be/B4Fk2KNHzFY?t=1h12m58s) by Konstantin Vorontsov `video` `in russian`)  
  ["Doubly Robust Policy Evaluation and Learning"](https://arxiv.org/abs/1103.4601) by Dudik, Langford, Li `paper` ([overview](https://youtu.be/gzxRDw3lXv8?t=35m45s) by Robert Schapire `video`) ([notes](https://medium.com/@sharaf/a-paper-a-day-12-doubly-robust-policy-evaluation-and-learning-7e6a09665d7f))  
  ["Taming the Monster: A Fast and Simple Algorithm for Contextual Bandits"](https://arxiv.org/abs/1402.0555) by Agarwal et al. `paper` ([overview](https://youtube.com/watch?v=mi_G5tw7Etg) by Alekh Agarwal `video`) ([overview](https://youtu.be/gzxRDw3lXv8?t=37m8s) by Robert Schapire `video`)  
  [**"Making Contextual Decisions with Low Technical Debt"**](#making-contextual-decisions-with-low-technical-debt-agarwal-et-al) by Agarwal et al. `paper` `summary`  
  ["A Contextual Bandit Bake-off"](https://arxiv.org/abs/1802.04064) by Bietti, Agarwal, Langford `paper` ([overview](https://youtu.be/zr6H4kR8vTg?t=50m36s) by John Langford `video`)  

----

  ["Multi-armed Bandit Experiments in the Online Service Economy"](https://research.google.com/pubs/pub42550.html) by Steven Scott `paper`

  ["Reinforcement Learning in Industry"](http://videolectures.net/deeplearning2017_le_roux_recommendation_system/) by Nicolas Le Roux `video`  
  ["Counterfactual Evaluation and Learning for Search, Recommendation and Ad Placement"](http://www.cs.cornell.edu/~adith/CfactSIGIR2016/) by Thorsten Joachims and Adith Swaminathan `video`  
  ["Deep Learning from Logged Interventions"](https://youtube.com/watch?v=lzA5K4im2no) by Thorsten Joachims `video`  

  [**Microsoft Custom Decision Service**](#making-contextual-decisions-with-low-technical-debt-agarwal-et-al)

----

  "Contextual bandits are simple reinforcement learning problems without persistent state. At each step an agent is presented with a context x and a choice of one of K possible actions a. Different actions yield different unknown rewards r. The agent must pick the action that yields the highest expected reward. The context is assumed to be presented independent of any previous actions, rewards or contexts. An agent builds a model of the distribution of the rewards conditioned upon the action and the context: P(r|x,a,w). It then uses this model to pick its action. Note, importantly, that an agent does not know what reward it could have received for an action that it did not pick, a difficulty often known as “the absence of counterfactual”. As the agent’s model P(r|x,a,w) is trained online, based upon the actions chosen, unless exploratory actions are taken, the agent may perform suboptimally."

  "Removing credit assignment problem from reinforcement learning yields contextual bandit setting which is tractable similar to supervised learning problems."

  "In supervised learning you know how good actions you didn't take are as well, which is not the case in bandits and in reinforcement learning in general."

----

  goal:  
  - learn through experimentation (in policies from given class, not in states of environment) to do (almost) as well as best policy from policy class  
  - assume policy class finite, but typically extremely large  
  - policies may be very complex and expressive  

  problems:  
  - need to be learning about all policies simultaneously while also performing as well as the best one  
  - when action selected, only observe reward for policies that would have chosen same action  
  - exploration vs exploitation on gigantic scale (exploration in space of policies)  

  challenges:  
  - computational efficiency  
  - very large policy space  
  - optimal statistical performance (regret)  
  - adversarial setting  

  effective methods:  
  - obtain sound statistical estimates from biased samples  
  - learn highly complex behaviors (i.e. policies from very large space)  
  - attain efficiency using previously developed methods (i.e. oracle)  
  - harness power of combining policies  
  - achieve explicit conditions using an optimization approach  

----

  "A/B testing only uses data collected using a policy to evaluate this policy. Using a fixed exploration dataset, accurate counterfactual estimates of how arbitrary policies would have performed can be computed without actually running them in real time. This is precisely the question A/B testing attempts to answer, except A/B testing must run a live experiment to test each policy."

  "Contextual bandits allow testing and optimization over exponentially more policies for a given number of events. In one realistic scenario, one can handle 1 billion policies for the data collection cost of 21 A/B tests. The essential reason for such an improvement is that each data point can be used to evaluate all the policies picking the same action for the same context (i.e., make the same decision for the same input features rather than just a single policy as in A/B testing). An important property is that policies being tested do not need to be approved, implemented in production, and run live for a period of time (thus saving much business and engineering effort). Furthermore, the policies do not even need to be known during data collection."



---
### model-based methods

  - learning a model of the world's state and state-transition dynamics  
  - planning using the model  
	* improving a policy or value function through computation rather than by gathering further data  
	* using the model to look ahead from some states, imagining from each something about its future  


  two fundamental problems in sequential decision making ([overview](https://youtu.be/2pWv7GOvuf0?t=1h16m16s) by David Silver `video`):  
  - reinforcement learning  
	* environment is initially unknown  
	* agent interacts with environment  
	* agent improves its policy  
  - planning  
	* model of environment is known or learned  
	* agent performs computations with model (without interaction with environment)  
	* agent improves its policy  


  model-free methods:  
  - *(plus)* can handle systems with arbitrarily complex dynamics and costs  
  - *(minus)* significantly less sample-efficient  

  model-based methods:  
  - *(plus)* sample efficiency: learn from scratch with a small number of trials  
  - *(minus)* modeling bias: complex dynamics and costs can cause learning to fail  


  failure modes of model-based RL ([overview](https://facebook.com/icml.imls/videos/2366831430268790?t=601) by David Silver `video`):  
  - *observation model*: predict/simulate all observations  
    * model focuses on irrelevant details  
    * planning is intractable (too many pixels)  
  - *environment model*: predict/simulate true state  
    * true state is unknown, unknowable  
    * planning is intractable (agent is smaller than world)  
  - *one-step model*: focus on predictions over a single step  
    * model errors compound over many steps  
    * planning is intractable (world has long horizon)  


  planning methods:  
  - forward methods  
	* lookahead tree building  
  - global methods  
	* approximate dynamic programming  
	* policy search  
	* hybrids  
  - hybrid forward and global methods  

----

  ["The Next Big Step in AI: Planning with a Learned Model"](https://youtube.com/watch?v=6-Uiq8-wKrg) by Richard Sutton `video`  
  ["The Grand Challenge of Knowledge"](http://www.fields.utoronto.ca/video-archive/2016/10/2267-16158) (41:35) by Richard Sutton `video`  
  ["Open Questions in Model-based RL"](https://youtube.com/watch?v=OeIVfQz3FUc) by Richard Sutton `video`  
  ["Toward a General AI-Agent Architecture"](https://slideslive.com/38924024/toward-a-general-aiagent-architecture) by Richard Sutton `video` *(SuperDyna)*  

  ["Deep Networks for Model-based RL"](https://pscp.tv/w/1mnGelLjoBWKX) by Timothy Lillicrap `video`

  ["Planning and Models"](https://youtube.com/watch?v=Xrxrd8nl4YI) by Hado van Hasselt `video`  
  ["Integrating Learning and Planning"](https://youtube.com/watch?v=ItMutbeOHtc) by David Silver `video`  
  ["Value Focused Models"](https://facebook.com/icml.imls/videos/2366831430268790?t=410) by David Silver `video`  
  ["Model-Based RL"](https://youtube.com/watch?v=8JbZStpxg80) by Martha White `video`  

  ["Structure and Priors in RL"](https://slideslive.com/38915870/panel-questions) discussion `video`

----

  ["The Bitter Lesson"](http://www.incompleteideas.net/IncIdeas/BitterLesson.html) by Richard Sutton ([talk](http://www.fields.utoronto.ca/video-archive/2016/10/2267-16158) `video`)  
  ["Do we still need models or just more data and compute?"](https://staff.fnwi.uva.nl/m.welling/wp-content/uploads/Model-versus-Data-AI-1.pdf) by Max Welling  

  ["Model-based Reinforcement Learning: A Survey"](https://arxiv.org/abs/2006.16712) by Moerland et al. `paper`

----

  [**interesting papers**](#interesting-papers---model-based-methods)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-based-methods)  

----

  - [**optimal control**](#optimal-control)  
  - [**Monte Carlo Tree Search**](#monte-carlo-tree-search)  
  - [**Guided Policy Search**](#guided-policy-search)  
  - [**deep model-based learning**](#deep-model-based-learning)  
  - [**bayesian reinforcement learning**](#bayesian-reinforcement-learning)  



----
#### optimal control

  ["The Shades of Reinforcement Learning"](https://youtube.com/watch?v=OmpzeWym7HQ) by John Tsitsiklis `video`

----

  [overview](http://argmin.net/2018/02/01/control-tour) by Benjamin Recht

  ["An Outsider's Tour of Reinforcement Learning"](http://argmin.net/2018/06/25/outsider-rl) by Benjamin Recht  
  ["A Tour of Reinforcement Learning: The View from Continuous Control"](https://arxiv.org/abs/1806.09460) by Benjamin Recht `paper`  

  ["Optimization Perspectives on Learning to Control"](https://youtube.com/watch?v=nF2-39a29Pw) tutorial by Benjamin Recht `video`  

  ["Learning for Dynamics and Control"](https://l4dc.mit.edu) workshop ([videos](https://youtube.com/playlist?list=PLYx2nCJDi_QFrGOmIM0ale8T_1Fqu8OIF))

----

  ["Sampling and Exploration for Control of Physical Systems"](https://facebook.com/icml.imls/videos/2265408103721327?t=591) by Emo Todorov `video` *(critique of MDP framework)*  
  ["Is (Deep) Reinforcement Learning Barking Up The Wrong Tree?"](https://youtube.com/watch?v=2GW7ozcUCFE) by Chris Atkeson `video`  
  ["What Should Be Learned?"](https://youtu.be/WRsxoVB8Yng?t=7h7m15s) by Chris Atkeson `video`  



----
#### Monte Carlo Tree Search

  [overview](https://youtube.com/watch?v=ItMutbeOHtc&t=1h4m32s) by David Silver `video`  
  [overview](https://youtube.com/watch?v=mZtlW_xtarI&t=45m12s) by Sergey Levine `video`  
  [overview](https://youtube.com/watch?v=onBYsen2_eA) by Michael Littman `video`  
  [overview](https://yadi.sk/i/lOAUu7o13JBHFz) by Fedor Ratnikov `video` `in russian`  

----

  [overview](https://int8.io/monte-carlo-tree-search-beginners-guide) by Kamil Czarnogorski

  ["A Survey of Monte Carlo Tree Search Methods"](http://www.cameronius.com/cv/mcts-survey-master.pdf) by Browne et al. `paper`

  [**"Mastering the Game of Go with Deep Neural Networks and Tree Search"**](#mastering-the-game-of-go-with-deep-neural-networks-and-tree-search-silver-et-al) by Silver et al. `paper` `summary`  
  ["Combining Online and Offline Knowledge in UCT"](http://machinelearning.org/proceedings/icml2007/papers/387.pdf) by Gelly and Silver `paper` ([talk](https://youtube.com/watch?v=Bm7zah_LrmE) `video`)  
  [**"Deep Learning for Real-Time Atari Game Play Using Offline Monte-Carlo Tree Search Planning"**](#deep-learning-for-real-time-atari-game-play-using-offline-monte-carlo-tree-search-planning-guo-singh-lee-lewis-wang) by Guo et al. `paper` `summary`  
  [**"A Monte-Carlo AIXI Approximation"**](https://github.com/brylevkirill/notes/blob/Artificial%20Intelligence.md#a-monte-carlo-aixi-approximation-mc-aixi-ctw-agent-veness-ng-hutter-uther-silver) by Veness et al. `paper` `summary`  

  [**interesting papers**](#interesting-papers---model-based-methods)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-based-methods)  



----
#### Guided Policy Search

  learning a model-based teacher policy that supervises training of a neural network student policy

  - uses expert trajectories obtained previously to learn locally linear approximations of environment dynamics  
  - uses optimal control algorithms to find the locally linear optimal policies corresponding to these dynamics  
  - uses supervised learning to train neural network controller to fit trajectories generated by these policies  

  "GPS takes a few sequences of actions from another controller which could be constructed using a separate method such as optimal control. GPS learns from them by using supervised learning in combination with importance sampling which corrects for off-policy samples. This approach effectively biases the search towards a good (local) optimum. GPS works in a loop, by optimising policies to match sampled trajectories, and  optimising trajectory guiding distributions to match the policy and minimise costs."

----

  [overview](http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/) by Pieter Abbeel (part 2) `video`  
  [overview](http://youtube.com/watch?v=EtMyH_--vnU) by Sergey Levine `video`  
  [overview](https://video.seas.harvard.edu/media/ME+Sergey+Levine+2015+-04-01/1_gqqp9r3o/23375211) by Sergey Levine `video`  

  ["Optimal Control and Trajectory Optimization"](https://youtube.com/watch?v=mZtlW_xtarI) by Sergey Levine `video`  
  ["Learning Policies by Imitating Optimal Control"](https://youtube.com/watch?v=o0Ebur3aNMo) by Sergey Levine `video`  

----

  [**"Guided Policy Search"**](#guided-policy-search-levine-koltun) by Levine et al. `paper` `summary`  
  [**"Learning Neural Network Policies with Guided Policy Search under Unknown Dynamics"**](#learning-neural-network-policies-with-guided-policy-search-under-unknown-dynamics-levine-abbeel) by Levine et al. `paper` `summary`  
  [**"Learning Contact-Rich Manipulation Skills with Guided Policy Search"**](#learning-contact-rich-manipulation-skills-with-guided-policy-search-levine-wagener-abbeel) by Levine et al. `paper` `summary`  
  [**"End-to-End Training of Deep Visuomotor Policies"**](#end-to-end-training-of-deep-visuomotor-policies-levine-finn-darrell-abbeel) by Levine et al. `paper` `summary`  



----
#### deep model-based learning

  challenges:  
  - planning with learned model is dangerous  
    * planning looks for actions sequence maximizing expected return  
    * planning looks for and exploits imperfections in learned model  
  - compounding errors  
    * errors in transition model compound over given trajectory  
    * return can be totally wrong by the end of long trajectory  
  - deep value/policy networks can plan implicitly  
    * each layer performs computational step  
    * n-layer network can lookahead n steps  
    * are transition models required at all?  

----

  [overview](https://slideslive.com/38915863/learning-models-for-representations-and-planning) by Timothy Lillicrap `video`

  ["Model-based Deep Reinforcement Learning"](https://youtube.com/watch?v=iC2a7M9voYU) by Chelsea Finn `video`  
  ["Learning Dynamical System Models from Data"](https://youtube.com/watch?v=qVsLk5CVy_c) by Sergey Levine `video`  
  ["Advanced Model Learning"](https://youtube.com/watch?v=6EasN2FAIX0) by Chelsea Finn `video`  

  ["Approximate Learning in POMDPs"](https://youtu.be/aV4wz7FAXmo?t=1h1m55s) by Pavel Shvechikov `video`  
  ["Approximate Learning in POMDPs"](https://yadi.sk/i/pMdw-_uI3Gke7Z) (35:54) by Pavel Shvechikov `video` `in russian`  
  ["Deep Recurrent Q-Network"](https://youtube.com/watch?v=bE5DIJvZexc) by Alexander Fritzler `video` `in russian`  
  ["Deep Reinforcement Learning with Memory"](http://93.180.23.59/videos/video/2420/in/channel/1/) by Sergey Bartunov `video` `in russian`  

----

  [**"Benchmarking Model-Based Reinforcement Learning"**](#benchmarking-model-based-reinforcement-learning-wang-et-al) by Wang et al. `summary`

----

  [**interesting papers**](#interesting-papers---model-based-methods)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-based-methods)  



----
#### bayesian reinforcement learning

  ["Bayesian Reinforcement Learning: A Survey"](https://arxiv.org/abs/1609.04436) by Ghavamzadeh et al. `paper`

----

  [**policy search in Bayes-Adaptive MDP**](#bayesian-reinforcement-learning---policy-search-in-bayes-adaptive-mdp)  
  [**reinforcement learning as inference**](#bayesian-reinforcement-learning---policy-search-as-inference)  
  [**universal reinforcement learning**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#universal-artificial-intelligence)  
  [**active inference**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#active-inference)  

----

  [**bayesian inference and learning**](https://github.com/brylevkirill/notes/blob/master/Bayesian%20Inference%20and%20Learning.md)


----
#### bayesian reinforcement learning - policy search in Bayes-Adaptive MDP

  [overview](https://youtu.be/5rev-zVx1Ps?t=58m45s) by Marc Toussaint `video`  
  [overview](https://youtu.be/sGuiWX07sKw?t=1h9m2s) by David Silver `video`  
  [overview](https://slideslive.com/38922727/bayesadaptive-deep-reinforcement-learning-via-metalearning) by Shimon Whiteson `video`  

  ["Reinforcement Learning: Beyond Markov Decision Processes"](https://youtube.com/watch?v=_dkaynuKUFE) by Alexey Seleznev `video` `in russian`  
  ["Partially Observable Markov Decision Process in Reinforcement Learning"](https://yadi.sk/i/pMdw-_uI3Gke7Z) by Pavel Shvechikov `video` `in russian`  
  ["Planning in Partially Observable Markov Decision Process"](https://yadi.sk/i/lOAUu7o13JBHFz) (55:08) by Pavel Shvechikov `video` `in russian`  

----

  ["Optimal Learning: Computational Procedures for Bayes-adaptive Markov Decision Processes"](https://researchgate.net/publication/34273562_Optimal_learning_microform_computational_procedures_for_Bayes-adaptive_Markov_decision_processes) by Duff and Barto `paper`  
  ["An Analytic Solution to Discrete Bayesian Reinforcement Learning"](https://researchgate.net/publication/221346184_An_analytic_solution_to_discrete_Bayesian_reinforcement_learning) by Poupart et al. `paper`  
  ["Bayes-Adaptive POMDPs"](https://papers.nips.cc/paper/3333-bayes-adaptive-pomdps) by Ross et al. `paper`  
  ["Monte-Carlo Planning in Large POMDPs"](https://papers.nips.cc/paper/4031-monte-carlo-planning-in-large-pomdps) by Silver et al. `paper`
	([overview](https://yadi.sk/i/lOAUu7o13JBHFz) (1:39:35) by Pavel Shvechikov `video` `in russian`, [demo](https://youtube.com/watch?v=fXuOeNM_yEk) `video`)  
  [**"Planning to Be Surprised: Optimal Bayesian Exploration in Dynamic Environments"**](#planning-to-be-surprised-optimal-bayesian-exploration-in-dynamic-environments-sun-gomez-schmidhuber) by Sun et al. `paper` `summary`  
  [**"Efficient Bayes-Adaptive Reinforcement Learning using Sample-Based Search"**](#efficient-bayes-adaptive-reinforcement-learning-using-sample-based-search-guez-silver-dayan) by Guez et al. `paper` `summary`  
  ["Learning in POMDPs with Monte Carlo Tree Search"](http://proceedings.mlr.press/v70/katt17a.html) by Katt et al. `paper`  
  ["Variational Inference for Data-Efficient Model Learning in POMDPs"](https://arxiv.org/abs/1805.09281) by Tschiatschek et al. `paper`  
  ["VariBAD: A Very Good Method for Bayes-Adaptive Deep RL via Meta-Learning"](https://arxiv.org/abs/1910.08348) by Zintgraf et al. `paper` ([overview](https://slideslive.com/38922727/bayesadaptive-deep-reinforcement-learning-via-metalearning) by Shimon Whiteson `video`)  

----

  BRL agent aims to maximise expected sum of future rewards obtained when interacting with unknown Markov Decision Process while using some prior knowledge.  
  BRL agent maintains distribution over worlds and either samples a world and acts as if it is real, or chooses action by reasoning about full distribution.  
  Bayes-Adaptive Markov Decision Process is an MDP with a state being a concatenation of beliefs about actual state, transition function and reward function.  
  Under this framework actions that yield highest instant reward and actions that maximise gathering of knowledge about environment are often very different.  
  BAMDP framework leads to rigorous definition of optimal solution based on finding policy that reaches optimal balance between exploration and exploitation.  


----
#### bayesian reinforcement learning - reinforcement learning as inference

  ["A Case Against Generative Models in RL?"](https://youtube.com/watch?v=EA2RtXsLSWU) by Shakir Mohamed `video`  
  ["Bayesian Policy Search"](https://youtu.be/AggqBRdz6CQ?t=9m53s) by Shakir Mohamed `video`  
  ["Connections Between Inference and Control"](https://youtu.be/iOYiPhu5GEk?t=2m34s) by Sergey Levine `video` ([write-up](https://arxiv.org/abs/1805.00909))  

  ["Reinforcement Learning as Probabilistic Inference"](https://youtube.com/watch?v=j8T8Xt8TM8Q) by Pavel Temirchev `video` `in russian`  
  ["Reinforcement Learning as Probabilistic Inference"](https://youtube.com/watch?v=pYsXIPEkSxs) by Pavel Temirchev `video` `in russian`  
  ["Reinforcement Learning through the Lenses of Variational Inference"](https://youtube.com/watch?v=6v3RxQycT0E) by Sergey Bartunov `video`  
  ["Bayesian Inference for Reinforcement Learning"](https://youtube.com/watch?v=KZd-jkmeIcU) by Sergey Bartunov `video` `in russian`  

----

  ["Reinforcement Learning and Control as Probabilistic Inference: Tutorial and Review"](https://arxiv.org/abs/1805.00909) by Levine `paper` ([talk](https://youtu.be/iOYiPhu5GEk?t=2m34s) `video`)  
  ["Making Sense of Reinforcement Learning and Probabilistic Inference"](https://openreview.net/forum?id=S1xitgHtvS) by O'Donoghue `paper` et al.  
  ["VIREL: A Variational Inference Framework for Reinforcement Learning"](https://arxiv.org/abs/1811.01132) by Fellows et al.  
  [**"Reinforced Variational Inference"**](#reinforced-variational-inference-weber-heess-eslami-schulman-wingate-silver) by Weber et al. `paper` `summary`  



---
### value-based methods

  value-focused model focuses exclusively on value function(s) ([overview](https://facebook.com/icml.imls/videos/2366831430268790?t=764) by David Silver `video`):  
  - sufficient for optimal planning => ignores irrelevant details  
  - trained end-to-end over multiple steps => avoids compounding errors  

  many-valued focused model:  
  - predicts many different value functions  
    * e.g different policies, discounts, rewards  
  - prodives data efficiency  
    * similar to observation models  
  - solution is a consistent model for all value functions  
    * if model is consistent with "core" value functions  

----

  ["Temporal-Difference Learning"](http://videolectures.net/deeplearning2017_sutton_td_learning/) by Richard Sutton `video`

  ["Markov Decision Process"](https://youtube.com/watch?v=lfHX2hHRMVQ) by David Silver `video`  
  ["Planning by Dynamic Programming"](https://youtube.com/watch?v=Nd1-UUMVfz4) by David Silver `video`  
  ["Model-Free Prediction"](https://youtube.com/watch?v=PnHCvfgC_ZA) by David Silver `video`  
  ["Model Free Control"](https://youtube.com/watch?v=0g4j2k_Ggc4) by David Silver `video`  
  ["Value Function Approximation"](http://youtube.com/watch?v=UoPei5o4fps) by David Silver `video`  

  ["Value Iteration and Policy Iteration"](https://youtube.com/watch?v=IL3gVyJMmhg) by John Schulman `video`  
  "Q-Function Learning Methods" by John Schulman
	([first part](https://youtube.com/watch?v=Wnl-Qh2UHGg&t=19m06s),
	[second part](https://youtube.com/watch?v=h1-pj4Y9-kM)) `video`  

  ["Approximate Dynamic Programming and Batch Reinforcement Learning"](http://videolectures.net/DLRLsummerschool2018_farahmand_batch_RL) by Amir-massoud Farahmand `video`

  ["Temporal Difference"](https://yadi.sk/i/cVawsPkK3EtGJj) by Fedor Ratnikov `video` `in russian`  
  "Value-based Methods" by Fedor Ratnikov
	([first part](https://yadi.sk/i/I7XcP6vU3ExNrT), [second part](https://yadi.sk/i/XbqNQmjm3ExNsq)) `video` `in russian`  

----

  ["The Paths Perspective on Value Learning"](https://distill.pub/2019/paths-perspective-on-value-learning) by Greydanus and Olah

----

  [**interesting papers**](#interesting-papers---value-based-methods)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-free-methods)  

----

  methods:  
  - [**Deep Q-Network**](#deep-q-network-dqn)



----
#### Deep Q-Network (DQN)

  [overview](http://youtube.com/watch?v=dV80NAlEins) by Nando de Freitas `video`  
  [overview](http://youtube.com/watch?v=fevMOp5TDQs) by Vlad Mnih `video`  

  [from value function approximation to Deep Q-Network](http://youtu.be/UoPei5o4fps?t=1h9m) by David Silver `video`  
  [from Fitted Value Iteration to Deep Q-Network](http://videolectures.net/deeplearning2017_szepesvari_theory_of_rl/#t=2929) by Czaba Szepesvari `video`  
  ["Approximate Reinforcement Learning"](https://yadi.sk/i/AHDU2p_j3FT3nr) by Fedor Ratnikov `video` `in russian`  

  [derivations](http://www.alexirpan.com/rl-derivations/#q-learning) by Alex Irpan

----

  latest developments:  
  - [overview](http://youtube.com/watch?v=bsuvM1jO-4w) by Vlad Mnih `video`  
  - [overview](http://youtu.be/fevMOp5TDQs?t=53m32s) by Vlad Mnih `video`  
  - [overview](http://techtalks.tv/talks/deep-reinforcement-learning/62360/) by David Silver `video`  
  - [overview](http://youtu.be/qLaDWKd61Ig?t=9m16s) by David Silver `video`  
  - [overview](http://videolectures.net/rldm2015_silver_reinforcement_learning/) by David Silver `video`  
  - [overview](https://yadi.sk/i/yBO0q4mI3GAxYd) by Alexander Fritzler `video` `in russian`  
  - [overview](http://youtube.com/watch?v=mrgJ53TIcQc) (Pavlov) `in russian`

----

  [**interesting papers**](#interesting-papers---value-based-methods)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-free-methods)  

----

  - naive Q-learning oscillates or diverges with neural networks  
    * data is sequential  
    * successive samples are correlated, non-iid  
  - policy changes rapidly with slight changes to Q-values  
    * policy may oscillate  
    * distribution of data can swing from one extreme to another  
  - scale of rewards and Q-values is unknown  
    * naive Q-learning gradients can be large  
    * unstable when backpropagated  

  Deep Q-Network:  
  - use experience replay  
    * break correlations in data, bring us back to iid setting  
    * learn from all past policies  
    * using off-policy Q-learning  
  - freeze target Q-network  
    * avoid oscillations  
    * break correlations between Q-network and target  
  - clip rewards or normalize network adaptively to sensible range  
    * robust gradients  



---
### policy-based methods

  [overview](https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html) by Lilian Weng  
  [overview](https://danieltakeshi.github.io/2017/03/28/going-deeper-into-reinforcement-learning-fundamentals-of-policy-gradients) by Daniel Takeshi  

----

  [overview](http://youtube.com/watch?v=KHZVXao4qXs) by David Silver `video`  
  [overview](http://youtube.com/watch?v=S_gwYj1Q-44) by Pieter Abbeel `video`  

  [tutorial](https://channel9.msdn.com/Events/Neural-Information-Processing-Systems-Conference/Neural-Information-Processing-Systems-Conference-NIPS-2016/Deep-Reinforcement-Learning-Through-Policy-Optimization) by Pieter Abbeel and John Schulman `video`
	([slides](http://people.eecs.berkeley.edu/~pabbeel/nips-tutorial-policy-optimization-Schulman-Abbeel.pdf))  
  [tutorial](http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/) by Pieter Abbeel `video`  

  course by John Schulman (parts [1](https://youtube.com/watch?v=BB-BhTn6DCM), [2](https://youtube.com/watch?v=_t5fpZuuf-4), [3](https://youtube.com/watch?v=Fauwwkiy-bo), [4](https://youtube.com/watch?v=IDSA2wAACr0)) `video`  
  course by John Schulman (parts [1](https://youtube.com/watch?v=aUrX-rP_ss4), [2](https://youtube.com/watch?v=oPGVsoBonLM), [3](https://youtube.com/watch?v=rO7Dx8pSJQw), [4](https://youtube.com/watch?v=gb5Q2XL5c8A)) `video`  

  [overview](https://youtu.be/eeJ1-bUnwRI?t=49m57s) by Olivier Sigaud `video`  
  ["Advanced Policy Gradient Methods"](https://youtube.com/watch?v=ycCtmp4hcUs) by Joshua Achiam `video`  

  [overview](https://yadi.sk/i/I3M09HKQ3GKBiP) by Fedor Ratnikov `video` `in russian`  
  [overview](https://youtu.be/mrgJ53TIcQc?t=41m35s) by Alexey Seleznev `video` `in russian`  

----

  [**interesting papers**](#interesting-papers---policy-based-methods)  
  [**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-free-methods)  

----

  methods:  
  - derivative-free  
    * [**Cross-Entropy Method**](#cross-entropy-method-cem)  (no policy gradient estimation)  
    * [**Evolution Strategies**](#evolution-strategies-es)  (derivative-free policy gradient estimation using finite differences)  
  - likelihood ratio policy gradient  
    * [**REINFORCE**](#reinforce)  (policy gradient estimation using simple baseline for returns)  
    * [**Trust Region Policy Optimization**](#trust-region-policy-optimization-trpo)  (policy gradient estimation using natural gradient / trust region)  
    * [**Proximal Policy Optimization**](#proximal-policy-optimization-ppo)  (KL-constrained policy gradient estimation without using natural gradient)  
    * [**Actor-Critic**](#actor-critic-ac), [**Advantage Actor-Critic**](#advantage-actor-critic-a2c)  (policy gradient estimation using critic as baseline for returns)  
  - pathwise derivative policy gradient  
    * [**Deep Deterministic Policy Gradient**](#deep-deterministic-policy-gradient-ddpg)  (policy gradient estimation using gradient of critic as model of returns)  
    * [**Stochastic Value Gradient**](#stochastic-value-gradient-svg)  (policy gradient estimation using gradient of critic or gradient of environment model)  

  what's the right core model-free algorithm is not clear:  
  - *derivative-free policy optimization*:  scalable, very sample-inefficient, more robust, no off-policy  
  - *policy gradient optimization*:  scalable, not sample-efficient, not robust, no off-policy  
  - *trust region policy optimization*:  less scalable, more sample-efficient, more robust, no off-policy  
  - *value-based policy optimization*:  scalable in state space, more sample-efficient, not robust, more off-policy  

  [overview](https://youtu.be/eeJ1-bUnwRI?t=1h58m38s) of methods (the big picture) by Olivier Sigaud `video`

----

  "Policy gradient methods are attractive because they are end-to-end: there is explicit policy and principled approach that directly optimizes expected reward."  

  limitations of policy gradient optimization:  
  - inefficient use of data, large number of samples required  
    * each experience is only used to compute one gradient (on-policy)  
    * given a batch of trajectories what's the most we can do with it?  
  - hard to choose reasonable stepsize that works for the whole optimization  
    * we have a gradient estimate, no objective for line search  
    * statistics of data (observations and rewards) change during learning  

  "For reinforcement learning there are two widely known ways of optimizing a policy based on sampled sequences of actions and outcomes: There’s (a) likelihood-ratio gradient estimator, which updates the policy such that action sequences that lead to higher scores happen more often and that doesn’t need gradients, and (b) pathwise derivative gradient estimator, which adjusts individual actions such that the policy results in a higher score and that needs gradients. Likelihood-ratio estimator changes probabilities of experienced paths by shifting probability mass towards better ones and, unlike pathwise estimator, does not try to change the paths. While pathwise methods may be more sample-efficient, they work less generally due to high bias and don’t scale up as well to very high-dimensional problems."



----
#### Cross-Entropy Method (CEM)

  no policy gradient estimation, evolutionary algorithm with selection operator buth without recombination and mutation operators

  "If your policy has a small number of parameters (say 20), and sometimes even if it has a moderate number (say 2000), you might be better off using the Cross-Entropy Method than any of the fancy methods. It works like this:  
  - Sample n sets of parameters from some prior that allows for closed-form updating, e.g. a multivariate Gaussian.  
  - For each parameter set, compute a noisy score by running your policy on the environment you care about.  
  - Take the top 20% percentile (say) of sampled parameter sets. Fit a Gaussian distribution to this set, then go to (1) and repeat using this as the new prior."  

----

  [overview](http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement#t=517) by Pieter Abbeel `video`  
  [overview](https://channel9.msdn.com/Events/Neural-Information-Processing-Systems-Conference/Neural-Information-Processing-Systems-Conference-NIPS-2016/Deep-Reinforcement-Learning-Through-Policy-Optimization) by Pieter Abbeel (07:07) `video`  
  [overview](https://youtu.be/aUrX-rP_ss4?t=27m20s) by John Schulman `video`  
  [overview](https://yadi.sk/i/5yf_4oGI3EDJhJ) by Fedor Ratnikov `video` `in russian`  

  ["The Cross Entropy method for Fast Policy Search"](http://aaai.org/Papers/ICML/2003/ICML03-068.pdf) by Mannor, Rubinstein, Gat `paper`



----
#### Evolution Strategies (ES)

  policy gradient estimation using finite differences instead of derivative of loss function  
  ES does not fully exploit architecture of policy network or temporal structure of problem  

  "Evolutionary computation is one of the most useful practical methods for direct search in policy space, especially when there is no teacher who knows which output actions the system should produce at which time. Especially in partially observable environments where memories of previous events are needed to disambiguate states, this often works much better than other reinforcement learning techniques based on dynamic programming. In case of teacher-given desired output actions or labels, gradient descent such as backpropagation (also through time) usually works much better, especially for NNs with many weights."

  [*(Juergen Schmidhuber)*](https://reddit.com/r/MachineLearning/comments/2xcyrl/i_am_jürgen_schmidhuber_ama/cp48nkc/)

----

  <http://scholarpedia.org/article/Evolution_strategies>

  [overview](https://lilianweng.github.io/lil-log/2019/09/05/evolution-strategies.html) by Lilian Weng  
  [overview](http://blog.otoro.net/2017/10/29/visual-evolution-strategies/) by David Ha  

  [overview](https://youtube.com/watch?v=SQtOI9jsrJ0) by Xi Chen `video`  
  [overview](https://youtube.com/watch?v=rHAasIIGIEc) by Evgenia Elistratova `video` `in russian`  

  ["Completely Derandomized Self-Adaptation in Evolution Strategies"](https://www.lri.fr/~hansen/cmaartic.pdf) (CMA-ES) by Hansen and Ostermeier `paper`  
  ["Natural Evolution Strategies"](http://jmlr.org/papers/volume15/wierstra14a/wierstra14a.pdf) by Wierstra et al. `paper`  
  [**"Evolution Strategies as a Scalable Alternative to Reinforcement Learning"**](#evolution-strategies-as-a-scalable-alternative-to-reinforcement-learning-salimans-ho-chen-sutskever) by Salimans, Ho, Chen, Sutskever `paper` `summary`  
  ["Improving Exploration in Evolution Strategies for Deep Reinforcement Learning via a Population of Novelty-Seeking Agents"](https://arxiv.org/abs/1712.06560) by Conti et al. `paper`  
  ["Playing Atari with Six Neurons"](https://arxiv.org/abs/1806.01363) by Cuccu et al. `paper`  

  ["Evolutionary Computation for Reinforcement Learning"](http://cs.ox.ac.uk/publications/publication10159-abstract.html) by Shimon Whiteson `paper`  
  ["Evolutionary Algorithms for Reinforcement Learning"](https://arxiv.org/abs/1106.0221) by Moriarty, Schultz, Grefenstette `paper`  



----
#### REINFORCE

  likelihood ratio policy gradient estimation

----

  introduction by Andrej Karpathy ([post](http://karpathy.github.io/2016/05/31/rl), [talk](https://youtube.com/watch?v=tqrcjHuNdmQ) `video`)   
  [introduction](http://kvfrans.com/simple-algoritms-for-solving-cartpole/) by Kevin Frans  
  [introduction](https://www.alexirpan.com/rl-derivations/#reinforce) by Alex Irpan  

  ["The Policy of Truth"](http://argmin.net/2018/02/20/reinforce/) by Benjamin Recht  *(REINFORCE is nothing more than random search)*

  [overview](http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/#t=1003) by Pieter Abbeel `video`  
  overview by John Schulman ([part 1](https://youtube.com/watch?v=oPGVsoBonLM), [part 2](https://youtube.com/watch?v=oPGVsoBonLM)) `video`  



----
#### Trust Region Policy Optimization (TRPO)

  [**"Trust Region Policy Optimization"**](#trust-region-policy-optimization-schulman-levine-moritz-jordan-abbeel) by Schulman et al. `paper` `summary`



----
#### Proximal Policy Optimization (PPO)

  [**"Proximal Policy Optimization Algorithms"**](#proximal-policy-optimization-algorithms-schulman-wolski-dhariwal-radford-klimov) by Schulman et al. `paper` `summary`



----
#### Actor-Critic (AC)

  [overview](http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement#t=2985) by Pieter Abbeel `video`

----

  - [**Advantage Actor-Critic (A2C)**](#advantage-actor-critic-a2c)


----
#### Advantage Actor-Critic (A2C)

  [**"Asynchronous Methods for Deep Reinforcement Learning"**](#asynchronous-methods-for-deep-reinforcement-learning-mnih-badia-mirza-graves-lillicrap-harley-silver-kavukcuoglu) by Mnih et al. `paper` `summary`



----
#### pathwise derivative policy gradient

  "For reinforcement learning there are two widely known ways of optimizing a policy based on sampled sequences of actions and outcomes: There’s (a) likelihood-ratio gradient estimator, which updates the policy such that action sequences that lead to higher scores happen more often and that doesn’t need gradients, and (b) pathwise derivative gradient estimator, which adjusts individual actions such that the policy results in a higher score and that needs gradients. Likelihood-ratio estimator changes probabilities of experienced paths by shifting probability mass towards better ones and, unlike pathwise estimator, does not try to change the paths. While pathwise methods may be more sample-efficient, they work less generally due to high bias and don’t scale up as well to very high-dimensional problems."

----

  [overview](http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/#t=3724) by Pieter Abbeel `video`

  - [**Deep Deterministic Policy Gradient (DDPG)**](#deep-deterministic-policy-gradient-ddpg)  
  - [**Stochastic Value Gradient (SVG)**](#stochastic-value-gradient-svg)  


----
#### Deep Deterministic Policy Gradient (DDPG)

  [**"Continuous Control with Deep Reinforcement Learning"**](#continuous-control-with-deep-reinforcement-learning-lillicrap-hunt-pritzel-heess-erez-tassa-silver-wierstra) by Lillicrap et al. `paper` `summary`


----
#### Stochastic Value Gradient (SVG)

  [**"Learning Continuous Control Policies by Stochastic Value Gradients"**](#learning-continuous-control-policies-by-stochastic-value-gradients-heess-wayne-silver-lillicrap-tassa-erez) by Heess et al. `paper` `summary`



---
### interesting papers

  - [**applications**](#interesting-papers---applications)  
  - [**exploration and intrinsic motivation**](#interesting-papers---exploration-and-intrinsic-motivation)  
  - [**hierarchical reinforcement learning**](#interesting-papers---hierarchical-reinforcement-learning)  
  - [**model-based methods**](#interesting-papers---model-based-methods)  
  - [**value-based methods**](#interesting-papers---value-based-methods)  
  - [**policy-based methods**](#interesting-papers---policy-based-methods)  
  - [**behavioral cloning**](#interesting-papers---behavioral-cloning)  
  - [**inverse reinforcement learning**](#interesting-papers---inverse-reinforcement-learning)  


interesting recent papers:  
  - [**model-free methods**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-free-methods)  
  - [**model-based methods**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-based-methods)  
  - [**exploration and intrinsic motivation**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)  
  - [**hierarchical**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---hierarchical)  
  - [**transfer**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---transfer)  
  - [**imitation**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---imitation)  
  - [**multi-agent**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---multi-agent)  



---
### interesting papers - applications

[**selected papers**](https://yadi.sk/d/tiaE7sdi3WEhDS)

----
#### ["Challenges of Real-World Reinforcement Learning"](https://arxiv.org/abs/1904.12901) Dulac-Arnold, Mankowitz, Hester
>	"Reinforcement learning has proven its worth in a series of artificial domains, and is beginning to show some successes in real-world scenarios. However, much of the research advances in RL are often hard to leverage in real-world systems due to a series of assumptions that are rarely satisfied in practice. We present a set of nine unique challenges that must be addressed to productionize RL to real world problems. For each of these challenges, we specify the exact meaning of the challenge, present some approaches from the literature, and specify some metrics for evaluating that challenge. An approach that addresses all nine challenges would be applicable to a large number of real world problems. We also present an example domain that has been modified to present these challenges as a testbed for practical RL research."

>	"1. Training off-line from the fixed logs of an external behavior policy.  
>	2. Learning on the real system from limited samples.  
>	3. High-dimensional continuous state and action spaces.  
>	4. Safety constraints that should never or at least rarely be violated.  
>	5. Tasks that may be partially observable, alternatively viewed as non-stationary or stochastic.  
>	6. Reward functions that are unspecified, multi-objective, or risk-sensitive.  
>	7. System operators who desire explainable policies and actions.  
>	8. Inference that must happen in real-time at the control frequency of the system.  
>	9. Large and/or unknown delays in the system actuators, sensors, or rewards."


#### ["Deep Reinforcement Learning: An Overview"](https://arxiv.org/abs/1701.07274) Li
>	"We give an overview of recent exciting achievements of deep reinforcement learning. We start with background of deep learning and reinforcement learning, as well as introduction of testbeds. Next we discuss Deep Q-Network and its extensions, asynchronous methods, policy optimization, reward, and planning. After that, we talk about attention and memory, unsupervised learning, and learning to learn. Then we discuss various applications of RL, including games, in particular, AlphaGo, robotics, spoken dialogue systems (a.k.a. chatbot), machine translation, text sequence prediction, neural architecture design, personalized web services, healthcare, finance, and music generation. We mention topics/papers not reviewed yet. After listing a collection of RL resources, we close with discussions."

  - `slides` <https://dropbox.com/s/kzkc8t61t7tz9eu/AISeminar.pdf>


#### ["Grandmaster Level in StarCraft II using Multi-agent Reinforcement Learning"](https://storage.googleapis.com/deepmind-media/research/alphastar/AlphaStar_unformatted.pdf) Vinyals et al.
  `AlphaStar`
>	"Many real-world applications require artificial agents to compete and coordinate with other agents in complex environments. As a stepping stone to this goal, the domain of StarCraft has emerged as an important challenge for artificial intelligence research, owing to its iconic and enduring status among the most difficult professional esports, and its relevance to the real world in terms of its raw complexity and multi-agent challenges. Over the course of a decade and numerous competitions, the strongest agents have simplified important aspects of the game, utilised superhuman capabilities, or employed hand-crafted subsystems. Despite these advantages, no previous agent has come close to matching the overall skill of top StarCraft players. We chose to address the challenge of StarCraft using general-purpose learning methods that are in principle applicable to other complex domains: a multi-agent reinforcement learning algorithm that uses data from both human and agent games within a diverse league of continually adapting strategies and counter-strategies, each represented by deep neural networks. We evaluated our agent, AlphaStar, in the full game of StarCraft II, through a series of online games against human players. AlphaStar was rated at Grandmaster level for all three StarCraft races and above 99.8% of officially ranked human players."

  - `post` <https://deepmind.com/blog/article/AlphaStar-Grandmaster-level-in-StarCraft-II-using-multi-agent-reinforcement-learning>
  - `video` <https://youtube.com/watch?v=6eiErYh_FeY>
  - `video` <https://slideslive.com/38922724/grandmaster-level-in-starcraft-ii-using-multiagent-reinforcement-learning) (Vinyals)
  - `video` <https://youtu.be/3UdH3lPF7nE> (Vinyals)
  - `video` <https://youtu.be/Kedt2or9xlo> (Vinyals)
  - `video` <https://slideslive.com/38916905/alphastar-mastering-the-game-of-starcraft-ii> (Silver)
  - `video` <https://youtu.be/mzjGNo9Tz4g?t=10m53s> (Silver)
  - `video` <https://youtube.com/watch?v=eZCI7zu_DlM> (Gibson)
  - `video` <https://youtube.com/watch?v=BTLCdge7uSQ> (Kilcher)


#### ["Human-level Performance in First-person Multiplayer Games with Population-based Deep Reinforcement Learning"](https://arxiv.org/abs/1807.01281) Jaderberg et al.
  `FTW`
>	"The real-world contains multiple agents, each learning and acting independently to cooperate and compete with other agents, and environments reflecting this degree of complexity remain an open challenge. In this work, we demonstrate for the first time that an agent can achieve human-level in a popular 3D multiplayer first-person video game, Quake III Arena Capture the Flag, using only pixels and game points as input. These results were achieved by a novel two-tier optimisation process in which a population of independent RL agents are trained concurrently from thousands of parallel matches with agents playing in teams together and against each other on randomly generated environments. Each agent in the population learns its own internal reward signal to complement the sparse delayed reward from winning, and selects actions using a novel temporally hierarchical representation that enables the agent to reason at multiple timescales. During game-play, these agents display human-like behaviours such as navigating, following, and defending based on a rich learned representation that is shown to encode high-level game knowledge. In an extensive tournament-style evaluation the trained agents exceeded the win-rate of strong human players both as teammates and opponents, and proved far stronger than existing state-of-the-art agents."

>	"The proposed training algorithm stabilises the learning process in partially observable multi-agent environments by concurrently training a diverse population of agents who learn by playing with each other, and in addition the agent population provides a mechanism for meta-optimisation. We solve the prohibitively hard credit assignment problem of learning from the sparse and delayed episodic team win/loss signal (optimising thousands of actions based on a single final reward) by enabling agents to evolve an internal reward signal that acts as a proxy for winning and provides denser rewards. Finally, we meet the memory and long-term temporal reasoning requirements of high-level, strategic CTF play by introducing an agent architecture that features a multi-timescale representation, reminiscent of what has been observed in primate cerebral cortex, and an external working memory module, broadly inspired by human episodic memory."

>	"Actions in this model are generated conditional on a stochastic latent variable, whose distribution is modulated by a more slowly evolving prior process. The variational objective function encodes a trade-off between maximising expected reward and consistency between the two timescales of inference. Whereas some previous hierarchical RL agents construct explicit hierarchical goals or skills, this agent architecture is conceptually more closely related to work on building hierarchical temporal representations and recurrent latent variable models for sequential data. The resulting model constructs a temporally hierarchical representation space in a novel way to promote the use of memory and temporally coherent action sequences."

>	"Intuitively, this objective function captures the idea that the slow LSTM generates a prior on z which predicts the evolution of z for the subsequent τ steps, while the fast LSTM generates a variational posterior on z that incorporates new observations, but adheres to the predictions made by the prior. All the while, z must be a useful representation for maximising reward and auxiliary task performance. This architecture can be easily extended to more than two hierarchical layers, but we found in practice that more layers made little difference on this task. We also augmented this dual-LSTM agent with shared DNC memory to further increase its ability to store and recall past experience."

>	"This can be seen as a two-tier reinforcement learning problem. The inner optimisation maximises Jinner, the agents’ expected future discounted internal rewards. The outer optimisation of Jouter can be viewed as a meta-game, in which the meta-reward of winning the match is maximised with respect to internal reward schemes and hyperparameters, with the inner optimisation providing the meta transition dynamics. We solve the inner optimisation with RL, and the outer optimisation with Population Based Training. PBT is an online evolutionary process which adapts internal rewards and hyperparameters and performs model selection by replacing under-performing agents with mutated versions of better agents. This joint optimisation of the agent policy using RL together with the optimisation of the RL procedure itself towards a high-level goal proves to be an effective and generally applicable strategy, and utilises the potential of combining learning and evolution in large scale learning systems."

----
>	"To make things even more interesting, we consider a variant of CTF in which the map layout changes from match to match. As a consequence, our agents are forced to acquire general strategies rather than memorising the map layout. Additionally, to level the playing field, our learning agents experience the world of CTF in a similar way to humans: they observe a stream of pixel images and issue actions through an emulated game controller."

  - `post` <https://deepmind.com/blog/capture-the-flag-science>
  - `video` <https://youtube.com/watch?v=NXkD77ioGi0> (demo)
  - `video` <https://youtube.com/watch?v=dltN4MxV1RI> (demo)
  - `video` <https://youtube.com/watch?v=MvFABFWPBrw>
  - `video` <https://youtu.be/N8_gVrIPLQM?t=1h10m> (Silver)
  - `video` <https://youtube.com/watch?v=_bSmby9ohIc> (Egorov) `in russian`
  - `paper` <https://science.sciencemag.org/content/364/6443/859>


#### ["Mastering Atari, Go, Chess and Shogi by Planning with a Learned Model"](https://arxiv.org/abs/1911.08265) Schrittwieser et al.
  `MuZero`
>	"Constructing agents with planning capabilities has long been one of the main challenges in the pursuit of artificial intelligence. Tree-based planning methods have enjoyed huge success in challenging domains, such as chess and Go, where a perfect simulator is available. However, in real-world problems the dynamics governing the environment are often complex and unknown. In this work we present the MuZero algorithm  which, by combining a tree-based search with a learned model, achieves superhuman performance in a range of challenging and visually complex domains, without any knowledge of their underlying dynamics. MuZero learns a model that, when applied iteratively, predicts the quantities most directly relevant to planning: the reward, the action-selection policy, and the value function. When evaluated on 57 different Atari games - the canonical video game environment for testing AI techniques, in which model-based planning approaches have historically struggled - our new algorithm achieved a new state of the art. When evaluated on Go, chess and shogi, without any knowledge of the game rules, MuZero matched the superhuman performance of the AlphaZero algorithm that was supplied with the game rules."

>	"Planning algorithms rely on knowledge of the environment’s dynamics, such as the rules of the game or an accurate simulator, preventing their direct application to real-world domains like robotics, industrial control, or intelligent assistants. Model-based reinforcement learning aims to address this issue by first learning a model of the environment’s dynamics, and then planning with respect to the learned model. Classically, this model is represented by a MDP consisting of two components: a state transition model, predicting the next state, and a reward model, predicting the expected reward during that transition. Once a model has been constructed, it is straightforward to apply MDP planning algorithms, such as value iteration or Monte-Carlo Tree Search, to compute the optimal value or optimal policy for the MDP. In large or partially observed environments, the algorithm must first construct the state representation that the model should predict. This tripartite separation between representation learning, model learning, and planning is potentially problematic since the agent is not able to optimize its representation or model for the purpose of effective planning, so that, for example modeling errors may compound during planning."

>	"Typically, environment models have either focused on reconstructing the true environmental state, or the sequence of full observations. They either build a latent state-space model that is sufficient to reconstruct the observation stream at pixel level, or to predict its future latent states, which facilitates more efficient planning but still focuses the majority of the model capacity on potentially irrelevant detail. None of these prior methods has constructed a model that facilitates effective planning in visually complex domains such as Atari; results lag behind well-tuned, model-free methods, even in terms of data efficiency. Instead, the most successful methods are based on model-free RL - i.e. they estimate the optimal policy and/or value function directly from interactions with the environment. However, model-free algorithms are in turn far from the state of the art in domains that require precise and sophisticated lookahead, such as chess and Go."

>	"The main idea of the algorithm is to predict those aspects of the future that are directly relevant for planning. The model receives the observation (e.g. an image of the Go board or the Atari screen) as an input and transforms it into a hidden state. The hidden state is then updated iteratively by a recurrent process that receives the previous hidden state and a hypothetical next action. At every one of these steps the model predicts the policy (e.g. the move to play), value function (e.g. the predicted winner), and immediate reward (e.g. the points scored by playing a move). The model is trained end-to-end, with the sole objective of accurately estimating these three important quantities, so as to match the improved estimates of policy and value generated by search as well as the observed reward. There is no direct constraint or requirement for the hidden state to capture all information necessary to reconstruct the original observation, drastically reducing the amount of information the model has to maintain and predict; nor is there any requirement for the hidden state to match the unknown, true state of the environment; nor any other constraints on the semantics of state. Instead, the hidden states are free to represent state in whatever way is relevant to predicting current and future values and policies. Intuitively, the agent can invent, internally, the rules or dynamics that lead to most accurate planning."

>	"MuZero builds upon AlphaZero’s powerful search and search-based policy iteration algorithms, but incorporates a learned model into the training procedure. MuZero also extends AlphaZero to a broader set of environments including single agent domains and non-zero rewards at intermediate time."

>	"In AlphaZero the planning process makes use of two separate components: a simulator implements the rules of the game, which are used to update the state of the game while traversing the search tree; and a neural network jointly predicts the corresponding policy and value of a board position produced by the simulator. Specifically, AlphaZero use knowledge of the rules of the game in three places: (1) state transitions in the search tree, (2) actions available at each node of the search tree, (3) episode termination within the search tree. In MuZero, all of these have been replaced with the use of a single implicit model learned by a neural network:  
>	1) State transitions. AlphaZero had access to a perfect simulator of the true dynamics process. In contrast, MuZero employs a learned dynamics model within its search. Under this model, each node in the tree is represented by a corresponding hidden state; by providing a hidden state and an action to the model the search algorithm can transition to a new node.  
>	2) Actions available. AlphaZero used the set of legal actions obtained from the simulator to mask the prior produced by the network everywhere in the search tree. MuZero only masks legal actions at the root of the search tree where the environment can be queried, but does not perform any masking within the search tree. This is possible because the network rapidly learns not to predict actions that never occur in the trajectories it is trained on.  
>	3) Terminal nodes. AlphaZero stopped the search at tree nodes representing terminal states and used the terminal value provided by the simulator instead of the value produced by the network. MuZero does not give special treatment to terminal nodes and always uses the value predicted by the network. Inside the tree, the search can proceed past a terminal node - in this case the network is expected to always predict the same value. This is achieved by treating terminal states as absorbing states during training.  
>	In addition, MuZero is designed to operate in the general reinforcement learning setting: single-agent domains with discounted intermediate rewards of arbitrary magnitude. In contrast, AlphaGo Zero and AlphaZero were designed to operate in two-player games with undiscounted terminal rewards of ±1."  

>	"Value prediction networks are perhaps the closest precursor to MuZero: they learn an MDP model grounded in real actions; the unrolled MDP is trained such that the cumulative sum of rewards, conditioned on the actual sequence of actions generated by a simple lookahead search, matches the real environment. Unlike MuZero there is no policy prediction, and the search only utilizes value prediction."

>	"We compared the performance of search in AlphaZero , using a perfect model, to the performance of search in MuZero, using a learned model. The fully trained AlphaZero or MuZero was evaluated by comparing MCTS with different thinking times. MuZero matched the performance of a perfect model, even when doing much larger searches (up to 10s thinking time) than those from which the model was trained (around 0.1s thinking time)."

>	"We also investigated the scalability of planning across all Atari games. We compared MCTS with different numbers of simulations, using the fully trained MuZero. The improvements due to planning are much less marked than in Go, perhaps because of greater model inaccuracy; performance improved slightly with search time, but plateaued at around 100 simulations. Even with a single simulation – i.e. when selecting moves solely according to the policy network – MuZero performed well, suggesting that, by the end of training, the raw policy has learned to internalise the benefits of search."

>	"We tested our model-based learning algorithm against a comparable model-free learning algorithm. When evaluated on Ms. Pacman, our model-free algorithm achieved identical results to R2D2, but learned significantly slower than MuZero and converged to a much lower final score. We conjecture that the search-based policy improvement step of MuZero provides a stronger learning signal than the high bias, high variance targets used by Q-learning."

  - `post` <http://www.furidamu.org/blog/2020/12/22/muzero-intuition>
  - `post` <https://deepmind.com/blog/article/muzero-mastering-go-chess-shogi-and-atari-without-rules>
  - `video` <https://youtube.com/playlist?list=PLnn6VZp3hqNsrsp_Bg-bEfzzhJ3SuEZE9>
  - `video` <https://youtube.com/watch?v=L0A86LmH7Yw> (Schrittwieser)
  - `video` <https://slideslive.com/38922736/latebreaking-papers-mastering-atari-go-chess-and-shogi-by-planning-with-a-learned-model> (Schrittwieser)
  - `video` <https://youtube.com/watch?v=vt5jOSy7cz8> (Schrittwieser)
  - `video` <https://pscp.tv/w/1mnGelLjoBWKX> (44:00) (Lillicrap)
  - `video` <https://youtube.com/watch?v=We20YSAJZSE> (Kilcher)
  - `video` <https://slideslive.com/38923124/nonsupervised-learning-and-decision-making?t=1832> (Rezende)
  - `video` <https://youtu.be/BGyRM5vCkfw?t=26m54s> (Engalych) `in russian`
  - `notes` <https://www.shortscience.org/paper?bibtexKey=journals/corr/1911.08265>
  - `paper` <https://rdcu.be/ccErB> ("Nature" magazine)
  - `paper` ["Vector Quantized Models for Planning"](https://arxiv.org/abs/2106.04615) by Ozair et al.
  - `paper` ["Learning and Planning in Complex Action Spaces"](https://arxiv.org/abs/2104.06303) by Hubert et al.
  - `paper` ["Online and Offline Reinforcement Learning by Planning with a Learned Model"](https://arxiv.org/abs/2104.06294) by Schrittwieser et al. ([talk](https://youtube.com/watch?v=pgZhGavMHcU) `video`, [post](https://www.furidamu.org/blog/2021/12/04/online-and-offline-reinforcement-learning-by-planning-with-a-learned-model)) *(MuZero Unplugged)*


#### ["Mastering the Game of Go without Human Knowledge"](https://deepmind.com/documents/119/agz_unformatted_nature.pdf) Silver et al.
  `AlphaGo Zero`
>	"A long-standing goal of artificial intelligence is an algorithm that learns, tabula rasa, superhuman proficiency in challenging domains. Recently, AlphaGo became the first program to defeat a world champion in the game of Go. The tree search in AlphaGo evaluated positions and selected moves using deep neural networks. These neural networks were trained by supervised learning from human expert moves, and by reinforcement learning from self-play. Here, we introduce an algorithm based solely on reinforcement learning, without human data, guidance, or domain knowledge beyond game rules. AlphaGo becomes its own teacher: a neural network is trained to predict AlphaGo’s own move selections and also the winner of AlphaGo’s games. This neural network improves the strength of tree search, resulting in higher quality move selection and stronger self-play in the next iteration. Starting tabula rasa, our new program AlphaGo Zero achieved superhuman performance, winning 100-0 against the previously published, champion-defeating AlphaGo."

>	"AlphaGo Zero learns two functions (which take as input the current board):
>	- A prior over moves p is trained to predict what AlphaGo will eventually decide to do
>	- A value function v is trained to predict which player will win (if AlphaGo plays both sides)
>	Both are trained with supervised learning. Once we have these two functions, AlphaGo actually picks its moves by using 1600 steps of Monte Carlo Tree Search, using p and v to guide the search. It trains p to bypass this expensive search process and directly pick good moves. As p improves, the expensive search becomes more powerful, and p chases this moving target."

>	"AlphaGo Zero uses a quite different approach to deep RL than typical (model-free) algorithms such as policy gradient or Q-learning. By using AlphaGo search we massively improve the policy and self-play outcomes - and then we apply simple, gradient based updates to train the next policy + value network. This appears to be much more stable than incremental, gradient-based policy improvements that can potentially forget previous improvements."  
>	"We chose to focus more on reinforcement learning, as we believed it would ultimately take us beyond human knowledge. Our recent results actually show that a supervised-only approach can achieve a surprisingly high performance - but that reinforcement learning was absolutely key to progressing far beyond human levels."  

>	"AlphaGo improves the policy through REINFORCE, which is highly sample-inefficient. Then, it learns the value function for that policy. In REINFORCE one generates trajectories and then changes their probability based on the outcome of the match.  
>	AlphaGo Zero, on the other hand, changes the trajectories themselves. During self-play, an expert (MCTS) tells the policy-value network how to improve its policy-part right away. Moreover, the improved move is the one that's played, so, in the end, the outcome will be based on the improved policy. Therefore we're basically doing Generalized Policy Iteration because we're greedily improving the policy as we go and learning the value of this improved policy."  

>	"Differences from AlphaGo:  
>	- No human data. Learns solely by self-play reinforcement learning, starting from random.  
>	- No human features. Only takes raw board as input.  
>	- Single neural network. Policy and value networks are combined into one neural network (resnet).  
>	- Simpler search. No randomised Monte-Carlo rollouts, only uses neural network to evaluate."  

----
>	"There's a continuum between expert iteration and policy gradients. Let's say we have a two probability distributions, called policy and expert. We can write down a distance between them in two different ways. (1) KL[policy, expert] = policy * log(expert) - S[policy] (2) KL[expert, policy] = expert * log(policy) + constant. Policy gradients uses (1), and we set expert = exp(advantage estimate). AGZ uses (2) and defines expert using MCTS on the policy. The continuum between policy gradients and AGZ arises because we can vary the amount of work we put into computing the expert policy. On one extreme, policy gradient methods use a very cheap-to-compute expert: the advantage function estimate. On the other extreme, AGZ uses a very expensive-to-compute expert (via MCTS), which is much better than the current policy. Another dimension in this expert space is the bias-variance tradeoff: whether we use a Monte-Carlo estimate of returns or a learned value function. I'm curious to know under what conditions you benefit from using a more expensive expert. Anyway, I think there are a lot of interesting experiments left to do to analyze the space of algorithms between policy gradients and expert iteration."  

  - `post` <https://deepmind.com/blog/alphago-zero-learning-scratch/>
  - `video` <https://youtube.com/playlist?list=PLnn6VZp3hqNsrsp_Bg-bEfzzhJ3SuEZE9>
  - `video` <https://vimeo.com/252184928/#t=711> (Silver)
  - `video` <https://youtu.be/DXNqYSNvnjA?t=16m41s> (Hassabis)
  - `video` <https://youtube.com/watch?v=6fKG4wJ7uBk> (Baudis)
  - `video` <https://youtube.com/watch?v=XuzIqE2IshY> (Kington)
  - `video` <https://youtube.com/watch?v=_x9bXso3wo4> (Hinzman)
  - `video` <https://youtu.be/V0HNXVSrvhg?t=1h20m45s> + <https://youtu.be/Lz5_xFGt2hA?t=3m11s> (Grinchuk) `in russian`
  - `video` <https://youtu.be/BGyRM5vCkfw?t=16m30s> (Engalych) `in russian`
  - `video` <https://youtu.be/WM4HC720Cms?t=1h34m49s> (Nikolenko) `in russian`
  - `video` <https://youtu.be/zHjE07NBA_o?t=1h10m24s> (Kozlov) `in russian`
  - `post` <http://depthfirstlearning.com/2018/AlphaGoZero>
  - `post` <http://inference.vc/alphago-zero-policy-improvement-and-vector-fields/>
  - `post` <http://tim.hibal.org/blog/alpha-zero-how-and-why-it-works/>
  - `post` <https://reddit.com/r/MachineLearning/comments/76xjb5/ama_we_are_david_silver_and_julian_schrittwieser/dolnq31/> (Anthony)
  - `notes` <https://blog.acolyer.org/2017/11/17/mastering-the-game-of-go-without-human-knowledge/>
  - `notes` <https://dropbox.com/s/fuwhivftv998f6q/AlphaGoZeroPseudoCode.pdf>
  - `code` <https://github.com/pytorch/ELF/tree/master/src_py/elfgames/go>
  - `code` <https://github.com/tensorflow/minigo>
  - `code` <https://github.com/leela-zero/leela-zero>
  - `code` <https://github.com/maxpumperla/deep_learning_and_the_game_of_go>
  - `paper` ["Reinforcement Learning as Classification: Leveraging Modern Classifiers"](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.7.474&rep=rep1&type=pdf) by Lagoudakis and Parr
  - `paper` ["Approximate Modified Policy Iteration and its Application to the Game of Tetris"](http://jmlr.org/papers/v16/scherrer15a.html) by Scherrer et al.


#### ["Mastering the Game of Go with Deep Neural Networks and Tree Search"](https://storage.googleapis.com/deepmind-media/alphago/AlphaGoNaturePaper.pdf) Silver et al.
  `AlphaGo`
>	"The game of Go has long been viewed as the most challenging of classic games for artificial intelligence due to its enormous search space and the difficulty of evaluating board positions and moves. We introduce a new approach to computer Go that uses value networks to evaluate board positions and policy networks to select moves. These deep neural networks are trained by a novel combination of supervised learning from human expert games, and reinforcement learning from games of self-play. Without any lookahead search, the neural networks play Go at the level of state-of-the-art Monte-Carlo tree search programs that simulate thousands of random games of self-play. We also introduce a new search algorithm that combines Monte-Carlo simulation with value and policy networks. Using this search algorithm, our program AlphaGo achieved a 99.8% winning rate against other Go programs, and defeated the European Go champion by 5 games to 0. This is the first time that a computer program has defeated a human professional player in the full-sized game of Go, a feat previously thought to be at least a decade away."

----
>	"Google AlphaGo is a historical tour of AI ideas: 70s (Alpha-Beta), 80s/90s (reinforcement learning & self-play), 00's (Monte-Carlo), 10's (deep neural networks)."  
>	"The most important application of reinforcement learning here is to learn a value function which aims to predict with which probability a certain position will lead to winning the game. The learned expert moves are already good, but the network that produces them did not learn with the objective to win the game, but only to minimize the differences to the teacher values in the training data set."  

  - <https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#games> (demo)
  - `video` <https://youtube.com/playlist?list=PLnn6VZp3hqNsrsp_Bg-bEfzzhJ3SuEZE9>
  - `video` <http://youtube.com/watch?v=4D5yGiYe8p4> (Silver)
  - `video` <http://youtube.com/watch?v=LX8Knl0g0LE> (Huang)
  - `video` <http://youtu.be/CvL-KV3IBcM?t=31m55s> (Graepel)
  - `video` <http://youtube.com/watch?v=UMm0XaCFTJQ> (Sutton, Szepesvari, Bowling, Hayward, Muller)
  - `video` <https://youtube.com/watch?v=BGyRM5vCkfw> (Engalych) `in russian`
  - `video` <https://youtu.be/WM4HC720Cms?t=1h18m21s> (Nikolenko) `in russian`
  - `video` <https://youtube.com/watch?v=zHjE07NBA_o> (Kozlov) `in russian`
  - `notes` <https://github.com/Rochester-NRT/RocAlphaGo/wiki>
  - `code` <https://github.com/brilee/MuGo>
  - `code` <https://github.com/maxpumperla/deep_learning_and_the_game_of_go>


#### ["Thinking Fast and Slow with Deep Learning and Tree Search"](https://arxiv.org/abs/1705.08439) Anthony, Tian, Barber
  `Expert Iteration` `ExIt`
>	"Sequential decision making problems, such as structured prediction, robotic control, and game playing, require a combination of planning policies and generalisation of those plans. In this paper, we present Expert Iteration (ExIt), a novel reinforcement learning algorithm which decomposes the problem into separate planning and generalisation tasks. Planning new policies is performed by tree search, while a deep neural network generalises those plans. Subsequently, tree search is improved by using the neural network policy to guide search, increasing the strength of new plans. In contrast, standard deep Reinforcement Learning algorithms rely on a neural network not only to generalise plans, but to discover them too. We show that ExIt outperforms REINFORCE for training a neural network to play the board game Hex, and our final tree search agent, trained tabula rasa, defeats MoHex 1.0, the most recent Olympiad Champion player to be publicly released."

>	"Planning new policies is performed by tree search, while a deep neural network generalises those plans."  
>	"Expert Iteration can be viewed as an extension of Imitation Learning methods to domains where the best known experts are unable to achieve satisfactory performance. In standard IL an apprentice is trained to imitate the behaviour of an expert. In ExIt, we extend this to an iterative learning process. Between each iteration, we perform an Expert Improvement step, where we bootstrap the (fast) apprentice policy to increase the performance of the (comparatively slow) expert."  
>	"Imitation Learning is generally appreciated to be easier than Reinforcement Learning, and this partly explains why ExIt is more successful than model-free methods like REINFORCE. Furthermore, for MCTS to recommend a move, it must be unable to find any weakness with its search. Effectively, therefore, a move played by MCTS is good against a large selection of possible opponents. In contrast, in regular self play (in which the opponent move is made by the network playing as the opposite colour), moves are recommended if they beat only this single opponent under consideration. This is, we believe, a key insight into why ExIt works well (when using MCTS as the expert) - the apprentice effectively learns to play well against many opponents."  

>	"ExIt is closely analogous to the Bellman update in Q-learning and can be viewed as analog of dynamic programming where neural networks replace lookup tables."

>	"ExIt is a version of Approximate Policy Iteration, where the policy improvement operator performs a multiple-step policy improvement, rather than a 1-step greedy improvement."

  - `post` <https://davidbarber.github.io/blog/2017/11/07/Learning-From-Scratch-by-Thinking-Fast-and-Slow-with-Deep-Learning-and-Tree-Search/> (Barber)
  - `post` <https://reddit.com/r/MachineLearning/comments/76xjb5/ama_we_are_david_silver_and_julian_schrittwieser/dolnq31/> (Anthony)
  - `paper` ["Dual Policy Iteration"](https://arxiv.org/abs/1805.10755) by Sun et al.


#### ["Policy Gradient Search: Online Planning and Expert Iteration without Search Trees"](https://arxiv.org/abs/1904.03646) Anthony, Nishihara, Moritz, Salimans, Schulman
  `Expert Iteration` `PGS-ExIt`
>	"Monte Carlo Tree Search algorithms perform simulation-based search to improve policies online. During search, the simulation policy is adapted to explore the most promising lines of play. MCTS has been used by state-of-the-art programs for many problems, however a disadvantage to MCTS is that it estimates the values of states with Monte Carlo averages, stored in a search tree; this does not scale to games with very high branching factors. We propose an alternative simulation-based search method which adapts a neural network simulation policy online via policy gradient updates, avoiding the need for a search tree. In Hex, PGS achieves comparable performance to MCTS, and an agent trained using Expert Iteration with PGS was able defeat MoHex 2.0, the strongest open-source Hex agent, in 9x9 Hex."

>	"We test PGS on 9x9 and 13x13 Hex, a domain where MCTS has been used in all state-of-the-art players since 2009. We find that PGS is significantly stronger than MCS, and competitive with MCTS. Additionally, we show that Policy Gradient Search Expert Iteration is able to defeat MOHEX 2.0 in 9x9 Hex tabula rasa, the first agent to do so without using explicit search trees."

>	"MCTS builds an explicit search tree, storing visit counts and value estimates at each node - in other words, creating a tabular value function.  To be effective, this requires that nodes in the search tree are visited multiple times. This is true in many classical board games, but many real world problems have large branching factors that make MCTS hard to use. Large branching factors can be caused by very large action spaces, or chance nodes. In the case of large action spaces, a prior policy can be used to discount weak actions, reducing the effective branching factor. Stochastic transitions are harder to deal with, as prior policies cannot be used to reduce the branching factor at chance nodes. In contrast, Monte Carlo Search algorithms have no such requirement. Whereas MCTS uses value estimates in each node to adapt the simulation policy, MCS algorithms have a fixed simulation policy throughout the search. However, because MCS does not improve the quality of simulations during search, it produces significantly weaker play than MCTS."

>	"Policy Gradient Search trains its simulation policy during search using policy gradient RL. This gives the advantages of an adaptive simulation policy, without requiring an explicit search tree to be built. Simulation policy is represented by a neural network with identical architecture to the global policy network. At the start of each game, the parameters of the policy network are set to those of the global policy network. Once we reach a final state for the simulation sL after t steps, we estimate the value of this state using the global value network, and use this estimate to update the simulation policy parameters using REINFORCE. These updates can be seen as fine-tuning the global policy to the current sub-game."

>	"PGS is more expensive than MCS because it must perform the policy gradient update to the neural network parameters. The backward pass through our network takes approximately twice as long as the forward pass, making PGS 3-4 times more expensive than MCS. In order to reduce the computational cost of the algorithm, during policy gradient search, we adapt the parameters of the policy head only. This reduces the flops used by the backward pass by a factor of over 100, making the difference in computational cost between MCS and PGS negligible."

>	"PGS-ExIt decomposes the overall RL problem into many sub-problems, one per self-play game, and attempts to solve (or at least make progress on) each of the sub-problems with a model-free RL algorithm. The solutions to sub-problems are distilled back into a global network."

>	"PGS is also effective during training when used within the Expert Iteration framework, resulting in the first competitive Hex agent trained tabula rasa without use of a search tree. In contrast, similar REINFORCE algorithm alone was previously been found to not be competitve with an ExIt algorithm that used MCTS experts. Ablations show that PGS-ExIt significantly outperforms MCS in the Expert Iteration framework, and also provide the first empirical data showing that MCTS-ExIt algorithms outperform traditional policy iteration approaches."

>	"The results presented in this work are on the deterministic, discrete action space domain of Hex. This allowed for direct comparison to MCTS, but the most exciting potential applications of PGS are to problems where MCTS cannot be readily used, such as problems with stochastic state transitions or continuous action spaces."

  - `paper` ["Sample-Based Learning and Search with Permanent and Transient Memories"](https://researchgate.net/publication/221346457_Sample-based_learning_and_search_with_permanent_and_transient_memories) by Silver et al. ([talk](http://videolectures.net/icml08_silver_sbl) `video`) *(Dyna-2)*


#### ["Combining Deep Reinforcement Learning and Search for Imperfect-Information Games"](https://arxiv.org/abs/2007.13544) Brown et al.
  `ReBeL`
>	"The combination of deep reinforcement learning and search at both training and test time is a powerful paradigm that has led to a number of successes in single-agent settings and perfect-information games, best exemplified by AlphaZero. However, prior algorithms of this form cannot cope with imperfect-information games. This paper presents ReBeL, a general framework for self-play reinforcement learning and search that provably converges to a Nash equilibrium in any two-player zero-sum game. In the simpler setting of perfect-information games, ReBeL reduces to an algorithm similar to AlphaZero. Results in two different imperfect-information games show ReBeL converges to an approximate Nash equilibrium. We also show ReBeL achieves superhuman performance in heads-up no-limit Texas hold'em poker, while using far less domain knowledge than any prior poker AI."

  - `post` <https://ai.facebook.com/blog/rebel-a-general-game-playing-ai-bot-that-excels-at-poker-and-more>
  - `video` <https://youtube.com/watch?v=mCldyXOYNok> (Brown)
  - `video` <https://youtube.com/watch?v=BhUWvQmLzSk> (Kilcher)


#### ["DeepStack: Expert-Level Artificial Intelligence in No-Limit Poker"](http://arxiv.org/abs/1701.01724) Moravcik et al.
  `DeepStack`
>	"Artificial intelligence has seen a number of breakthroughs in recent years, with games often serving as significant milestones. A common feature of games with these successes is that they involve information symmetry among the players, where all players have identical information. This property of perfect information, though, is far more common in games than in real-world problems. Poker is the quintessential game of imperfect information, and it has been a longstanding challenge problem in artificial intelligence. In this paper we introduce DeepStack, a new algorithm for imperfect information settings such as poker. It combines recursive reasoning to handle information asymmetry, decomposition to focus computation on the relevant decision, and a form of intuition about arbitrary poker situations that is automatically learned from selfplay games using deep learning. In a study involving dozens of participants and 44,000 hands of poker, DeepStack becomes the first computer program to beat professional poker players in heads-up no-limit Texas hold’em. Furthermore, we show this approach dramatically reduces worst-case exploitability compared to the abstraction paradigm that has been favored for over a decade."

>	"DeepStack is the first computer program to defeat professional poker players at heads-up nolimit Texas Hold’em, an imperfect information game with 10^160 decision points. Notably it achieves this goal with almost no domain knowledge or training from expert human games. The implications go beyond just being a significant milestone for artificial intelligence. DeepStack is a paradigmatic shift in approximating solutions to large, sequential imperfect information games. Abstraction and offline computation of complete strategies has been the dominant approach for almost 20 years. DeepStack allows computation to be focused on specific situations that arise when making decisions and the use of automatically trained value functions. These are two of the core principles that have powered successes in perfect information games, albeit conceptually simpler to implement in those settings. As a result, for the first time the gap between the largest perfect and imperfect information games to have been mastered is mostly closed. As “real life consists of bluffing, deception, asking yourself what is the other man going to think”, DeepStack also has implications for seeing powerful AI applied more in settings that do not fit the perfect information assumption. The old paradigm for handling imperfect information has shown promise in applications like defending strategic resources and robust decision making as needed for medical treatment recommendations. The new paradigm will hopefully open up many more possibilities."

>	"Imperfect information games require more complex reasoning than similarly sized perfect information games. The correct decision at a particular moment depends upon the probability distribution over private information that the opponent holds, which is revealed through their past actions. However, how our opponent’s actions reveal that information depends upon their knowledge of our private information and how our actions reveal it. This kind of recursive reasoning is why one cannot easily reason about game situations in isolation, which is at the heart of heuristic search methods for perfect information games. Competitive AI approaches in imperfect information games typically reason about the entire game and produce a complete strategy prior to play. Counterfactual regret minimization is one such technique that uses self-play to do recursive reasoning through adapting its strategy against itself over successive iterations. If the game is too large to be solved directly, the common response is to solve a smaller, abstracted game. To play the original game, one translates situations and actions from the original game to the abstract game."

>	"DeepStack takes a fundamentally different approach. It continues to use the recursive reasoning of CFR to handle information asymmetry. However, it does not compute and store a complete strategy prior to play and so has no need for explicit abstraction. Instead it considers each particular situation as it arises during play, but not in isolation. It avoids reasoning about the entire remainder of the game by substituting the computation beyond a certain depth with a fast approximate estimate. This estimate can be thought of as DeepStack’s intuition: a gut feeling of the value of holding any possible private cards in any possible poker situation. Finally, DeepStack’s intuition, much like human intuition, needs to be trained. We train it with deep learning using examples generated from random poker situations. We show that DeepStack is theoretically sound, produces strategies substantially more difficult to exploit than abstraction-based techniques, and defeats professional poker players at HUNL with statistical significance."

----
>	"In the past, perfect information games (chess, checkers, go) have been easier algorithmically than imperfect information games like poker. Powerful techniques like Alpha-Beta search, heuristic functions, depth-limited lookahead & Monte Carlo Tree Search work with perfect information games. They allow an AI to ignore the past and focus its computation on the tiny, immediate subgame most relevant for choosing actions. Until now, these techniques didn't really work in imperfect info games like poker, due to uncertainty about what each player knows. There is no single state to search from, but a set of states for each player. Past actions reveal info about what cards they hold. In imperfect info games like poker, local search hasn’t performed well. Had to solve the whole game at once, not as small fragments. But poker games are huge, and except for smallest versions, can't be solved exactly. Dominant technique was to solve a simplified game. This was called Abstraction-Solving-Translation. Simplify a game, solve it, use the simplified strategy in the real game. That simplification introduces mistakes. In some games, this still worked well enough to beat pros. AST didn't work well in No-Limit poker. Humans exploited simplified betting, and in huge pots, fine details of cards matter. This is the DeepStack breakthrough: it reintroduces powerful local search techniques to the imperfect info setting. No abstraction! It only considers a small local subgame to pick actions, given the "public state" and summary info of earlier actions in the hand. Early in the game, Deep Learning supplies a heuristic function to avoid searching to the end of the game. On the turn & river, it solves from the current decision until the end of the game and re-solves after every opponent action. On the preflop & flop, it solves to the end of the round then consults a deep neural net for value estimate of playing the turn/river. This NN is trained from randomly-generated hands (no human data needed) and must return value of every hand for each player. Deep Stack doesn't abstract cards or have to translate opponents bets. It always gets these details exactly right. This means there are no easy exploits, & we developed a new exploitability measurement program, Local Best Response, to show this. Also lets DeepStack play with any stacks/blinds. Can play freezeouts, cash games, etc. Earlier programs were specific to 1 stack size!"

>	"Compared to Libratus, on the turn/river both programs are pretty similar: both use the same "continual resolving" trick (and counterfactual regret minimization). Biggest difference is preflop/flop. DeepStack uses continual resolving there too, so it can't get tricked by bet size attacks. Libratus used the old precomputed-strategy method for preflop/flop. It had holes they had to patch overnight, as pros found them. DeepStack can play any stack sizes, so can do freezeouts, cash games, etc. Libratus can only do 200bb stacks. Last big difference is resources. Libratus runs on a huge supercomputer, Cepheus only needs a laptop with a good GPU."

>	"DeepStack does not compute and store a complete strategy prior to play. DeepStack computes a strategy based on the current state of the game for only the remainder of the hand, not maintaining one for the full game, which leads to lower overall exploitability."

>	"Despite using ideas from abstraction, DeepStack is fundamentally different from abstraction-based approaches, which compute and store a strategy prior to play. While DeepStack restricts the number of actions in its lookahead trees, it has no need for explicit abstraction as each re-solve starts from the actual public state, meaning DeepStack always perfectly understands the current situation."

>	"DeepStack is the first theoretically sound application of heuristic search methods—which have been famously successful in games like checkers, chess, and Go - to imperfect information games."

>	"At a conceptual level, DeepStack’s continual re-solving, “intuitive” local search and sparse lookahead trees describe heuristic search, which is responsible for many AI successes in perfect information games. Until DeepStack, no theoretically sound application of heuristic search was known in imperfect information games."

>	"During re-solving, DeepStack doesn’t need to reason about the entire remainder of the game because it substitutes computation beyond a certain depth with a fast approximate estimate, DeepStack’s "intuition" - a gut feeling of the value of holding any possible private cards in any possible poker situation. Finally, DeepStack’s intuition, much like human intuition, needs to be trained. We train it with deep learning using examples generated from random poker situations."

>	"Part of DeepStack's development is also a technique designed to find flaws in poker strategies. Local Best Response (LBR) is one of the cool new algorithms in Science paper. LBR looks directly at the strategy, like what a human could get from playing millions of hands to know its range. Older programs get beat by LBR for 4x more than folding every hand! DeepStack has no holes exposed by the LBR algorithm."

  - <https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#games> (demo)
  - `paper` <http://science.sciencemag.org/content/early/2017/03/01/science.aam6960>
  - `video` <https://youtube.com/playlist?list=PLX7NnbJAq7PlA2XpynViLOigzWtmr6QVZ> (demo matches)
  - `video` <https://vimeo.com/248532904> (Bowling)
  - `video` <https://youtu.be/02xIkHowQOk?t=11m45s> (Bowling)
  - `video` <https://youtube.com/watch?v=qndXrHcV1sM> (Bowling)
  - `video` <http://videolectures.net/aaai2017_bowling_sandholm_poker/#t=177> (Bowling)
  - `video` <https://youtube.com/watch?v=eFlgrFLJ9Vk> (Valenzano)
  - `post` <https://www.depthfirstlearning.com/2018/DeepStack>
  - <http://deepstack.ai>
  - <http://twitter.com/DeepStackAI>
  - `code` <https://github.com/lifrordi/DeepStack-Leduc>


#### ["Deep Counterfactual Regret Minimization"](https://arxiv.org/abs/1811.00164) Brown, Lerer, Gross, Sandholm
  `Deep CFR`
>	"Counterfactual Regret Minimization is the leading framework for solving large imperfect-information games. It converges to an equilibrium by iteratively traversing the game tree. In order to deal with extremely large games, abstraction is typically applied before running CFR. The abstracted game is solved with tabular CFR, and its solution is mapped back to the full game. This process can be problematic because aspects of abstraction are often manual and domain specific, abstraction algorithms may miss important strategic nuances of the game, and there is a chicken-and-egg problem because determining a good abstraction requires knowledge of the equilibrium of the game. This paper introduces Deep Counterfactual Regret Minimization, a form of CFR that obviates the need for abstraction by instead using deep neural networks to approximate the behavior of CFR in the full game. We show that Deep CFR is principled and achieves strong performance in large poker games. This is the first non-tabular variant of CFR to be successful in large games."

>	"Most popular RL algorithms do not converge to good policies (equilibria) in imperfect-information games in theory or in practice. Rather than use tabular CFR with abstraction, this paper introduces a form of CFR, which we refer to as Deep Counterfactual Regret Minimization, that uses function approximation with deep neural networks to approximate the behavior of tabular CFR on the full, unabstracted game. We prove that Deep CFR converges to an Epsilon-Nash equilibrium in two-player zero-sum games and empirically evaluate performance in poker variants, including heads-up limit Texas hold’em. We show Deep CFR outperforms Neural Fictitious Self Play (NFSP) (Heinrich & Silver, 2016), which was the prior leading function approximation algorithm for imperfect-information games, and that Deep CFR is competitive with domain-specific tabular abstraction techniques."

----
>	"The CFR algorithm is actually somewhat similar to Q-learning, but the connection is difficult to see because the algorithms came out of different communities, so the notation is all different."

  - `video` <https://slideslive.com/38917930/learning-theory-games?t=3959> (Brown)
  - <https://reddit.com/r/MachineLearning/comments/ceece3/ama_we_are_noam_brown_and_tuomas_sandholm>
  - <https://int8.io/counterfactual-regret-minimization-for-poker-ai>
  - <http://modelai.gettysburg.edu/2013/cfr/index.html#description>
  - `code` <https://github.com/EricSteinberger/Deep-CFR>
  - `paper` ["Single Deep Counterfactual Regret Minimization"](https://arxiv.org/abs/1901.07621) by Steinberger


#### ["Mastering Chess and Shogi by Self-Play with a General Reinforcement Learning Algorithm"](https://arxiv.org/abs/1712.01815) Silver et al.
  `AlphaZero`
>	"The game of chess is the most widely-studied domain in the history of artificial intelligence. The strongest programs are based on a combination of sophisticated search techniques, domain-specific adaptations, and handcrafted evaluation functions that have been refined by human experts over several decades. In contrast, the AlphaGo Zero program recently achieved superhuman performance in the game of Go, by tabula rasa reinforcement learning from games of self-play. In this paper, we generalise this approach into a single AlphaZero algorithm that can achieve, tabula rasa, superhuman performance in many challenging domains. Starting from random play, and given no domain knowledge except the game rules, AlphaZero achieved within 24 hours a superhuman level of play in the games of chess and shogi (Japanese chess) as well as Go, and convincingly defeated a world-champion program in each case."

----
>	"no opening book, no endgame database, no heuristics, no anything"

>	"One reason why MCTS is so effective compared to Alpha-Beta when you start to use function approximators is that neural network will inevitably have approximation errors. Alpha-Beta search is kind of minimax search and is like glorified big max operator alternating with mins, which will pick out biggest errors in function approximation and propagate it to the root of search tree. Whilst MCTS is averaging over evaluations which tends to cancel out errors in search and can be more effective because of that."

----
>	"AlphaGo Zero tuned the hyper-parameter of its search by Bayesian optimization. In AlphaZero they reuse the same hyper-parameters for all games without game-specific tuning. The sole exception is the noise that is added to the prior policy to ensure exploration; this is scaled in proportion to the typical number of legal moves for that game type. Like AlphaGo Zero, the board state is encoded by spatial planes based only on the basic rules for each game. The actions are encoded by either spatial planes or a flat vector, again based only on the basic rules for each game. They applied the AlphaZero algorithm to chess, shogi, and also Go. Unless otherwise specified, the same algorithm settings, network architecture, and hyper-parameters were used for all three games."

  - <https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#games> (demo)
  - `post` <https://deepmind.com/blog/article/alphazero-shedding-new-light-grand-games-chess-shogi-and-go>
  - `video` <https://youtube.com/playlist?list=PLnn6VZp3hqNsrsp_Bg-bEfzzhJ3SuEZE9>
  - `video` <https://vimeo.com/252184928#t=1468> (Silver)
  - `video` <https://youtu.be/N8_gVrIPLQM?t=47m9s> (Silver)
  - `video` <https://youtube.com/watch?v=mzjGNo9Tz4g> (Silver)
  - `video` <https://youtu.be/3N9phq_yZP0?t=12m43s> (Hassabis)
  - `video` <https://youtu.be/DXNqYSNvnjA?t=21m24s> (Hassabis)
  - `video` <https://youtu.be/BGyRM5vCkfw?t=22m2s> (Engalych) `in russian`
  - `video` <https://youtu.be/WM4HC720Cms?t=1h34m49s> (Nikolenko) `in russian`
  - `notes` <https://blog.acolyer.org/2018/01/10/mastering-chess-and-shogi-by-self-play-with-a-general-reinforcement-learning-algorithm/>
  - `code` <https://lczero.org>
  - `paper` ["Monte-Carlo Tree Search as Regularized Policy Optimization"](https://arxiv.org/abs/2007.12509) by Grill et al.


#### ["Giraffe: Using Deep Reinforcement Learning to Play Chess"](http://arxiv.org/abs/1509.01549) Lai
>	"This report presents Giraffe, a chess engine that uses self-play to discover all its domain-specific knowledge, with minimal hand-crafted knowledge given by the programmer. Unlike previous attempts using machine learning only to perform parameter tuning on hand-crafted evaluation functions, Giraffe’s learning system also performs automatic feature extraction and pattern recognition. The trained evaluation function performs comparably to the evaluation functions of state-of-the-art chess engines - all of which containing thousands of lines of carefully hand-crafted pattern recognizers, tuned over many years by both computer chess experts and human chess masters. Giraffe is the most successful attempt thus far at using end-to-end machine learning to play chess. We also investigated the possibility of using probability thresholds instead of depth to shape search trees. Depth-based searches form the backbone of virtually all chess engines in existence today, and is an algorithm that has become well-established over the past half century. Preliminary comparisons between a basic implementation of probability-based search and a basic implementation of depth-based search showed that our new probability-based approach performs moderately better than the established approach. There are also evidences suggesting that many successful ad-hoc add-ons to depth-based searches are generalized by switching to a probability-based search. We believe the probability-based search to be a more fundamentally correct way to perform minimax. Finally, we designed another machine learning system to shape search trees within the probability-based search framework. Given any position, this system estimates the probability of each of the moves being the best move without looking ahead. The system is highly effective - the actual best move is within the top 3 ranked moves 70% of the time, out of an average of approximately 35 legal moves from each position. This also resulted in a significant increase in playing strength. With the move evaluator guiding a probability-based search using the learned evaluator, Giraffe plays at approximately the level of an FIDE International Master (top 2.2% of tournament chess players with an official rating)."

>	"In this project, we investigated the use of deep reinforcement learning with automatic feature extraction in the game of chess. The results show that the learned system performs at least comparably to the best expert-designed counterparts in existence today, many of which have been fine tuned over the course of decades. The beauty of this approach is in its generality. While it was not explored in this project due to time constraint, it is likely that this approach can easily be ported to other zero-sum turn-based board games, and achieve state-of-art performance quickly, especially in games where there has not been decades of intense research into creating a strong AI player. In addition to the machine learning aspects of the project, we introduced and tested an alternative variant of the decades-old minimax algorithm, where we apply probability boundaries instead of depth boundaries to limit the search tree. We showed that this approach is at least comparable and quite possibly superior to the approach that has been in use for the past half century. We also showed that this formulation of minimax works especially well with our probability-based machine learning approach. Efficiency is always a major consideration when switching from an expert system to a machine learning approach, since expert systems are usually more efficient to evaluate than generic models. This is especially important for applications like a chess engine, where being able to search nodes quickly is strongly correlated with playing strength. Some earlier attempts at applying neural network to chess have been thwarted by large performance penalties. Giraffe’s optimized implementation of neural network, when combined with the much higher vector arithmetics throughput of modern processors and effective caching, allows it to search at a speed that is less than 1 order of magnitude slower than the best modern chess engines, thus making it quite competitive against many chess engines in gameplay without need for time handicap. With all our enhancements, Giraffe is able to play at the level of an FIDE International Master on a modern mainstream PC. While that is still a long way away from the top engines today that play at super-Grandmaster levels, it is able to defeat many lower-tier engines, most of which search an order of magnitude faster. One of the original goals of the project is to create a chess engine that is less reliant on brute-force than its contemporaries, and that goal has certainly been achieved. Unlike most chess engines in existence today, Giraffe derives its playing strength not from being able to see very far ahead, but from being able to evaluate tricky positions accurately, and understanding complicated positional concepts that are intuitive to humans, but have been elusive to chess engines for a long time. This is especially important in the opening and end game phases, where it plays exceptionally well."

>	"It is clear that Giraffe’s evaluation function has at least comparable positional understanding compared to evaluation functions of top engines in the world, which is remarkable because their evaluation functions are all carefully hand-designed behemoths with hundreds of parameters that have been tuned both manually and automatically over several years, and many of them have been worked on by human grandmasters. The test suite likely under-estimates the positional understanding of Giraffe compared to other engines, because most of the themes tested by the test suite are generally well-understood concepts in computer chess that are implemented by many engines, and since the test suite is famous, it is likely that at least some of the engines have been tuned specifically against the test suite. Since Giraffe discovered all the evaluation features through self-play, it is likely that it knows about patterns that have not yet been studied by humans, and hence not included in the test suite. As far as we are aware, this is the first successful attempt at using machine learning to create a chess evaluation function from self-play, including automatic feature extraction (many previous attempts are weight-tuning for hand-designed features), starting from minimal hand-coded knowledge, and achieving comparable performance to state-of-the-art expert-designed evaluation functions."

  - `code` <https://bitbucket.org/waterreaction/giraffe>
  - `paper` ["KnightCap: A Chess Program that Learns by Combining TD(lambda) with Game-tree Search"](https://arxiv.org/abs/cs/9901002) by Baxter, Tridgell, Weaver *(TDLeaf(lambda))*


#### ["Bootstrapping from Game Tree Search"](https://papers.nips.cc/paper/3722-bootstrapping-from-game-tree-search) Veness, Silver, Uther, Blair
  `TreeStrap`
>	"In this paper we introduce a new algorithm for updating the parameters of a heuristic evaluation function, by updating the heuristic towards the values computed by an alpha-beta search. Our algorithm differs from previous approaches to learning from search, such as Samuel’s checkers player and the TD-Leaf algorithm, in two key ways. First, we update all nodes in the search tree, rather than a single node. Second, we use the outcome of a deep search, instead of the outcome of a subsequent search, as the training signal for the evaluation function. We implemented our algorithm in a chess program Meep, using a linear heuristic function. After initialising its weight vector to small random values, Meep was able to learn high quality weights from self-play alone. When tested online against human opponents, Meep played at a master level, the best performance of any chess program with a heuristic learned entirely from self-play."

  - `video` <http://videolectures.net/nips09_veness_bfg/> (Veness)


#### ["Thinking Fast and Slow with Deep Learning and Tree Search"](https://arxiv.org/abs/1705.08439) Anthony, Tian, Barber
  `Expert Iteration` `ExIt`
>	"Sequential decision making problems, such as structured prediction, robotic control, and game playing, require a combination of planning policies and generalisation of those plans. In this paper, we present Expert Iteration, a novel reinforcement learning algorithm which decomposes the problem into separate planning and generalisation tasks. Planning new policies is performed by tree search, while a deep neural network generalises those plans. Subsequently, tree search is improved by using the neural network policy to guide search, increasing the strength of new plans. In contrast, standard deep Reinforcement Learning algorithms rely on a neural network not only to generalise plans, but to discover them too. We show that ExIt outperforms REINFORCE for training a neural network to play the board game Hex, and our final tree search agent, trained tabula rasa, defeats MOHEX, the previous state-of-the-art Hex player."

>	"ExIt can be viewed as an extension of Imitation Learning methods to domains where the best known experts are unable to achieve satisfactory performance. In standard IL an apprentice is trained to imitate the behaviour of an expert. In ExIt, we extend this to an iterative learning process. Between each iteration, we perform an Expert Improvement step, where we bootstrap the (fast) apprentice policy to increase the performance of the (comparatively slow) expert."

>	"Imitation Learning is generally appreciated to be easier than Reinforcement Learning, and this partly explains why ExIt is more successful than model-free methods like REINFORCE. Furthermore, for MCTS to recommend a move, it must be unable to find any weakness with its search. Effectively, therefore, a move played by MCTS is good against a large selection of possible opponents. In contrast, in regular self play (in which the opponent move is made by the network playing as the opposite colour), moves are recommended if they beat only this single opponent under consideration. This is, we believe, a key insight into why ExIt works well (when using MCTS as the expert) - the apprentice effectively learns to play well against many opponents."

  - `post` <https://davidbarber.github.io/blog/2017/11/07/Learning-From-Scratch-by-Thinking-Fast-and-Slow-with-Deep-Learning-and-Tree-Search/> (Barber)
  - `post` <https://reddit.com/r/MachineLearning/comments/76xjb5/ama_we_are_david_silver_and_julian_schrittwieser/dolnq31/> (Anthony)


#### ["Ranked Reward: Enabling Self-Play Reinforcement Learning for Combinatorial Optimization"](https://arxiv.org/abs/1807.01672) Laterre et al.
>	"Adversarial self-play in two-player games has delivered impressive results when used with reinforcement learning algorithms that combine deep neural networks and tree search. Algorithms like AlphaZero and Expert Iteration learn tabula-rasa, producing highly informative training data on the fly. However, the self-play training strategy is not directly applicable to single-player games. Recently, several practically important combinatorial optimization problems, such as the traveling salesman problem and the bin packing problem, have been reformulated as reinforcement learning problems, increasing the importance of enabling the benefits of self-play beyond two-player games. We present the Ranked Reward (R2) algorithm which accomplishes this by ranking the rewards obtained by a single agent over multiple games to create a relative performance metric. Results from applying the R2 algorithm to instances of a two-dimensional and three-dimensional bin packing problems show that it outperforms generic Monte Carlo tree search, heuristic algorithms and integer programming solvers. We also present an analysis of the ranked reward mechanism, in particular, the effects of problem instances with varying difficulty and different ranking thresholds."

  - `post` <https://builders.intel.com/ai/membership/instadeep>
  - `audio` <https://twimlai.com/twiml-talk-302-deep-reinforcement-learning-for-logistics-at-instadeep-with-karim-beguir> (Beguir)


#### ["Solving the Rubik’s Cube Without Human Knowledge"](https://arxiv.org/abs/1805.07470) McAleer, Agostinelli, Shmakov, Baldi
>	"A generally intelligent agent must be able to teach itself how to solve problems in complex domains with minimal human supervision. Recently, deep reinforcement learning algorithms combined with self-play have achieved superhuman proficiency in Go, Chess, and Shogi without human data or domain knowledge. In these environments, a reward is always received at the end of the game; however, for many combinatorial optimization environments, rewards are sparse and episodes are not guaranteed to terminate. We introduce Autodidactic Iteration: a novel reinforcement learning algorithm that is able to teach itself how to solve the Rubik’s Cube with no human assistance. Our algorithm is able to solve 100% of randomly scrambled cubes while achieving a median solve length of 30 moves - less than or equal to solvers that employ human domain knowledge."

>	"Autodidactic Iteration trains the value function through an iterative supervised learning process. In each iteration, the inputs to the neural network are created by starting from the goal state and randomly taking actions. The targets seek to estimate the optimal value function by performing a breadth-first search from each input state and using the current network to estimate the value of each of the leaves in the tree. Updated value estimates for the root nodes are obtained by recursively backing up the values for each node using a max operator. The policy network is similarly trained by constructing targets from the move that maximizes the value. After the network is trained, it is combined with MCTS to efficiently solve the Rubik’s Cube."

  - `video` <https://youtube.com/watch?v=DYKS0rC98ME> (Lapan) `in russian`
  - `post` <https://www.alexirpan.com/2019/10/29/openai-rubiks.html>


#### ["AlphaD3M: Machine Learning Pipeline Synthesis"](https://www.cs.columbia.edu/~idrori/AlphaD3M.pdf) Drori et al.
  `AlphaD3M` `meta-learning` `ICML 2018`
>	"We introduce AlphaD3M, an automatic machine learning system based on meta reinforcement learning using sequence models with self play. AlphaD3M is based on edit operations performed over machine learning pipeline primitives providing explainability. We compare AlphaD3M with state-of-the-art AutoML systems: Autosklearn, Autostacker, and TPOT, on OpenML datasets. AlphaD3M achieves competitive performance while being an order of magnitude faster, reducing computation time from hours to minutes, and is explainable by design."

>	"Inspired by AlphaZero, we frame the problem of pipeline synthesis for model discovery as a single-player game (McAleer et al., 2018): the player iteratively builds a pipeline by selecting among a set of actions which are insertion, deletion, replacement of pipeline parts. An inherent advantage of this approach is that at the end of the process, once there is a working pipeline, it is completely explainable, including all the actions and decisions which led to its synthesis. Another advantage is that our approach leverages recent advances in deep reinforcement learning using self play, specifically expert iteration and AlphaZero, by using a neural network for predicting pipeline performance and action probabilities, along with a Monte-Carlo Tree Search, which takes strong decisions based on the network. The process progresses by self play with iterative self improvement, and is known to be highly efficient at finding a solution to search problems in very high dimensional spaces. We evaluate our approach using the OpenML dataset on the tasks of classification and regression, demonstrating competitive performance and computation times an order of magnitude faster than other AutoML systems."

>	"Game. AlphaZero: Go, chess. AlphaD3M: AutoML  
	Unit. AlphaZero: piece. AlphaD3M: pipeline primitive  
	State. AlphaZero: configuration. AlphaD3M: meta data, task, pipeline  
	Action. AlphaZero: move. AlphaD3M: insert, delete, replace  
	Reward. AlphaZero: win, lose, draw. AlphaD3M: pipeline performance"  

>	"Our goal is to search within a large space for the machine learning, and pre and post processing primitives and parameters which together constitute a pipeline for solving a task on a given dataset. The problem is that of high dimensional search. Although the datasets differ, the solution pipelines contain recurring patterns. Just as a data scientist develops intuition and patterns about the pipeline components, we use a neural network along with a Monte-Carlo tree search in an iterative process. This combination results in the network AlphaD3M: Machine Learning Pipeline Synthesis learning these patterns while the search splits the problem into components and looks ahead for solutions. By self play and evaluations the network improves, incorporating a better intuition. An advantage of this iterative dual process is that it is computationally efficient in high dimensional search."

>	"A pipeline is a data mining work flow, of pre-processing, feature extraction, feature selection, estimation, and post-processing primitives. Our architecture models meta data and an entire pipeline chain as state rather than individual primitives. A pipeline, together with the meta data and problem definition is analogous to an entire game board configuration. The actions are transitions from one state (pipeline) to another."

>	"We presented the first single player AlphaZero game representation applied to meta learning by modeling meta-data, task, and entire pipelines as state."

  - `slides` <https://cims.nyu.edu/~drori/alphad3m-slides.pdf>
  - `paper` ["Automatic Machine Learning by Pipeline Synthesis using Model-Based Reinforcement Learning and a Grammar"](https://arxiv.org/abs/1905.10345) by Drori et al.


#### ["Towards AlphaChem: Chemical Synthesis Planning with Tree Search and Deep Neural Network Policies"](https://arxiv.org/abs/1702.00020) Segler, Preus, Waller
>	"Retrosynthesis is a technique to plan the chemical synthesis of organic molecules, for example drugs, agro- and fine chemicals. In retrosynthes is, a search tree is built by analysing molecules recursively and dissecting them into simpler molecular building blocks until one obtains a set of known building blocks. The search space is intractably large, and it is difficult to determine the value of retrosynthetic positions. Here, we propose to model retrosynthesis as a Markov Decision Process. In combination with a Deep Neural Network policy learned from essentially the complete published knowledge of chemistry, Monte Carlo Tree Search (MCTS) can be used to evaluate positions. In exploratory studies, we demonstrate that MCTS with neural network policies outperforms the traditionally used best-first search with hand-coded heuristics."

  - `video` <https://youtu.be/N8_gVrIPLQM?t=1h45s> (Silver)


#### ["Terrain-Adaptive Locomotion Skills Using Deep Reinforcement Learning"](http://www.cs.ubc.ca/~van/papers/2016-TOG-deepRL/2016-TOG-deepRL.pdf) Peng, Berseth, van de Panne
>	"Reinforcement learning offers a promising methodology for developing skills for simulated characters, but typically requires working with sparse hand-crafted features. Building on recent progress in deep reinforcement learning, we introduce a mixture of actor-critic experts approach that learns terrain-adaptive dynamic locomotion skills using high-dimensional state and terrain descriptions as input, and parameterized leaps or steps as output actions. MACE learns more quickly than a single actor-critic approach and results in actor-critic experts that exhibit specialization. Additional elements of our solution that contribute towards efficient learning include Boltzmann exploration and the use of initial actor biases to encourage specialization. Results are demonstrated for multiple planar characters and terrain classes."

>	"We introduce a novel mixture of actor-critic experts architecture to enable accelerated learning. MACE develops n individual control policies and their associated value functions, which each then specialize in particular regimes of the overall motion. During final policy execution, the policy associated with the highest value function is executed, in a fashion analogous to Q-learning with discrete actions. We show the benefits of Boltzmann exploration and various algorithmic features for our problem domain."

  - `video` <https://youtube.com/watch?v=KPfzRSBzNX4> + <https://youtube.com/watch?v=A0BmHoujP9k> (demo)
  - `video` <https://youtube.com/watch?v=mazfn4dHPRM> + <https://youtube.com/watch?v=RTuSHI5FNzg> (overview)
  - `code` <https://github.com/xbpeng/DeepTerrainRL>


#### ["Making Contextual Decisions with Low Technical Debt"](http://arxiv.org/abs/1606.03966) Agarwal et al.
  `Project Custom Decision`
>	"Applications and systems are constantly faced with decisions that require picking from a set of actions based on contextual information. Reinforcement-based learning algorithms such as contextual bandits can be very effective in these settings, but applying them in practice is fraught with technical debt, and no general system exists that supports them completely. We address this and create the first general system for contextual learning, called the Decision Service. Existing systems often suffer from technical debt that arises from issues like incorrect data collection and weak debuggability, issues we systematically address through our ML methodology and system abstractions. The Decision Service enables all aspects of contextual bandit learning using four system abstractions which connect together in a loop: explore (the decision space), log, learn, and deploy. Notably, our new explore and log abstractions ensure the system produces correct, unbiased data, which our learner uses for online learning and to enable real-time safeguards, all in a fully reproducible manner. The Decision Service has a simple user interface and works with a variety of applications: we present two live production deployments for content recommendation that achieved click-through improvements of 25-30%, another with 18% revenue lift in the landing page, and ongoing applications in tech support and machine failure handling. The service makes real-time decisions and learns continuously and scalably, while significantly lowering technical debt."

>	"We have presented the Decision Service: a powerful tool to support the complete data lifecycle, which automates many of the burdensome tasks that data scientists face such as gathering the right data and deploying in an appropriate manner. Instead, a data scientist can focus on more core tasks such as finding the right features, representation, or signal to optimize against. The data lifecycle support also makes basic application of the Decision Service feasible without a data scientist. To assist in lowering the barrier to entry, we are exploring techniques based on expert learning and hyperparameter search that may further automate the process. Since the policy evaluation techniques can provide accurate predictions of online performance, such automations are guaranteed to be statistically sound. We are also focusing on making the decision service easy to deploy and use because we believe this is key to goal of democratizing machine learning for everyone. The Decision Service can also naturally be extended to a greater variety of problems, all of which can benefit from data lifecycle support. Plausible extensions might address advanced variants like reinforcement and active learning, and simpler ones like supervised learning."

----
>	"It is the first general purpose reinforcement-based learning system. Wouldn’t it be great if Reinforcement Learning algorithms could easily be used to solve all reinforcement learning problems? But there is a well-known problem: It’s very easy to create natural RL problems for which all standard RL algorithms (epsilon-greedy Q-learning, SARSA, etc) fail catastrophically. That’s a serious limitation which both inspires research and which I suspect many people need to learn the hard way. Removing the credit assignment problem from reinforcement learning yields the Contextual Bandit setting which we know is generically solvable in the same manner as common supervised learning problems."

>	"Many people have tried to create online learning system that do not take into account the biasing effects of decisions. These fail near-universally. For example they might be very good at predicting what was shown (and hence clicked on) rather that what should be shown to generate the most interest."

>	"We need a system that explores over appropriate choices with logging of features, actions, probabilities of actions, and outcomes. These must then be fed into an appropriate learning algorithm which trains a policy and then deploys the policy at the point of decision. The system enables a fully automatic causally sound learning loop for contextual control of a small number of actions. It is strongly scalable, for example a version of this is in use for personalized news on MSN."

  - <https://azure.microsoft.com/en-us/services/cognitive-services/personalizer/>
  - <https://azure.microsoft.com/en-us/services/cognitive-services/custom-decision-service/>
  - <http://research.microsoft.com/en-us/projects/mwt/>
  - `video` <https://youtube.com/watch?v=7ic_d5TeIUk> (Langford)
  - `video` <https://vimeo.com/240429210> (Langford, Agarwal)
  - `video` <https://youtube.com/watch?v=5JXRbhPLSQw> (Agarwal)
  - `video` <https://youtu.be/N5x48g2sp8M?t=52m> (Schapire)
  - `audio` <https://youtube.com/watch?v=ZUVLo07459U> (Langford)
  - `audio` <https://youtu.be/3q4OvzIyPug?t=6m12s> (Agarwal)
  - `post` <http://hunch.net/?p=4464948> (Langford)
  - `post` <http://machinedlearnings.com/2017/01/reinforcement-learning-as-service.html> (Mineiro)
  - `code` <https://github.com/Microsoft/mwt-ds>
  - `paper` ["Taming the Monster: A Fast and Simple Algorithm for Contextual Bandits"](https://arxiv.org/abs/1402.0555) by Agarwal et al.


#### ["Off-policy Evaluation for Slate Recommendation"](https://arxiv.org/abs/1605.04812) Swaminathan, Krishnamurthy, Agarwal, Dudík, Langford, Jose, Zitouni
>	"This paper studies the evaluation of policies that recommend an ordered set of items (e.g., a ranking) based on some context---a common scenario in web search, ads, and recommendation. We build on techniques from combinatorial bandits to introduce a new practical estimator that uses logged data to estimate a policy's performance. A thorough empirical evaluation on real-world data reveals that our estimator is accurate in a variety of settings, including as a subroutine in a learning-to-rank task, where it achieves competitive performance. We derive conditions under which our estimator is unbiased---these conditions are weaker than prior heuristics for slate evaluation---and experimentally demonstrate a smaller bias than parametric approaches, even when these conditions are violated. Finally, our theory and experiments also show exponential savings in the amount of required data compared with general unbiased estimators."

  - `video` <https://facebook.com/nipsfoundation/videos/1554741347950432?t=222> (Swaminathan)
  - `video` ["Counterfactual Evaluation and Learning for Search, Recommendation and Ad Placement"](http://www.cs.cornell.edu/~adith/CfactSIGIR2016/) tutorial by Adith Swaminathan and Thorsten Joachims


#### ["Top-K Off-Policy Correction for a REINFORCE Recommender System"](https://arxiv.org/abs/1812.02353) Chen, Beutel, Covington, Jain, Belletti, Chi
  `YouTube`
>	"Industrial recommender systems deal with extremely large action spaces – many millions of items to recommend. Moreover, they need to serve billions of users, who are unique at any point in time, making a complex user state space. Luckily, huge quantities of logged implicit feedback (e.g., user clicks, dwell time) are available for learning. Learning from the logged feedback is however subject to biases caused by only observing feedback on recommendations selected by the previous versions of the recommender. In this work, we present a general recipe of addressing such biases in a production top-K recommender system at YouTube, built with a policy-gradient-based algorithm, i.e. REINFORCE. The contributions of the paper are: (1) scaling REINFORCE to a production recommender system with an action space on the orders of millions; (2) applying off-policy correction to address data biases in learning from logged feedback collected from multiple behavior policies; (3) proposing a novel top-K off-policy correction to account for our policy recommending multiple items at a time; (4) showcasing the value of exploration. We demonstrate the efficacy of our approaches through a series of simulations and multiple live experiments on YouTube."

  - `video` <https://youtube.com/watch?v=HEqQ2_1XRTs> (Chen)
  - `video` <https://youtube.com/watch?v=Ys3YY7sSmIA> (Chang)
  - `video` <https://youtu.be/FNmh-eGYAv0?t=23m12s> (Chi)
  - `video` <https://youtu.be/umyNVwePCtw?t=6m42s> (Bugaychenko) `in russian`
  - `post` <https://towardsdatascience.com/top-k-off-policy-correction-for-a-reinforce-recommender-system-e34381dceef8>
  - `press` <https://nytimes.com/interactive/2019/06/08/technology/youtube-radical.html>


#### ["Reinforcement Learning for Slate-based Recommender Systems: A Tractable Decomposition and Practical Methodology"](https://arxiv.org/abs/1905.12767) Ie et al.
  `SLATEQ` `YouTube` `IJCAI-2019`
>	"Most practical recommender systems focus on estimating immediate user engagement without considering the long-term effects of recommendations on user behavior. Reinforcement learning (RL) methods offer the potential to optimize recommendations for long-term user engagement. However, since users are often presented with slates of multiple items - which may have interacting effects on user choice - methods are required to deal with the combinatorics of the RL action space. In this work, we address the challenge of making slate-based recommendations to optimize long-term value using RL. Our contributions are three-fold. (i) We develop SLATEQ, a decomposition of value-based temporal-difference and Q-learning that renders RL tractable with slates. Under mild assumptions on user choice behavior, we show that the long-term value (LTV) of a slate can be decomposed into a tractable function of its component item-wise LTVs. (ii) We outline a methodology that leverages existing myopic learning-based recommenders to quickly develop a recommender that handles LTV. (iii) We demonstrate our methods in simulation, and validate the scalability of decomposed TD-learning using SLATEQ in live experiments on YouTube."

  - `video` <http://www.fields.utoronto.ca/video-archive/2019/02/2509-19619> (41:12) (Boutilier)
  - `post` <https://medium.com/analytics-vidhya/slateq-a-scalable-algorithm-for-slate-recommendation-problems-735a1c24458c>


#### ["QT-Opt: Scalable Deep Reinforcement Learning for Vision-Based Robotic Manipulation"](https://arxiv.org/abs/1806.10293) Kalashnikov et al.
  `QT-Opt`
>	"In this paper, we study the problem of learning vision-based dynamic manipulation skills using a scalable reinforcement learning approach. We study this problem in the context of grasping, a longstanding challenge in robotic manipulation. In contrast to static learning behaviors that choose a grasp point and then execute the desired grasp, our method enables closed-loop vision-based control, whereby the robot continuously updates its grasp strategy based on the most recent observations to optimize long-horizon grasp success. To that end, we introduce QT-Opt, a scalable self-supervised vision-based reinforcement learning framework that can leverage over 580k real-world grasp attempts to train a deep neural network Q-function with over 1.2M parameters to perform closed-loop, real-world grasping that generalizes to 96% grasp success on unseen objects. Aside from attaining a very high success rate, our method exhibits behaviors that are quite distinct from more standard grasping systems: using only RGB vision-based perception from an over-the-shoulder camera, our method automatically learns regrasping strategies, probes objects to find the most effective grasps, learns to reposition objects and perform other non-prehensile pre-grasp manipulations, and responds dynamically to disturbances and perturbations."

  - `video` <http://www.fields.utoronto.ca/video-archive/2019/10/2509-21418> (19:54) (Levine)
  - `video` <https://youtu.be/U1dD8UALTu0?t=16m25s> (Levine)
  - `video` <https://video.ethz.ch/events/2018/corl/c7111aff-c968-43cd-ad0f-b42ddcccbf62.html> (Kalashnikov)


#### ["Learning Dexterous In-Hand Manipulation"](https://arxiv.org/abs/1808.00177) OpenAI et al.
  `Dactyl`
>	"We use reinforcement learning to learn dexterous in-hand manipulation policies which can perform vision-based object reorientation on a physical Shadow Dexterous Hand. The training is performed in a simulated environment in which we randomize many of the physical properties of the system like friction coefficients and an object's appearance. Our policies transfer to the physical robot despite being trained entirely in simulation. Our method does not rely on any human demonstrations, but many behaviors found in human manipulation emerge naturally, including finger gaiting, multi-finger coordination, and the controlled use of gravity. Our results were obtained using the same distributed RL system that was used to train OpenAI Five."

  - `post` <https://blog.openai.com/learning-dexterity>
  - `video` <https://youtube.com/watch?v=jwSbzNHGflM> (demo)
  - `video` <https://youtube.com/watch?v=DKe8FumoD4E> (demo)
  - `video` <https://youtu.be/WRsxoVB8Yng?t=57m55s> (Zaremba)
  - `video` <https://youtu.be/w3ues-NayAs?t=16m26s> (Sutskever)
  - `video` <https://facebook.com/icml.imls/videos/2265408103721327?t=1200> (Todorov)



---
### interesting papers - exploration and intrinsic motivation

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----

  * [**bayesian exploration**](#interesting-papers---exploration-and-intrinsic-motivation---bayesian-exploration)
  * [**auxiliary tasks**](#interesting-papers---exploration-and-intrinsic-motivation---auxiliary-tasks)
  * information theoretic and distributional models
    - [**uncertainty motivation (novelty)**](#interesting-papers---exploration-and-intrinsic-motivation---information-theoretic-and-distributional-models---uncertainty-motivation)
    - [**information gain motivation (bayesian surprise)**](#interesting-papers---exploration-and-intrinsic-motivation---information-theoretic-and-distributional-models---information-gain-motivation)
    - [**empowerment motivation**](#interesting-papers---exploration-and-intrinsic-motivation---information-theoretic-and-distributional-models---empowerment-motivation)
  * predictive models
    - [**predictive novelty motivation (prediction error)**](#interesting-papers---exploration-and-intrinsic-motivation---predictive-models---predictive-novelty-motivation)
    - [**learning progress motivation (prediction gain)**](#interesting-papers---exploration-and-intrinsic-motivation---predictive-models---learning-progress-motivation)
    - [**predictive familiarity motivation (homeostasis)**](#interesting-papers---exploration-and-intrinsic-motivation---predictive-models---predictive-familiarity-motivation)
  * competence-based models
    - [**competence progress motivation (automated curriculum learning)**](#interesting-papers---exploration-and-intrinsic-motivation---competence-based-models---competence-progress-motivation)

----
#### ["How Can We Define Intrinsic Motivation"](http://pyoudeyer.com/epirob08OudeyerKaplan.pdf) Oudeyer, Kaplan
>	"Intrinsic motivation is a crucial mechanism for open-ended cognitive development since it is the driver of spontaneous exploration and curiosity. Yet, it has so far only been conceptualized in ad hoc manners in the epigenetic robotics community. After reviewing different approaches to intrinsic motivation in psychology, this paper presents a unified definition of intrinsic motivation, based on the theory of Daniel Berlyne. Based on this definition, we propose a landscape of types of computational approaches, making it possible to position existing and future models relative to each other, and we show that important approaches are still to be explored."


#### ["Computational Theories of Curiosity-Driven Learning"](https://arxiv.org/abs/1802.10546) Oudeyer
>	"What are the functions of curiosity? What are the mechanisms of curiosity-driven learning? We approach these questions about the living using concepts and tools from machine learning and developmental robotics. We argue that curiosity-driven learning enables organisms to make discoveries to solve complex problems with rare or deceptive rewards. By fostering exploration and discovery of a diversity of behavioural skills, and ignoring these rewards, curiosity can be efficient to bootstrap learning when there is no information, or deceptive information, about local improvement towards these problems. We also explain the key role of curiosity for efficient learning of world models. We review both normative and heuristic computational frameworks used to understand the mechanisms of curiosity in humans, conceptualizing the child as a sense-making organism. These frameworks enable us to discuss the bi-directional causal links between curiosity and learning, and to provide new hypotheses about the fundamental role of curiosity in self-organizing developmental structures through curriculum learning. We present various developmental robotics experiments that study these mechanisms in action, both supporting these hypotheses to understand better curiosity in humans and opening new research avenues in machine learning and artificial intelligence. Finally, we discuss challenges for the design of experimental paradigms for studying curiosity in psychology and cognitive neuroscience."


#### ["Where Do Rewards Come From?"](https://researchgate.net/publication/200744428_Where_Do_Rewards_Come_From) Singh, Lewis, Barto
  `optimal reward framework`
>	"Reinforcement learning has achieved broad and successful application in cognitive science in part because of its general formulation of the adaptive control problem as the maximization of a scalar reward function. The computational reinforcement learning framework is motivated by correspondences to animal reward processes, but it leaves the source and nature of the rewards unspecified. This paper advances a general computational framework for reward that places it in an evolutionary context, formulating a notion of an optimal reward function given a fitness function and some distribution of environments. Novel results from computational experiments show how traditional notions of extrinsically and intrinsically motivated behaviors may emerge from such optimal reward functions. In the experiments these rewards are discovered through automated search rather than crafted by hand. The precise form of the optimal reward functions need not bear a direct relationship to the fitness function, but may nonetheless confer significant advantages over rewards based only on fitness."

----
>	"Most often the starting point is an agent-designer that has an objective reward function that specifies preferences over agent behavior. What should the agent's reward function be? A single reward function confounds two roles simultaneously in RL agents:  
>	1. (Preferences) It expresses the agent-designer's preferences over behaviors; used to evaluate agent behavior.  
>	2. (Parameters) Through the reward hypothesis it expresses the RL agent's goals/purposes and becomes parameters of actual agent behaviour; used to guide agent behavior.  
>	These roles are distinct; yet it seems to make sense to confound these two roles to align the interests of the agent with the designer.  
>	The overall message: breaking this confound can help!"  

>	"rewards vs reward signals:  
>	Rewards are objects or events that make us come back for more. We need them for survival and use them for behavioral choices that maximize them.  
>	Reward neurons produce reward signals and use them for influencing brain activity that controls our actions, decisions and choices."  

  - `video` <http://videolectures.net/deeplearning2017_singh_reinforcement_learning/#t=1192> (Singh)
  - `video` <https://youtube.com/watch?v=MhIP1SOqlS8> (Singh)
  - `video` <https://youtu.be/_4oL3DDCwCw?t=11m47s> (Singh)
  - `video` <https://youtu.be/DtUSF3QHWIM?t=7m33s> (Singh)
  - `video` <https://coursera.org/lecture/prediction-control-function-approximation/satinder-singh-on-intrinsic-rewards-TKPHV> (Singh)
  - `video` <https://youtu.be/aJI_9SoBDaQ?t=17m9s> + <https://youtu.be/aJI_9SoBDaQ?t=28m14s> (Barto)
  - `paper` ["What Can Learned Intrinsic Rewards Capture?"](https://arxiv.org/abs/1912.05500) by Zheng et al.


#### ["Intrinsically Motivated Reinforcement Learning: An Evolutionary Perspective"](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.180.1045) Singh, Lewis, Barto, Sorg
  `optimal reward framework`
>	"There is great interest in building intrinsic motivation into artificial systems using the reinforcement learning framework. Yet, what intrinsic motivation may mean computationally, and how it may differ from extrinsic motivation, remains a murky and controversial subject. In this article, we adopt an evolutionary perspective and define a new optimal reward framework that captures the pressure to design good primary reward functions that lead to evolutionary success across environments. The results of two computational experiments show that optimal primary reward signals may yield both emergent intrinsic and extrinsic motivation. The evolutionary perspective and the associated optimal reward framework thus lead to the conclusion that there are no hard and fast features distinguishing intrinsic and extrinsic reward computationally. Rather, the directness of the relationship between rewarding behavior and evolutionary success varies along a continuum."

  - `video` <https://youtu.be/aJI_9SoBDaQ?t=17m9s> + <https://youtu.be/aJI_9SoBDaQ?t=28m14s> (Barto)



---
### interesting papers - exploration and intrinsic motivation - bayesian exploration

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----
#### ["Planning to Be Surprised: Optimal Bayesian Exploration in Dynamic Environments"](https://arxiv.org/abs/1103.5708) Sun, Gomez, Schmidhuber
>	"How should the agent choose the actions such that the knowledge about the environment accumulates as quickly as possible? In this paper, this question is addressed under a classical framework, in which the agent improves its model of the environment through probabilistic inference, and learning progress is measured in terms of Shannon information gain. We show that the agent can, at least in principle, optimally choose actions based on previous experiences, such that the cumulative expected information gain is maximized. We then consider a special case, namely exploration in finite MDPs, where we demonstrate, both in theory and through experiment, that the optimal Bayesian exploration strategy can be effectively approximated by solving a sequence of dynamic programming problems."

>	"An optimal Bayesian framework for curiosity-driven exploration using learning progress. After proving that Information Gain is additive in expectation, a dynamic programming based algorithm was proposed to maximize Information Gain. Experiments however were limited to small tabular MDPs with a Dirichlet prior on transition probabilities."

  - `video` <https://youtu.be/WYnLlk58EUE?t=12m22s>


#### ["Efficient Bayes-Adaptive Reinforcement Learning using Sample-Based Search"](https://arxiv.org/abs/1205.3109) Guez, Silver, Dayan
>	"Bayesian model-based reinforcement learning is a formally elegant approach to learning optimal behaviour under model uncertainty, trading off exploration and exploitation in an ideal way. Unfortunately, finding the resulting Bayes-optimal policies is notoriously taxing, since the search space becomes enormous. In this paper we introduce a tractable, sample-based method for approximate Bayes-optimal planning which exploits Monte-Carlo tree search. Our approach outperformed prior Bayesian model-based RL algorithms by a significant margin on several well-known benchmark problems – because it avoids expensive applications of Bayes rule within the search tree by lazily sampling models from the current beliefs. We illustrate the advantages of our approach by showing it working in an infinite state space domain which is qualitatively out of reach of almost all previous work in Bayesian exploration."

>	"We suggested a sample-based algorithm for Bayesian RL called BAMCP that significantly surpassed the performance of existing algorithms on several standard tasks. We showed that BAMCP can tackle larger and more complex tasks generated from a structured prior, where existing approaches scale poorly. In addition, BAMCP provably converges to the Bayes-optimal solution. The main idea is to employ Monte-Carlo tree search to explore the augmented Bayes-adaptive search space efficiently. The naive implementation of that idea is the proposed BA-UCT algorithm, which cannot scale for most priors due to expensive belief updates inside the search tree. We introduced three modifications to obtain a computationally tractable sample-based algorithm: root sampling, which only requires beliefs to be sampled at the start of each simulation; a model-free RL algorithm that learns a rollout policy; and the use of a lazy sampling scheme to sample the posterior beliefs cheaply."

  - `video` <https://youtu.be/sGuiWX07sKw?t=1h35m58s> (Silver)


#### ["Learning to Optimize via Posterior Sampling"](https://arxiv.org/abs/1301.2609) Russo, van Roy
>	"This paper considers the use of a simple posterior sampling algorithm to balance between exploration and exploitation when learning to optimize actions such as in multi-armed bandit problems. The algorithm, also known as Thompson Sampling and as probability matching, offers significant advantages over the popular upper confidence bound (UCB) approach, and can be applied to problems with finite or infinite action spaces and complicated relationships among action rewards. We make two theoretical contributions. The first establishes a connection between posterior sampling and UCB algorithms. This result lets us convert regret bounds developed for UCB algorithms into Bayesian regret bounds for posterior sampling. Our second theoretical contribution is a Bayesian regret bound for posterior sampling that applies broadly and can be specialized to many model classes. This bound depends on a new notion we refer to as the eluder dimension, which measures the degree of dependence among action rewards. Compared to UCB algorithm Bayesian regret bounds for specific model classes, our general bound matches the best available for linear models and is stronger than the best available for generalized linear models. Further, our analysis provides insight into performance advantages of posterior sampling, which are highlighted through simulation results that demonstrate performance surpassing recently proposed UCB algorithms."

>	"The Thompson Sampling algorithm randomly selects an action according to the probability it is optimal. Although posterior sampling was first proposed almost eighty years ago, it has until recently received little attention in the literature on multi-armed bandits. While its asymptotic convergence has been established in some generality, not much else is known about its theoretical properties in the case of dependent arms, or even in the case of independent arms with general prior distributions. Our work provides some of the first theoretical guarantees."

>	"Our interest in posterior sampling is motivated by several potential advantages over UCB algorithms. While particular UCB algorithms can be extremely effective, performance and computational tractability depends critically on the confidence sets used by the algorithm. For any given model, there is a great deal of design flexibility in choosing the structure of these sets. Because posterior sampling avoids the need for confidence bounds, its use greatly simplifies the design process and admits practical implementations in cases where UCB algorithms are computationally onerous. In addition, we show through simulations that posterior sampling outperforms various UCB algorithms that have been proposed in the literature."

>	"In this paper, we make two theoretical contributions. The first establishes a connection between posterior sampling and UCB algorithms. In particular, we show that while the regret of a UCB algorithm can be bounded in terms of the confidence bounds used by the algorithm, the Bayesian regret of posterior sampling can be bounded in an analogous way by any sequence of confidence bounds. In this sense, posterior sampling preserves many of the appealing theoretical properties of UCB algorithms without requiring explicit, designed, optimism. We show that, due to this connection, existing analysis available for specific UCB algorithms immediately translates to Bayesian regret bounds for posterior sampling."

>	"Our second theoretical contribution is a Bayesian regret bound for posterior sampling that applies broadly and can be specialized to many specific model classes. Our bound depends on a new notion of dimension that measures the degree of dependence among actions. We compare our notion of dimension to the Vapnik-Chervonenkis dimension and explain why that and other measures of dimension used in the supervised learning literature do not suffice when it comes to analyzing posterior sampling."

----
>	"Authors describe an approach to addressing the limitations of the optimistic approach that serves as the basis for the UCB family of algorithms. They describe a method that considers not only the immediate single-period regret but also the information gain to learn from the partial feedback and to optimize the exploration-exploitation trade online."

  - `video` <http://videolectures.net/rldm2015_van_roy_function_randomization/> (van Roy)


#### ["Why is Posterior Sampling Better than Optimism for Reinforcement Learning?"](http://arxiv.org/abs/1607.00215) Osband, van Roy
>	"Computational results demonstrate that posterior sampling for reinforcement learning (PSRL) dramatically outperforms algorithms driven by optimism, such as UCRL2. We provide insight into the extent of this performance boost and the phenomenon that drives it. We leverage this insight to establish an O(H√S√A√T) expected regret bound for PSRL in finite-horizon episodic Markov decision processes, where H is the horizon, S is the number of states, A is the number of actions and T is the time elapsed. This improves upon the best previous bound of O(HS√A√T) for any reinforcement learning algorithm."

>	"We consider a well-studied reinforcement learning problem in which an agent interacts with a Markov decision process with the aim of maximizing expected cumulative reward. Our focus is on the tabula rasa case, in which the agent has virtually no prior information about the MDP. As such, the agent is unable to generalize across state-action pairs and may have to gather data at each in order to learn an effective decision policy. Key to performance is how the agent balances between exploration to acquire information of long-term benefit and exploitation to maximize expected near-term rewards. In principle, dynamic programming can be applied to compute the so-called Bayes-optimal solution to this problem. However, this is computationally intractable for anything beyond the simplest of toy problems. As such, researchers have proposed and analyzed a number of heuristic reinforcement learning algorithms.

>	The literature on efficient reinforcement learning offers statistical efficiency guarantees for computationally tractable algorithms. These provably efficient algorithms predominantly address the exploration-exploitation trade-off via optimism in the face of uncertainty (OFU): when at a state, the agent assigns to each action an optimistically biased while statistically plausible estimate of future value and selects the action with the greatest estimate. If a selected action is not near-optimal, the estimate must be overly optimistic, in which case the agent learns from the experience. Efficiency relative to less sophisticated exploration strategies stems from the fact that the agent avoids actions that neither yield high value nor informative data.

>	An alternative approach, based on Thompson sampling, involves sampling a statistically plausibly set of action values and selecting the maximizing action. These values can be generated, for example, by sampling from the posterior distribution over MDPs and computing the state-action value function of the sampled MDP. This approach is called posterior sampling for reinforcement learning (PSRL). Computational results demonstrate that PSRL dramatically outperforms algorithms based on OFU. The primary aim of this paper is to provide insight into the extent of this performance boost and the phenomenon that drives it.

>	We argue that applying OFU in a manner that competes with PSRL in terms of statistical efficiency would require intractable computation. As such, OFU-based algorithms presented in the literature sacrifice statistical efficiency to attain computational tractability. We will explain how these algorithms are statistically inefficient. We will also leverage this insight to produce an O(H√S√A√T) expected regret bound for PSRL in finite-horizon episodic Markov decision processes, where H is the horizon, S is the number of states, A is the number of actions and T is the time elapsed. This improves upon the best previous bound of O(HS√A√T) for any reinforcement learning algorithm. We discuss why we believe PSRL satisfies a tighter O(√H√S√A√T), though we have not proved that. We present computational results chosen to enhance insight on how learning times scale with problem parameters. These empirical scalings match our theoretical predictions."

>	"PSRL is orders of magnitude more statistically efficient than UCRL and S-times less computationally expensive. In the future, we believe that analysts will be able to formally specify an OFU approach to RL whose statistical efficiency matches PSRL. However, we argue that the resulting confidence sets which address both the coupling over H and S will result in a computationally intractable optimization problem. For this reason, computationally efficient approaches to OFU RL will sacrifice statistical efficiency; this is why posterior sampling is better than optimism for reinforcement learning."

  - `video` <http://videolectures.net/rldm2015_van_roy_function_randomization/> (van Roy)
  - `video` <https://youtube.com/watch?v=ck4GixLs4ZQ> (Osband) ([slides](https://docs.google.com/presentation/d/1lis0yBGT-uIXnAsi0vlP3SuWD2svMErJWy_LYtfzMOA/))
  - `code` <https://sudeepraja.github.io/PSRL/>
  - `code` <https://github.com/iosband/TabulaRL>


#### ["A Tutorial on Thompson Sampling"](https://arxiv.org/abs/1707.02038) Russo, van Roy, Kazerouni, Osband, Wen
>	"Thompson sampling is an algorithm for online decision problems where actions are taken sequentially in a manner that must balance between exploiting what is known to maximize immediate performance and investing to accumulate new information that may improve future performance. The algorithm addresses a broad range of problems in a computationally efficient manner and is therefore enjoying wide use. This tutorial covers the algorithm and its application, illustrating concepts through a range of examples, including Bernoulli bandit problems, shortest path problems, dynamic pricing, recommendation, active learning with neural networks, and reinforcement learning in Markov decision processes. Most of these problems involve complex information structures, where information revealed by taking an action informs beliefs about other actions. We will also discuss when and why Thompson sampling is or is not effective and relations to alternative algorithms."

  - `code` <https://colab.research.google.com/github/iosband/ts_tutorial/blob/master/ts_tutorial_intro.ipynb>


#### ["Nonparametric General Reinforcement Learning"](https://jan.leike.name/publications/Nonparametric%20General%20Reinforcement%20Learning%20-%20Leike%202016.pdf) Leike
>	"Reinforcement learning problems are often phrased in terms of Markov decision processes. In this thesis we go beyond MDPs and consider reinforcement learning in environments that are non-Markovian, non-ergodic and only partially observable. Our focus is not on practical algorithms, but rather on the fundamental underlying problems: How do we balance exploration and exploitation? How do we explore optimally? When is an agent optimal? We follow the nonparametric realizable paradigm: we assume the data is drawn from an unknown source that belongs to a known countable class of candidates.  
>	First, we consider the passive (sequence prediction) setting, learning from data that is not independent and identically distributed. We collect results from artificial intelligence, algorithmic information theory, and game theory and put them in a reinforcement learning context: they demonstrate how agent can learn the value of its own policy. Next, we establish negative results on Bayesian reinforcement learning agents, in particular AIXI. We show that unlucky or adversarial choices of the prior cause the agent to misbehave drastically. Therefore Legg-Hutter intelligence and balanced Pareto optimality, which depend crucially on the choice of the prior, are entirely subjective. Moreover, in the class of all computable environments every policy is Pareto optimal. This undermines all existing optimality properties for AIXI.  
>	However, there are Bayesian approaches to general reinforcement learning that satisfy objective optimality guarantees: We prove that Thompson sampling is asymptotically optimal in stochastic environments in the sense that its value converges to the value of the optimal policy. We connect asymptotic optimality to regret given a recoverability assumption on the environment that allows the agent to recover from mistakes. Hence Thompson sampling achieves sublinear regret in these environments.  
>	AIXI is known to be incomputable. We quantify this using the arithmetical hierarchy, and establish upper and corresponding lower bounds for incomputability. Further, we show that AIXI is not limit computable, thus cannot be approximated using finite computation. However there are limit computable ε-optimal approximations to AIXI. We also derive computability bounds for knowledge-seeking agents, and give a limit computable weakly asymptotically optimal reinforcement learning agent.  
>	Finally, our results culminate in a formal solution to the grain of truth problem: A Bayesian agent acting in a multi-agent environment learns to predict the other agents’ policies if its prior assigns positive probability to them (the prior contains a grain of truth). We construct a large but limit computable class containing a grain of truth and show that agents based on Thompson sampling over this class converge to play ε-Nash equilibria in arbitrary unknown computable multi-agent environments."

----
>	"Recently it was revealed that these optimality notions are trivial or subjective: a Bayesian agent does not explore enough to lose the prior’s bias, and a particularly bad prior can make the agent conform to any arbitrarily bad policy as long as this policy yields some rewards. These negative results put the Bayesian approach to (general) RL into question. We remedy the situation by showing that using Bayesian techniques an agent can indeed be optimal in an objective sense."

>	"The agent we consider is known as Thompson sampling or posterior sampling. It samples an environment ρ from the posterior, follows the ρ-optimal policy for one effective horizon (a lookahead long enough to encompass most of the discount function’s mass), and then repeats. We show that this agent’s policy is asymptotically optimal in mean (and, equivalently, in probability). Furthermore, using a recoverability assumption on the environment, and some (minor) assumptions on the discount function, we prove that the worst-case regret is sublinear. This is the first time convergence and regret bounds of Thompson sampling have been shown under such general conditions."

  - `video` <https://youtube.com/watch?v=hSiuJuvTBoE> (Leike)
  - `paper` ["Thompson Sampling is Asymptotically Optimal in General Environments"](https://arxiv.org/abs/1602.07905) by Leike et al.


#### ["Weight Uncertainty in Neural Networks"](https://arxiv.org/abs/1505.05424) Blundell, Cornebise, Kavukcuoglu, Wierstra
>	"We introduce a new, efficient, principled and backpropagation-compatible algorithm for learning a probability distribution on the weights of a neural network, called Bayes by Backprop. It regularises the weights by minimising a compression cost, known as the variational free energy or the expected lower bound on the marginal likelihood. We show that this principled kind of regularisation yields comparable performance to dropout on MNIST classification. We then demonstrate how the learnt uncertainty in the weights can be used to improve generalisation in non-linear regression problems, and how this weight uncertainty can be used to drive the exploration-exploitation trade-off in reinforcement learning."

>	"P(r|x,a,w) can be modelled by a neural network where w are the weights of the neural network. However if this network is simply fit to observations and the action with the highest expected reward taken at each time, the agent can under-explore, as it may miss more rewarding actions."

>	"Thompson sampling is a popular means of picking an action that trades-off between exploitation (picking the best known action) and exploration (picking what might be a suboptimal arm to learn more). Thompson sampling usually necessitates a Bayesian treatment of the model parameters. At each step, Thompson sampling draws a new set of parameters and then picks the action relative to those parameters. This can be seen as a kind of stochastic hypothesis testing: more probable parameters are drawn more often and thus refuted or confirmed the fastest. More concretely Thompson sampling proceeds as follows:  
>	1. Sample a new set of parameters for the model.  
>	2. Pick the action with the highest expected reward according to the sampled parameters.  
>	3. Update the model. Go to 1."  

>	"Thompson sampling is easily adapted to neural networks using the variational posterior:  
>	1. Sample weights from the variational posterior: w ∼ q(w|θ).  
>	2. Receive the context x.  
>	3. Pick the action a that maximizes E P(r|x,a,w) [r]  
>	4. Receive reward r.  
>	5. Update variational parameters θ. Go to 1."  

>	"Note that it is possible to decrease the variance of the gradient estimates, trading off for reduced exploration, by using more than one Monte Carlo sample, using the corresponding networks as an ensemble and picking the action by minimising the average of the expectations."  

>	"Initially the variational posterior will be close to the prior, and actions will be picked uniformly. As the agent takes actions, the variational posterior will begin to converge, and uncertainty on many parameters can decrease, and so action selection will become more deterministic, focusing on the high expected reward actions discovered so far. It is known that variational methods under-estimate uncertainty which could lead to under-exploration and premature convergence in practice, but we did not find this in practice."

  - `video` <http://videolectures.net/icml2015_blundell_neural_network/> (Blundell)
  - `code` <https://github.com/tabacof/bayesian-nn-uncertainty>
  - `code` <https://github.com/blei-lab/edward/blob/master/examples/bayesian_nn.py>
  - `code` <https://github.com/ferrine/gelato>
  - `code` <https://gist.github.com/rocknrollnerd/c5af642cf217971d93f499e8f70fcb72>


#### ["Deep Exploration via Bootstrapped DQN"](http://arxiv.org/abs/1602.04621) Osband, Blundell, Pritzel, van Roy
>	"Efficient exploration in complex environments remains a major challenge for reinforcement learning. We propose bootstrapped DQN, a simple algorithm that explores in a computationally and statistically efficient manner through use of randomized value functions. Unlike dithering strategies such as Epsilon-greedy exploration, bootstrapped DQN carries out temporally-extended (or deep) exploration; this can lead to exponentially faster learning. We demonstrate these benefits in complex stochastic MDPs and in the large-scale Arcade Learning Environment. Bootstrapped DQN substantially improves learning times and performance across most Atari games."

>	"One of the reasons deep RL algorithms learn so slowly is that they do not gather the right data to learn about the problem. These algorithms use dithering (taking random actions) to explore their environment - which can be exponentially less efficient that deep exploration which prioritizes potentially informative policies over multiple timesteps. There is a large literature on algorithms for deep exploration for statistically efficient reinforcement learning. The problem is that none of these algorithms are computationally tractable with deep learning. We present the first practical reinforcement learning algorithm that combines deep learning with deep exploration."

>	"In this paper we present bootstrapped DQN as an algorithm for efficient reinforcement learning in complex environments. We demonstrate that the bootstrap can produce useful uncertainty estimates for deep neural networks. Bootstrapped DQN can leverage these uncertainty estimates for deep exploration even in difficult stochastic systems; it also produces several state of the art results in Atari 2600. Bootstrapped DQN is computationally tractable and also naturally scalable to massive parallel systems as per (Nair et al., 2015). We believe that, beyond our specific implementation, randomized value functions represent a promising alternative to dithering for exploration. Bootstrapped DQN practically combines efficient generalization with exploration for complex nonlinear value functions.

>	"Our algorithm, bootstrapped DQN, modifies DQN to produce distribution over Q-values via the bootstrap. At the start of each episode, bootstrapped DQN samples a single Q-value function from its approximate posterior. The agent then follows the policy which is optimal for that sample for the duration of the episode. This is a natural extension of the Thompson sampling heuristic to RL that allows for temporally extended (or deep) exploration. Bootstrapped DQN exhibits deep exploration unlike the naive application of Thompson sampling to RL which resample every timestep."

>	"By contrast, Epsilon-greedy strategies are almost indistinguishable for small values of Epsilon and totally ineffectual for larger values. Our heads explore a diverse range of policies, but still manage to each perform well individually."

>	"Unlike vanilla DQN, bootstrapped DQN can know what it doesn’t know."

>	"Uncertainty estimates allow an agent to direct its exploration at potentially informative states and actions. In bandits, this choice of directed exploration rather than dithering generally categorizes efficient algorithms. The story in RL is not as simple, directed exploration is not enough to guarantee efficiency; the exploration must also be deep. Deep exploration means exploration which is directed over multiple time steps; it can also be called “planning to learn” or “far-sighted” exploration. Unlike bandit problems, which balance actions which are immediately rewarding or immediately informative, RL settings require planning over several time steps. For exploitation, this means that an efficient agent must consider the future rewards over several time steps and not simply the myopic rewards. In exactly the same way, efficient exploration may require taking actions which are neither immediately rewarding, nor immediately informative."

>	"Unlike bandit algorithms, an RL agent can plan to exploit future rewards. Only an RL agent with deep exploration can plan to learn."

>	"Bootstrapped DQN explores in a manner similar to the provably-efficient algorithm PSRL but it uses a bootstrapped neural network to approximate a posterior sample for the value. Unlike PSRL, bootstrapped DQN directly samples a value function and so does not require further planning steps. This algorithm is similar to RLSVI, which is also provably-efficient, but with a neural network instead of linear value function and bootstrap instead of Gaussian sampling. The analysis for the linear setting suggests that this nonlinear approach will work well so long as the distribution {Q1, .., QK} remains stochastically optimistic, or at least as spread out as the “correct” posterior."

>	"Interestingly, we did not find that using dropout produced satisfying confidence intervals for this task. Bootstrapped uncertainty estimates for the Q-value functions have another crucial advantage over dropout which does not appear in the supervised problem. Unlike random dropout masks trained against random target networks, our implementation of bootstrap DQN trains against its own temporally consistent target network. This means that our bootstrap estimates are able to “bootstrap” (in the TD sense) on their ownestimates of the long run value. This is important to quantify the long run uncertainty over Q and drive deep exploration."

----
  Yarin Gal:  
>	"This technique to estimate model uncertainty uses an ensemble of deterministic models, meaning that each model in the ensemble produces a point estimate rather than a distribution. It works by independently training many randomly initialised instances of a model on the same dataset (or different random subsets in the case of bootstrapping), and given an input test point, evaluating the sample variance of the outputs from all deterministic models. Even though this approach is more computationally efficient than many Bayesian approaches to model uncertainty (apart from the need to represent the parameters of multiple models), its produced uncertainty estimates lack in many ways as explained in the next illustrative example. To see this, let’s see what would happen if each deterministic model were to be given by an RBF network (whose predictions coincide with the predictive mean of a Gaussian process with a squared-exponential covariance function). An RBF network predicts zero for test points far from the training data. This means that in an ensemble of RBF networks, each and every network will predict zero for a given test point far from the training data. As a result, the sample variance of this technique will be zero at the given test point. The ensemble of models will have very high confidence in its prediction of zero even though the test point lies far from the data! This limitation can be alleviated by using an ensemble of probabilistic models instead of deterministic models. Even though the RBF network’s predictions coincide with the predictive mean of the SE Gaussian process, by using a Gaussian process we could also make use of its predictive variance. The Gaussian process predictions far from the training data will have large model uncertainty. In the ensemble, we would thus wish to take into account each model’s confidence as well as its mean (by sampling an output from each model’s predictive distribution before calculating our sample variance)."

  - `video` <http://youtube.com/watch?v=Zm2KoT82O_M> + <http://youtube.com/watch?v=0jvEcC5JvGY> (demo)
  - `video` <http://youtube.com/watch?v=6SAdmG3zAMg>
  - `video` <https://youtu.be/ck4GixLs4ZQ?t=1h27m39s> (Osband) + [slides](https://docs.google.com/presentation/d/1lis0yBGT-uIXnAsi0vlP3SuWD2svMErJWy_LYtfzMOA/)
  - `video` <http://videolectures.net/rldm2015_van_roy_function_randomization/#t=1830> (van Roy)
  - `video` <https://yadi.sk/i/yBO0q4mI3GAxYd> (47:07) (Fritzler) `in russian`
  - `video` <https://youtu.be/mrgJ53TIcQc?t=32m24s> (Pavlov) `in russian`
  - `code` <https://github.com/Kaixhin/Atari>
  - `code` <https://github.com/iassael/torch-bootstrapped-dqn>
  - `code` <https://github.com/carpedm20/deep-rl-tensorflow>


#### ["Deep Exploration via Randomized Value Functions"](https://arxiv.org/abs/1703.07608) Osband, Russo, Wen, van Roy
>	"We study the use of randomized value functions to guide deep exploration in reinforcement learning. This offers an elegant means for synthesizing statistically and computationally efficient exploration with common practical approaches to value function learning. We present several reinforcement learning algorithms that leverage randomized value functions and demonstrate their efficacy through computational studies. We also prove a regret bound that establishes statistical efficiency with a tabular representation."

>	"A very recent thread of work builds on count-based (or upper-confidence-bound-based) exploration schemes that operate with value function learning. These methods maintain a density over the state-action space of pseudo-counts, which represent the quantity of data gathered that is relevant to each state-action pair. Such algorithms may offer a viable approach to deep exploration with generalization. There are, however, some potential drawbacks. One is that a separate representation is required to generalize counts, and it's not clear how to design an effective approach to this. As opposed to the optimal value function, which is fixed by the environment, counts are generated by the agent’s choices, so there is no single target function to learn. Second, the count model generates reward bonuses that distort data used to fit the value function, so the value function representation needs to be designed to not only capture properties of the true optimal value function but also such distorted versions. Finally, these approaches treat uncertainties as uncoupled across state-action pairs, and this can incur a substantial negative impact on statistical efficiency."

  - `video` <https://youtube.com/watch?v=lfQEPWj97jk> (Osband)
  - `video` <http://techtalks.tv/talks/generalization-and-exploration-via-randomized-value-functions/62467/> (Osband)
  - `video` <https://youtu.be/ck4GixLs4ZQ?t=33m7s> (Osband)
  - `video` <https://vimeo.com/252186381> (van Roy)


#### ["Risk versus Uncertainty in Deep Learning: Bayes, Bootstrap and the Dangers of Dropout"](http://bayesiandeeplearning.org/papers/BDL_4.pdf) Osband
  - <https://github.com/brylevkirill/notes/blob/master/Deep%20Learning.md#risk-versus-uncertainty-in-deep-learning-bayes-bootstrap-and-the-dangers-of-dropout-osband>


#### ["Noisy Networks for Exploration"](https://arxiv.org/abs/1706.10295) Fortunato et al.
>	"We introduce NoisyNet, a deep reinforcement learning agent with parametric noise added to its weights, and show that the induced stochasticity of the agent’s policy can be used to aid efficient exploration. The parameters of the noise are learned with gradient descent along with the remaining network weights. NoisyNet is straightforward to implement and adds little computational overhead. We find that replacing the conventional exploration heuristics for A3C, DQN and dueling agents (entropy reward and epsilon-greedy respectively) with NoisyNet yields substantially higher scores for a wide range of Atari games, in some cases advancing the agent from sub to super-human performance."

>	"We have presented a general method for exploration in deep reinforcement learning that shows significant performance improvements across many Atari games in three different agent architectures. In particular, we observe that in games such as Asterix and Freeway that the standard DQN and A3C perform poorly compared with the human player, NoisyNet-DQN and NoisyNet-A3C achieve super human performance. Our method eliminates the need for epsilon-greedy and the entropy bonus commonly used in Q-learning-style and policy gradient methods, respectively. Instead we show that better exploration is possible by relying on perturbations in weight space to drive exploration. This is in contrast to many other methods that add intrinsic motivation signals that may destabilise learning or change the optimal policy. Another interesting feature of the NoisyNet approach is that the degree of exploration is contextual and varies from state to state based upon per-weight variances."

  - `code` <https://github.com/Kaixhin/NoisyNet-A3C>
  - `code` <https://github.com/andrewliao11/NoisyNet-DQN>
  - `paper` [**"On Bonus Based Exploration Methods In The Arcade Learning Environment"**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#on-bonus-based-exploration-methods-in-the-arcade-learning-environment-taiga-fedus-machado-courville-bellemare) by Taiga et al. `summary`


#### ["RL^2: Fast Reinforcement Learning via Slow Reinforcement Learning"](http://arxiv.org/abs/1611.02779) Duan, Schulman, Chen, Bartlett, Sutskever, Abbeel
>	"Deep reinforcement learning has been successful in learning sophisticated behaviors automatically; however, the learning process requires a huge number of trials. In contrast, animals can learn new tasks in just a few trials, benefiting from their prior knowledge about the world. This paper seeks to bridge this gap. Rather than designing a "fast" reinforcement learning algorithm, we propose to represent it as a recurrent neural network and learn it from data. In our proposed method, RL^2, the algorithm is encoded in the weights of the RNN, which are learned slowly through a general-purpose ("slow") RL algorithm. The RNN receives all information a typical RL algorithm would receive, including observations, actions, rewards, and termination flags; and it retains its state across episodes in a given Markov Decision Process. The activations of the RNN store the state of the "fast" RL algorithm on the current (previously unseen) MDP. We evaluate RL^2 experimentally on both small-scale and large-scale problems. On the small-scale side, we train it to solve randomly generated multi-arm bandit problems and finite MDPs. After RL^2 is trained, its performance on new MDPs is close to human-designed algorithms with optimality guarantees. On the large-scale side, we test RL^2 on a vision-based navigation task and show that it scales up to high-dimensional problems."

>	"Although Bayesian reinforcement learning provides a solid framework for incorporating prior knowledge into the learning process, exact computation of the Bayesian update is intractable in all but the simplest cases. Thus, practical reinforcement learning algorithms often incorporate a mixture of Bayesian and domain-specific ideas to bring down sample complexity and computational burden. Notable examples include guided policy search with unknown dynamics and PILCO. These methods can learn a task using a few minutes to a few hours of real experience, compared to days or even weeks required by previous methods. However, these methods tend to make assumptions about the environment (e.g., instrumentation for access to the state at learning time), or become computationally intractable in high-dimensional settings. Rather than hand-designing domain-specific reinforcement learning algorithms, we take a different approach in this paper: we view the learning process of the agent itself as an objective, which can be optimized using standard reinforcement learning algorithms. The objective is averaged across all possible MDPs according to a specific distribution, which reflects the prior that we would like to distill into the agent. We structure the agent as a recurrent neural network, which receives past rewards, actions, and termination flags as inputs in addition to the normally received observations. Furthermore, its internal state is preserved across episodes, so that it has the capacity to perform learning in its own hidden activations. The learned agent thus also acts as the learning algorithm, and can adapt to the task at hand when deployed."

>	"MDPs encountered in real world = tiny subset of all MDPs that could be defined"  
>	"How to acquire a good prior for real-world MDPs?"  
>	"How to design algorithms that make use of such prior information?"  
>	"Key idea: learn a fast RL algorithm that make use of such prior information"  

>	"This paper suggests a different approach for designing better reinforcement learning algorithms: instead of acting as the designers ourselves, learn the algorithm end-to-end using standard reinforcement learning techniques. That is, the “fast” RL algorithm is a computation whose state is stored in the RNN activations, and the RNN’s weights are learned by a general-purpose “slow” reinforcement learning algorithm."

>	"RL agent = RNN = generic computation architecture  
>	- different weights in the RNN means different RL algorithm and prior  
>	- different activations in the RNN means different current policy  
>	- meta-train objective can be optimized with existing (slow) RL algorithm"  

>	"RNN is made to ingest multiple rollouts from many different MDPs and then perform a policy gradient update through the entire temporal span of the RNN. The hope is that the RNN will learn a faster RL algorithm in its memory weights."  
>	"Suppose L represents an RNN. Let Envk(a) be a function that takes an action, uses it to interact with the MDP representing task k, and returns the next observation o, reward r, and a termination flag d. Then we have:  
>	xt = [ot−1, at−1, rt−1, dt−1]  
>	L(ht, xt) = [at, ht+1]  
>	Envk(at) = [ot, rt, dt]  
>	To train this RNN, we sample N MDPs from M and obtain k rollouts for each MDP by running the MDP through the RNN as above. We then compute a policy gradient update to move the RNN parameters in a direction which maximizes the returns over the k trials performed for each MDP."  

  - `video` <https://facebook.com/nipsfoundation/videos/1554594181298482?t=451> (Abbeel)
  - `video` <http://www.fields.utoronto.ca/video-archive/2017/02/2267-16530> (19:00) (Abbeel)
  - `video` <https://facebook.com/icml.imls/videos/2265408103721327?t=5121> (Abbeel)
  - `video` <https://youtu.be/SfCa1HQMkuw?t=1h16m56s> (Schulman)
  - `video` <https://youtu.be/BskhUBPRrqE?t=6m37s> (Sutskever)
  - `post` <https://lilianweng.github.io/lil-log/2019/06/23/meta-reinforcement-learning.html#on-the-origin-of-meta-rl>
  - `notes` <https://github.com/DanielTakeshi/Paper_Notes/blob/master/reinforcement_learning/RL2-Fast_Reinforcement_Learning_via_Slow_Reinforcement_Learning.md>
  - `paper` [**"Learning to Reinforcement Learn"**](#learning-to-reinforcement-learn-wang-et-al) by Wang et al. `summary`


#### ["Learning to Reinforcement Learn"](http://arxiv.org/abs/1611.05763) Wang et al.
>	"In recent years deep reinforcement learning systems have attained superhuman performance in a number of challenging task domains. However, a major limitation of such applications is their demand for massive amounts of training data. A critical present objective is thus to develop deep RL methods that can adapt rapidly to new tasks. In the present work we introduce a novel approach to this challenge, which we refer to as deep meta-reinforcement learning. Previous work has shown that recurrent networks can support meta-learning in a fully supervised context. We extend this approach to the RL setting. What emerges is a system that is trained using one RL algorithm, but whose recurrent dynamics implement a second, quite separate RL procedure. This second, learned RL algorithm can differ from the original one in arbitrary ways. Importantly, because it is learned, it is configured to exploit structure in the training domain. We unpack these points in a series of seven proof-of-concept experiments, each of which examines a key aspect of deep meta-RL. We consider prospects for extending and scaling up the approach, and also point out some potentially important implications for neuroscience."

>	"learning to explore"  
>	"outer episodes (sample a new bandit problem / MDP) and inner episodes (of sampled MDP)"  
>	"use RNN policy with no state reset between inner episodes for outer POMDP"  

  - `video` <https://vimeo.com/250399556> (Wang)
  - `video` <https://youtu.be/Y85Zn50Eczs?t=20m18s> (Botvinick)
  - `video` <https://youtu.be/LnXgs73OUjE?t=29m20s> (Botvinick)
  - `video` <https://youtu.be/3t06ajvBtl0?t=1h11s> (Botvinick)
  - `post` <https://lilianweng.github.io/lil-log/2019/06/23/meta-reinforcement-learning.html#on-the-origin-of-meta-rl>
  - `post` <https://lesswrong.com/posts/Wnqua6eQkewL3bqsF/matt-botvinick-on-the-spontaneous-emergence-of-learning>
  - `paper` ["Reinforcement Learning, Fast and Slow"](https://www.cell.com/trends/cognitive-sciences/fulltext/S1364-6613(19)30061-0) by Botvinick et al. ([talk](https://slideslive.com/38915872/metareinforcement-learning-an-appreciation) by Botvinick `video`) ([talk](https://youtube.com/watch?v=b0LddBiF5jM) by Botvinick `video`) ([overview](https://youtube.com/watch?v=_N_nFzMtWkA) by Kilcher `video`)
  - `paper` ["RL^2: Fast Reinforcement Learning via Slow Reinforcement Learning"](#rl2-fast-reinforcement-learning-via-slow-reinforcement-learning-duan-schulman-chen-bartlett-sutskever-abbeel) by Duan et al. `summary`



---
### interesting papers - exploration and intrinsic motivation - auxiliary tasks

[interesting recent papers](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----
#### ["Hindsight Experience Replay"](https://arxiv.org/abs/1707.01495) Andrychowicz et al.
  `HER` `curriculum learning` `auxiliary tasks`
>	Dealing with sparse rewards is one of the biggest challenges in Reinforcement Learning. We present a novel technique called Hindsight Experience Replay which allows sample-efficient learning from rewards which are sparse and binary and therefore avoid the need for complicated reward engineering. It can be combined with an arbitrary off-policy RL algorithm and may be seen as a form of implicit curriculum. We demonstrate our approach on the task of manipulating objects with a robotic arm. In particular, we run experiments on three different tasks: pushing, sliding, and pick-and-place, in each case using only binary rewards indicating whether or not the task is completed. Our ablation studies show that Hindsight Experience Replay is a crucial ingredient which makes training possible in these challenging environments. We show that our policies trained on a physics simulation can be deployed on a physical robot and successfully complete the task."

>	"Get reward signal from any experience by simply assuming the goal equals whatever happened."  
>	"HER may be seen as a form of implicit curriculum as the goals used for replay naturally shift from ones which are simple to achieve even by a random agent to more difficult ones. However, in contrast to explicit curriculum, HER does not require having any control over the distribution of initial environment states."  
>	"Not only does HER learn with extremely sparse rewards, in our experiments it also performs better with sparse rewards than with shaped ones. These results are indicative of the practical challenges with reward shaping, and that shaped rewards would often constitute a compromise on the metric we truly care about (such as binary success/failure)."  

  - `post` <https://blog.openai.com/ingredients-for-robotics-research/>
  - <https://sites.google.com/site/hindsightexperiencereplay/> (demo)
  - `video` <https://facebook.com/nipsfoundation/videos/1554594181298482?t=2280> (Abbeel)
  - `video` <https://youtu.be/TERCdog1ddE?t=50m45s> (Abbeel)
  - `video` <https://youtu.be/JX5E0Tt7K10?t=3m50s> (Sutskever)
  - `video` <https://youtu.be/BCzFs9Xb9_o?t=21m2s> (Sutskever)
  - `video` <https://youtu.be/RvEwFvl-TrY?t=19m18s> (Sutskever)
  - `video` <https://youtu.be/BXe2A5i4ESw?t=10m42s> (Fournier)
  - `video` <https://youtu.be/qvxgsxQFHgQ?t=5m20s> (Ivanov) `in russian`
  - `post` <https://danieltakeshi.github.io/2018/02/28/sample-efficient-rl>
  - `notes` <https://yobibyte.github.io/files/paper_notes/her.pdf>
  - `post` <https://jangirrishabh.github.io/2018/03/25/Overcoming-exploration-demos.html>
  - `code` <https://github.com/openai/baselines/tree/master/baselines/her>
  - `paper` ["Universal Value Function Approximators"](https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#schaul-horgan-gregor-silver---universal-value-function-approximators) by Schaul et al. `summary`
  - `paper` ["Hindsight Policy Gradients"](https://arxiv.org/abs/1711.06006) by Rauber et al.


#### ["Reinforcement Learning with Unsupervised Auxiliary Tasks"](http://arxiv.org/abs/1611.05397) Jaderberg, Mnih, Czarnecki, Schaul, Leibo, Silver, Kavukcuoglu
  `UNREAL`
>	"Deep reinforcement learning agents have achieved state-of-the-art results by directly maximising cumulative reward. However, environments contain a much wider variety of possible training signals. In this paper, we introduce an agent that also maximises many other pseudo-reward functions simultaneously by reinforcement learning. All of these tasks share a common representation that, like unsupervised learning, continues to develop in the absence of extrinsic rewards. We also introduce a novel mechanism for focusing this representation upon extrinsic rewards, so that learning can rapidly adapt to the most relevant aspects of the actual task. Our agent significantly outperforms the previous state-of-theart on Atari, averaging 880% expert human performance, and a challenging suite of first-person, three-dimensional Labyrinth tasks leading to a mean speedup in learning of 10× and averaging 87% expert human performance on Labyrinth."

>	"Auxiliary tasks:
	- pixel changes: learn a policy for maximally changing the pixels in a grid of cells overlaid over the images
	- network features: learn a policy for maximally activating units in a specific hidden layer
	- reward prediction: predict the next reward given some historical context
	- value function replay: value function regression for the base agent with varying window for n-step returns"

>	"By using these tasks we force the agent to learn about the controllability of its environment and the sorts of sequences which lead to rewards, and all of this shapes the features of the agent."

>	"This approach exploits the multithreading capabilities of standard CPUs. The idea is to execute many instances of our agent in parallel, but using a shared model. This provides a viable alternative to experience replay, since parallelisation also diversifies and decorrelates the data. Our asynchronous actor-critic algorithm, A3C, combines a deep Q-network with a deep policy network for selecting actions. It achieves state-of-the-art results, using a fraction of the training time of DQN and a fraction of the resource consumption of Gorila."

  - `post` <https://deepmind.com/blog/reinforcement-learning-unsupervised-auxiliary-tasks/>
  - `video` <https://youtube.com/watch?v=Uz-zGYrYEjA> (demo)
  - `video` <https://youtube.com/watch?v=VVLYTqZJrXY> (Jaderberg)
  - `video` <https://facebook.com/iclr.cc/videos/1712224178806641?t=4545> (Jaderberg)
  - `video` <https://youtu.be/bsuvM1jO-4w?t=20m7s> (Mnih)
  - `video` <https://youtu.be/Yvll3P1UW5k?t=8m42s> (Abbeel)
  - `video` <https://youtube.com/watch?v=-YiMVR3HEuY> (Kilcher)
  - `video` <https://yadi.sk/i/_2_0yqeW3HDbcn> (18:25) (Panin) `in russian`
  - `notes` <http://www.shortscience.org/paper?bibtexKey=journals/corr/1611.05397>
  - `code` <https://github.com/miyosuda/unreal>



---
### interesting papers - exploration and intrinsic motivation - information theoretic and distributional models - uncertainty motivation

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----
#### ["Action-Conditional Video Prediction using Deep Networks in Atari Games"](https://arxiv.org/abs/1507.08750) Oh, Guo, Lee, Lewis, Singh
>	"Motivated by vision-based reinforcement learning problems, in particular Atari games from the recent benchmark Aracade Learning Environment, we consider spatio-temporal prediction problems where future (image-)frames are dependent on control variables or actions as well as previous frames. While not composed of natural scenes, frames in Atari games are high-dimensional in size, can involve tens of objects with one or more objects being controlled by the actions directly and many other objects being influenced indirectly, can involve entry and departure of objects, and can involve deep partial observability. We propose and evaluate two deep neural network architectures that consist of encoding, action-conditional transformation, and decoding layers based on convolutional neural networks and recurrent neural networks. Experimental results show that the proposed architectures are able to generate visually-realistic frames that are also useful for control over approximately 100-step action-conditional futures in some games. To the best of our knowledge, this paper is the first to make and evaluate long-term predictions on high-dimensional video conditioned by control inputs."

>	"Modeling videos (i.e., building a generative model) is still a very challenging problem because it usually involves high-dimensional natural-scene data with complex temporal dynamics. Thus, recent studies have mostly focused on modeling simple video data, such as bouncing balls or small video patches, where the next frame is highly predictable based on the previous frames. In many applications, however, future frames are not only dependent on previous frames but also on additional control or action variables. For example, the first-person-view in a vehicle is affected by wheel-steering and acceleration actions. The camera observation of a robot is similarly dependent on its movement and changes of its camera angle. More generally, in vision-based reinforcement learning problems, learning to predict future images conditioned on future actions amounts to learning a model of the dynamics of the agent-environment interaction; such transition-models are an essential component of model-based learning approaches to RL."

>	"The encoding part computes high-level abstractions of input frames, the action-conditional transformation part predicts the abstraction of the next frame conditioned on the action, and finally the decoding part maps the predicted high-level abstraction to a detailed frame. The feedforward architecture takes the last 4 frames as input while the recurrent architecture takes just the last frame but has recurrent connections. Our experimental results on predicting images in Atari games show that our architectures are able to generate realistic frames over 100-step action-conditional future frames without diverging. We show that the representations learned by our architectures 1) approximately capture natural similarity among actions, and 2) discover which objects are directly controlled by the agent’s actions and which are only indirectly influenced or not controlled at all. We evaluated the usefulness of our architectures for control in two ways: 1) by replacing emulator frames with predicted frames in a previously-learned model-free controller (DQN; DeepMind’s state of the art Deep-Q-Network for Atari Games), and 2) by using the predicted frames to drive a more informed than random exploration strategy to improve a model-free controller (also DQN)."

>	approximate visitation counting in a learned state embedding using Gaussian kernels

  - <https://sites.google.com/a/umich.edu/junhyuk-oh/action-conditional-video-prediction> (demo)
  - `video` <https://youtu.be/igm38BakyAg?t=15m26s> (Lee)
  - `video` <http://research.microsoft.com/apps/video/default.aspx?id=259646> (17:30)
  - `code` <https://github.com/junhyukoh/nips2015-action-conditional-video-prediction>


#### ["Unifying Count-Based Exploration and Intrinsic Motivation"](http://arxiv.org/abs/1606.01868) Bellemare, Srinivasan, Ostrovski, Schaul, Saxton, Munos
  `DQN-CTS` `NIPS 2016`
>	"We consider an agent's uncertainty about its environment and the problem of generalizing this uncertainty across observations. Specifically, we focus on the problem of exploration in non-tabular reinforcement learning. Drawing inspiration from the intrinsic motivation literature, we use density models to measure uncertainty, and propose a novel algorithm for deriving a pseudo-count from an arbitrary density model. This technique enables us to generalize count-based exploration algorithms to the non-tabular case. We apply our ideas to Atari 2600 games, providing sensible pseudo-counts from raw pixels. We transform these pseudo-counts into intrinsic rewards and obtain significantly improved exploration in a number of hard games, including the infamously difficult Montezuma's Revenge."

>	"Many of hard RL problems share one thing in common: rewards are few and far between. In reinforcement learning, exploration is the process by which an agent comes to understand its environment and discover where the reward is. Most practical RL applications still rely on crude algorithms, like epsilon-greedy (once in awhile, choose a random action), because more theoretically-motivated approaches don't scale. But epsilon-greedy is quite data inefficient, and often can't even get off the ground. In this paper we show that it's possible to use simple density models (assigning probabilities to states) to "count" the number of times we've visited a particular state. We call the output of our algorithm a pseudo-count. Pseudo-counts give us a handle on uncertainty: how confident are we that we've explored this part of the game?"

>	"Intrinsic motivation offers a different perspective on exploration. Intrinsic motivation algorithms typically use novelty signals - surrogates for extrinsic rewards - to drive curiosity within an agent, influenced by classic ideas from psychology. To sketch out some recurring themes, these novelty signals might be prediction error (Singh et al., 2004; Stadie et al., 2015), value error (Simsek and Barto, 2006), learning progress (Schmidhuber, 1991), or mutual information (Still and Precup, 2012; Mohamed and Rezende, 2015). The idea also finds roots in continual learning (Ring, 1997). In Thrun’s taxonomy, intrinsic motivation methods fall within the category of error-based exploration."

>	"We provide what we believe is the first formal evidence that intrinsic motivation and count-based exploration are but two sides of the same coin. Our main result is to derive a pseudo-count from a sequential density model over the state space. We only make the weak requirement that such a model should be learning-positive: observing x should not immediately decrease its density. In particular, counts in the usual sense correspond to the pseudo-counts implied by the data’s empirical distribution. We expose a tight relationship between the pseudo-count, a variant of Schmidhuber’s compression progress which we call prediction gain, and Bayesian information gain."

>	"Theorem 1 suggests that using an exploration bonus proportional to Nn^(x)^(-1/2), similar to the MBIE-EB bonus, leads to a behaviour at least as exploratory as one derived from an information gain bonus. Since pseudo-counts correspond to empirical counts in the tabular setting, this approach also preserves known theoretical guarantees. In fact, we are confident pseudo-counts may be used to prove similar results in non-tabular settings."

>	"Unlike many intrinsic motivation algorithms, pseudo-counts also do not rely on learning a forward (transition and/or reward) model. This point is especially important because a number of powerful density models for images exist (Van den Oord et al., 2016), and because optimality guarantees cannot in general exist for intrinsic motivation algorithms based on forward models."

----
>	"Take maximum likelihood based tabular approach in RMAX and replace it with high-dimensional density estimator, and rather than estimating transition function just try to estimate unconditional probability of being in a state. Because it is a high-dimensional density estimator it won't be count-based the way tabular model of RMAX would be. But in a pseudo-count approach we ask ourselves, suppose this method was a count-based (which it is not), what counts need to be in order to explain the change in estimated probability that results from updating the model with a new data point. Then it can be used to drive systematic exploration similar to RMAX."

>	"Authors derived pseudo-counts from Context Tree Switching density models over states and used those to form intrinsic rewards."

>	"Bayesian surprise: maximize KL between posterior (after seeing observation) and prior (before seeing it).  
>	Prediction gain: maximize change in prediction error before and after seeing an observation - approximates bayesian surprise."

>	"Although I'm a bit bothered by the assumption of the density model being "learning-positive", which seems central to their theoretical derivation of pseudo-counts: after you observe a state, your subjective probability of observing it again immediately should generally decrease unless you believe that the state is a fixed point attractor with high probability. I can see that in practice the assumption works well in their experimental setting since they use pixel-level factored models and, by the nature of the ATARI games they test on, most pixels don't change value from frame to frame, but in a more general setting, e.g. a side-scroller game or a 3D first-person game this assumption would not hold."

  - `video` <https://youtube.com/watch?v=0yI2wJ6F8r0> + <https://youtube.com/watch?v=qeeTok1qDZk> + <https://youtube.com/watch?v=EzQwCmGtEHs> (demo)
  - `video` <https://youtu.be/qSfd27AgcEk?t=29m5s> (Bellemare)
  - `video` <https://youtu.be/WuFMrk3ZbkE?t=1h27m37s> (Bellemare)
  - `video` <https://slideslive.com/38922727/bayesadaptive-deep-reinforcement-learning-via-metalearning> (Whiteson)
  - `video` <https://youtu.be/qduxl-vKz1E?t=1h16m30s> (Seleznev) `in russian`
  - `video` <https://youtube.com/watch?v=qKyOLNVpknQ> (Pavlov) `in russian`
  - `notes` <http://pemami4911.github.io/paper-summaries/deep-rl/2016/10/08/unifying-count-based-exploration-and-intrinsic-motivation.html>
  - `paper` ["Approximate Exploration through State Abstraction"](https://arxiv.org/abs/1808.09819) by Taiga et al.
  - `paper` [**"On Bonus Based Exploration Methods In The Arcade Learning Environment"**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#on-bonus-based-exploration-methods-in-the-arcade-learning-environment-taiga-fedus-machado-courville-bellemare) by Taiga et al. `summary`


#### ["Count-Based Exploration with Neural Density Models"](http://arxiv.org/abs/1703.01310) Ostrovski, Bellemare, van den Oord, Munos
  `DQN-PixelCNN` `ICML 2017`
>	"Bellemare et al. (2016) introduced the notion of a pseudo-count to generalize count-based exploration to non-tabular reinforcement learning. This pseudo-count is derived from a density model which effectively replaces the count table used in the tabular setting. Using an exploration bonus based on this pseudo-count and a mixed Monte Carlo update applied to a DQN agent was sufficient to achieve state-of-the-art on the Atari 2600 game Montezuma's Revenge. In this paper we consider two questions left open by their work: First, how important is the quality of the density model for exploration? Second, what role does the Monte Carlo update play in exploration? We answer the first question by demonstrating the use of PixelCNN, an advanced neural density model for images, to supply a pseudo-count. In particular, we examine the intrinsic difficulties in adapting Bellemare et al's approach when assumptions about the model are violated. The result is a more practical and general algorithm requiring no special apparatus. We combine PixelCNN pseudo-counts with different agent architectures to dramatically improve the state of the art on several hard Atari games. One surprising finding is that the mixed Monte Carlo update is a powerful facilitator of exploration in the sparsest of settings, including Montezuma's Revenge."

  - `video` <http://youtube.com/watch?v=qSfd27AgcEk> (Bellemare)
  - `video` <https://vimeo.com/238243932> (Bellemare)
  - `video` <http://videolectures.net/DLRLsummerschool2018_bellemare_deep_RL/#t=3474> (Bellemare)
  - `video` <https://youtu.be/EMv1AVLOnto?t=1m49s> (Svidchenko) `in russian`
  - `paper` [**"Unifying Count-Based Exploration and Intrinsic Motivation"**](#unifying-count-based-exploration-and-intrinsic-motivation-bellemare-srinivasan-ostrovski-schaul-saxton-munos) by Bellemare et al. `summary`
  - `paper` [**"On Bonus Based Exploration Methods In The Arcade Learning Environment"**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#on-bonus-based-exploration-methods-in-the-arcade-learning-environment-taiga-fedus-machado-courville-bellemare) by Taiga et al. `summary`


#### ["\#Exploration: A Study of Count-Based Exploration for Deep Reinforcement Learning"](http://arxiv.org/abs/1611.04717) Tang et al.
  `NIPS 2017`
>	"Count-based exploration algorithms are known to perform near-optimally when used in conjunction with tabular reinforcement learning methods for solving small discrete Markov decision processes (MDPs). It is generally thought that count-based methods cannot be applied in high-dimensional state spaces, since most states will only occur once. Recent deep RL exploration strategies are able to deal with high-dimensional continuous state spaces through complex heuristics, often relying on optimism in the face of uncertainty or intrinsic motivation. In this work, we describe a surprising finding: a simple generalization of the classic count-based approach can reach near state-of-the-art performance on various highdimensional and/or continuous deep RL benchmarks. States are mapped to hash codes, which allows to count their occurrences with a hash table. These counts are then used to compute a reward bonus according to the classic count-based exploration theory. We find that simple hash functions can achieve surprisingly good results on many challenging tasks. Furthermore, we show that a domain-dependent learned hash code may further improve these results. Detailed analysis reveals important aspects of a good hash function: 1) having appropriate granularity and 2) encoding information relevant to solving the MDP. This exploration strategy achieves near state-of-the-art performance on both continuous control tasks and Atari 2600 games, hence providing a simple yet powerful baseline for solving MDPs that require considerable exploration."

>	"The authors encourage exploration by adding a pseudo-reward of the form beta/sqrt(count(state)) for infrequently visited states. State visits are counted using Locality Sensitive Hashing (LSH) based on an environment-specific feature representation like raw pixels or autoencoder representations. The authors show that this simple technique achieves gains in various classic RL control tasks and several games in the ATARI domain. While the algorithm itself is simple there are now several more hyperaprameters to tune: The bonus coefficient beta, the LSH hashing granularity (how many bits to use for hashing) as well as the type of feature representation based on which the hash is computed, which itself may have more parameters. The experiments don't paint a consistent picture and different environments seem to need vastly different hyperparameter settings, which in my opinion will make this technique difficult to use in practice."

  - `videos` <https://facebook.com/icml.imls/videos/2265408103721327?t=4692> (Abbeel)
  - `videos` <https://youtu.be/EMv1AVLOnto?t=11m37s> (Svidchenko) `in russian`
  - `slides` <https://phillipi.github.io/6.882/notes/Wk6/2-3_12_2019_Exploration.pdf> (Tang)
  - `notes` <http://www.shortscience.org/paper?bibtexKey=journals%2Fcorr%2F1611.04717>
  - `notes` <https://github.com/DanielTakeshi/Paper_Notes/blob/master/reinforcement_learning/%23Exploration:_A_Study_of_Count-Based_Exploration_for_Deep_Reinforcement_Learning.md>


#### ["EX2: Exploration with Exemplar Models for Deep Reinforcement Learning"](https://arxiv.org/abs/1703.01260) Fu, Co-Reyes, Levine
>	"Deep reinforcement learning algorithms have been shown to learn complex tasks using highly general policy classes. However, sparse reward problems remain a significant challenge. Exploration methods based on novelty detection have been particularly successful in such settings but typically require generative or predictive models of the observations, which can be difficult to train when the observations are very high-dimensional and complex, as in the case of raw images. We propose a novelty detection algorithm for exploration that is based entirely on discriminatively trained exemplar models, where classifiers are trained to discriminate each visited state against all others. Intuitively, novel states are easier to distinguish against other states seen during training. We show that this kind of discriminative modeling corresponds to implicit density estimation, and that it can be combined with count-based exploration to produce competitive results on a range of popular benchmark tasks, including state-of-the-art results on challenging egocentric observations in the vizDoom benchmark."


#### ["Episodic Curiosity through Reachability"](https://arxiv.org/abs/1810.02274) Savinov et al.
  `EC` `uncertainty motivation` `novelty` `ICLR 2019`
>	"Rewards are sparse in the real world and most of today’s reinforcement learning algorithms struggle with such sparsity. One solution to this problem is to allow the agent to create rewards for itself - thus making rewards dense and more suitable for learning. In particular, inspired by curious behaviour in animals, observing something novel could be rewarded with a bonus. Such bonus is summed up with the real task reward - making it possible for RL algorithms to learn from the combined reward. We propose a new curiosity method which uses episodic memory to form the novelty bonus. To determine the bonus, the current observation is compared with the observations in memory. Crucially, the comparison is done based on how many environment steps it takes to reach the current observation from those in memory - which incorporates rich information about environment dynamics. This allows us to overcome the known “couch-potato” issues of prior work - when the agent finds a way to instantly gratify itself by exploiting actions which lead to hardly predictable consequences. We test our approach in visually rich 3D environments in VizDoom, DMLab and MuJoCo. In navigational tasks from VizDoom and DMLab, our agent outperforms the state-of-the-art curiosity method ICM. In MuJoCo, an ant equipped with our curiosity module learns locomotion out of the first-person-view curiosity only."

  - <https://sites.google.com/view/episodic-curiosity> (demo)
  - `post` <https://ai.googleblog.com/2018/10/curiosity-and-procrastination-in.html>
  - `video` <https://youtu.be/qvxgsxQFHgQ?t=1h14m21s> (Ivanov) `in russian`



---
### interesting papers - exploration and intrinsic motivation - information theoretic and distributional models - information gain motivation

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----
#### ["Planning to Be Surprised: Optimal Bayesian Exploration in Dynamic Environments"](https://arxiv.org/abs/1103.5708) Sun, Gomez, Schmidhuber
  - <https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#planning-to-be-surprised-optimal-bayesian-exploration-in-dynamic-environments-sun-gomez-schmidhuber>


#### ["Planning to Explore via Self-Supervised World Models"](https://arxiv.org/abs/2005.05960) Sekar, Rybkin, Daniilidis, Abbeel, Hafner, Pathak
  `Plan2Explore` `planning to explore` `ICML 2020`
>	"Reinforcement learning allows solving complex tasks, however, the learning tends to be task-specific and the sample efficiency remains a challenge. We present Plan2Explore, a self-supervised reinforcement learning agent that tackles both these challenges through a new approach to self-supervised exploration and fast adaptation to new tasks, which need not be known during exploration. During exploration, unlikeprior methods which retrospectively compute the novelty of observations after the agent has already reached them, our agent acts efficiently by leveraging planning to seek out expected future novelty. After exploration, the agent quickly adapts to multiple downstream tasks in a zero or a few-shot manner. We evaluate on challenging control tasks from high-dimensional image inputs. Without any training supervision or task-specific interaction, Plan2Explore outperforms prior self-supervised exploration methods, and in fact, almost matches the performances oracle which has access to rewards."

  - <https://ramanans1.github.io/plan2explore>
  - `post` <https://bair.berkeley.edu/blog/2020/10/06/plan2explore/>
  - `post` <https://blog.ml.cmu.edu/2020/10/06/plan2explore/>
  - `video` <https://youtube.com/watch?v=gan79mAVfq8> (Pathak)
  - `video` <https://pscp.tv/w/1mnGelLjoBWKX> (1:03:12) (Lillicrap)
  - `video` <https://youtube.com/watch?v=GyEzjW1m7kU> (Rybkin)
  - `video` <https://youtube.com/watch?v=IiBFqnNu7A8> (Kilcher)


#### ["Model-Based Active Exploration"](https://arxiv.org/abs/1810.12162) Shyam, Jaskowski, Gomez
  `MAX` `planning to explore` `pure exploration` `ICML 2019`
>	"Efficient exploration is an unsolved problem in Reinforcement Learning which is usually addressed by reactively rewarding the agent for fortuitously encountering novel situations. This paper introduces an efficient active exploration algorithm, Model-Based Active eXploration, which uses an ensemble of forward models to plan to observe novel events. This is carried out by optimizing agent behaviour with respect to a measure of novelty derived from the Bayesian perspective of exploration, which is estimated using the disagreement between the futures predicted by the ensemble members. We show empirically that in semi-random discrete environments where directed exploration is critical to make progress, MAX is at least an order of magnitude more efficient than strong baselines. MAX scales to high-dimensional continuous environments where it builds task-agnostic models that can be used for any downstream task."

>	"While MAX can be used in conjunction with conventional policy learning to maximize external reward, this paper focuses on pure exploration: exploration disregarding or in the absence of external reward, followed by exploitation. This setup is more natural in situations where it is useful to do task-agnostic exploration and learn models that can later be exploited for multiple tasks, including those that are not known a priori."

>	"Current exploration methods are reactive: the agent accidentally observes something “novel” and then decides to obtain more information about it. Further exploration in the vicinity of the novel state is carried out typically through an exploration bonus or intrinsic motivation reward, which have to be unlearned once the novelty has worn off, making exploration inefficient — a problem we refer to as over-commitment. However, exploration can also be active, where the agent seeks out novelty based on its own “internal” estimate of what action sequences will lead to interesting transitions. This approach is inherently more powerful than reactive exploration, but requires a method to predict the consequences of actions and their degree of novelty. This problem can be formulated optimally in the Bayesian setting where the novelty of a given state transition can be measured by the disagreement between the next-state predictions made by probable models of the environment. MAX approximates the idealized distribution using an ensemble of learned forward dynamics models. The algorithm identifies learnable unknowns or uncertainty representing novelty in the environment by measuring the amount of conflict between the predictions of the constituent models. It then constructs exploration policies to resolve those conflicts by visiting the relevant area. Unlearnable unknowns or risk, such as random noise in the environment does not interfere with the process since noise manifests as confusion among all models and not as a conflict."

>	"The key idea behind our approach to active exploration in the environment, or the external Markov Decision Process, is to use a surrogate or exploration MDP where the novelty of transitions can be estimated before they have actually been encountered by the agent in the environment. In the standard RL setting, a policy would be learned to take actions that maximize some function of the external reward received from the environment according to r, i.e., the return. Because pure active exploration does not care about r, and true transition function of environment dynamics is unknown, the amount of new information conveyed about the environment by state transitions that could be caused by an exploration policy has to be used as the learning signal. From the Bayesian perspective, this can be captured by the KL-divergence between P(T), the (prior) distribution over transition functions before a particular transition φ, and P(T|φ), the posterior distribution after φ has occurred. This is commonly referred to as Information Gain."

>	"Exploration policies were regularly trained with SAC from scratch with the utilities re-calculated using the latest models to avoid over-commitment. The first phase of training involved only the fixed dataset containing the transitions experienced by the agent so-far. For active methods (MAX and TVAX), this was followed by an additional phase, when the policies were updated by the data generated exclusively from the “imaginary” exploration MDP. Note that this learning in “imagination” being possible through the use of an ensemble of models distinguishes active methods from reactive methods."

>	"Our work is inspired by the framework developed in Schmidhuber (1997; 2002), in which two adversarial reward maximizing modules called the left brain and the right brain bet on outcomes of experimental protocols or algorithms they have collectively generated and agreed upon. Each brain is intrinsically motivated to outwit or surprise the other by proposing an experiment such that the other agrees on the experimental protocol but disagrees on the predicted outcome. After having executed the action sequence protocol approved by both brains, the surprised loser pays a reward to the winner in a zero-sum game. MAX greatly simplifies this previous active exploration framework, distilling certain essential aspects. Two or more predictive models that may compute different hypotheses about the consequences of the actions of the agent, given observations, are still used. However, there is only one reward maximizer or RL machine which is separate from the predictive models."

  - `code` <https://github.com/nnaisense/max>
  - `paper` [**"What's Interesting?"**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#whats-interesting-schmidhuber) by Schmidhuber `summary`


#### ["VIME: Variational Information Maximizing Exploration"](http://arxiv.org/abs/1605.09674) Houthooft, Chen, Duan, Schulman, Turck, Abbeel
  `VIME`
>	"Scalable and effective exploration remains a key challenge in reinforcement learning. While there are methods with optimality guarantees in the setting of discrete state and action spaces, these methods cannot be applied in high-dimensional greedy exploration or adding Gaussian noise to the controls. This paper introduces Variational Information Maximizing Exploration (VIME), an exploration strategy based on maximization of information gain about the agent’s belief of environment dynamics. We propose a practical implementation, using variational inference in Bayesian neural networks which efficiently handles continuous state and action spaces. VIME modifies the MDP reward function, and can be applied with several different underlying RL algorithms. We demonstrate that VIME achieves significantly better performance compared to heuristic exploration methods across a variety of continuous control tasks and algorithms, including tasks with very sparse rewards."

>	"We have proposed Variational Information Maximizing Exploration, a curiosity-driven exploration strategy for continuous control tasks. Variational inference is used to approximate the posterior distribution of a Bayesian neural network that represents the environment dynamics. Using information gain in this learned dynamics model as intrinsic rewards allows the agent to optimize for both external reward and intrinsic surprise simultaneously. Empirical results show that VIME performs significantly better than heuristic exploration methods across various continuous control tasks and algorithms. As future work, we would like to investigate measuring surprise in the value function and using the learned dynamics model for planning."

>	"This paper proposes a curiosity-driven exploration strategy, making use of information gain about the agent’s internal belief of the dynamics model as a driving force. This principle can be traced back to the concepts of curiosity and surprise (Schmidhuber). Within this framework, agents are encouraged to take actions that result in states they deem surprising - i.e., states that cause large updates to the dynamics model distribution. We propose a practical implementation of measuring information gain using variational inference. Herein, the agent’s current understanding of the environment dynamics is represented by a Bayesian neural networks. We also show how this can be interpreted as measuring compression improvement, a proposed model of curiosity (Schmidhuber). In contrast to previous curiosity-based approaches, our model scales naturally to continuous state and action spaces. The presented approach is evaluated on a range of continuous control tasks, and multiple underlying RL algorithms. Experimental results show that VIME achieves significantly better performance than naïve exploration strategies."

>	"Variational inference is used to approximate the posterior distribution of a Bayesian neural network that represents the environment dynamics. Using information gain in this learned dynamics model as intrinsic rewards allows the agent to optimize for both external reward and intrinsic surprise simultaneously."  
>	"r'(st,at,st+1) = r(st,at) + μ * DKL[p(θ|ξt,at,st+1)||p(θ|ξt)]"  

>	"It is possible to derive an interesting relationship between compression improvement - an intrinsic reward objective defined in Schmidhuber's Artificial Curiosity and Creativity theory, and the information gain. The agent’s curiosity is equated with compression improvement, measured through C(ξt; φt-1) - C(ξt; φt), where C(ξ; φ) is the description length of ξ using φ as a model. Furthermore, it is known that the negative variational lower bound can be viewed as the description length. Hence, we can write compression improvement as L[q(θ; φt), ξt] - L[q(θ; φt-1), ξt]. In addition, due to alternative formulation of the variational lower bound, compression improvement can be written as (log p(ξt) - DKL[q(θ; φt)||p(θ|ξt)]) - (log p(ξt) - DKL[q(θ; φt-1)||p(θ|ξt)]). If we assume that φt perfectly optimizes the variational lower bound for the history ξt, then DKL[q(θ; φt)||p(θ|ξt)] = 0, which occurs when the approximation equals the true posterior, i.e., q(θ; φt) = p(θ|ξt). Hence, compression improvement becomes DKL[p(θ|ξt-1) || p(θ|ξt)]. Therefore, optimizing for compression improvement comes down to optimizing the KL divergence from the posterior given the past history ξt-1 to the posterior given the total history ξt. As such, we arrive at an alternative way to encode curiosity than information gain, namely DKL[p(θ|ξt)||p(θ|ξt,at,st+1)], its reversed KL divergence. In experiments, we noticed no significant difference between the two KL divergence variants. This can be explained as both variants are locally equal when introducing small changes to the parameter distributions. Investigation of how to combine both information gain and compression improvement is deferred to future work."

  - <https://goo.gl/fyxLvI> (demo)
  - `video` <https://youtube.com/watch?v=nbbMSMv3v5k>
  - `video` <https://youtu.be/WRFqzYWHsZA?t=18m38s> (Abbeel)
  - `video` <https://facebook.com/icml.imls/videos/2265408103721327?t=4996> (Abbeel)
  - `video` <https://youtube.com/watch?v=sRIjxxjVrnY> (Panin)
  - `video` <https://yadi.sk/i/_2_0yqeW3HDbcn> (32:16) (Panin) `in russian` ([slides](https://yadi.sk/i/8sx42nau3HEYKg) `in english`)
  - `notes` <http://pemami4911.github.io/paper-summaries/2016/09/04/VIME.html>
  - `code` <https://github.com/openai/vime>
  - [**Artificial Curiosity and Creativity**](https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#artificial-curiosity-and-creativity) theory of Juergen Schmidhuber



---
### interesting papers - exploration and intrinsic motivation - information theoretic and distributional models - empowerment motivation

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----
#### ["Empowerment - An Introduction"](https://arxiv.org/abs/1310.1863) Salge, Glackin, Polani
>	"Is it better for you to own a corkscrew or not? If asked, you as a human being would likely say “yes”, but more importantly, you are somehow able to make this decision. You are able to decide this, even if your current acute problems or task do not include opening a wine bottle. Similarly, it is also unlikely that you evaluated several possible trajectories your life could take and looked at them with and without a corkscrew, and then measured your survival or reproductive fitness in each. When you, as a human cognitive agent, made this decision, you were likely relying on a behavioural “proxy”, an internal motivation that abstracts the problem of evaluating a decision impact on your overall life, but evaluating it in regard to some simple fitness function. One example would be the idea of curiosity, urging you to act so that your experience new sensations and learn about the environment. On average, this should lead to better and richer models of the world, which give you a better chance of reaching your ultimate goals of survival and reproduction."

>	"But how about questions such as, would you rather be rich than poor, sick or healthy, imprisoned or free? While each options offers some interesting new experience, there seems to be a consensus that rich, healthy and free is a preferable choice. We think that all these examples, in addition to the question of tool ownership above, share a common element of preparedness. Everything else being equal it is preferable to be prepared, to keep ones options open or to be in a state where ones actions have the greatest influence on ones direct environment."

>	"The concept of Empowerment, in a nutshell, is an attempt at formalizing and quantifying these degrees of freedom (or options) that an organism or agent has as a proxy for “preparedness”; preparedness, in turn, is considered a proxy for prospective fitness via the hypothesis that preparedness would be a good indicator to distinguish promising from less promising regions in the prospective fitness landscape, without actually having to evaluate the full fitness landscape."

>	"Empowerment aims to reformulate the options or degrees of freedom that an agent has as the agent’s control over its environment; and not only of its control - to be reproducible, the agent needs to be aware of its control influence and sense it. Thus, empowerment is a measure of both the control an agent has over its environment, as well as its ability to sense this control. Note that this already hints at two different perspectives to evaluate the empowerment of an agent. From the agent perspective empowerment can be a tool for decision making, serving as a behavioural proxy for the agent. This empowerment value can be skewed by the quality of the agent world model, so it should be more accurately described as the agent’s approximation of its own empowerment, based on its world model. The actual empowerment depends both on the agent’s embodiment, and the world the agent is situated in. More precisely, there is a specific empowerment value for the current state of the world (the agent’s current empowerment), and there is an averaged value over all possible states of the environment, weighted by their probability (the agent’s average empowerment)."

>	"Empowerment, as introduced by Klyubin et al. (2005), aims to formalize the combined notion of an agent controlling its environment and sensing this control in the language of information theory. The idea behind this is that this should provide us with a utility function that is inherently local, universal and task-independent.  
>	1. Local means that the knowledge of the local dynamics of the agent is enough to compute it, and that it is not necessary to know the whole system to determine one’s empowerment. Ideally, the information that the agent itself can acquire should be enough.  
>	2. Universal means that it should be possible to apply empowerment “universally” to every possible agent-world interaction. This is achieved by expressing it in the language of information theory and thus making it applicable for any system that can be probabilistically expressed.  
>	3. Task-independent means that empowerment is not evaluated in regard to a specific goal or external reward state. Instead, empowerment is determined by the agent’s embodiment in the world. In particular, apart from minor niche-dependent parameters, the empowerment formalism should have the very same structure in most situations."  

>	"More concretely, the proposed formulation of empowerment defines it via the concept of potential information flow, or channel capacity, between an agent’s actuator state at earlier times and their sensor state at a later time. The idea behind this is that empowerment would quantify how much an agent can reliably and perceptibly influence the world."

>	"The different scenarios presented here, and in the literature on empowerment in general, are highlighting an important aspect of the empowerment flavour of intrinsic motivation algorithms, namely its universality. The same principle that organizes a swarm of agents into a pattern can also swing the pendulum into an upright position, seek out a central location in a maze, be driven towards a manipulable object, or drive the evolution of sensors. The task-independent nature reflected in this list can be both a blessing and a curse. In many cases the resulting solution, such as swinging the pendulum into the upright position, is the goal implied by default by a human observer. However, if indeed a goal is desired that differs from this default, then empowerment will not be the best solution. At present, the question of how to integrate explicit non-default goals into empowerment is fully open."

>	"Let us conclude with a remark regarding the biological empowerment hypotheses in general: the fact that the default behaviours produced by empowerment seem often to match what intuitive expectations concerning default behaviour seem to imply, there is some relevance in investigating whether some of these behaviours are indeed approximating default behaviours observed in nature. A number of arguments in favour of why empowerment maximizing or similar behaviour could be relevant in biology have been made in (Klyubin et al. 2008), of which in this review we mainly highlighted its role as a measure of sensorimotor efficiency and the advantages that an evolutionary process would confer to more informationally efficient perception-action configurations."

  - `video` <https://slideslive.com/38909803/tutorial-on-comparing-intrinsic-motivations-in-a-unified-framework> (1:11:15) (Biehl)
  - `paper` ["All Else Being Equal Be Empowered"](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.101.9018&rep=rep1&type=pdf) by Klyubin, Polani, Nehaniv
  - `paper` ["Empowerment: A Universal Agent-Centric Measure of Contro"](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.297.8746&rep=rep1&type=pdf) by Klyubin, Polani, Nehaniv


#### ["Variational Information Maximisation for Intrinsically Motivated Reinforcement Learning"](http://arxiv.org/abs/1509.08731) Mohamed, Rezende
>	"The mutual information is a core statistical quantity that has applications in all areas of machine learning, whether this is in training of density models over multiple data modalities, in maximising the efficiency of noisy transmission channels, or when learning behaviour policies for exploration by artificial agents. Most learning algorithms that involve optimisation of the mutual information rely on the Blahut-Arimoto algorithm - an enumerative algorithm with exponential complexity that is not suitable for modern machine learning applications. This paper provides a new approach for scalable optimisation of the mutual information by merging techniques from variational inference and deep learning. We develop our approach by focusing on the problem of intrinsically-motivated learning, where the mutual information forms the definition of a well-known internal drive known as empowerment. Using a variational lower bound on the mutual information, combined with convolutional networks for handling visual input streams, we develop a stochastic optimisation algorithm that allows for scalable information maximisation and empowerment-based reasoning directly from pixels to actions."

>	"We have developed a new approach for scalable estimation of the mutual information by exploiting recent advances in deep learning and variational inference. We focussed specifically on intrinsic motivation with a reward measure known as empowerment, which requires at its core the efficient computation of the mutual information. By using a variational lower bound on the mutual information, we developed a scalable model and efficient algorithm that expands the applicability of empowerment to high-dimensional problems, with the complexity of our approach being extremely favourable when compared to the complexity of the Blahut-Arimoto algorithm that is currently the standard. The overall system does not require a generative model of the environment to be built, learns using only interactions with the environment, and allows the agent to learn directly from visual information or in continuous state-action spaces. While we chose to develop the algorithm in terms of intrinsic motivation, the mutual information has wide applications in other domains, all which stand to benefit from a scalable algorithm that allows them to exploit the abundance of data and be applied to large-scale problems."

----
>	"Authors developed a scalable method of approximating empowerment, the mutual information between an agent’s actions and the future state of the environment, using variational methods."

>	"This paper presents a variational approach to the maximisation of mutual information in the context of a reinforcement learning agent. Mutual information in this context can provide a learning signal to the agent that is "intrinsically motivated", because it relies solely on the agent's state/beliefs and does not require from the ("outside") user an explicit definition of rewards. Specifically, the learning objective, for a current state s, is the mutual information between the sequence of K actions a proposed by an exploration distribution w(a|s) and the final state s' of the agent after performing these actions. To understand what the properties of this objective, it is useful to consider the form of this mutual information as a difference of conditional entropies: I(a,s'|s) = H(a|s) - H(a|s',s) Where I(.|.) is the (conditional) mutual information and H(.|.) is the (conditional) entropy. This objective thus asks that the agent find an exploration distribution that explores as much as possible (i.e. has high H(a|s) entropy) but is such that these actions have predictable consequences (i.e. lead to predictable state s' so that H(a|s',s) is low). So one could think of the agent as trying to learn to have control of as much of the environment as possible, thus this objective has also been coined as "empowerment".

>	"Interestingly, the framework allows to also learn the state representation s as a function of some "raw" representation x of states."

>	"A major distinction with VIME is that empowerment doesn’t necessarily favor exploration - as stated by Mohamed and Rezende, agents are only ‘curious’ about parts of its environment that can be reached within its internal planning horizon."

  - `video` <https://youtube.com/watch?v=tMiiKXPirAQ> + <https://youtube.com/watch?v=LV5jYY-JFpE> (demo)
  - `video` <https://youtube.com/watch?v=WCE9hhPbCmc> + <https://youtube.com/watch?v=DpQKpSAMauY> (Kretov) `in russian`
  - `notes` <http://www.shortscience.org/paper?bibtexKey=conf/nips/MohamedR15>


#### ["Variational Intrinsic Control"](http://arxiv.org/abs/1611.07507) Gregor, Rezende, Wierstra
>	"In this paper we introduce a new unsupervised reinforcement learning method for discovering the set of intrinsic options available to an agent. This set is learned by maximizing the number of different states an agent can reliably reach, as measured by the mutual information between the set of options and option termination states. To this end, we instantiate two policy gradient based algorithms, one that creates an explicit embedding space of options and one that represents options implicitly. The algorithms also provide an explicit measure of empowerment in a given state that can be used by an empowerment maximizing agent. The algorithm scales well with function approximation and we demonstrate the applicability of the algorithm on a range of tasks."

>	"The second scenario is that in which the long-term goal of the agent is to get to a state with a maximal set of available intrinsic options – the objective of empowerment (Salge et al., 2014). This set of options consists of those that the agent knows how to use. Note that this is not the theoretical set of all options: it is of no use to the agent that it is possible to do something if it is unable to learn how  to do it. Thus, to maximize empowerment, the agent needs to simultaneously learn how to control the environment as well – it needs to discover the options available to it. The agent should in fact not aim for states where it has the most control according to its current abilities, but for states where it expects it will achieve the most control after learning. Being able to learn available options is thus fundamental to  becoming empowered."

>	"Let us compare this to the commonly used intrinsic motivation objective of maximizing the amount of model-learning progress, measured as the difference in compression of its experience before and after learning (Schmidhuber, 1991; 2010; Bellemare et al., 2016; Houthooft et al., 2016). The empowerment objective differs from this in a fundamental manner: the primary goal is not to understand or predict the observations but to control the environment. This is an important point – agents can often control an environment perfectly well without much understanding, as exemplified by canonical model-free reinforcement learning algorithms, where agents only model action-conditioned expected returns. Focusing on such understanding might significantly distract and impair the agent, as such reducing the control it achieves."

----
>	"Instead of curiosity, agent can be motivated by empowerment - attempt to maximize mutual information between the agent's actions and the consequences of its actions, i.e. state the actions will lead to. One way to do it is to classify the high level 'option' that determined the actions from the final state, while keeping the option's entropy high (contrastive estimation)."

  - `video` <https://youtu.be/DSYzHPW26Ig?t=2h9m23s> (Graves)
  - `video` <https://facebook.com/icml.imls/videos/2265408103721327?t=5749> (Abbeel)



---
### interesting papers - exploration and intrinsic motivation - predictive models - predictive novelty motivation

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----
#### ["Curiosity-driven Exploration by Self-supervised Prediction"](https://arxiv.org/abs/1705.05363) Pathak, Agrawal, Efros, Darrell
  `ICM` `prediction error`
>	"In many real-world scenarios, rewards extrinsic to the agent are extremely sparse, or absent altogether. In such cases, curiosity can serve as an intrinsic reward signal to enable the agent to explore its environment and learn skills that might be useful later in its life. We formulate curiosity as the error in an agent's ability to predict the consequence of its own actions in a visual feature space learned by a self-supervised inverse dynamics model. Our formulation scales to high-dimensional continuous state spaces like images, bypasses the difficulties of directly predicting pixels, and, critically, ignores the aspects of the environment that cannot affect the agent. The proposed approach is evaluated in two environments: VizDoom and Super Mario Bros. Three broad settings are investigated: 1) sparse extrinsic reward, where curiosity allows for far fewer interactions with the environment to reach the goal; 2) exploration with no extrinsic reward, where curiosity pushes the agent to explore more efficiently; and 3) generalization to unseen scenarios (e.g. new levels of the same game) where the knowledge gained from earlier experience helps the agent explore new places much faster than starting from scratch."

>	"Our main contribution is in designing an intrinsic reward signal based on prediction error of the agent’s knowledge about its environment that scales to high-dimensional continuous state spaces like images, bypasses the hard problem of predicting pixels and is unaffected by the unpredictable aspects of the environment that do not affect the agent."

>	"Adding representation network able to filter out information from the observed state that is not relevant to predict how the agent actions affect the future state."

>	"Using inverse models to avoid learning anything that the agent cannot control to reduce risk and using prediction error in the latent space to perform reactive exploration."

  - `post` <https://pathak22.github.io/noreward-rl/index.html> (demo)
  - `video` <https://vimeo.com/237270588> (Pathak)
  - `video` <https://facebook.com/icml.imls/videos/2265408103721327?t=4865> (Abbeel)
  - `video` <https://youtube.com/watch?v=_Z9ZP1eiKsI> (Kilcher)
  - `video` <https://youtu.be/RwLTrQUyDvA?t=18m2s> (Diaz Rodriguez)
  - `video` <https://youtu.be/qvxgsxQFHgQ?t=55m6s> (Ivanov) `in russian`
  - `post` <https://navneet-nmk.github.io/2018-08-10-first-post>
  - `code` <https://github.com/pathak22/noreward-rl>
  - `code` <https://github.com/navneet-nmk/pytorch-rl/blob/master/models/CuriosityDrivenExploration.py>
  - `paper` [**"On Bonus Based Exploration Methods In The Arcade Learning Environment"**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#on-bonus-based-exploration-methods-in-the-arcade-learning-environment-taiga-fedus-machado-courville-bellemare) by Taiga et al. `summary`


#### ["Learning to Play with Intrinsically-Motivated Self-Aware Agents"](https://arxiv.org/abs/1802.07442) Haber, Mrowca, Fei-Fei, Yamins
  `prediction error`
>	"Infants are experts at playing, with an amazing ability to generate novel structured behaviors in unstructured environments that lack clear extrinsic reward signals. We seek to mathematically formalize these abilities using a neural network that implements curiosity-driven intrinsic motivation. Using a simple but ecologically naturalistic simulated environment in which an agent can move and interact with objects it sees, we propose a "world-model" network that learns to predict the dynamic consequences of the agent's actions. Simultaneously, we train a separate explicit "self-model" that allows the agent to track the error map of its own world-model, and then uses the self-model to adversarially challenge the developing world-model. We demonstrate that this policy causes the agent to explore novel and informative interactions with its environment, leading to the generation of a spectrum of complex behaviors, including ego-motion prediction, object attention, and object gathering. Moreover, the world-model that the agent learns supports improved performance on object dynamics prediction, detection, localization and recognition tasks."

  - `video` <https://youtu.be/qvxgsxQFHgQ?t=47m46s> (Ivanov) `in russian`


#### ["Large-Scale Study of Curiosity-Driven Learning"](https://arxiv.org/abs/1808.04355) Burda, Edwards, Pathak, Storkey, Darrell, Efros
  `prediction error`
>	"Reinforcement learning algorithms rely on carefully engineering environment rewards that are extrinsic to the agent. However, annotating each environment with hand-designed, dense rewards is not scalable, motivating the need for developing reward functions that are intrinsic to the agent. Curiosity is a type of intrinsic reward function which uses prediction error as reward signal. In this paper: (a) We perform the first large-scale study of purely curiosity-driven learning, i.e. without any extrinsic rewards, across 54 standard benchmark environments, including the Atari game suite. Our results show surprisingly good performance, and a high degree of alignment between the intrinsic curiosity objective and the hand-designed extrinsic rewards of many game environments. (b) We investigate the effect of using different feature spaces for computing prediction error and show that random features are sufficient for many popular RL game benchmarks, but learned features appear to generalize better (e.g. to novel game levels in Super Mario Bros.). (c) We demonstrate limitations of the prediction-based rewards in stochastic setups."

  - <https://pathak22.github.io/large-scale-curiosity>
  - `video` <https://youtube.com/watch?v=l1FqtAHfJLI>
  - `video` <https://youtu.be/8NR6euSDfsM?t=9m4s> (Darrell)
  - `video` <https://vk.com/video-44016343_456240849> (Efros)
  - `video` <https://slideslive.com/38909803/tutorial-on-comparing-intrinsic-motivations-in-a-unified-framework> (1:29:06) (Biehl)
  - `video` <https://youtu.be/qvxgsxQFHgQ?t=59m45s> (Ivanov) `in russian`
  - `video` <https://youtu.be/EMv1AVLOnto?t=19m42s> (Svidchenko) `in russian`
  - `code` <https://github.com/openai/large-scale-curiosity>
  - `paper` ["Curiosity-driven Exploration by Self-supervised Prediction"](#large-scale-study-of-curiosity-driven-learning-burda-edwards-pathak-storkey-darrell-efros) by Burda et al. `summary`
  - `paper` [**"On Bonus Based Exploration Methods In The Arcade Learning Environment"**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#on-bonus-based-exploration-methods-in-the-arcade-learning-environment-taiga-fedus-machado-courville-bellemare) by Taiga et al. `summary`


#### ["Exploration by Random Network Distillation"](https://arxiv.org/abs/1810.12894) Burda, Edwards, Storkey, Klimov
  `RND` `prediction error`
>	"We introduce an exploration bonus for deep reinforcement learning methods that is easy to implement and adds minimal overhead to the computation performed. The bonus is the error of a neural network predicting features of the observations given by a fixed randomly initialized neural network. We also introduce a method to flexibly combine intrinsic and extrinsic rewards. We find that the random network distillation bonus combined with this increased flexibility enables significant progress on several hard exploration Atari games. In particular we establish state of the art performance on Montezuma’s Revenge, a game famously difficult for deep reinforcement learning methods. To the best of our knowledge, this is the first method that achieves better than average human performance on this game without using demonstrations or having access to the underlying state of the game, and occasionally completes the first level."

>	"In general, prediction errors can be attributed to a number of factors:  
>	1. Amount of training data. Prediction error is high where few similar examples were seen by the predictor (epistemic uncertainty).  
>	2. Stochasticity. Prediction error is high because the target function is stochastic (aleatoric uncertainty). Stochastic transitions are a source of such error for forward dynamics prediction.  
>	3. Model misspecification. Prediction error is high because necessary information is missing, or the model class is too limited to fit the complexity of the target function.  
>	4. Learning dynamics. Prediction error is high because the optimization process fails to find a predictor in the model class that best approximates the target function.  
>	Factor 1 is what allows one to use prediction error as an exploration bonus. In practice the prediction error is caused by a combination of all of these factors, not all of them desirable. For instance if the prediction problem is forward dynamics, then factor 2 results in the ‘noisy-TV’ problem. This is the thought experiment where an agent that is rewarded for errors in the prediction of its forward dynamics model gets attracted to local sources of entropy in the environment. A TV showing white noise would be such an attractor, as would a coin flip.  
>	To avoid the undesirable factors 2 and 3, methods such as those by Schmidhuber (1991a); Oudeyer et al. (2007); Lopes et al. (2012); Achiam & Sastry (2017) instead use a measurement of how much the prediction model improves upon seeing a new datapoint. However these approaches tend to be computationally expensive and hence difficult to scale.  
>	RND obviates factors 2 and 3 since the target network can be chosen to be deterministic and inside the model-class of the predictor network."  
  - `post` <https://blog.openai.com/reinforcement-learning-with-prediction-based-rewards> (demo)
  - `video` <https://youtu.be/ElyFDUab30A?t=17m37s> (Sutskever)
  - `video` <https://youtu.be/X-B3nAN7YRM?t=7m8s> (Sutskever)
  - `video` <https://youtu.be/qvxgsxQFHgQ?t=19m27s> (Ivanov) `in russian`
  - `video` <https://youtu.be/EMv1AVLOnto?t=17m44s> (Svidchenko) `in russian`
  - `code` <https://github.com/openai/random-network-distillation>
  - `paper` [**"On Bonus Based Exploration Methods In The Arcade Learning Environment"**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#on-bonus-based-exploration-methods-in-the-arcade-learning-environment-taiga-fedus-machado-courville-bellemare) by Taiga et al. `summary`


#### ["Self-Supervised Exploration via Disagreement"](https://arxiv.org/abs/1906.04161) Pathak, Gandhi, Gupta
  `prediction error variance` `ICML 2019`
>	"Efficient exploration is a long-standing problem in sensorimotor learning. Major advances have been demonstrated in noise-free, non-stochastic domains such as video games and simulation. However, most of these formulations either get stuck in environments with stochastic dynamics or are too inefficient to be scalable to real robotics setups. In this paper, we propose a formulation for exploration inspired by the work in active learning literature. Specifically, we train an ensemble of dynamics models and incentivize the agent to explore such that the disagreement of those ensembles is maximized. This allows the agentto learn skills by exploring in a self-supervised manner without any external reward. Notably, we further leverage the disagreement objective to optimize the agent’s policy in a differentiable manner, without using reinforcement learning, which results in a sample-efficient exploration. We demonstrate the efficacy of this formulation across a variety of benchmark environments including stochastic-Atari, Mujoco and Unity. Finally, we implement our differentiable exploration on a real robot which learns to interact with objects completely from scratch."

----
>	"similar to SOTA methods in determinstic environments but does not get stuck in stochastic scenarios (TV with remote)"

  - <https://pathak22.github.io/exploration-by-disagreement>
  - `video` <https://facebook.com/icml.imls/videos/355035025132741?t=4611> (Pathak)
  - `code` <https://github.com/pathak22/exploration-by-disagreement>



---
### interesting papers - exploration and intrinsic motivation - predictive models - learning progress motivation

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----
#### ["Automated Curriculum Learning for Neural Networks"](https://arxiv.org/abs/1704.03003) Graves, Bellemare, Menick, Munos, Kavukcuoglu
>	"We introduce a method for automatically selecting the path, or syllabus, that a neural network follows through a curriculum so as to maximise learning efficiency. A measure of the amount that the network learns from each data sample is provided as a reward signal to a nonstationary multi-armed bandit algorithm, which then determines a stochastic syllabus. We consider a range of signals derived from two distinct indicators of learning progress: rate of increase in prediction accuracy, and rate of increase in network complexity. Experimental results for LSTM networks on three curricula demonstrate that our approach can significantly accelerate learning, in some cases halving the time required to attain a satisfactory performance level."

>	"We focus on variants of prediction gain, and also introduce a novel class of progress signals which we refer to as complexity gain. Derived from minimum description length principles, complexity gain equates acquisition of knowledge with an increase in effective information encoded in the network weights."  

>	"VIME uses a reward signal that is closely related to variational complexity gain. The difference is that while VIME measures the KL between the posterior before and after a step in parameter space, we consider the change in KL between the posterior and prior induced by the step. Therefore, while VIME looks for any change to the posterior, we focus only on changes that alter the divergence from the prior. Further research will be needed to assess the relative merits of the two signals."  

>	"For maximum likelihood training, we found prediction gain to be the most consistent signal, while for variational inference training, gradient variational complexity gain performed best. Importantly, both are instantaneous, in the sense that they can be evaluated using only the samples used for training."  

>	"Complexity gain: maximize increase in complexity of (regularized) predictive model. Assumes a parsimonious model will only increase complexity if it discovers a meaningful regularity."

  - `video` <https://youtu.be/-u32TOPGIbQ?t=2m43s> (Graves)
  - `video` <https://youtu.be/DSYzHPW26Ig?t=2h3m37s> (Graves)
  - `video` <https://vimeo.com/237275086> (Bellemare)
  - `notes` <https://blog.tomrochette.com/machine-learning/papers/alex-graves-automated-curriculum-learning-for-neural-networks>
  - `post` <https://lilianweng.github.io/lil-log/2020/01/29/curriculum-for-reinforcement-learning.html>



---
### interesting papers - exploration and intrinsic motivation - predictive models - predictive familiarity motivation


#### ["SMiRL: Surprise Minimizing RL in Dynamic Environments"](https://arxiv.org/abs/1912.05510) Berseth et al.
  `SMiRL` `homeostasis`
>	"All living organisms struggle against the forces of nature to carve out a maintainable niche. We propose that such a search for order amidst chaos might offer a unifying principle for the emergence of useful behaviors in artificial agents. We formalize this idea into an unsupervised reinforcement learning method called Surprise Minimizing RL. SmiRL alternates between learning a density model to evaluate the surprise of a stimulus, and improving the policy to seek more predictable stimuli. This process maximizes a lower-bound on the negative entropy of the states, which can be seen as maximizing the agent's ability to maintain order in the environment. The policy seeks out stable and repeatable situations that counteract the environment's prevailing sources of entropy. This might include avoiding other hostile agents, or finding a stable, balanced pose for a bipedal robot in the face of disturbance forces. We demonstrate that our surprise minimizing agents can successfully play Tetris, Doom, control a humanoid to avoid falls, and navigate to escape enemies in a maze without any task-specific reward supervision. We further show that SMiRL can be used together with a standard task rewards to accelerate reward-driven learning."

----
>	"The key insight utilized by our method is that, in contrast to simple simulated domains, realistic environments exhibit dynamic phenomena that gradually increase entropy over time. An agent that resists this growth in entropy must take active and coordinated actions, thus learning increasingly complex behaviors. This is different from commonly proposed intrinsic exploration methods based on novelty, which instead seek to visit novel states and increase entropy. SMiRL holds promise for a new kind of unsupervised RL method that produces behaviors that are closely tied to the prevailing disruptive forces, adversaries, and other sources of entropy in the environment."

>	"While on the surface, SMiRL minimizes surprise and curiosity approaches like ICM maximize novelty, they are in fact not mutually incompatible. In particular, while ICM maximizes novelty with respect to a learned transition model, SMiRL minimizes surprise with respect to a learned state distribution. We can combine ICM and SMiRL to achieve even better results on the Treadmill environment."

  - <https://sites.google.com/view/surpriseminimization> (demo)
  - `post` <https://people.eecs.berkeley.edu/~gberseth/smirl-surprise-minimizing-rl-in-dynamic-environments.html>
  - `video` <http://www.fields.utoronto.ca/video-archive/2019/10/2509-21418> (36:15) (Levine)
  - `video` <https://youtu.be/U1dD8UALTu0?t=34m25s> (Levine)
  - `video` <https://youtu.be/qvxgsxQFHgQ?t=11m27s> (Ivanov) `in russian`



---
### interesting papers - exploration and intrinsic motivation - competence-based models - competence progress motivation

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---exploration-and-intrinsic-motivation)

----
#### ["Driven by Compression Progress: A Simple Principle Explains Essential Aspects of Subjective Beauty, Novelty, Surprise, Interestingness, Attention, Curiosity, Creativity, Art, Science, Music, Jokes"](http://arxiv.org/abs/0812.4360) Schmidhuber
  - <https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#driven-by-compression-progress-a-simple-principle-explains-essential-aspects-of-subjective-beauty-novelty-surprise-interestingness-attention-curiosity-creativity-art-science-music-jokes-schmidhuber>


#### ["Automated Curriculum Learning for Neural Networks"](https://arxiv.org/abs/1704.03003) Graves, Bellemare, Menick, Munos, Kavukcuoglu
  - <https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#automated-curriculum-learning-for-neural-networks-graves-bellemare-menick-munos-kavukcuoglu>


#### ["Automatic Goal Generation for Reinforcement Learning Agents"](https://arxiv.org/abs/1705.06366) Held, Geng, Florensa, Abbeel
>	"Reinforcement learning is a powerful technique to train an agent to perform a task. However, an agent that is trained using reinforcement learning is only capable of achieving the single task that is specified via its reward function. Such an approach does not scale well to settings in which an agent needs to perform a diverse set of tasks, such as navigating to varying positions in a room or moving objects to varying locations. Instead, we propose a method that allows an agent to automatically discover the range of tasks that it is capable of performing in its environment. We use a generator network to propose tasks for the agent to try to achieve, each task being specified as reaching a certain parametrized sub-set of the state-space. The generator network is optimized using adversarial training to produce tasks that are always at the appropriate level of difficulty for the agent. Our method thus automatically produces a curriculum of tasks for the agent to learn. We show that, by using this framework, an agent can efficiently and automatically learn to perform a wide set of tasks without requiring any prior knowledge of its environment. Our method can also learn to achieve tasks with sparse rewards, which traditionally pose significant challenges."

  - <https://sites.google.com/view/goalgeneration4rl>
  - `video` <https://facebook.com/icml.imls/videos/429963197518201?t=2655> (Florensa)
  - `post` <https://lilianweng.github.io/lil-log/2020/01/29/curriculum-for-reinforcement-learning.html>



---
### interesting papers - hierarchical reinforcement learning

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---hierarchical)  
[**interesting recent papers - transfer**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---transfer)  

----
#### ["Why Does Hierarchy (Sometimes) Work So Well in Reinforcement Learning?"](https://arxiv.org/abs/1909.10618) Nachum, Tang, Lu, Gu, Lee, Levine
>	"Hierarchical reinforcement learning has demonstrated significant success at solving difficult reinforcement learning (RL) tasks. Previous works have motivated the use of hierarchy by appealing to a number of intuitive benefits, including learning over temporally extended transitions, exploring over temporally extended periods, and training and exploring in a more semantically meaningful action space, among others. However, in fully observed, Markovian settings, it is not immediately clear why hierarchical RL should provide benefits over standard "shallow" RL architectures. In this work, we isolate and evaluate the claimed benefits of hierarchical RL on a suite of tasks encompassing locomotion, navigation, and manipulation. Surprisingly, we find that most of the observed benefits of hierarchy can be attributed to improved exploration, as opposed to easier policy learning or imposed hierarchical structures. Given this insight, we present exploration techniques inspired by hierarchy that achieve performance competitive with hierarchical RL while at the same time being much simpler to use and implement."

>	"Makes sense, right?  
>	- Hierarchy is natural decomposition of many real-world tasks  
>	- Learning over longer temporal abstractions  
>	- Higher-level actions are more semantically meaningful  
>	Or does it?  
>	- Do any of these hypotheses on the benefit of hierarchy actually matter in practice?  
>	- Thought experiment: Almost all the practical successes of HRL are on Markovian environments. Theoretically, a shallow policy should be able to solve these without issue."  

  - `video` <https://slideslive.com/38922026/deep-reinforcement-learning-2?t=3192> (Nachum)
  - `video` <https://youtu.be/HZg4BgZGAi8?t=16m22s> (Sychev) `in russian`


#### ["Human-level Performance in First-person Multiplayer Games with Population-based Deep Reinforcement Learning"](https://arxiv.org/abs/1807.01281) Jaderberg et al.
  `FTW`
  - <https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#human-level-performance-in-first-person-multiplayer-games-with-population-based-deep-reinforcement-learning-jaderberg-et-al>


#### ["Stochastic Neural Networks for Hierarchical Reinforcement Learning"](https://arxiv.org/abs/1704.03012) Florensa, Duan, Abbeel
>	"Deep reinforcement learning has achieved many impressive results in recent years. However, many of the deep RL algorithms still employ naive exploration strategies, and they have been shown to perform poorly in tasks with sparse rewards, and/or with long horizons. To tackle these challenges, there are two common approaches. The first approach is to design a hierarchy over the actions, which would require domain-specific knowledge and careful hand-engineering. A different line of work utilizes domain-agnostic intrinsic rewards to guide exploration, which has been shown to be effective in tasks with sparse rewards. However, it is unclear how the knowledge of solving a task can be utilized for other tasks, leading to a high sample complexity overall for the entire collection of tasks. In this paper, we propose a general framework for learning useful skills in a pre-training environment, which can then be utilized in downstream tasks by training a high-level policy over these skills. To learn these skills, we use stochastic neural networks (SNNs) combined with a proxy reward, the design of which requires very minimal domain knowledge about the downstream tasks. Our experiments show that this combination is effective in learning a wide span of interpretable skills in a sample-efficient way, and, when used on downstream tasks, can significantly boost the learning performance uniformly across all these tasks."

>	"We propose a framework for learning a diverse set of skills using stochastic neural networks with minimum supervision, and utilize these skills in a hierarchical architecture to solve challenging tasks with sparse rewards. Our framework successfully combines two parts, firstly an unsupervised procedure to learn a large span of skills using proxy rewards and secondly a hierarchical structure that encapsulates the latter span of skills and allows to re-use them in future tasks. The span of skills learning can be greatly improved by using stochastic neural networks as policies and their additional expressiveness and multimodality. The bilinear integration and the mutual information bonus are key to consistently yield a wide, interpretable span of skills. As for the hierarchical structure, we demonstrate how drastically it can boost the exploration of an agent in a new environment and we demonstrate its relevance for solving complex tasks as mazes or gathering."

>	"One limitations of our current approach is the switching between skills for unstable agents, as reported in the Appendix D.2 for the “Ant” robot. There are multiple future directions to make our framework more robust to such challenging robots, like learning a transition policy or integrating switching in the pretrain task. Other limitations of our current approach are having fixed sub-policies and fixed switch time T during the training of downstream tasks. The first issue can be alleviated by introducing end-to-end training, for example using the new straight-through gradient estimators for Stochastic Computations Graphs with discrete latents (Jang et al., 2016; Maddison et al., 2016). The second issue is not critical for static tasks like the ones used here, as studied in Appendix C.3. But in case of becoming a bottleneck for more complex dynamic tasks, a termination policy could be learned by the Manager, similar to the option framework. Finally, we only used feedforward architectures and hence the decision of what skill to use next only depends on the observation at the moment of switching, not using any sensory information gathered while the previous skill was active. This limitation could be eliminated by introducing a recurrent architecture at the Manager level."

>	"Our SNN hierarchical approach outperforms state-of-the-art intrinsic motivation results like VIME (Houthooft et al., 2016)."

  - `video` <https://youtube.com/playlist?list=PLEbdzN4PXRGVB8NsPffxsBSOCcWFBMQx3> (demo)
  - `code` <https://github.com/florensacc/snn4hrl>


#### ["The Option-Critic Architecture"](http://arxiv.org/abs/1609.05140) Bacon, Harb, Precup
>	"Temporal abstraction is key to scaling up learning and planning in reinforcement learning. While planning with temporally extended actions is well understood, creating such abstractions autonomously from data has remained challenging. We tackle this problem in the framework of options. We derive policy gradient theorems for options and propose a new option-critic architecture capable of learning both the internal policies and the termination conditions of options, in tandem with the policy over options, and without the need to provide any additional rewards or subgoals. Experimental results in both discrete and continuous environments showcase the flexibility and efficiency of the framework."

>	"We developed a general, gradient-based approach for learning simultaneously the intra-option policies and termination conditions, as well as the policy over options, in order to optimize a performance objective for the task at hand. Our ALE experiments demonstrate successful end-to-end training of the options in the presence of nonlinear function approximation. As noted, our approach only requires specifying the number of options. However, if one wanted to use additional pseudo-rewards, the option-critic framework would easily accommodate it. The internal policies and termination function gradients would simply need to be taken with respect to the pseudo-rewards instead of the task reward. A simple instance of this idea, which we used in some of the experiments, is to use additional rewards to encourage options that are indeed temporally extended, by adding a penalty whenever a switching event occurs."

>	"Our approach can work seamlessly with any other heuristic for biasing the set of options towards some desirable property (e.g. compositionality or sparsity), as long as it can be expressed as an additive reward structure. However, as seen in the results, such biasing is not necessary to produce good results. The option-critic architecture relies on the policy gradient theorem, and as discussed in (Thomas 2014), the gradient estimators can be biased in the Qt discounted case. By introducing factors of the form γ^t Π i=1 [1 − βi] in our updates (Thomas 2014, eq (3)), it would be possible to obtain unbiased estimates. However, we do not recommend this approach, since the sample complexity of the unbiased estimators is generally too high and the biased estimators performed well in our experiments."

>	"Perhaps the biggest remaining limitation of our work is the assumption that all options apply everywhere. In the case of function approximation, a natural extension to initiation sets is to use a classifier over features, or some other form of function approximation. As a result, determining which options are allowed may have similar cost to evaluating a policy over options (unlike in the tabular setting, where options with sparse initiation sets lead to faster decisions). This is akin to eligibility traces, which are more expensive than using no trace in the tabular case, but have the same complexity with function approximation. If initiation sets are to be learned, the main constraint that needs to be added is that the options and the policy over them lead to an ergodic chain in the augmented state-option space. This can be expressed as a flow condition that links initiation sets with terminations. The precise description of this condition, as well as sparsity regularization for initiation sets, is left for future work."

----
>	"The Option-Critic provides a policy gradient for learning options in an end-to-end manner and leverages an augmented state space in order to do so."  
>	"The Option-Critic consists of two components: 1) each option should use primitive actions that are better, 2) find good termination conditions (lengthen when the option is good, terminate when it’s bad). A third term also encourages the meta-policy to take better options."  

  - `video` <https://youtube.com/watch?v=8r_EoYnPjGk> (Bacon)
  - `video` <https://vimeo.com/249559422> (Precup)
  - `video` <https://youtu.be/ARfpQzRCWT4?t=39m> (Nikishin)
  - `video` <https://youtube.com/watch?v=ID150Tl-MMw&t=56m55s> (Abbeel)
  - `slides` <http://pierrelucbacon.com/optioncritic-aaai2017-slides.pdf>
  - `poster` <http://pierrelucbacon.com/optioncriticposter.pdf>
  - `notes` <http://tsong.me/blog/option-critic/>
  - `code` <https://github.com/jeanharb/option_critic>


#### ["Universal Value Function Approximators"](http://jmlr.org/proceedings/papers/v37/schaul15.pdf) Schaul, Horgan, Gregor, Silver
>	"Value functions are a core component of reinforcement learning systems. The main idea is to construct a single function approximator V(s; θ) that estimates the long-term reward from any state s, using parameters θ. In this paper we introduce universal value function approximators V(s, g; θ) that generalise not just over states s but also over goals g. We develop an efficient technique for supervised learning of UVFAs, by factoring observed values into separate embedding vectors for state and goal, and then learning a mapping from s and g to these factored embedding vectors. We show how this technique may be incorporated into a reinforcement learning algorithm that updates the UVFA solely from observed rewards. Finally, we demonstrate that a UVFA can successfully generalise to previously unseen goals."

>	"Value functions may be used to represent knowledge beyond the agent’s overall goal. General value functions Vg(s) represent the utility of any state s in achieving a given goal g (e.g. a waypoint), represented by a pseudo-reward function that takes the place of the real rewards in the problem. Each such value function represents a chunk of knowledge about the environment: how to evaluate or control a specific aspect of the environment (e.g. progress toward a waypoint). A collection of general value functions provides a powerful form of knowledge representation that can be utilised in several ways. For example, the Horde architecture consists of a discrete set of value functions (‘demons’), all of which may be learnt simultaneously from a single stream of experience, by bootstrapping off-policy from successive value estimates. Each value function may also be used to generate a policy or option, for example by acting greedily with respect to the values, and terminating at goal states. Such a collection of options can be used to provide a temporally abstract action-space for learning or planning. Finally, a collection of value functions can be used as a predictive representation of state, where the predicted values themselves are used as a feature vector. In large problems, the value function is typically represented by a function approximator V(s, θ), such as a linear combination of features or a neural network with parameters θ. The function approximator exploits the structure in the state space to efficiently learn the value of observed states and generalise to the value of similar, unseen states. However, the goal space often contains just as much structure as the state space. Consider for example the case where the agent’s goal is described by a single desired state: it is clear that there is just as much similarity between the value of nearby goals as there is between the value of nearby states. Our main idea is to extend the idea of value function approximation to both states s and goals g, using a universal value function approximator V(s, g, θ). A sufficiently expressive function approximator can in principle identify and exploit structure across both s and g. By universal, we mean that the value function can generalise to any goal g in a set G of possible goals: for example a discrete set of goal states; their power set; a set of continuous goal regions; or a vector representation of arbitrary pseudo-reward functions. This UVFA effectively represents an infinite Horde of demons that summarizes a whole class of predictions in a single object. Any system that enumerates separate value functions and learns each individually (like the Horde) is hampered in its scalability, as it cannot take advantage of any shared structure (unless the demons share parameters). In contrast, UVFAs can exploit two kinds of structure between goals: similarity encoded a priori in the goal representations g, and the structure in the induced value functions discovered bottom-up. Also, the complexity of UVFA learning does not depend on the number of demons but on the inherent domain complexity. This complexity is larger than standard value function approximation, and representing a UVFA may require a rich function approximator such as a deep neural network. Learning a UVFA poses special challenges. In general, the agent will only see a small subset of possible combinations of states and goals (s, g), but we would like to generalise in several ways. Even in a supervised learning context, when the true value Vg(s) is provided, this is a challenging regression problem."

>	"On the Atari game of Ms Pacman, we then demonstrate that UVFAs can scale to larger visual input spaces and different types of goals, and show they generalize across policies for obtaining possible pellets."

>	"This paper has developed a universal approximator for goal-directed knowledge. We have demonstrated that our UVFA model is learnable either from supervised targets, or directly from real experience; and that it generalises effectively to unseen goals. We conclude by discussing several ways in which UVFAs may be used. First, UVFAs can be used for transfer learning to new tasks with the same dynamics but different goals. Specifically, the values V(s, g; θ) in a UVFA can be used to initialise a new, single value function Vg(s) for a new task with unseen goal g. We demonstrate that an agent which starts from transferred values in this fashion can learn to solve the new task g considerably faster than random value initialization. Second, generalized value functions can be used as features to represent state; this is a form of predictive representation. A UVFA compresses a large or infinite number of predictions into a short feature vector. Specifically, the state embedding φ(s) can be used as a feature vector that represents state s. Furthermore, the goal embedding φ(g) can be used as a separate feature vector that represents state g. These features can capture non-trivial structure in the domain. Third, a UVFA could be used to generate temporally abstract options. For any goal g a corresponding option may be constructed that acts (soft-)greedily with respect to V(s, g; θ) and terminates e.g. upon reaching g. The UVFA then effectively provides a universal option that represents (approximately) optimal behaviour towards any goal g∈ G. This in turn allows a hierarchical policy to choose any goal g∈ G as a temporally abstract action. Finally, a UVFA could also be used as a universal option model. Specifically, if pseudorewards are defined by goal achievement, then V(s, g; θ) approximates the (discounted) probability of reaching g from s, under a policy that tries to reach it."

  - `video` <http://videolectures.net/icml2015_schaul_universal_value/> (Schaul)
  - `slides` <http://schaul.site44.com/publications/uvfa-slides.pdf>



---
### interesting papers - model-based methods

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-based-methods)

----
####  ["Making the World Differentiable: On Using Self-Supervised Fully Recurrent Neural Networks for Dynamic Reinforcement Learning and Planning in Non-Stationary Environments"](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.5472) Schmidhuber
  `1990`
>	"First a brief introduction to reinforcement learning and to supervised learning with recurrent networks in non-stationary environments is given. The introduction also covers the basic principle of gradient descent through frozen model networks as employed by Werbos, Jordan, Munro, Robinson and Fallside, and Nguyen and Widrouw. This principle allows supervised learning techniques to be employed for reinforcement learning. Then a general algorithm for a reinforcement learning neural network with internal and external feedback in a non-stationary reactive environment is described. Internal feedback is given by connections that allow cyclic activation flow through the network. External feedback is given by output actions that may change the state of the environment thus influencing subsequent input activations. The network's main goal is to receive as much reinforcement (or as little 'pain') as possible. In theory, arbitrary time lags between actions and ulterior consequences are possible. The 'visible' environment may be 'non-Markovian'. Although the approach is based on 'supervised' learning algorithms for fully recurrent dynamic networks, no teacher is required. An adaptive model of the environmental dynamics is constructed which includes a model of future reinforcement to be received. This model is used for learning goal directed behavior. The algorithm may concurrently learn the model and learn to pursue the main goal. To attack certain problems with the parallel version of the algorithm, 'adaptive randomness' is introduced. The algorithm is applied to a reinforcement learning task in a non-Markovian environment. A connection to 'meta-learning' {learning how to learn} is noted. An extension of the algorithm is described which includes a vector-valued adaptive critic element (based on Sutton's TD-methods). The possibility of using the model for learning by planning (by 'mental simulation' of the environmental dynamics) is investigated. Finally it is described how the algorithm can be augmented by dynamic curiosity and boredom. This can be done by introducing (delayed) reinforcement for controller actions that increase the model network's knowledge about the world. This in turn requires the model network to model its own ignorance, thus showing a rudimentary form of introspective behavior."

  - `paper` ["An On-Line Algorithm for Dynamic Reinforcement Learning and Planning in Reactive Environments"](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.45.1868) by Schmidhuber
  - `paper` ["Reinforcement Learning in Markovian and Non-Markovian Environments"](http://papers.nips.cc/paper/393-reinforcement-learning-in-markovian-and-non-markovian-environments) by Schmidhuber


#### ["On Learning to Think: Algorithmic Information Theory for Novel Combinations of Reinforcement Learning Controllers and Recurrent Neural World Models"](http://arxiv.org/abs/1511.09249) Schmidhuber
  - <https://github.com/brylevkirill/notes/blob/master/Artificial%20Intelligence.md#on-learning-to-think-algorithmic-information-theory-for-novel-combinations-of-reinforcement-learning-controllers-and-recurrent-neural-world-models-schmidhuber>


#### ["World Models"](https://arxiv.org/abs/1803.10122) Ha, Schmidhuber
>	"We explore building generative neural network models of popular reinforcement learning environments. Our world model can be trained quickly in an unsupervised manner to learn a compressed spatial and temporal representation of the environment. By using features extracted from the world model as inputs to an agent, we can train a very compact and simple policy that can solve the required task. We can even train our agent entirely inside of its own hallucinated dream generated by its world model, and transfer this policy back into the actual environment."

>	"Like early RNN-based C–M systems, ours simulates possible futures time step by time step, without profiting from human-like hierarchical planning or abstract reasoning, which often ignores irrelevant spatial-temporal details. However, the more general Learning To Think (Schmidhuber, 2015a) approach is not limited to this rather naive approach. Instead it allows a recurrent C to learn to address subroutines of the recurrent M, and reuse them for problem solving in arbitrary computable ways, e.g., through hierarchical planning or other kinds of exploiting parts of M’s program-like weight matrix. A recent One Big Net (Schmidhuber, 2018) extension of the C–M approach collapses C and M into a single network, and uses PowerPlay-like (Schmidhuber, 2013; Srivastava et al.,2012) behavioural replay (where the behaviour of a teacher net is compressed into a student net (Schmidhuber, 1992)) to avoid forgetting old prediction and control skills when learning new ones."

  - <https://worldmodels.github.io>
  - `video` <https://youtube.com/watch?v=HzA8LRqhujk> (Ha)
  - `video` <https://youtu.be/Yvll3P1UW5k?t=34m20s> (Abbeel)
  - `video` <https://youtu.be/HRp6DH5M7Co?t=18m24s> (Abbeel)
  - `video` <https://youtube.com/watch?v=dPsXxLyqpfs> (Kilcher)
  - `video` <https://youtube.com/watch?v=0JxOpJd3w8w> (Svidchenko) `in russian`
  - `video` <https://youtu.be/qvxgsxQFHgQ?t=40m46s> (Ivanov) `in russian`
  - `post` <https://coherencedrivers.wordpress.com/2018/04/04/comment-on-world-models>
  - `paper` [**"Making the World Differentiable: On Using Self-Supervised Fully Recurrent Neural Networks for Dynamic Reinforcement Learning and Planning in Non-Stationary Environments**"](#making-the-world-differentiable-on-using-self-supervised-fully-recurrent-neural-networks-for-dynamic-reinforcement-learning-and-planning-in-non-stationary-environments-schmidhuber) by Schmidhuber `summary`


#### ["Benchmarking Model-Based Reinforcement Learning"](https://arxiv.org/abs/1907.02057) Wang et al.
>	"Model-based reinforcement learning is widely seen as having the potential to be significantly more sample efficient than model-free RL. However, research in model-based RL has not been very standardized. It is fairly common for authors to experiment with self-designed environments, and there are several separate lines of research, which are sometimes closed-sourced or not reproducible. Accordingly, it is an open question how these various existing MBRL algorithms perform relative to each other. To facilitate research in MBRL, in this paper we gather a wide collection of MBRL algorithms and propose over 18 benchmarking environments specially designed for MBRL. We benchmark these algorithms with unified problem settings, including noisy environments. Beyond cataloguing performance, we explore and unify the underlying algorithmic differences across MBRL algorithms. We characterize three key research challenges for future MBRL research: the dynamics bottleneck, the planning horizon dilemma, and the early-termination dilemma."

>	"We benchmark the performance of a wide collection of existing MBRL algorithms, evaluating their sample efficiency, asymptotic performance and robustness. Across this very substantial benchmarking, there is no clear consistent best MBRL algorithm, suggesting lots of opportunities for future work bringing together the strengths of different approaches."

>	"Benchmarked MBRL algorithms are divided into: 1) Dyna-style Algorithms (Model-Ensemble Trust-Region Policy Optimization (ME-TRPO)), Stochastic Lower Bound Optimization (SLBO), Model-Based Meta-Policy-Optimization ((MB-MPO)), 2) Policy Search with Backpropagation through Time (Probabilistic Inference for Learning Control (PILCO), Iterative Linear Quadratic-Gaussian (iLQG), Guided Policy Search (GPS), Stochastic Value Gradients (SVG)), and 3) Shooting Algorithms (Random Shooting (RS), Mode-Free Model-Based (MB-MF), Probabilistic Ensembles with Trajectory Sampling (PETS))."

>	"In the Dyna algorithm, training iterates between two steps. First, using the current policy, data is gathered from interaction with the environment and then used to learn the dynamics model. Second, the policy is improved with imagined data generated by the learned model. This class of algorithms learn policies using model-free algorithms with rich imaginary experience without interaction with the real environment."  
>	"Contrary to Dyna-style algorithms, where the learned dynamics models are used to provide imagined data, policy search with backpropagation through time exploits the model derivatives. Consequently, these algorithms are able to compute the analytic gradient of the RL objective with respect to the policy, and improve the policy accordingly."  
>	"Shooting Algorithms provide a way to approximately solve the receding horizon problem posed in model predictive control when dealing with non-linear dynamics and non-convex reward functions. Their popularity has increased with the use of neural networks for modelling dynamics."  

>	"Based on the empirical evaluation, we propose three main causes that stagnate the performance of model-based methods: 1) Dynamics bottleneck: algorithms with learned dynamics are stuck at performance local minima significantly worse than using ground-truth dynamics, i.e. the performance does not increase when more data is collected. 2) Planning horizon dilemma: while increasing the planning horizon provides more accurate reward estimation, it can result in performance drops due to the curse of dimensionality and modelling errors. 3) Early termination dilemma: early termination is commonly used in MFRL for more directed exploration, to achieve faster learning. However, similar performance gain are not yet observed in MBRL algorithms, which limits their effectiveness in complex environments."

  - <http://www.cs.toronto.edu/~tingwuwang/mbrl.html>


#### ["Mastering Atari, Go, Chess and Shogi by Planning with a Learned Model"](https://arxiv.org/abs/1911.08265) Schrittwieser et al.
  `MuZero` `learning to plan` `learning abstract environment model`
  - <https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#mastering-atari-go-chess-and-shogi-by-planning-with-a-learned-model-schrittwieser-et-al>


#### ["Value Prediction Network"](https://arxiv.org/abs/1707.03497) Oh, Singh, Lee
  `VPN` `learning to plan` `learning abstract environment model`
>	"This paper proposes a novel deep reinforcement learning architecture, called Value Prediction Network, which integrates model-free and model-based RL methods into a single neural network. In contrast to typical model-based RL methods, VPN learns a dynamics model whose abstract states are trained to make option-conditional predictions of future values (discounted sum of rewards) rather than of future observations. Our experimental results show that VPN has several advantages over both model-free and model-based baselines in a stochastic environment where careful planning is required but building an accurate observation-prediction model is difficult. Furthermore, VPN outperforms Deep Q-Network on several Atari games even with short-lookahead planning, demonstrating its potential as a new way of learning a good state representation."

>	"VPN learns an MDP model grounded in real actions; the unrolled MDP is trained such that the cumulative sum of rewards, conditioned on the actual sequence of actions generated by a simple lookahead search, matches the real environment."

>	"VPN combines model-based RL (i.e., learning the dynamics of an abstract state space sufficient for computing future rewards and values) and model-free RL (i.e., mapping the learned abstract states to rewards and values) in a unified framework. In order to train a VPN, we propose a combination of temporal-difference search (TD search) and n-step Q-learning. In brief, VPNs learn to predict values via Q-learning and rewards via supervised learning. At the same time, VPNs perform lookahead planning to choose actions and compute bootstrapped target Q-values."

>	"Extends the Predictron model from policy evaluation to optimal control."

>	"Uses the model to construct a look-ahead tree only when constructing bootstrap targets and selecting actions, similarly to TD-search. Crucially, the model is not embedded in a planning algorithm during optimisation."

  - `video` <http://videolectures.net/deeplearning2017_singh_reinforcement_learning/#t=4366> (Singh)
  - `video` <https://facebook.com/icml.imls/videos/2366831430268790?t=1814> (Silver)
  - `video` <https://youtu.be/PRQ8-FwDPRE?t=16m> (Holland)
  - `video` <https://youtu.be/RwLTrQUyDvA?t=14m58s> (Diaz Rodriguez)
  - `notes` <https://www.shortscience.org/paper?bibtexKey=journals/corr/OhSL17>
  - `notes` <https://medium.com/arxiv-bytes/summary-value-prediction-networks-vpn-474c0b080b2a>


#### ["The Predictron: End-to-End Learning and Planning"](https://arxiv.org/abs/1612.08810) Silver et al.
  `Predictron` `learning to plan` `learning abstract environment model`
>	"One of the key challenges of artificial intelligence is to learn models that are effective in the context of planning. In this document we introduce the predictron architecture. The predictron consists of a fully abstract model, represented by a Markov reward process, that can be rolled forward multiple "imagined" planning steps. Each forward pass of the predictron accumulates internal rewards and values over multiple planning depths. The predictron is trained end-to-end so as to make these accumulated values accurately approximate the true value function. We applied the predictron to procedurally generated random mazes and a simulator for the game of pool. The predictron yielded significantly more accurate predictions than conventional deep neural network architectures."

>	"The Predictron consists of a fully abstract model, represented by a Markov reward process, that can be rolled forward multiple “imagined" planning steps. Each forward pass of the predictron accumulates internal rewards and values over multiple planning depths. The predictron is trained end-to-end so as to make these accumulated values accurately approximate the true value function."

>	"The Predictron is a quite different approach to model-based RL which focuses end-to-end on predicting the value function. The main idea of these methods is to construct an abstract MDP model such that planning in the abstract MDP is equivalent to planning in the real environment. This equivalence is achieved by ensuring value equivalence, i.e. that, starting from the same real state, the cumulative reward of a trajectory through the abstract MDP matches the cumulative reward of a trajectory in the real environment. The Predictron first introduced value equivalent models for predicting value (without actions). Although the underlying model still takes the form of an MDP, there is no requirement for its transition model to match real states in the environment. Instead the MDP model is viewed as a hidden layer of a deep neural network. The unrolled MDP is trained such that the expected cumulative sum of rewards matches the expected value with respect to the real environment, e.g. by temporal-difference learning."

>	"Trains deep network to implicitly plan via iterative rollouts."  
>	"Uses implicit environment model which does not capture dynamics."  
>	"Aims at learning Markov reward process rather than solving MDP."  

  - `video` <https://youtube.com/watch?v=BeaLdaN2C3Q> (demo)
  - `video` <https://facebook.com/icml.imls/videos/2366831430268790?t=410> (Silver)
  - `video` <https://vimeo.com/238243832> (Hasselt)
  - `video` <https://youtube.com/watch?v=ID150Tl-MMw&t=55m9s> (Abbeel)
  - `video` <https://youtu.be/bsuvM1jO-4w?t=38m6s> (Mnih)
  - `video` <http://videolectures.net/deeplearning2017_singh_reinforcement_learning/#t=4366> (Singh)
  - `code` <https://github.com/zhongwen/predictron>
  - `code` <https://github.com/muupan/predictron>


#### ["Value Iteration Networks"](http://arxiv.org/abs/1602.02867) Tamar, Wu, Thomas, Levine, Abbeel
  `VIN` `learning to plan` `learning abstract environment model`
>	"We introduce the value iteration network (VIN): a fully differentiable neural network with a ‘planning module’ embedded within. VINs can learn to plan, and are suitable for predicting outcomes that involve planning-based reasoning, such as policies for reinforcement learning. Key to our approach is a novel differentiable approximation of the value-iteration algorithm, which can be represented as a convolutional neural network, and trained end-to-end using standard backpropagation. We evaluate VIN based policies on discrete and continuous path-planning domains, and on a natural-language based search task. We show that by learning an explicit planning computation, VIN policies generalize better to new, unseen domains."

>	"The introduction of powerful and scalable RL methods has opened up a range of new problems for deep learning. However, few recent works investigate policy architectures that are specifically tailored for planning under uncertainty, and current RL theory and benchmarks rarely investigate the generalization properties of a trained policy. This work takes a step in this direction, by exploring better generalizing policy representations. Our VIN policies learn an approximate planning computation relevant for solving the task, and we have shown that such a computation leads to better generalization in a diverse set of tasks, ranging from simple gridworlds that are amenable to value iteration, to continuous control, and even to navigation of Wikipedia links. In future work we intend to learn different planning computations, based on simulation, or optimal linear control, and combine them with reactive policies, to potentially develop RL solutions for task and motion planning"

>	"In our experiment in continuous control we used hierarchical policy: high-level policy solved low-resolution map and low-level policy executed it. This is very different from options/skills framework. There is one smooth policy that implements everything. We don't need to learn initiation sets or termination sets. But more importantly, the motivation for using hierarchy here was different. The motivation wasn't to increase learning rate or exploration - the motivation was to generalize. We understood that low-resolution map is sufficient for doing planning which promotes generalization, but low-level policy uses the fact that dynamics is similar across different tasks."

----
>	"Its contribution is to offer a new way to think about value iteration in the context of deep networks. It shows how the CNN architecture can be hijacked to implement the Bellman optimality operator, and how the backprop signal can be used to learn a deterministic model of the underlying MDP."

>	"Value iteration is similar enough to a sequence of convolutions and max-pooling layers that you can emulate an (unrolled) planning computation with a deep network. This allows neural nets to do planning, e.g. moving from start to goal in grid-world, or navigating a website to find query."

----
>	"The value function V_{n}(s') takes the place of the input to the layer, while P(s'|s,a) form the weights of |A| convolution channels. In many tasks of interest such as grid world navigation, P(s'|s,a) reflects the locality of the problem since transitions are only possible to nearby states. This is analogous to the locality of convolutional kernels in standard CNNs, which is useful due to the hierarchical structure in natural images. Due to this connection, value iteration can be performed by a differentiable Value Iteration block that is composed of recursively connecting K such convolutional blocks. One must then choose K in such a way as to ensure convergence while not incurring a high computational cost by setting it to be too large."

----
>	"Trains deep network to implicitly plan via iterative rollouts."  
>	"Uses implicit environment model which does not capture dynamics."  

  - `video` <https://youtu.be/ID150Tl-MMw?t=54m24s> (demo)
  - `video` <https://youtube.com/watch?v=tXBHfbHHlKc> (Tamar) ([slides](http://technion.ac.il/~danielm/icml_slides/Talk7.pdf))
  - `video` <https://channel9.msdn.com/Events/Neural-Information-Processing-Systems-Conference/Neural-Information-Processing-Systems-Conference-NIPS-2016/Value-Iteration-Networks> (Tamar)
  - `video` <http://www.fields.utoronto.ca/video-archive/2017/02/2267-16530> (31:50) (Abbeel)
  - `video` <https://youtu.be/bsuvM1jO-4w?t=38m6s> (Mnih)
  - `video` <https://facebook.com/icml.imls/videos/2366831430268790?t=2099> (Silver)
  - `notes` <https://github.com/karpathy/paper-notes/blob/master/vin.md>
  - `notes` <https://github.com/DanielTakeshi/Paper_Notes/blob/master/reinforcement_learning/Value_Iteration_Networks.md>
  - `notes` <https://blog.acolyer.org/2017/02/09/value-iteration-networks/>
  - `paper` ["Cognitive Mapping and Planning for Visual Navigation"](https://arxiv.org/abs/1702.03920) by Gupta et al.


#### ["Learning and Policy Search in Stochastic Dynamic Systems with Bayesian Neural Networks"](https://arxiv.org/abs/1605.07127) Depeweg, Hernandez-Lobato, Doshi-Velez, Udluft
>	"We present an algorithm for policy search in stochastic dynamical systems using model-based reinforcement learning. The system dynamics are described with Bayesian neural networks (BNNs) that include stochastic input variables. These input variables allow us to capture complex statistical patterns in the transition dynamics (e.g. multi-modality and heteroskedasticity), which are usually missed by alternative modeling approaches. After learning the dynamics, our BNNs are then fed into an algorithm that performs random roll-outs and uses stochastic optimization for policy learning. We train our BNNs by minimizing α-divergences with α = 0.5, which usually produces better results than other techniques such as variational Bayes. We illustrate the performance of our method by solving a challenging problem where model-based approaches usually fail and by obtaining promising results in real-world scenarios including the control of a gas turbine and an industrial benchmark."

>	"Proposed approach enables automatic identification of arbitrary stochastic patterns such as multimodality and heteroskedasticity, without having to manually incorporate these into the model."

>	"We have extended Bayesian neural network with addition of a random input noise source z. This enables principled Bayesian inference over complex stochastic functions. We have also presented an algorithm that uses random roll-outs and stochastic optimization for learning a parameterized policy in a batch scenario. Our BNNs with random inputs have allowed us to solve a challenging benchmark problem where model-based approaches usually fail."

>	"For safety, we believe having uncertainty over the underlying stochastic functions will allow us to optimize policies by focusing on worst case results instead of on average performance. For exploration, having uncertainty on the stochastic functions will be useful for efficient data collection."

>	"The optimal policy can be significantly affected by the noise present in the state transitions. This is illustrated by the drunken spider story, in which a spider has two possible paths to go home: either by crossing the bridge or by walking around the lake. In the absence of noise, the bridge option is prefered since it is shorter. However, after heavily drinking alcohol, the spider’s movements may randomly deviate left or right. Since the bridge is narrow, and spiders do not like swimming, the prefered trajectory is now to walk around the lake. The previous example shows how noise can significantly affect optimal control. For example, the optimal policy may change depending on whether the level of noise is high or low. Therefore, we expect to obtain significant improvements in model-based reinforcement learning by capturing with high accuracy any noise patterns present in the state transition data."

  - `post` <https://medium.com/towards-data-science/bayesian-neural-networks-with-random-inputs-for-model-based-reinforcement-learning-36606a9399b4> (Hernandez-Lobato)
  - `video` <https://youtube.com/watch?v=0H3EkUPENSY> (Hernandez-Lobato)
  - `video` <https://youtube.com/watch?v=J4KLWjZ1QVM> (Hernandez-Lobato)
  - `video` <https://youtu.be/AKcWQ_9aQSI?t=1h36m10s> (in russian)
  - `code` <https://github.com/siemens/policy_search_bb-alpha>


#### ["Action-Conditional Video Prediction using Deep Networks in Atari Games"](http://arxiv.org/abs/1507.08750) Oh, Guo, Lee, Lewis, Singh
  - <https://github.com/brylevkirill/notes/blob/master/Reinforcement%20Learning.md#action-conditional-video-prediction-using-deep-networks-in-atari-games-oh-guo-lee-lewis-singh>


#### ["Deep Learning for Real-Time Atari Game Play Using Offline Monte-Carlo Tree Search Planning"](https://papers.nips.cc/paper/5421-deep-learning-for-real-time-atari-game-play-using-offline-monte-carlo-tree-search-planning) Guo, Singh, Lee, Lewis, Wang
>	"The combination of modern Reinforcement Learning and Deep Learning approaches holds the promise of making significant progress on challenging applications requiring both rich perception and policy-selection. The Arcade Learning Environment provides a set of Atari games that represent a useful benchmark set of such applications. A recent breakthrough in combining model-free reinforcement learning with deep learning, called DQN, achieves the best realtime agents thus far. Planning-based approaches achieve far higher scores than the best model-free approaches, but they exploit information that is not available to human players, and they are orders of magnitude slower than needed for real-time play. Our main goal in this work is to build a better real-time Atari game playing agent than DQN. The central idea is to use the slow planning-based agents to provide training data for a deep-learning architecture capable of real-time play. We proposed new agents based on this idea and show that they outperform DQN."

----
>	"run planning algorithm on episodes to get dataset (screen, best action) + train CNN policy as classification task with cross entropy loss"  
>	"deterministic version of ALE"  
>	"Upper Confidence Bound 1 applied to trees (UCT) as planning algorithm"  
>	"DAGGER algorithm for data collection"  

  - `video` <https://youtube.com/watch?v=B3b6NLUxN3U> (Singh)
  - `video` <https://youtube.com/watch?v=igm38BakyAg> (Lee)
  - `video` <https://youtube.com/watch?v=mZtlW_xtarI&t=59m25s> (Levine)
  - `video` <https://youtu.be/ywzZJ4L32xc?t=6m39s> (Pavlov)



---
### interesting papers - value-based methods

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-free-methods)

----
#### ["Human-level Control Through Deep Reinforcement Learning"](https://goo.gl/jHRkZr) Mnih et al.
>	"The theory of reinforcement learning provides a normative account, deeply rooted in psychological and neuroscientific perspectives on animal behaviour, of how agents may optimize their control of an environment. To use reinforcement learning successfully in situations approaching real-world complexity, however, agents are confronted with a difficult task: they must derive efficient representations of the environment from high-dimensional sensory inputs, and use these to generalize past experience to new situations. Remarkably, humans and other animals seem to solve this problem through a harmonious combination of reinforcement learning and hierarchical sensory processing systems, the former evidenced by a wealth of neural data revealing notable parallels between the phasic signals emitted by dopaminergic neurons and temporal difference reinforcement learning algorithms. While reinforcement learning agents have achieved some successes in a variety of domains, their applicability has previously been limited to domains in which useful features can be handcrafted, or to domains with fully observed, low-dimensional state spaces. Here we use recent advances in training deep neural networks to develop a novel artificial agent, termed a deep Q-network, that can learn successful policies directly from high-dimensional sensory inputs using end-to-end reinforcement learning. We tested this agent on the challenging domain of classic Atari 2600 games. We demonstrate that the deep Q-network agent, receiving only the pixels and the game score as inputs, was able to surpass the performance of all previous algorithms and achieve a level comparable to that of a professional human games tester across a set of 49 games, using the same algorithm, network architecture and hyperparameters. This work bridges the divide between high-dimensional sensory inputs and actions, resulting in the first artificial agent that is capable of learning to excel at a diverse array of challenging tasks."

  - `video` <http://youtube.com/watch?v=re6hkcTWVUY> (demo)
  - `video` <http://youtube.com/watch?v=iqXKQf2BOSE> (demo)
  - `video` <http://youtube.com/watch?v=EfGD2qveGdQ> (demo)
  - `video` <http://youtube.com/user/eldubro/videos> (demo)
  - <http://cs.stanford.edu/people/karpathy/convnetjs/demo/rldemo.html> (demo)
  - `video` <https://youtube.com/watch?v=rFwQDDbYTm4> (Kilcher)
  - `video` <http://youtube.com/watch?v=fevMOp5TDQs> (Mnih)
  - `video` <http://youtube.com/watch?v=dV80NAlEins> (de Freitas)
  - `video` [from value function approximation to Deep Q-Network](http://youtu.be/UoPei5o4fps?t=1h9m) (Silver)
  - `video` [from Fitted Value Iteration to Deep Q-Network](http://videolectures.net/deeplearning2017_szepesvari_theory_of_rl/#t=2929) (Szepesvari)
  - `video` <https://youtube.com/watch?v=teDuLk3cIeI> + <https://youtube.com/watch?v=ugjjjtuVshY> (Pogrebnyakov)
  - `video` <https://yadi.sk/i/AHDU2p_j3FT3nr> + <https://yadi.sk/i/EeUeheri3FT3ra> (Ratnikov, Vasilev) `in russian`
  - `paper` <http://nature.com/nature/journal/v518/n7540/full/nature14236.html>
  - `paper` ["Playing Atari with Deep Reinforcement Learning"](https://arxiv.org/abs/1312.5602) by Mnih et al.


#### ["Dueling Network Architectures for Deep Reinforcement Learning"](http://arxiv.org/abs/1511.06581) Wang, Schaul, Hessel, van Hasselt, Lanctot, de Freitas
>	"In recent years there have been many successes of using deep representations in reinforcement learning. Still, many of these applications use conventional architectures, such as convolutional networks, LSTMs, or auto-encoders. In this paper, we present a new neural network architecture for model-free reinforcement learning. Our dueling network represents two separate estimators: one for the state value function and one for the state-dependent action advantage function. The main benefit of this factoring is to generalize learning across actions without imposing any change to the underlying reinforcement learning algorithm. Our results show that this architecture leads to better policy evaluation in the presence of many similar-valued actions. Moreover, the dueling architecture enables our RL agent to outperform the state-of-the-art on the Atari 2600 domain."

>	"The advantage of the dueling architecture lies partly in its ability to learn the state-value function efficiently. With every update of the Q values in the dueling architecture, the value stream V is updated – this contrasts with the updates in a single-stream architecture where only the value for one of the actions is updated, the values for all other actions remain untouched. This more frequent updating of the value stream in our approach allocates more resources to V, and thus allows for better approximation of the state values, which in turn need to be accurate for temporal difference-based methods like Q-learning to work. This phenomenon is reflected in the experiments, where the advantage of the dueling architecture over single-stream Q networks grows when the number of actions is large. Furthermore, the differences between Q-values for a given state are often very small relative to the magnitude of Q. For example, after training with DDQN on the game of Seaquest, the average action gap (the gap between the Q values of the best and the second best action in a given state) across visited states is roughly 0.04, whereas the average state value across those states is about 15. This difference in scales can lead to small amounts of noise in the updates which can lead to reorderings of the actions, and thus make the nearly greedy policy switch abruptly. The dueling architecture with its separate advantage stream is robust to such effects."

----
>	"In advantage learning one throws away information that is not needed for coming up with a good policy. The argument is that throwing away information allows you to focus your resources on learning what is important. As an example consider Tetris when you gain a unit reward for every time step you survive. Arguably the optimal value function takes on large values when the screen is near empty, while it takes on small values when the screen is near full. The range of differences can be enormous (from millions to zero). However, for optimal decision making how long you survive does not matter. What matters is the small differences in how the screen is filled up because this is what determines where to put the individual pieces. If you learn an action value function and your algorithm focuses on something like the mean square error, i.e., getting the magnitudes right, it is very plausible that most resources of the learning algorithm will be spent on capturing how big the values are, while little resource will be spent on capturing the value differences between the actions. This is what advantage learning can fix. The fix comes because advantage learning does not need to wait until the value magnitudes are properly captured before it can start learning the value differences. As can be seen from this example, advantage learning is expected to make a bigger difference where the span of optimal values is orders of magnitudes larger than action-value differences."

>	"Many recent developments blur the distinction between model and algorithm. This is profound - at least for someone with training in statistics. Ziyu Wang replaced the convnet of DQN and re-run exactly the same algorithm but with a different net (a slight modification of the old net with two streams which he calls the dueling architecture). That is, everything is the same, but only the representation (neural net) changed slightly to allow for computation of not only the Q function, but also the value and advantage functions. The simple modification resulted in a massive performance boost. For example, for the Seaquest game, DQN of the Nature paper scored 4,216 points, while the modified net of Ziyu leads to a score of 37,361 points. For comparison, the best human we have found scores 40,425 points. Importantly, many modifications of DQN only improve on the 4,216 score by a few hundred points, while the Ziyu's network change using the old vanilla DQN code and gradient clipping increases the score by nearly a factor of 10. I emphasize that what Ziyu did was he changed the network. He did not change the algorithm. However, the computations performed by the agent changed remarkably. Moreover, the modified net could be used by any other Q learning algorithm. RL people typically try to change equations and write new algorithms, instead here the thing that changed was the net. The equations are implicit in the network. One can either construct networks or play with equations to achieve similar goals."

  - `video` <https://youtube.com/watch?v=TpGuQaswaHs> + <https://youtube.com/watch?v=oNLITLfrvQY> (demo)
  - `video` <http://techtalks.tv/talks/dueling-network-architectures-for-deep-reinforcement-learning/62381/> (Wang)
  - `video` <https://youtu.be/fevMOp5TDQs?t=58m24s> (Mnih)
  - `video` <https://yadi.sk/i/yBO0q4mI3GAxYd> (56:26) (Fritzler) `in russian`
  - `video` <https://youtu.be/fnwo3GCmyEo?t=37m50s> (Fritzler) `in russian`
  - `video` <https://youtu.be/mrgJ53TIcQc?t=35m4s> (Pavlov) `in russian`
  - `post` <http://torch.ch/blog/2016/04/30/dueling_dqn.html>
  - `code` <https://github.com/higgsfield/RL-Adventure/blob/master/3.dueling%20dqn.ipynb>
  - `code` <https://github.com/carpedm20/deep-rl-tensorflow>
  - `code` <https://github.com/Kaixhin/Atari>
  - `code` <https://github.com/tambetm/gymexperiments>


#### ["Deep Reinforcement Learning with Double Q-Learning"](http://arxiv.org/abs/1509.06461) van Hasselt, Guez, Silver
>	"The popular Q-learning algorithm is known to overestimate action values under certain conditions. It was not previously known whether, in practice, such overestimations are common, whether this harms performance, and whether they can generally be prevented. In this paper, we answer all these questions affirmatively. In particular, we first show that the recent DQN algorithm, which combines Q-learning with a deep neural network, suffers from substantial overestimations in some games in the Atari 2600 domain. We then show that the idea behind the Double Q-learning algorithm, which was introduced in a tabular setting, can be generalized to work with large-scale function approximation. We propose a specific adaptation to the DQN algorithm and show that the resulting algorithm not only reduces the observed overestimations, as hypothesized, but that this also leads to much better performance on several games."

>	"This paper has five contributions. First, we have shown why Q-learning can be overoptimistic in large-scale problems, even if these are deterministic, due to the inherent estimation errors of learning. Second, by analyzing the value estimates on Atari games we have shown that these overestimations are more common and severe in practice than previously acknowledged. Third, we have shown that Double Q-learning can be used at scale to successfully reduce this overoptimism, resulting in more stable and reliable learning. Fourth, we have proposed a specific implementation called Double DQN, that uses the existing architecture and deep neural network of the DQN algorithm without requiring additional networks or parameters. Finally, we have shown that Double DQN finds better policies, obtaining new state-of-the-art results on the Atari 2600 domain."

----
>	"On each step of Q-learning, the agent updates its action value estimates towards the observed reward and the estimated value of the maximal action in the next state. This target represents the highest value the agent thinks it could obtain from the current state and action, given the observed reward. Unfortunately, this simple update rule has been shown to suffer from overestimation bias. The agent updates with the maximum over action values might be large because an action’s value actually is high, or it can be misleadingly high simply because of the stochasticity or errors in the estimator. With many actions, there is a higher probability that one of the estimates is large simply due to stochasticity and the agent will overestimate the value. This issue is particularly problematic under function approximation, and can significantly impede the quality of the learned policy or even lead to failures of Q-learning."

>	"Double Q-learning is introduced to instead ensure underestimation bias. The idea of is to maintain two unbiased independent estimators of the action values. The expected action value of estimator one is selected for the maximal action from estimator two, which is guaranteed not to overestimate the true maximum action value. Double DQN has been shown to significantly improve performance over Q-learning. However, this is not a complete answer to this problem, because trading overestimation bias for underestimation bias is not always desirable."

  - `video` <https://youtu.be/qLaDWKd61Ig?t=32m52s> (Silver)
  - `video` <https://youtu.be/fevMOp5TDQs?t=53m42s> (Mnih)
  - `video` <https://youtube.com/watch?v=FTfkpCCaORI> (Rana)
  - `video` <https://yadi.sk/i/yBO0q4mI3GAxYd> (15:02) (Fritzler) `in russian`
  - `video` <https://youtu.be/fnwo3GCmyEo?t=18m54s> (Fritzler) `in russian`
  - `video` <https://youtu.be/mrgJ53TIcQc?t=17m31s> (Pavlov) `in russian`
  - `code` <https://github.com/higgsfield/RL-Adventure/blob/master/2.double%20dqn.ipynb>
  - `code` <https://github.com/carpedm20/deep-rl-tensorflow>
  - `code` <https://github.com/Kaixhin/Atari>


#### ["Prioritized Experience Replay"](http://arxiv.org/abs/1511.05952) Schaul, Quan, Antonoglou, Silver
>	"Experience replay lets online reinforcement learning agents remember and reuse experiences from the past. In prior work, experience transitions were uniformly sampled from a replay memory. However, this approach simply replays transitions at the same frequency that they were originally experienced, regardless of their significance. In this paper we develop a framework for prioritizing experience, so as to replay important transitions more frequently, and therefore learn more efficiently. We use prioritized experience replay in the Deep Q-Network algorithm, which achieved human-level performance in Atari games. DQN with prioritized experience replay achieves a new state-of-the-art, outperforming DQN with uniform replay on 42 out of 57 games."

>	"Online reinforcement learning agents incrementally update their parameters (of the policy, value function or model) while they observe a stream of experience. In their simplest form, they discard incoming data immediately, after a single update. Two issues with this are (a) strongly correlated updates that break the i.i.d. assumption of many popular stochastic gradient-based algorithms, and (b) the rapid forgetting of possibly rare experiences that would be useful later on. Experience replay a ddresses both of these issues: with experience stored in a replay memory, it becomes possible to break the temporal correlations by mixing more and less recent experience for the updates, and rare experience will be used for more than just a single update. DQN used a large sliding-window replay memory, sampled from it uniformly at random, and effectively revisited each transition eight times. In general, experience replay can reduce the amount of experience required to learn, and replace it with more computation and more memory – which are often cheaper resources than the RL agent’s interactions with its environment."

>	"In this paper, we investigate how prioritizing which transitions are replayed can make experience replay more efficient and effective than if all transitions are replayed uniformly. The key idea is that an RL agent can learn more effectively from some transitions than from others. Transitions may be more or less surprising, redundant, or task-relevant. Some transitions may not be immediately useful to the agent, but might become so when the agent competence increases (Schmidhuber, 1991). We propose to more frequently replay transitions with high expected learning progress, as measured by the magnitude of their temporal-difference error. This prioritization can lead to a loss of diversity, which we alleviate with stochastic prioritization, and introduce bias, which we correct with importance sampling."

>	"Using a replay memory leads to design choices at two levels: which experience to store and which to forget, and which experience to replay (and how to do so). This paper addresses only the latter: making the most effective use of the replay memory for learning, assuming that its contents are outside of our control."

>	"We find that adding prioritized replay to DQN leads to a substantial improvement in final score on 42 out of 57 games, with the median normalized performance score across 57 games increased from 69% to 97%. Furthermore, we find that the boost from prioritized experience replay is complementary to the one from introducing Double Q-learning into DQN: performance increases another notch, leading to the current state-of-the-art on the Atari benchmark. Compared to Double DQN, the mean performance increased from 389% to 551%, and the median performance from 110% to 128% bringing additional games such as River Raid, Seaquest and Surround to a human level for the first time, and making large jumps on others (e.g., Atlantis, Gopher, James Bond 007 or Space Invaders)."

>	"We stumbled upon another phenomenon (obvious in retrospect), namely that some fraction of the visited transitions are never replayed before they drop out of the sliding window memory, and many more are first replayed only a long time after they are encountered. Also, uniform sampling is implicitly biased toward out-of-date transitions that were generated by a policy that has typically seen hundreds of thousands of updates since. Prioritized replay with its bonus for unseen transitions directly corrects the first of these issues, and also tends to help with the second one, as more recent transitions tend to have larger error – this is because old transitions will have had more opportunities to have them corrected, and because novel data tends to be less well predicted by the value function."

>	"We hypothesize that deep neural networks interact with prioritized replay in another interesting way. When we distinguish learning the value given a representation (i.e., the top layers) from learning an improved representation (i.e., the bottom layers), then transitions for which the representation is good will quickly reduce their error and then be replayed much less, increasing the learning focus on others where the representation is poor, thus putting more resources into distinguishing aliased states – if the observations and network capacity allow for it."

>	"Feedback for Exploration: An interesting side-effect of prioritized replay is that the total number Mi that a transition will end up being replayed varies widely, and this gives a rough indication of how useful it was to the agent. This potentially valuable signal can be fed back to the exploration strategy that generates the transitions. For example, we could sample exploration hyper-parameters (such as the fraction of random actions, the Boltzmann temperature, or the amount of intrinsic reward to mix in) from a parameterized distribution at the beginning of each episode, monitor the usefulness of the experience via Mi, and update the distribution toward generating more useful experience. Or, in a parallel system like the Gorila agent, it could guide resource allocation between a collection of concurrent but heterogeneous “actors”, each with different exploration hyper-parameters."

>	"Prioritized Memories: Considerations that help determine which transitions to replay are likely to be relevant for determining which memories to store and when to erase them (i.e., when it becomes unlikely that we would ever want to replay them anymore). An explicit control over which memories to keep or erase can help reduce the required total memory size, because it reduces redundancy (frequently visited transitions will have low error, so many of them will be dropped), while automatically adjusting for what has been learned already (dropping many of the ‘easy’ transitions) and biasing the contents of the memory to where the errors remain high. This is a non-trivial aspect, because memory requirements for DQN are currently dominated by the size of the replay memory, no longer by the size of the neural network. Erasing is a more final decision than reducing the replay probability, thus an even stronger emphasis of diversity may be necessary, for example by tracking the age of each transitions and using it to modulate the priority in such a way as to preserve sufficient old experience to prevent cycles (related to ‘hall of fame’ ideas in multi-agent literature) or collapsing value functions. The priority mechanism is also flexible enough to permit integrating experience from other sources, such as from a planner or from human expert trajectories, since knowing the source can be used to modulate each transition’s priority, for example in such a way as to preserve a sufficient fraction of external experience in memory."

>	"Numerous neuroscience studies have identified mechanisms of experience replay in the hippocampus of rodents, where sequences of prior experience are replayed, either during awake resting or sleep, and in particular that this happens more for rewarded paths. Furthermore, there is a likely link between increased replay of an experience, and how much can be learned from it, or its TD-error."

  - `video` <https://youtu.be/fevMOp5TDQs?t=56m51s> (Mnih)
  - `video` <https://yadi.sk/i/yBO0q4mI3GAxYd> (33:13) (Fritzler) `in russian`
  - `video` <https://youtu.be/fnwo3GCmyEo?t=26m29s> (Fritzler) `in russian`
  - `video` <https://youtu.be/mrgJ53TIcQc?t=25m43s> (Pavlov) `in russian`
  - `notes` <http://www.shortscience.org/paper?bibtexKey=journals/corr/1511.05952>
  - `code` <https://github.com/higgsfield/RL-Adventure/blob/master/4.prioritized%20dqn.ipynb>
  - `code` <https://github.com/Kaixhin/Atari>
  - `code` <https://github.com/carpedm20/deep-rl-tensorflow>


#### ["Deep Successor Reinforcement Learning"](https://arxiv.org/abs/1606.02396) Kulkarni, Saeedi, Gautam, Gershman
>	"Learning robust value functions given raw observations and rewards is now possible with model-free and model-based deep reinforcement learning algorithms. There is a third alternative, called Successor Representations, which decomposes the value function into two components – a reward predictor and a successor map. The successor map represents the expected future state occupancy from any given state and the reward predictor maps states to scalar rewards. The value function of a state can be computed as the inner product between the successor map and the reward weights. In this paper, we present DSR, which generalizes SR within an end-to-end deep reinforcement learning framework. DSR has several appealing properties including: increased sensitivity to distal reward changes due to factorization of reward and world dynamics, and the ability to extract bottleneck states (subgoals) given successor maps trained under a random policy. We show the efficacy of our approach on two diverse environments given raw pixel observations – simple grid-world domains (MazeBase) and the Doom game engine."

  - `video` <https://youtube.com/watch?v=OCHwXxSW70o> (Kulkarni)
  - `video` <https://youtube.com/watch?v=kNqXCn7K-BM> (Garipov)
  - `code` <https://github.com/Ardavans/DSR>


#### ["Learning to Act by Predicting the Future"](https://arxiv.org/abs/1611.01779) Dosovitskiy, Koltun
>	"We present an approach to sensorimotor control in immersive environments. Our approach utilizes a high-dimensional sensory stream and a lower-dimensional measurement stream. The cotemporal structure of these streams provides a rich supervisory signal, which enables training a sensorimotor control model by interacting with the environment. The model is trained using supervised learning techniques, but without extraneous supervision. It learns to act based on raw sensory input from a complex three-dimensional environment. The presented formulation enables learning without a fixed goal at training time, and pursuing dynamically changing goals at test time. We conduct extensive experiments in three-dimensional simulations based on the classical first-person game Doom. The results demonstrate that the presented approach outperforms sophisticated prior formulations, particularly on challenging tasks. The results also show that trained models successfully generalize across environments and goals. A model trained using the presented approach won the Full Deathmatch track of the Visual Doom AI Competition, which was held in previously unseen environments."

>	"application of deep successor reinforcement learning"

>	"uses supervised learning to predict future values of measurements (possibly rewards) given actions, which sidesteps traditional reinforcement learning algorithms"

  - `video` <https://youtube.com/watch?v=947bSUtuSQ0> + <https://youtube.com/watch?v=947bSUtuSQ0> (demo)
  - `video` <https://facebook.com/iclr.cc/videos/1712224178806641?t=3252> (Dosovitskiy)
  - `video` <https://youtube.com/watch?v=buUF5F8UCH8> (Lamb, Ozair)
  - `video` <https://youtube.com/watch?v=Q0ldKJbAwR8> (Dosovitskiy) `in russian`
  - `video` <https://yadi.sk/i/pMdw-_uI3Gke7Z> (1:02:03) (Shvechikov) `in russian`
  - `post` <https://danieltakeshi.github.io/2017/10/10/learning-to-act-by-predicting-the-future>
  - `post` <https://oreilly.com/ideas/reinforcement-learning-for-complex-goals-using-tensorflow>
  - `post` <https://flyyufelix.github.io/2017/11/17/direct-future-prediction.html>
  - `notes` <https://blog.acolyer.org/2017/05/12/learning-to-act-by-predicting-the-future/>
  - `code` <https://github.com/IntelVCL/DirectFuturePrediction>
  - `code` <https://github.com/NervanaSystems/coach/blob/master/agents/dfp_agent.py>
  - `code` <https://github.com/flyyufelix/Direct-Future-Prediction-Keras>


#### ["Deep Recurrent Q-Learning for Partially Observable MDPs"](http://arxiv.org/abs/1507.06527) Hausknecht, Stone
  `DRQN`
>	"Deep Reinforcement Learning has yielded proficient controllers for complex tasks. However, these controllers have limited memory and rely on being able to perceive the complete game screen at each decision point. To address these shortcomings, this article investigates the effects of adding recurrency to a Deep Q-Network by replacing the first post-convolutional fully-connected layer with a recurrent LSTM. The resulting Deep Recurrent Q-Network exhibits similar performance on standard Atari 2600 MDPs but better performance on equivalent partially observed domains featuring flickering game screens. Results indicate that given the same length of history, recurrency allows partial information to be integrated through time and is superior to alternatives such as stacking a history of frames in the network's input layer. We additionally show that when trained with partial observations, DRQN's performance at evaluation time scales as a function of observability. Similarly, when trained with full observations and evaluated with partial observations, DRQN's performance degrades more gracefully than that of DQN. We therefore conclude that when dealing with partially observed domains, the use of recurrency confers tangible benefits."

----
>	"Demonstrated that recurrent Q learning can perform the required information integration to resolve short-term partial observability (e.g. to estimate velocities) that is achieved via stacks of frames in the original DQN architecture."

  - `video` <https://youtu.be/aV4wz7FAXmo?t=1h9m> (Shvechikov)
  - `video` <https://yadi.sk/i/pMdw-_uI3Gke7Z> (36:29) (Fritzler) `in russian`
  - `video` <https://youtube.com/watch?v=bE5DIJvZexc> (Fritzler) `in russian`
  - `code` <https://github.com/mhauskn/dqn/tree/recurrent>
  - `code` <https://github.com/awjuliani/DeepRL-Agents/blob/master/Deep-Recurrent-Q-Network.ipynb>
  - `paper` [**"Playing FPS Games with Deep Reinforcement Learning"**](#playing-fps-games-with-deep-reinforcement-learning-lample-chaplot) by Lample and Chaplot `summary`


#### ["Playing FPS Games with Deep Reinforcement Learning"](https://arxiv.org/abs/1609.05521) Lample, Chaplot
  `DRQN`
>	"Advances in deep reinforcement learning have allowed autonomous agents to perform well on Atari games, often outperforming humans, using only raw pixels to make their decisions. However, most of these games take place in 2D environments that are fully observable to the agent. In this paper, we present the first architecture to tackle 3D environments in first-person shooter games, that involve partially observable states. Typically, deep reinforcement learning methods only utilize visual input for training. We present a method to augment these models to exploit game feature information such as the presence of enemies or items, during the training phase. Our model is trained to simultaneously learn these features along with minimizing a Q-learning objective, which is shown to dramatically improve the training speed and performance of our agent. Our architecture is also modularized to allow different models to be independently trained for different phases of the game. We show that the proposed architecture substantially outperforms built-in AI agents of the game as well as humans in deathmatch scenarios."

>	"We introduced a method to augment a DRQN model with high-level game information, and modularized our architecture to incorporate independent networks responsible for different phases of the game. These methods lead to dramatic improvements over the standard DRQN model when applied to complicated tasks like a deathmatch. We showed that the proposed model is able to outperform built-in bots as well as human players and demonstrated the generalizability of our model to unknown maps."

  - `video` <https://youtube.com/playlist?list=PLduGZax9wmiHg-XPFSgqGg8PEAV51q1FT> (demo)
  - `video` <http://on-demand.gputechconf.com/gtc/2018/video/S8467/> (Chaplot)
  - `code` <https://github.com/glample/Arnold>
  - `paper` [**"Deep Recurrent Q-Learning for Partially Observable MDPs"**](#deep-recurrent-q-learning-for-partially-observable-mdps-hausknecht-stone) by Hausknecht and Stone `summary`



---
### interesting papers - policy-based methods

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---model-free-methods)

----
#### ["Simple Random Search Provides a Competitive Approach to Reinforcement Learning"](https://arxiv.org/abs/1803.07055) Mania, Guy, Recht
>	"A common belief in model-free reinforcement learning is that methods based on random search in the parameter space of policies exhibit significantly worse sample complexity than those that explore the space of actions. We dispel such beliefs by introducing a random search method for training static, linear policies for continuous control problems, matching state-of-the-art sample efficiency on the benchmark MuJoCo locomotion tasks. Our method also finds a nearly optimal controller for a challenging instance of the Linear Quadratic Regulator, a classical problem in control theory, when the dynamics are not known. Computationally, our random search algorithm is at least 15 times more efficient than the fastest competing model-free methods on these benchmarks. We take advantage of this computational efficiency to evaluate the performance of our method over hundreds of random seeds and many different hyperparameter configurations for each benchmark task. Our simulations highlight a high variability in performance in these benchmark tasks, suggesting that commonly used estimations of sample efficiency do not adequately evaluate the performance of RL algorithms."

>	"For application to continuous control, we augment the basic random search method with three simple features. First, we scale each update step by the standard deviation of the rewards collected for computing that update step. Second, we normalize the system’s states by online estimates of their mean and standard deviation. Third, we discard from the computation of the update steps the directions that yield the least improvement of the reward."  

>	"Since the algorithm and policies are simple, we were able to perform extensive sensitivity studies, and observed that our method can find good solutions to highly nonconvex problems a large fraction of the time. Our results emphasize the high variance intrinsic to the training of policies for MuJoCo RL tasks. Therefore, it is not clear what is gained by evaluating RL algorithms on only a small numbers of random seeds, as is common in the RL literature. Evaluation on small numbers of random seeds does not capture performance adequately due to high variance."

>	"Though many RL researchers are concerned about minimizing sample complexity, it does not make sense to optimize the running time of an algorithm on a single instance. The running time of an algorithm is only a meaningful notion if either (a) evaluated on a family of instances, or (b) when clearly restricting the class of algorithms. Common RL practice, however, does not follow either (a) or (b). Instead researchers run algorithm A on task T with a given hyperparameter configuration, and plot a “learning curve” showing the algorithm reaches a target reward after collecting X samples. Then the “sample complexity” of the method is reported as the number of samples required to reach a target reward threshold, with the given hyperparameter configuration. However, any number of hyperparameter configurations can be tried. Any number of algorithmic enhancements can be added or discarded and then tested in simulation. For a fair measurement of sample complexity, should we not count the number of rollouts used for every tested hyperparameters?"

>	"More emphasis should be put on the development of model-based methods. For many problems, such methods have been observed to require fewer samples than model-free methods. Moreover, the physics of the systems should inform the parametric classes of models used for different problems. Model-based methods incur many computational challenges themselves, and it is quite possible that tools from deep RL such as improved tree search can provide new paths forward for tasks that require the navigation of complex and uncertain environments."

  - `post` <http://argmin.net/2018/03/20/mujocoloco/>
  - `post` <http://argmin.net/2018/03/26/outsider-rl/>
  - `code` <https://github.com/modestyachts/ARS>


#### ["Evolution Strategies as a Scalable Alternative to Reinforcement Learning"](https://arxiv.org/abs/1703.03864) Salimans, Ho, Chen, Sutskever
>	"We explore the use of Evolution Strategies, a class of black box optimization algorithms, as an alternative to popular RL techniques such as Q-learning and Policy Gradients. Experiments on MuJoCo and Atari show that ES is a viable solution strategy that scales extremely well with the number of CPUs available: By using hundreds to thousands of parallel workers, ES can solve 3D humanoid walking in 10 minutes and obtain competitive results on most Atari games after one hour of training time. In addition, we highlight several advantages of ES as a black box optimization technique: it is invariant to action frequency and delayed rewards, tolerant of extremely long horizons, and does not need temporal discounting or value function approximation."

>	"In future work we plan to apply evolution strategies to those problems for which reinforcement learning is less well-suited: problems with long time horizons and complicated reward structure. We are particularly interested in meta-learning, or learning-to-learn. A proof of concept for meta-learning in an RL setting was given by Duan et al. (2016b): Using ES instead of RL we hope to be able to extend these results. Another application which we plan to examine is to combine ES with fast low precision neural network implementations to fully make use of its gradient-free nature."

>	"Large source of difficulty in RL stems from the lack of informative gradients of policy performance: such gradients may not exist due to non-smoothness of the environment or policy, or may only be available as high-variance estimates because the environment usually can only be accessed via sampling."

>	"In addition to being easy to parallelize, and to having an advantage in cases with long action sequences and delayed rewards, black box optimization algorithms like ES have other advantages over reinforcement learning techniques that calculate gradients."

>	"The communication overhead of implementing ES in a distributed setting is lower than for reinforcement learning methods such as policy gradients and Q-learning, as the only information that needs to be communicated across processes are the scalar return and the random seed that was used to generate the perturbations ε, rather than a full gradient. Also, it can deal with maximally sparse and delayed rewards; there is no need for the assumption that time information is part of the reward."

>	"By not requiring backpropagation, black box optimizers reduce the amount of computation per episode by about two thirds, and memory by potentially much more. In addition, not explicitly calculating an analytical gradient protects against problems with exploding gradients that are common when working with recurrent neural networks. By smoothing the cost function in parameter space, we reduce the pathological curvature that causes these problems: bounded cost functions that are smooth enough can’t have exploding gradients. At the extreme, ES allows us to incorporate non-differentiable elements into our architecture, such as modules that use hard attention."

>	"Black box optimization methods are uniquely suited to capitalize on advances in low precision hardware for deep learning. Low precision arithmetic, such as in binary neural networks, can be performed much cheaper than at high precision. When optimizing such low precision architectures, biased low precision gradient estimates can be a problem when using gradient-based methods. Similarly, specialized hardware for neural network inference, such as TPUs, can be used directly when performing optimization using ES, while their limited memory usually makes backpropagation impossible."

>	"By perturbing in parameter space instead of action space, black box optimizers are naturally invariant to the frequency at which our agent acts in the environment. For reinforcement learning, on the other hand, it is well known that frameskip is a crucial parameter to get right for the optimization to succeed. While this is usually a solvable problem for games that only require short-term planning and action, it is a problem for learning longer term strategic behavior. For these problems, RL needs hierarchy to succeed, which is not as necessary when using black box optimization."

>	"The resemblance of ES to finite differences suggests the method will scale poorly with the dimension of the parameters θ. Theoretical analysis indeed shows that for general non-smooth optimization problems, the required number of optimization steps scales linearly with the dimension (Nesterov & Spokoiny, 2011). However, it is important to note that this does not mean that larger neural networks will perform worse than smaller networks when optimized using ES: what matters is the difficulty, or intrinsic dimension, of the optimization problem. To see that the dimensionality of our model can be completely separate from the effective dimension of the optimization problem, consider a regression problem where we approximate a univariate variable y with a linear model yˆ = x · w: if we double the number of features and parameters in this model by concatenating x with itself (i.e. using features x0 = (x, x)), the problem does not become more difficult. In fact, the ES algorithm will do exactly the same thing when applied to this higher dimensional problem, as long as we divide the standard deviation of the noise by two, as well as the learning rate. In practice, we observe slightly better results when using larger networks with ES. We hypothesize that this is due to the same effect that makes standard gradient-based optimization of large neural networks easier than for small ones: large networks have fewer local minima."

----
>	"Learning bigger model is faster in case of ES while it is slower in case of policy gradient."

>	"ES is able to focus on intrinsic dimensionality of the problem by ignoring irrelevant dimensions of problem."

>	"Every trick that helps backpropagation, also helps evolution strategies: scale of random initialization, batch normalization, Residual Networks."

----
>	"Solving 3D Humanoid with ES on one 18-core machine takes about 11 hours, which is on par with RL. However, when distributed across 80 machines and 1,440 CPU cores, ES can solve 3D Humanoid in just 10 min- utes, reducing experiment turnaround time by two orders of magnitude. Figure 1 shows that, for this task, ES is able to achieve linear speedup in the number of CPU cores."

>	"All games were trained for 1 billion frames, which requires about the same amount of neural network computation as the published 1-day results for A3C which uses 320 million frames. The difference is due to the fact that ES does not perform backpropagation and does not use a value function. By parallelizing the evaluation of perturbed parameters across 720 CPUs on Amazon EC2, we can bring down the time required for the training process to about one hour per game. After training, we compared final performance against the published A3C results and found that ES performed better in 23 games tested, while it performed worse in 28."

----
>	"Our work demonstrates that ES achieves strong performance, dispelling the common belief that ES methods are impossible to apply to high dimensional problems."  
>	"ES rivals the performance of standard RL techniques on modern benchmarks, while overcoming many of RL’s inconveniences. ES is simpler to implement (there is no need for backpropagation), it is easier to scale in a distributed setting, it does not suffer in settings with sparse rewards, and has fewer hyperparameters. This outcome is surprising because ES resembles simple hill-climbing in a high-dimensional space based only on finite differences along a few random directions at each step."  
>
>	"Mathematically, you’ll notice that this is also equivalent to estimating the gradient of the expected reward in the parameter space using finite differences, except we only do it along 100 random directions. Yet another way to see it is that we’re still doing RL (Policy Gradients, or REINFORCE specifically), where the agent’s actions are to emit entire parameter vectors using a gaussian policy."  
>	"Notice that the objective is identical to the one that RL optimizes: the expected reward. However, RL injects noise in the action space and uses backpropagation to compute the parameter updates, while ES injects noise directly in the parameter space. Another way to describe this is that RL is a “guess and check” on actions, while ES is a “guess and check” on parameters. Since we’re injecting noise in the parameters, it is possible to use deterministic policies (and we do, in our experiments). It is also possible to add noise in both actions and parameters to potentially combine the two approaches."  
>
>	"ES enjoys multiple advantages over RL algorithms:  
>	- No need for backpropagation. ES only requires the forward pass of the policy and does not require backpropagation (or value function estimation), which makes the code shorter and between 2-3 times faster in practice. On memory-constrained systems, it is also not necessary to keep a record of the episodes for a later update. There is also no need to worry about exploding gradients in RNNs. Lastly, we can explore a much larger function class of policies, including networks that are not differentiable (such as in binary networks), or ones that include complex modules (e.g. pathfinding, or various optimization layers).  
>	- Highly parallelizable. ES only requires workers to communicate a few scalars between each other, while in RL it is necessary to synchronize entire parameter vectors (which can be millions of numbers). Intuitively, this is because we control the random seeds on each worker, so each worker can locally reconstruct the perturbations of the other workers. Thus, all that we need to communicate between workers is the reward of each perturbation. As a result, we observed linear speedups in our experiments as we added on the order of thousands of CPU cores to the optimization.  
>	- Structured exploration. Some RL algorithms (especially policy gradients) initialize with random policies, which often manifests as random jitter on spot for a long time. This effect is mitigated in Q-Learning due to epsilon-greedy policies, where the max operation can cause the agents to perform some consistent action for a while (e.g. holding down a left arrow). This is more likely to do something in a game than if the agent jitters on spot, as is the case with policy gradients. Similar to Q-learning, ES does not suffer from these problems because we can use deterministic policies and achieve consistent exploration.  
>	- Credit assignment over long time scales. By studying both ES and RL gradient estimators mathematically we can see that ES is an attractive choice especially when the number of time steps in an episode is big, where actions have longlasting effects, or if no good value function estimates are available."  

----
>	"Mathematically, you’ll notice that this is also equivalent to estimating the gradient of the expected reward in the parameter space using finite differences, except we only do it along 100 random directions. Yet another way to see it is that we’re still doing RL (Policy Gradients, or REINFORCE specifically), where the agent’s actions are to emit entire parameter vectors using a gaussian policy."

>	"Notice that the objective is identical to the one that RL optimizes: the expected reward. However, RL injects noise in the action space and uses backpropagation to compute the parameter updates, while ES injects noise directly in the parameter space. Another way to describe this is that RL is a “guess and check” on actions, while ES is a “guess and check” on parameters. Since we’re injecting noise in the parameters, it is possible to use deterministic policies (and we do, in our experiments). It is also possible to add noise in both actions and parameters to potentially combine the two approaches."

----
>	"Data efficiency comparison. ES is less efficient than TRPO, but no worse than about a factor of 10."

>	"Wall clock comparison. On Atari, ES trained on 720 cores in 1 hour achieves comparable performance to A3C trained on 32 cores in 1 day. We were able to solve one of the hardest MuJoCo tasks (a 3D humanoid) using 1,440 CPUs across 80 machines in only 10 minutes. As a comparison, in a typical setting 32 A3C workers on one machine would solve this task in about 10 hours. We found that naively scaling A3C in a standard cloud CPU setting is challenging due to high communication bandwidth requirements."

>	"It is also important to note that supervised learning problems (e.g. image classification, speech recognition, or most other tasks in the industry), where one can compute the exact gradient of the loss function with backpropagation, are not directly impacted by these findings. For example, in our preliminary experiments we found that using ES to estimate the gradient on the MNIST digit recognition task can be as much as 1,000 times slower than using backpropagation. It is only in RL settings, where one has to estimate the gradient of the expected reward by sampling, where ES becomes competitive."

----
>	"This gradient estimator may be slightly biased as well as high variance. The second order Taylor approximation is the part where bias may be introduced, if the real objective function has non-negligible (i.e. weird) third order gradients. The size of the bias will be in the order of σ² so as long as σ is small, the bias is probably negligible from a practical perspective. Therefore you can kind of say ES provides an approximately unbiased gradient estimate. So this is basically SGD - as SGD only requires an unbiased estimate of gradients. The unbiased estimate typically comes from minibatches, but no-one said it cannot come from a different Monte Carlo estimate. In this respect, the only difference between backprop-SGD and ES is the source of randomness in the gradient estimator. Consequently, Adam or RMS-prop or Nesterov might still make perfect sense on top of these gradients, for example."

  - `post` <https://blog.openai.com/evolution-strategies/>
  - `video` <https://youtube.com/watch?v=SQtOI9jsrJ0> (Chen) `video`
  - `video` <http://youtube.com/watch?v=rHAasIIGIEc> (Elistratova) `in russian`
  - `video` <https://youtube.com/watch?v=Rd0UdJFYkqI> (Temirchev) `in russian`
  - `video` <https://youtube.com/watch?v=8jKC95KklT0> (Karazeev) `in russian`
  - `post` <http://inference.vc/evolutionary-strategies-embarrassingly-parallelizable-optimization/> (Huszar)
  - `post` <http://inference.vc/evolution-strategies-variational-optimisation-and-natural-es-2/> (Huszar)
  - `post` <http://davidbarber.github.io/blog/2017/04/03/variational-optimisation/> (Barber)
  - `post` <http://argmin.net/2017/04/03/evolution/> (Recht)
  - `post` <http://argmin.net/2018/03/20/mujocoloco/> (Recht)
  - `post` <http://blog.otoro.net/2017/10/29/visual-evolution-strategies/>
  - `notes` <https://lilianweng.github.io/lil-log/2019/09/05/evolution-strategies.html#openai-es-for-rl>
  - `notes` <https://lilianweng.github.io/lil-log/2018/02/19/a-long-peek-into-reinforcement-learning.html#evolution-strategies>
  - `code` <https://github.com/openai/evolution-strategies-starter>
  - `code` <https://github.com/atgambardella/pytorch-es>
  - `paper` ["Parameter-exploring Policy Gradients"](https://mediatum.ub.tum.de/doc/1287490/409330.pdf) by Sehnke et al.
  - `paper` ["Random Gradient-Free Minimization of Convex Functions"](https://mipt.ru/dcam/students/elective/a_5gc1te/RandomGradFree.PDF) by Nesterov
  - `paper` ["Stochastic Gradient Estimation with Finite Differences"](http://approximateinference.org/accepted/BuesingEtAl2016.pdf) by Buesing et al.
  -  <https://en.wikipedia.org/wiki/Simultaneous_perturbation_stochastic_approximation>


#### ["Asynchronous Methods for Deep Reinforcement Learning"](https://arxiv.org/abs/1602.01783) Mnih, Badia, Mirza, Graves, Lillicrap, Harley, Silver, Kavukcuoglu
  `A2C` `A3C`
>	"We propose a conceptually simple and lightweight framework for deep reinforcement learning that uses asynchronous gradient descent for optimization of deep neural network controllers. We present asynchronous variants of four standard reinforcement learning algorithms and show that parallel actor-learners have a stabilizing effect on training allowing all four methods to successfully train neural network controllers. The best performing method, an asynchronous variant of actor-critic, surpasses the current state-of-the-art on the Atari domain while training for half the time on a single multi-core CPU instead of a GPU. Furthermore, we show that asynchronous actor-critic succeeds on a wide variety of continuous motor control problems as well as on a new task of navigating random 3D mazes using a visual input."

>	"We have presented asynchronous versions of four standard reinforcement learning algorithms and showed that they are able to train neural network controllers on a variety of domains in a stable manner. Our results show that in our proposed framework stable training of neural networks through reinforcement learning is possible with both valuebased and policy-based methods, off-policy as well as onpolicy methods, and in discrete as well as continuous domains. When trained on the Atari domain using 16 CPU cores, the proposed asynchronous algorithms train faster than DQN trained on an Nvidia K40 GPU, with A3C surpassing the current state-of-the-art in half the training time. One of our main findings is that using parallel actorlearners to update a shared model had a stabilizing effect on the learning process of the three value-based methods we considered. While this shows that stable online Q-learning is possible without experience replay, which was used for this purpose in DQN, it does not mean that experience replay is not useful. Incorporating experience replay into the asynchronous reinforcement learning framework could substantially improve the data efficiency of these methods by reusing old data. This could in turn lead to much faster training times in domains like TORCS where interacting with the environment is more expensive than updating the model for the architecture we used."

----
>	- critic learns only state value function V(s) rather than action value function Q(s,a) and thus cannot pass back to actor gradients of value function with respect to action  
>	- critic approximates action value with rewards from several steps of experience and passes TD error to actor  
>	- exploiting multithreading capabilities and executing many instances of agent in parallel using shared model  
>	- alternative to experience replay since parallelization also diversifies and decorrelates experience data  

  - `video` <http://youtube.com/watch?v=0xo1Ldx3L5Q> (demo)
  - `video` <http://youtube.com/watch?v=nMR5mjCFZCw> (demo)
  - `video` <http://youtube.com/watch?v=Ajjc08-iPx8> (demo)
  - `video` <http://youtube.com/watch?v=9sx1_u2qVhQ> (Mnih)
  - `video` <http://techtalks.tv/talks/asynchronous-methods-for-deep-reinforcement-learning/62475/> (Mnih)
  - `video` <https://youtu.be/eeJ1-bUnwRI?t=1h49m19s> (Sigaud)
  - `post` <https://danieltakeshi.github.io/2018/06/28/a2c-a3c>
  - `post` <https://medium.com/@awjuliani/simple-reinforcement-learning-with-tensorflow-part-8-asynchronous-actor-critic-agents-a3c-c88f72a5e9f2>
  - `notes` <https://lilianweng.github.io/lil-log/2018/02/19/a-long-peek-into-reinforcement-learning.html#a3c>
  - `notes` <http://www.shortscience.org/paper?bibtexKey=journals%2Fcorr%2FMnihBMGLHSK16>
  - `code` <https://github.com/openai/baselines/tree/master/baselines/a2c>
  - `code` <https://github.com/ikostrikov/pytorch-a3c>


#### ["Trust Region Policy Optimization"](http://arxiv.org/abs/1502.05477) Schulman, Levine, Moritz, Jordan, Abbeel
  `TRPO`
>	"In this article, we describe a method for optimizing control policies, with guaranteed monotonic improvement. By making several approximations to the theoretically-justified scheme, we develop a practical algorithm, called Trust Region Policy Optimization. This algorithm is effective for optimizing large nonlinear policies such as neural networks. Our experiments demonstrate its robust performance on a wide variety of tasks: learning simulated robotic swimming, hopping, and walking gaits; and playing Atari games using images of the screen as input. Despite its approximations that deviate from the theory, TRPO tends to give monotonic improvement, with little tuning of hyperparameters."

>	"We proposed and analyzed trust region methods for optimizing stochastic control policies. We proved monotonic improvement for an algorithm that repeatedly optimizes a local approximation to the expected cost of the policy with a KL divergence penalty, and we showed that an approximation to this method that incorporates a KL divergence constraint achieves good empirical results on a range of challenging policy learning tasks, outperforming prior methods. Our analysis also provides a perspective that unifies policy gradient and policy iteration methods, and shows them to be special limiting cases of an algorithm that optimizes a certain objective subject to a trust region constraint. In the domain of robotic locomotion, we successfully learned controllers for swimming, walking and hopping in a physics simulator, using general purpose neural networks and minimally informative costs. To our knowledge, no prior work has learned controllers from scratch for all of these tasks, using a generic policy search method and non-engineered, general-purpose policy representations. In the game-playing domain, we learned convolutional neural network policies that used raw images as inputs. This requires optimizing extremely high-dimensional policies, and only two prior methods report successful results on this task. Since the method we proposed is scalable and has strong theoretical foundations, we hope that it will serve as a jumping-off point for future work on training large, rich function approximators for a range of challenging problems. At the intersection of the two experimental domains we explored, there is the possibility of learning robotic control policies that use vision and raw sensory data as input, providing a unified scheme for training robotic controllers that perform both perception and control. The use of more sophisticated policies, including recurrent policies with hidden state, could further make it possible to roll state estimation and control into the same policy in the partially-observed setting. By combining our method with model learning, it would also be possible to substantially reduce its sample complexity, making it applicable to real-world settings where samples are expensive."

----
>	"TRPO approximates Conservative Policy Iteration algorithm with trust region constraint."

>	"Combines theoretical ideas from Conservative Policy Gradient algorithm to prove that monotonic improvement can be guaranteed when one solves a series of subproblems of optimizing a bound on the policy performance. The conclusion is that one should use KL-divergence constraint."

>	"As you iteratively improve your policy, it’s important to constrain the KL divergence between the old and new policy to be less than some constant δ. This δ (in the unit of nats) is better than a fixed step size, since the meaning of the step size changes depending on what the rewards and problem structure look like at different points in training. This is called Trust Region Policy Optimization (or, in a first-order variant, Proximal Policy Optimization) and it matters more as we do more experience replay."

----
>	"There's an identity that was first proven by Sham and Kakade in 2002 that lets you express a policy in terms of how good it is compared to another, different, policy. Furthermore, you can show that using this identity, it's possible to guarantee that the policy improves during an update. The goal of TRPO is to maximize the improvement of the "new" policy that you get after optimization compared to the previous "old" policy. To do this, you have to assume that the state visitation distributions of the two policies are similar (this comes from the identity), which they will be if you constrain the KL-divergence between them (i.e. this is like saying "if the new policy is better than the old policy in every state, the new policy is better than the old policy")."  
>	"TRPO treats this as a constrained optimization problem; i.e. maximize the improvement of the new policy compared to the old policy such that the KL divergence is smaller than a given value. Since you need to take multiple update steps for non-convex constrained optimization (generally using the conjugate gradient method and line search) the advantage estimate is no longer on-policy during the optimization process because you're changing the weights of pi_new compared to pi_old, and then comparing using the rollout taken under pi_old. To correct for the now different policy distributions, importance sampling is used (and this actually falls out the aforementioned identity from Sham and Kakade)."  

----
>	"TRPO uses the notion of a trust region, which restricts optimization steps to within a region where the approximation of the true cost function still holds."

>	"As you iteratively improve your policy, it’s important to avoid parameter updates that change your policy too much, as enforced by constraining the KL divergence between the distributions predicted by the old and the new policy on a batch of data to be less than some constant δ. This δ (in the unit of nats) is better than a fixed step size, since the meaning of the step size changes depending on what the rewards and problem structure look like at different points in training. It matters more as we do more experience replay. Instead of conjugate gradients the simplest instantiation of this idea could be implemented by doing a line search and checking the KL along the way."

>	"To improve its policy, TRPO attempts to maximize the expectation of Q-values over the distribution of states and actions given by θnew:  
>	maxθ [Σs pθ(s) * (Σa πθ(a|s) * Qθold(s,a))]  subject to  DKL(pθold, pθ) ≤ δ

>	"This objective can be approximated by using an importance-sampled Monte Carlo estimate of Q-values, with a distribution of states sampled from policy θold. However, theres a constraint to updating θ: the average KL divergence between the new policy and old policy cannot be greater than a constant δ. This acts as a limiter on the step size we can take on each update, and can be compared to the natural gradient. The theory behind TRPO guarantees gradual improvement over the expected return of a policy."

>	"One downside to TRPO algorithm is its on-policy nature, requiring new Q-values after every policy update. We cannot use methods such as experience replay which reuse past information, so that we must acquire new Monte Carlo estimates of Q for every new policy. Furthermore, Monte Carlo estimates are known to have higher variance than methods such as one-step TD updates, since the return is affected by independent future decisions. Bringing this variance down requires many episodes of experience per policy update, making TRPO a data-heavy algorithm."

  - `video` <https://youtube.com/watch?v=jeid0wIrSn4> + <https://vimeo.com/113957342> (demo)
  - `video` <https://youtube.com/watch?v=CKaN5PgkSBc>
  - `video` <https://youtu.be/xe-z4i3l-iQ?t=30m35s> (Abbeel)
  - `video` <http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/#t=1630> (Abbeel)
  - `video` <https://youtube.com/watch?v=gb5Q2XL5c8A> (Schulman)
  - `video` <https://youtu.be/ycCtmp4hcUs?t=58m53s> (Achiam)
  - `video` <https://youtu.be/eeJ1-bUnwRI?t=1h35m20s> (Sigaud)
  - `video` <https://yadi.sk/i/1oyihBnm3HiKHm> + <https://yadi.sk/i/b0ol2gUV3HiKKJ> (Fritzler and Ratnikov) `in russian` ([slides](https://yadi.sk/i/9j6S4WVp3HgEdn) `in english`)
  - `video` <https://youtu.be/1slR-rGufmw?t=6m50s> (Grishin) `in russian`
  - `post` <http://depthfirstlearning.com/2018/TRPO>
  - `post` <https://towardsdatascience.com/the-pursuit-of-robotic-happiness-how-trpo-and-ppo-stabilize-policy-gradient-methods-545784094e3b>
  - `post` <http://kvfrans.com/what-is-the-natural-gradient-and-where-does-it-appear-in-trust-region-policy-optimization/>
  - `post` <http://www.alexirpan.com/rl-derivations/#natural-policy-gradient>
  - `notes` <https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html#trpo>
  - `notes` <http://www.shortscience.org/paper?bibtexKey=journals/corr/SchulmanLMJA15>
  - `notes` <https://towardsdatascience.com/introduction-to-various-reinforcement-learning-algorithms-part-ii-trpo-ppo-87f2c5919bb9>
  - `code` <https://github.com/openai/baselines/tree/master/baselines/trpo_mpi>
  - `code` <https://github.com/reinforceio/tensorforce/blob/master/tensorforce/models/trpo_model.py>
  - `code` <https://github.com/ikostrikov/pytorch-trpo>
  - `code` <https://github.com/kvfrans/parallel-trpo>
  - `paper` ["Approximately Optimal Approximate Reinforcement Learning"](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.7.7601) by Kakade, Langford


#### ["High-Dimensional Continuous Control Using Generalized Advantage Estimation"](http://arxiv.org/abs/1506.02438) Schulman, Moritz, Levine, Jordan, Abbeel
>	"Policy gradient methods are an appealing approach in reinforcement learning because they directly optimize the cumulative reward and can straightforwardly be used with nonlinear function approximators such as neural networks. The two main challenges are the large number of samples typically required, and the difficulty of obtaining stable and steady improvement despite the nonstationarity of the incoming data. We address the first challenge by using value functions to substantially reduce the variance of policy gradient estimates at the cost of some bias, with an exponentially-weighted estimator of the advantage function that is analogous to TD(lambda). We address the second challenge by using trust region optimization procedure for both the policy and the value function, which are represented by neural networks. Our approach yields strong empirical results on highly challenging 3D locomotion tasks, learning running gaits for bipedal and quadrupedal simulated robots, and learning a policy for getting the biped to stand up from starting out lying on the ground. In contrast to a body of prior work that uses hand-crafted policy representations, our neural network policies map directly from raw kinematics to joint torques. Our algorithm is fully model-free, and the amount of simulated experience required for the learning tasks on 3D bipeds corresponds to 1-2 weeks of real time."

>	"Policy gradient methods provide a way to reduce reinforcement learning to stochastic gradient descent, by providing unbiased gradient estimates. However, so far their success at solving difficult control problems has been limited, largely due to their high sample complexity. We have argued that the key to variance reduction is to obtain good estimates of the advantage function. We have provided an intuitive but informal analysis of the problem of advantage function estimation, and justified the generalized advantage estimator, which has two parameters which adjust the bias-variance tradeoff. We described how to combine this idea with trust region policy optimization and a trust region algorithm that optimizes a value function, both represented by neural networks. Combining these techniques, we are able to learn to solve difficult control tasks that have previously been out of reach for generic reinforcement learning methods. One question that merits future investigation is the relationship between value function estimation error and policy gradient estimation error. If this relationship were known, we could choose an error metric for value function fitting that is well-matched to the quantity of interest, which is typically the accuracy of the policy gradient estimation. Some candidates for such an error metric might include the Bellman error or projected Bellman error, as described in Bhatnagar et al. (2009). Another enticing possibility is to use a shared function approximation architecture for the policy and the value function, while optimizing the policy using generalized advantage estimation. While formulating this problem in a way that is suitable for numerical optimization and provides convergence guarantees remains an open question, such an approach could allow the value function and policy representations to share useful features of the input, resulting in even faster learning. In concurrent work, researchers have been developing policy gradient methods that involve differentiation with respect to the continuous-valued action (Lillicrap et al., 2015; Heess et al., 2015). While we found empirically that the one-step return (lambda = 0) leads to excessive bias and poor performance, these papers show that such methods can work when tuned appropriately. However, note that those papers consider control problems with substantially lower-dimensional state and action spaces than the ones considered here. A comparison between both classes of approach would be useful for future work."

  - `video` <https://youtu.be/gb5Q2XL5c8A?t=21m2s> + <https://youtube.com/watch?v=ATvp0Hp7RUI> + <https://youtube.com/watch?v=Pvw28wPEWEo> (demo)
  - `video` <https://youtu.be/xe-z4i3l-iQ?t=30m35s> (Abbeel)
  - `video` <https://youtu.be/rO7Dx8pSJQw?t=40m20s> (Schulman)
  - `post` <https://danieltakeshi.github.io/2017/04/02/notes-on-the-generalized-advantage-estimation-paper/>
  - `code` <https://github.com/joschu/modular_rl>
  - `code` <https://github.com/rll/deeprlhw2/blob/master/ppo.py>


#### ["Proximal Policy Optimization Algorithms"](https://arxiv.org/abs/1707.06347) Schulman, Wolski, Dhariwal, Radford, Klimov
  `PPO`
>	"We propose a new family of policy gradient methods for reinforcement learning, which alternate between sampling data through interaction with the environment, and optimizing a "surrogate" objective function using stochastic gradient ascent. Whereas standard policy gradient methods perform one gradient update per data sample, we propose a novel objective function that enables multiple epochs of minibatch updates. The new methods, which we call proximal policy optimization, have some of the benefits of trust region policy optimization, but they are much simpler to implement, more general, and have better sample complexity (empirically). Our experiments test PPO on a collection of benchmark tasks, including simulated robotic locomotion and Atari game playing, and we show that PPO outperforms other online policy gradient methods, and overall strikes a favorable balance between sample complexity, simplicity, and wall-time."

----
>	"There's an identity that was first proven by Sham and Kakade in 2002 that lets you express a policy in terms of how good it is compared to another, different, policy. Furthermore, you can show that using this identity, it's possible to guarantee that the policy improves during an update. The goal of both TRPO and PPO is to maximize the improvement of the "new" policy that you get after optimization compared to the previous "old" policy. To do this, you have to assume that the state visitation distributions of the two policies are similar (this comes from the identity), which they will be if you constrain the KL-divergence between them (i.e. this is like saying "if the new policy is better than the old policy in every state, the new policy is better than the old policy")."  
>	"TRPO treats this as a constrained optimization problem; i.e. maximize the improvement of the new policy compared to the old policy such that the KL divergence is smaller than a given value. Since you need to take multiple update steps for non-convex constrained optimization (generally using the conjugate gradient method and line search) the advantage estimate is no longer on-policy during the optimization process because you're changing the weights of pi_new compared to pi_old, and then comparing using the rollout taken under pi_old. To correct for the now different policy distributions, importance sampling is used (and this actually falls out the aforementioned identity from Sham and Kakade)."  
>	"PPO takes this idea, and applies it to first order methods. Say we want to do multiple gradient updates on a single batch of data in order to speed up learning -- the problem with this is that the Monte-Carlo return is no longer on-policy after the first gradient update. PPO uses importance sampling the same way that TRPO does to correct for the change in the policy distribution. In order to ensure that the two distributions remain close (to keep the state distributions close) a momentum term based on the KL divergence is added to decelerate the gradient update as it moves away from the initial policy over subsequent updates. The second way of doing PPO (using the clamped heuristic) involves taking the most pessimistic update at every step by clamping the gradient to a fixed region, and then taking whatever the minimum step is. This way, you effectively decelerate updates that move the new policy further and further away from the original policy (though you can still break it by taking too many update steps)."  

  - `post` <https://blog.openai.com/openai-baselines-ppo/> (demo)
  - `video` <https://youtu.be/xvRrgxcpaHY?t=28m34s> (Schulman)
  - `video` <https://youtu.be/ycCtmp4hcUs?t=1h7m> (Achiam)
  - `video` <https://youtu.be/eeJ1-bUnwRI?t=1h44m24s> (Sigaud)
  - `video` <https://youtube.com/watch?v=5P7I-xPq8u8> (Steenbrugge)
  - `video` <https://youtu.be/1slR-rGufmw?t=53m26s> (Grishin) `in russian`
  - `post` <https://learningai.io/projects/2017/07/28/ai-gym-workout.html>
  - `notes` <https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html#ppo>
  - `notes` <https://towardsdatascience.com/introduction-to-various-reinforcement-learning-algorithms-part-ii-trpo-ppo-87f2c5919bb9>
  - `notes` <https://github.com/DanielTakeshi/Paper_Notes/blob/master/reinforcement_learning/Proximal_Policy_Optimization_Algorithms.md>
  - `post` <https://towardsdatascience.com/the-pursuit-of-robotic-happiness-how-trpo-and-ppo-stabilize-policy-gradient-methods-545784094e3b>
  - `post` <http://blog.varunajayasiri.com/ml/ppo.html>
  - `post` <https://costa.sh/blog-the-32-implementation-details-of-ppo.html>
  - `paper` ["Implementation Matters in Deep RL: A Case Study on PPO and TRPO"](https://arxiv.org/abs/2005.12729) by Engstrom et al.


#### ["Deterministic Policy Gradient Algorithms"](http://jmlr.org/proceedings/papers/v32/silver14.html) Silver, Lever, Heess, Degris, Wierstra, Riedmiller
  `DPG`
>	"In this paper we consider deterministic policy gradient algorithms for reinforcement learning with continuous actions. The deterministic policy gradient has a particularly appealing form: it is the expected gradient of the action-value function. This simple form means that the deterministic policy gradient can be estimated much more efficiently than the usual stochastic policy gradient. To ensure adequate exploration, we introduce an off-policy actor-critic algorithm that learns a deterministic target policy from an exploratory behaviour policy. We demonstrate that deterministic policy gradient algorithms can significantly outperform their stochastic counter-parts in high-dimensional action spaces."

>	"Policy gradient algorithms are widely used in reinforcement learning problems with continuous action spaces. The basic idea is to represent the policy by a parametric probability distribution πθ(a|s) = P [a|s; θ] that stochastically selects action a in state s according to parameter vector θ. Policy gradient algorithms typically proceed by sampling this stochastic policy and adjusting the policy parameters in the direction of greater cumulative reward. In this paper we instead consider deterministic policies a=μθ(s). It is natural to wonder whether the same approach can be followed as for stochastic policies: adjusting the policy parameters in the direction of the policy gradient. It was previously believed that the deterministic policy gradient did not exist, or could only be obtained when using a model. However, we show that the deterministic policy gradient does indeed exist, and furthermore it has a simple model-free form that simply follows the gradient of the action-value function. In addition, we show that the deterministic policy gradient is the limiting case, as policy variance tends to zero, of the stochastic policy gradient."

>	"From a practical viewpoint, there is a crucial difference between the stochastic and deterministic policy gradients. In the stochastic case, the policy gradient integrates over both state and action spaces, whereas in the deterministic case it only integrates over the state space. As a result, computing the stochastic policy gradient may require more samples, especially if the action space has many dimensions. In order to explore the full state and action space, a stochastic policy is often necessary. To ensure that our deterministic policy gradient algorithms continue to explore satisfactorily, we introduce an off-policy learning algorithm. The basic idea is to choose actions according to a stochastic behaviour policy (to ensure adequate exploration), but to learn about a deterministic target policy (exploiting the efficiency of the deterministic policy gradient). We use the deterministic policy gradient to derive an off-policy actor-critic algorithm that estimates the action-value function using a differentiable function approximator, and then updates the policy parameters in the direction of the approximate action-value gradient. We also introduce a notion of compatible function approximation for deterministic policy gradients, to ensure that the approximation does not bias the policy gradient."

>	"We apply our deterministic actor-critic algorithms to several benchmark problems: a high-dimensional bandit; several standard benchmark reinforcement learning tasks with low dimensional action spaces; and a high-dimensional task for controlling an octopus arm. Our results demonstrate a significant performance advantage to using deterministic policy gradients over stochastic policy gradients, particularly in high dimensional tasks. In practice, the deterministic actor-critic significantly outperformed its stochastic counterpart by several orders of magnitude in a bandit with 50 continuous action dimensions, and solved a challenging reinforcement learning problem with 20 continuous action dimensions and 50 state dimensions. Furthermore, our algorithms require no more computation than prior methods: the computational cost of each update is linear in the action dimensionality and the number of policy parameters."

----
>	"DPG provides a continuous analogue to DQN, exploiting the differentiability of the Q-network to solve a wide variety of continuous control tasks."

  - `post` <https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html#dpg>


#### ["Continuous Control with Deep Reinforcement Learning"](http://arxiv.org/abs/1509.02971) Lillicrap, Hunt, Pritzel, Heess, Erez, Tassa, Silver, Wierstra
  `DDPG`
>	"We adapt the ideas underlying the success of Deep Q-Learning to the continuous action domain. We present an actor-critic, model-free algorithm based on the deterministic policy gradient that can operate over continuous action spaces. Using the same learning algorithm, network architecture and hyper-parameters, our algorithm robustly solves more than 20 simulated physics tasks, including classic problems such as cartpole swing-up, dexterous manipulation, legged locomotion and car driving. Our algorithm is able to find policies whose performance is competitive with those found by a planning algorithm with full access to the dynamics of the domain and its derivatives. We further demonstrate that for many of the tasks the algorithm can learn policies “end-to-end”: directly from raw pixel inputs."

>	"The work presented here combines insights from recent advances in deep learning and reinforcement learning, resulting in an algorithm that robustly solves challenging problems across a variety of domains with continuous action spaces, even when using raw pixels for observations. As with most reinforcement learning algorithms, the use of non-linear function approximators nullifies any convergence guarantees; however, our experimental results demonstrate that stable learning without the need for any modifications between environments. Interestingly, all of our experiments used substantially fewer steps of experience than was used by DQN learning to find solutions in the Atari domain. Nearly all of the problems we looked at were solved within 2.5 million steps of experience (and usually far fewer), a factor of 20 fewer steps than DQN requires for good Atari solutions. This suggests that, given more simulation time, DDPG may solve even more difficult problems than those considered here. A few limitations to our approach remain. Most notably, as with most model-free reinforcement approaches, DDPG requires a large number training episodes to find solutions. However, we believe that a robust model-free approach may be an important component of larger systems which may attack these limitations."

>	"While DQN solves problems with high-dimensional observation spaces, it can only handle discrete and low-dimensional action spaces. Many tasks of interest, most notably physical control tasks, have continuous (real valued) and high dimensional action spaces. DQN cannot be straightforwardly applied to continuous domains since it relies on a finding the action that maximises the action-value function, which in the continuous valued case requires an iterative optimization process at every step."

>	"In this work we present a model-free, off-policy actor-critic algorithm using deep function approximators that can learn policies in high-dimensional, continuous action spaces. Our work is based on the deterministic policy gradient algorithm. However, as we show below, a naive application of this actor-critic method with neural function approximators is unstable for challenging problems. Here we combine the actor-critic approach with insights from the recent success of Deep Q Network. Prior to DQN, it was generally believed that learning value functions using large, non-linear function approximators was difficult and unstable. DQN is able to learn value functions using such function approximators in a stable and robust way due to two innovations: 1. the network is trained off-policy with samples from a replay buffer to minimize correlations between samples; 2. the network is trained with a target Q network to give consistent targets during temporal difference backups. In this work we make use of the same ideas, along with batch normalization, a recent advance in deep learning."

>	"A key feature of the approach is its simplicity: it requires only a straightforward actor-critic architecture and learning algorithm with very few “moving parts”, making it easy to implement and scale to more difficult problems and larger networks. For the physical control problems we compare our results to a baseline computed by a planner that has full access to the underlying simulated dynamics and its derivatives. Interestingly, DDPG can sometimes find policies that exceed the performance of the planner, in some cases even when learning from pixels (the planner always plans over the true, low-dimensional state space)."

----
>	- continuous analogue to DQN which exploits differentiability of Q-network  
>	- instead of requiring samples from stochastic policy and encouraging samples with higher scores, use deterministic policy and get gradient information directly from second network that models score function  
>	- policy determinism allows policy to be optimized more easily and more sample efficiently due to action no longer being a random variable which must be integrated over in expectation  
>	- can be much more efficient in settings with very high-dimensional actions where sampling actions provides poor coverage of state-action space  

  - `video` <http://videolectures.net/rldm2015_silver_reinforcement_learning/#t=4043> (Silver)
  - `video` <http://youtu.be/qLaDWKd61Ig?t=39m> (Silver)
  - `video` <http://youtu.be/KHZVXao4qXs?t=52m58s> (Silver)
  - `video` <https://youtu.be/Y2XBiUtZo1k?t=27m10s> (Abbeel)
  - `video` <http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/#t=3724> (Abbeel)
  - `video` <https://youtu.be/rO7Dx8pSJQw?t=50m> (Schulman)
  - `video` <https://youtu.be/eeJ1-bUnwRI?t=55m38s> (Sigaud)
  - `video` <https://youtu.be/mrgJ53TIcQc?t=1h3m2s> (Seleznev) `in russian`
  - `post` <https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html#ddpg>
  - `post` <https://yanpanlau.github.io/2016/10/11/Torcs-Keras.html>
  - `post` <http://pemami4911.github.io/blog_posts/2016/08/21/ddpg-rl.html>
  - `code` <https://github.com/openai/baselines/tree/master/baselines/ddpg>
  - `paper` [**"Deterministic Policy Gradient Algorithms"**](#deterministic-policy-gradient-algorithms-silver-lever-heess-degris-wierstra-riedmiller) by Silver et al. `summary`


#### ["Learning Continuous Control Policies by Stochastic Value Gradients"](http://arxiv.org/abs/1510.09142) Heess, Wayne, Silver, Lillicrap, Tassa, Erez
>	"We present a unified framework for learning continuous control policies using backpropagation. It supports stochastic control by treating stochasticity in the Bellman equation as a deterministic function of exogenous noise. The product is a spectrum of general policy gradient algorithms that range from model-free methods with value functions to model-based methods without value functions. We use learned models but only require observations from the environment instead of observations from model-predicted trajectories, minimizing the impact of compounded model errors. We apply these algorithms first to a toy stochastic control problem and then to several physics-based control problems in simulation. One of these variants, SVG(1), shows the effectiveness of learning models, value functions, and policies simultaneously in continuous domains."

>	"We have shown that two potential problems with value gradient methods, their reliance on planning and restriction to deterministic models, can be exorcised, broadening their relevance to reinforcement learning. We have shown experimentally that the SVG framework can train neural network policies in a robust manner to solve interesting continuous control problems. Furthermore, we did not harness sophisticated generative models of stochastic dynamics, but one could readily do so, presenting great room for growth."

>	"Policy gradient algorithms maximize the expectation of cumulative reward by following the gradient of this expectation with respect to the policy parameters. Most existing algorithms estimate this gradient in a model-free manner by sampling returns from the real environment and rely on a likelihood ratio estimator. Such estimates tend to have high variance and require large numbers of samples or, conversely, low-dimensional policy parameterizations. A second approach to estimate a policy gradient relies on backpropagation instead of likelihood ratio methods. If a differentiable environment model is available, one can link together the policy, model, and reward function to compute an analytic policy gradient by backpropagation of reward along a trajectory. Instead of using entire trajectories, one can estimate future rewards using a learned value function (a critic) and compute policy gradients from subsequences of trajectories. It is also possible to backpropagate analytic action derivatives from a Q-function to compute the policy gradient without a model. Following Fairbank, we refer to methods that compute the policy gradient through backpropagation as value gradient methods. In this paper, we address two limitations of prior value gradient algorithms. The first is that, in contrast to likelihood ratio methods, value gradient algorithms are only suitable for training deterministic policies. Stochastic policies have several advantages: for example, they can be beneficial for partially observed problems; they permit on-policy exploration; and because stochastic policies can assign probability mass to off-policy trajectories, we can train a stochastic policy on samples from an experience database in a principled manner. When an environment model is used, value gradient algorithms have also been critically limited to operation in deterministic environments. By exploiting a mathematical tool known as “re-parameterization” that has found recent use for generative models, we extend the scope of value gradient algorithms to include the optimization of stochastic policies in stochastic environments. We thus describe our framework as Stochastic Value Gradient methods. Secondly, we show that an environment dynamics model, value function, and policy can be learned jointly with neural networks based only on environment interaction. Learned dynamics models are often inaccurate, which we mitigate by computing value gradients along real system trajectories instead of planned ones, a feature shared by model-free methods. This substantially reduces the impact of model error because we only use models to compute policy gradients, not for prediction, combining advantages of model-based and model-free methods with fewer of their drawbacks. We present several algorithms that range from model-based to model-free methods, flexibly combining models of environment dynamics with value functions to optimize policies in stochastic or deterministic environments. Experimentally, we demonstrate that SVG methods can be applied using generic neural networks with tens of thousands of parameters while making minimal assumptions about plans or environments. By examining a simple stochastic control problem, we show that SVG algorithms can optimize policies where model-based planning and likelihood ratio methods cannot. We provide evidence that value function approximation can compensate for degraded models, demonstrating the increased robustness of SVG methods over model-based planning. Finally, we use SVG algorithms to solve a variety of challenging, under-actuated, physical control problems, including swimming of snakes, reaching, tracking, and grabbing with a robot arm, fall-recovery for a monoped, and locomotion for a planar cheetah and biped."

----
>	"In policy-based and actor-critic methods, stochastic policy is usually defined as a fixed distribution over action domain with parameters whose values are adapted when training. SVG suggests a synthesis of model-based with model-free approaches that allows optimizing the distribution as a function by means of the standard gradient descent."

>	"Stochastic value gradients generalize DPG to stochastic policies in a number of ways, giving a spectrum from model-based to model-free algorithms. While SVG(0) is a direct stochastic generalization of DPG, SVG(1) combines an actor, critic and model f. The actor is trained through a combination of gradients from the critic, model and reward simultaneously."

----
>	"SVG tackles the problem of compounding model errors by using observations from the real environment, instead of the imagined one. To accommodate mismatch between model predictions and real transitions, the dynamics models in SVG are probabilistic. The policy is improved by computing the analytic gradient of the real trajectories with respect to the policy. Re-parametrization trick is used to permit back-propagation through the stochastic sampling."

>	- generalizes DPG to stochastic policies in a number of ways, giving spectrum from model-based to model-free algorithms  
>	- while SVG(0) is direct stochastic generalization of DPG, SVG(1) combines actor, critic and environment dynamics model  
>	- SVG can be used both with (SVG(0) and SVG(1)) and without (SVG(∞)) value critics  
>	- SVG can be used both with (SVG(∞) and SVG(1)) and without (SVG(0)) environment dynamics models  
>	- actor is trained through combination of gradients from critic, model and reward simultaneously  

  - `video` <https://youtu.be/PYdL7bcn_cM> (demo)
  - `video` <https://youtu.be/rO7Dx8pSJQw?t=50m> (Schulman)
  - `video` <http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/#t=3724> (Abbeel)
  - `video` <https://youtu.be/mrgJ53TIcQc?t=1h10m31s> (Seleznev) `in russian`
  - `notes` <http://www.shortscience.org/paper?bibtexKey=journals/corr/1510.09142>
  - `post` <https://bayesgroup.github.io/sufficient-statistics/posts/learning-continuous-control-policies-by-stochastic-value-gradients/> `in russian`


#### ["Reinforced Variational Inference"](http://approximateinference.org/accepted/WeberEtAl2015.pdf) Weber, Heess, Eslami, Schulman, Wingate, Silver
>	"Recent years have seen an increase in the complexity and scale of probabilistic models used to understand and analyze data, with a corresponding increase in the difficulty of performing inference. An important enabling factor in this context has been the development of stochastic gradient algorithms for learning variational approximations to posterior distributions. In a separate line of work researchers have been investigating how to use probabilistic inference for the problem of optimal control. By viewing control as an inference problem, they showed that they could ‘borrow’ algorithms from the inference literature (e.g. belief propagation) and turn them into control algorithms. In this work, we do just the opposite: we formally map the problem of learning approximate posterior distributions in variational inference onto the policy optimization problem in reinforcement learning, explaining this connection at two levels. We first provide a high level connection, where draws from the approximate posterior correspond to trajectory samples, free energies to expected returns, and where the core computation involves computing gradients of expectations. We follow by a more detailed, sequential mapping where Markov Decision Processes concepts (state, action, rewards and transitions) are clearly defined in the inference context. We then illustrate how this allows us to leverage ideas from RL for inference network learning, for instance by introducing the concept of value functions in sequential variational inference. For concreteness and simplicity, in the main text we focus on inference for a particular model class and derive the general case in the appendix."


#### ["Reward Augmented Maximum Likelihood for Neural Structured Prediction"](https://arxiv.org/abs/1609.00150) Norouzi, Bengio, Chen, Jaitly, Schuster, Wu, Schuurmans
>	"A key problem in structured output prediction is direct optimization of the task reward function that matters for test evaluation. This paper presents a simple and computationally efficient approach to incorporate task reward into a maximum likelihood framework. We establish a connection between the log-likelihood and regularized expected reward objectives, showing that at a zero temperature, they are approximately equivalent in the vicinity of the optimal solution. We show that optimal regularized expected reward is achieved when the conditional distribution of the outputs given the inputs is proportional to their exponentiated (temperature adjusted) rewards. Based on this observation, we optimize conditional log-probability of edited outputs that are sampled proportionally to their scaled exponentiated reward. We apply this framework to optimize edit distance in the output label space. Experiments on speech recognition and machine translation for neural sequence to sequence models show notable improvements over a maximum likelihood baseline by using edit distance augmented maximum likelihood."

>	"Neural sequence models use a maximum likelihood framework to maximize the conditional probability of the ground-truth outputs given corresponding inputs. These models do not explicitly consider the task reward during training, hoping that conditional log-likelihood would serve as a good surrogate for the task reward. Such methods make no distinction between alternative incorrect outputs: log-probability is only measured on the ground-truth input-output pairs, and all alternative outputs are equally penalized, whether near or far from the ground-truth target. We believe that one can improve upon maximum likelihood sequence models, if the difference in the rewards of alternative outputs is taken into account. A key property of ML training for locally normalized RNN models is that the objective function factorizes into individual loss terms, which could be efficiently optimized using stochastic gradient descend. In particular, ML training does not require any form of inference or sampling from the model during training, which leads to computationally efficient and easy to implementations."

>	"Alternatively, one can use reinforcement learning algorithms, such as policy gradient, to optimize expected task reward during training. Even though expected task reward seems like a natural objective, direct policy optimization faces significant challenges: unlike ML, the gradient for a mini-batch of training examples is extremely noisy and has a high variance; gradients need to be estimated via sampling from the model, which is a non-stationary distribution; the reward is often sparse in a high-dimensional output space, which makes it difficult to find any high value predictions, preventing learning from getting off the ground; and, finally, maximizing reward does not explicitly consider the supervised labels, which seems inefficient. In fact, all previous attempts at direct policy optimization for structured output prediction has started by bootstrapping from a previously trained ML solution and they use several heuristics and tricks to make learning stable."

>	"This paper presents a new approach to task reward optimization that combines the computational efficiency and simplicity of ML with the conceptual advantages of expected reward maximization. Our algorithm called reward augmented maximum likelihood simply adds a sampling step on top of the typical likelihood objective. Instead of optimizing conditional log-likelihood on training input-output pairs, given each training input, we first sample an output proportional to its exponentiated scaled reward. Then, we optimize log-likelihood on such auxiliary output samples given corresponding inputs. When the reward for an output is defined as its similarity to a ground-truth output, then the output sampling distribution is peaked at the ground-truth output, and its concentration is controlled by a temperature hyper-parameter."

>	"Surprisingly, we find that the best performance is achieved with output sampling distributions that put a lot of the weight away from the ground-truth outputs. In fact, in our experiments, the training algorithm rarely sees the original unperturbed outputs. Our results give further evidence that models trained with imperfect outputs and their reward values can improve upon models that are only exposed to a single ground-truth output per input."

>	"There are several critical differences between gradient estimators for RML loss (reward augmented maximum likelihood) and RL loss (regularized expected reward) that make SGD optimization of RML loss more desirable. First, for RML loss, one has to sample from a stationary distribution, the so called exponentiated payoff distribution, whereas for RL loss one has to sample from the model distribution as it is evolving. Not only sampling from the model could slow down training, but also one needs to employ several tricks to get a better estimate of the gradient of RL loss. Further, the reward is often sparse in a high-dimensional output space, which makes finding any reasonable predictions challenging, when RL loss is used to refine a randomly initialized model. Thus, smart model initialization is needed. By contrast, we initialize the models randomly and refine them using RML loss."

----
>	"This reads as another way to use a world model to mitigate the sample complexity of reinforcement learning (e.g., what if edit distance was just the initial model of the reward?)."

----
>	"Andrej Karpathy provided another perspective: We can also view the process of optimizing LRML as distilling the exponentiated payoff distribution q(y|y*;τ) into the model pθ(y|x). The objective reaches a maximum when these two distributions are equivalent. From this distillation view, the question is clear: how can we distill more complex objects into pθ? Concretely, this means we should develop more complex reward distributions q to use in this setup. We have seen two examples so far: the exponentiated payoff from the paper and the label smoothing example of the previous section. We could define q to be a complex pre-trained model or a mixture of experts, and use this training process to distill them into a single model pθ. We just need to make sure that we can efficiently sample from the q we select."

----
>	"Alec Radford mentioned that the data augmentation suggested in the paper sounds similar in spirit to virtual adversarial training, where the current model is encouraged to make robust predictions not only for the examples in the training set but also for inputs “nearby” those that exist in the training set. A high-level comparison:  
>	- Adversarial training can be seen as data-augmentation in the input space X. The RML objective does data-augmentation in the output space Y.  
>	- Adversarial training performs model-based data augmentation: the examples generated are those for which the current model is maximally vulnerable. RML training performs data-based augmentation: the examples generated have outputs that are “near” the ground-truth outputs. (Here 'near' is defined by the reward function.)"  

  - `video` ["Towards a Unified View of Supervised Learning and Reinforcement Learning"](https://youtu.be/fZNyHoXgV7M?t=24m59s) (Norouzi)
  - `video` <https://youtu.be/uohtFXD_39c?t=38m10s> (Samy Bengio)
  - `video` <http://youtube.com/watch?v=agA-rc71Uec> (Samy Bengio)
  - `video` <https://vimeo.com/240428387#t=58m19s> (Jaitly)
  - `notes` <http://drive.google.com/file/d/0B3Rdm_P3VbRDVUQ4SVBRYW82dU0> (Gauthier)
  - `notes` <http://www.shortscience.org/paper?bibtexKey=journals/corr/1609.00150>
  - `notes` <http://www.shortscience.org/paper?bibtexKey=conf%2Fnips%2FNorouziBCJSWS16>
  - `paper` ["Softmax Q-Distribution Estimation for Structured Prediction: A Theoretical Interpretation for RAML"](https://arxiv.org/abs/1705.07136) by Ma et al.


#### ["Reinforcement Learning with Deep Energy-Based Policies"](https://arxiv.org/abs/1702.08165) Haarnoja, Tang, Abbeel, Levine
  `SQL` `soft Q-learning` `policy gradient` `maximum entropy policy`
>	"We propose a method for learning expressive energy-based policies for continuous states and actions, which has been feasible only in tabular domains before. We apply our method to learning maximum entropy policies, resulting into a new algorithm, called soft Q-learning, that expresses the optimal policy via a Boltzmann distribution. We use the recently proposed amortized Stein variational gradient descent to learn a stochastic sampling network that approximates samples from this distribution. The benefits of the proposed algorithm include improved exploration and compositionality that allows transferring skills between tasks, which we confirm in simulated experiments with swimming and walking robots. We also draw a connection to actor-critic methods, which can be viewed performing approximate inference on the corresponding energy-based model."

>	"Fox et al. (2015) proposed soft Q-learning which extended the Q-learning with tabular form for the new Bellman optimality equation corresponding to the finite state finite action entropy-regularized MDP. The algorithm does not accomodate for function approximator due to the intractability of the log-sum-exp operation in the soft Q-learning update. To avoid such difficulty, Haarnoja et al. (2017) reformulates the update as an optimization which is approximated by samples from stein variational gradient descent (SVGD) sampler."

  - <https://sites.google.com/view/softqlearning/home> (demo)
  - `post` <http://bair.berkeley.edu/blog/2017/10/06/soft-q-learning/>
  - `video` <https://youtu.be/Y2XBiUtZo1k?t=12m38s> (Abbeel)
  - `video` <https://youtube.com/watch?v=IAJ1LywY6Zg> (Levine)
  - `video` <https://livestream.com/newyorkacademyofsciences/ml2018-2/videos/171320389> (14:47) (Levine)
  - `video` <https://vimeo.com/240428644#t=1h16m18s> (Levine)
  - `paper` ["Taming the Noise in Reinforcement Learning via Soft Updates"](https://arxiv.org/abs/1512.08562) by Fox, Pakman, Tishby


#### ["Equivalence Between Policy Gradients and Soft Q-Learning"](https://arxiv.org/abs/1704.06440) Schulman, Chen, Abbeel
  `soft Q-learning` `policy gradient` `maximum entropy policy`
>	"Two of the leading approaches for model-free reinforcement learning are policy gradient methods and Q-learning methods. Q-learning methods can be effective and sample-efficient when they work, however, it is not well-understood why they work, since empirically, the Q-values they estimate are very inaccurate. A partial explanation may be that Q-learning methods are secretly implementing policy gradient updates: we show that there is a precise equivalence between Q-learning and policy gradient methods in the setting of entropy-regularized reinforcement learning, that "soft" (entropy-regularized) Q-learning is exactly equivalent to a policy gradient method. We also point out a connection between Q-learning methods and natural policy gradient methods. Experimentally, we explore the entropy-regularized versions of Q-learning and policy gradients, and we find them to perform as well as (or slightly better than) the standard variants on the Atari benchmark. We also show that the equivalence holds in practical settings by constructing a Q-learning method that closely matches the learning dynamics of A3C without using a target network or ϵ-greedy exploration schedule."

  - `video` <https://youtube.com/watch?v=IAJ1LywY6Zg> (Levine)
  - `video` <https://livestream.com/newyorkacademyofsciences/ml2018-2/videos/171320389> (14:47) (Levine)
  - `video` <https://vimeo.com/240428644#t=1h16m18s> (Levine)
  - `video` <https://youtu.be/Y2XBiUtZo1k?t=1h47s> (Abbeel)
  - `video` <https://youtube.com/watch?v=gmWmQZvg6hA> + <https://youtube.com/watch?v=KMf6AANMMx0> (Konobeev) `in russian`
  - `post` <http://bair.berkeley.edu/blog/2017/10/06/soft-q-learning/>


#### ["A Unified View of Entropy-Regularized Markov Decision Processes"](https://arxiv.org/abs/1705.07798) Neu, Gomez, Jonsson
  `soft Q-learning` `policy gradient` `maximum entropy policy`
>	"We propose a general framework for entropy-regularized average-reward reinforcement learning in Markov decision processes (MDPs). Our approach is based on extending the linear-programming formulation of policy optimization in MDPs to accommodate convex regularization functions. Our key result is showing that using the conditional entropy of the joint state-action distributions as regularization yields a dual optimization problem closely resembling the Bellman optimality equations. This result enables us to formalize a number of state-of-the-art entropy-regularized reinforcement learning algorithms as approximate variants of Mirror Descent or Dual Averaging, and thus to argue about the convergence properties of these methods. In particular, we show that the exact version of the TRPO algorithm of Schulman et al. (2015) actually converges to the optimal policy, while the entropy-regularized policy gradient methods of Mnih et al. (2016) may fail to converge to a fixed point. Finally, we illustrate empirically the effects of using various regularization techniques on learning performance in a simple reinforcement learning setup."

  - `video` <http://videocrm.ca/Machine18/Machine18-20180426-1-GergelyNeu.mp4> (Neu)


#### ["Soft Actor-Critic: Off-Policy Maximum Entropy Deep Reinforcement Learning with a Stochastic Actor"](https://arxiv.org/abs/1801.01290) Haarnoja, Zhou, Abbeel, Levine
  `SAC` `soft Q-learning` `policy gradient` `maximum entropy policy` `on-policy + off-policy`
>	"Model-free deep reinforcement learning algorithms have been demonstrated on a range of challenging decision making and control tasks. However, these methods typically suffer from two major challenges: very high sample complexity and brittle convergence properties, which necessitate meticulous hyperparameter tuning. Both of these challenges severely limit the applicability of such methods to complex, real-world domains. In this paper, we propose soft actor-critic, an off-policy actor-critic deep RL algorithm based on the maximum entropy reinforcement learning framework. In this framework, the actor aims to maximize expected reward while also maximizing entropy. That is, to succeed at the task while acting as randomly as possible. Prior deep RL methods based on this framework have been formulated as Q-learning methods. By combining off-policy updates with a stable stochastic actor-critic formulation, our method achieves state-of-the-art performance on a range of continuous control benchmark tasks, outperforming prior on-policy and off-policy methods. Furthermore, we demonstrate that, in contrast to other off-policy algorithms, our approach is very stable, achieving very similar performance across different random seeds."

>	"Soft Q-learning algorithm for learning multi-modal stochastic policies via entropy maximization, leading to better exploration in environments with multi-modal reward landscapes, combined with actor-critic framework into Soft Actor-Critic, an off-policy actor-critic method in which the actor aims to maximize both the expected reward and the entropy of a stochastic policy."  
>	"SAC learns the soft Q-function of policy and the policy jointly. SAC is similar to DDPG but with a stochastic policy."  
>	"DDPG uses a Q-function estimator to enable off-policy learning, and a deterministic actor that maximizes this Q-function. As such, this method can be viewed both as a deterministic actor-critic algorithm and an approximate Q-learning algorithm. Unfortunately, the interplay between the deterministic actor network and the Q-function typically makes DDPG extremely difficult to stabilize and brittle to hyperparameter settings. As a consequence, it is difficult to extend DDPG to very complex, high-dimensional tasks, and on-policy policy gradient methods still tend to produce the best results in such settings. Our method instead combines off-policy actor-critic training with a stochastic actor, and further aims to maximize the entropy of this actor with an entropy maximization objective. We find that this actually results in a substantially more stable and scalable algorithm that, in practice, exceeds both the efficiency and final performance of DDPG."  
>	"Many actor-critic algorithms build on the standard, on-policy policy gradient formulation to update the actor, and many of them also consider the entropy of the policy, but instead of maximizing the entropy, they use it as an regularizer. This tends to improve stability, but results in very poor sample complexity. Maximum entropy reinforcement learning optimizes policies to maximize both the expected return and the expected entropy of the policy."  
>	"SAC is particularly well-suited for model-based RL as it uses an objective that (i) improves policy robustness which hinders adversarial model exploitation and (ii) develops multi-modal policies which could mitigate negative effects of planning with inaccurate models."  
>	"SAC implicitly acts as an empowerment-based directed exploration method (Mohamed & Rezende, 2015) due to its entropy bonus."  

  - `post` <http://bair.berkeley.edu/blog/2018/12/14/sac>
  - `post` <https://ai.googleblog.com/2019/01/soft-actor-critic-deep-reinforcement.html>
  - `video` <https://vimeo.com/252185258>
  - `video` <https://facebook.com/icml.imls/videos/430993334081854?t=6485> (Haarnoja)
  - `video` <https://livestream.com/newyorkacademyofsciences/ml2018-2/videos/171320389> (14:47) (Levine)
  - `video` <https://youtu.be/IAJ1LywY6Zg?t=21m4s> (Levine)
  - `video` <https://youtu.be/jAPJeJK18mw?t=24m45s> (Levine)
  - `video` <https://youtu.be/Y2XBiUtZo1k?t=41m37s> (Abbeel)
  - `video` <https://youtu.be/eeJ1-bUnwRI?t=1h51m28s> (Sigaud)
  - `video` <https://youtube.com/watch?v=IgNC1J25Ls8> (Grinchuk) `in russian`
  - `video` <https://youtube.com/watch?v=NiTJOw1aST4> (Grinchuk) `in russian`
  - `video` <https://youtu.be/OSzynwC1gow?t=14m58s> (Mosin) `in russian`
  - `post` <https://spinningup.openai.com/en/latest/algorithms/sac.html>
  - `notes` <https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html#sac>
  - `notes` <https://github.com/Scitator/papers/blob/master/papers/1801_soft_ac.md>
  - `code` <https://github.com/rail-berkeley/softlearning>
  - `code` <https://github.com/vitchyr/rlkit>
  - `code` <https://github.com/haarnoja/sac>
  - `paper` ["Reinforcement Learning and Control as Probabilistic Inference: Tutorial and Review"](https://arxiv.org/abs/1805.00909) by Levine ([talk](https://youtu.be/iOYiPhu5GEk?t=2m34s) `video`)
  - `paper` ["Soft Actor-Critic Algorithms and Applications"](https://arxiv.org/abs/1812.05905) by Haarnoja et al. ([notes](https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html#sac-with-automatically-adjusted-temperature))
  - `paper` ["Learning to Walk via Deep Reinforcement Learning"](https://arxiv.org/abs/1812.11103) by Haarnoja et al.
  - `paper` ["Learning to Walk in the Real World with Minimal Human Effort"](https://arxiv.org/abs/2002.08550) by Ha et al.



---
### interesting papers - imitation learning

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---imitation) on imitation learning

[papers](https://github.com/kristery/Awesome-Imitation-Learning)

----
#### ["A Reduction of Imitation Learning and Structured Prediction to No-Regret Online Learning"](https://arxiv.org/abs/1011.0686) Ross, Gordon, Bagnell
  `DAGGER`
>	"Sequential prediction problems such as imitation learning, where future observations depend on previous predictions (actions), violate the common i.i.d. assumptions made in statistical learning. This leads to poor performance in theory and often in practice. Some recent approaches (Daumé III et al., 2009; Ross and Bagnell, 2010) provide stronger guarantees in this setting, but remain somewhat unsatisfactory as they train either non-stationary or stochastic policies and require a large number of iterations. In this paper, we propose a new iterative algorithm, which trains a stationary deterministic policy, that can be seen as a no regret algorithm in an online learning setting. We show that any such no regret algorithm, combined with additional reduction assumptions, must find a policy with good performance under the distribution of observations it induces in such sequential settings. We demonstrate that this new approach outperforms previous approaches on two challenging imitation learning problems and a benchmark sequence labeling problem."

>	"We show that by batching over iterations of interaction with a system, no-regret methods, including the presented DAGGER approach can provide a learning reduction with strong performance guarantees in both imitation learning and structured prediction. In future work, we will consider more sophisticated strategies than simple greedy forward decoding for structured prediction, as well as using base classifiers that rely on Inverse Optimal Control (Abbeel and Ng, 2004; Ratliff et al., 2006) techniques to learn a cost function for a planner to aid prediction in imitation learning. Further we believe techniques similar to those presented, by leveraging a cost-to-go estimate, may provide an understanding of the success of online methods for reinforcement learning and suggest a similar data-aggregation method that can guarantee performance in such settings."

----
>	DAGGER = Dataset Aggregation

>	"non i.i.d. supervised learning from oracle demonstrations under own state distribution"

  - `video` <https://youtu.be/TUBBIgtQL_k?t=17m26s> + <https://youtu.be/6PYJFUu3eLQ?t=45s> (Levine)
  - `video` <https://youtu.be/kl_G95uKTHw?t=1h5m38s> (Levine)
  - `video` <http://videolectures.net/aistats2011_ross_reduction> (Ross)
  - `video` <https://youtube.com/watch?v=ZMhO1FO_j0o> (Ross)
  - `video` <https://youtu.be/0DkPUecLLpI?t=35s> (Ratnikov) `in russian`
  - `paper` <http://ciml.info/dl/v0_99/ciml-v0_99-ch18.pdf> (Daume)
  - `paper` ["Deeply AggreVaTeD: Differentiable Imitation Learning for Sequential Prediction"](https://arxiv.org/abs/1703.01030) by Sun et al.


#### ["Guided Policy Search"](http://vladlen.info/papers/guided-policy-search.pdf) Levine, Koltun
>	"Direct policy search can effectively scale to high-dimensional systems, but complex policies with hundreds of parameters often present a challenge for such methods, requiring numerous samples and often falling into poor local optima. We present a guided policy search algorithm that uses trajectory optimization to direct policy learning and avoid poor local optima. We show how differential dynamic programming can be used to generate suitable guiding samples, and describe a regularized importance sampled policy optimization that incorporates these samples into the policy search. We evaluate the method by learning neural network controllers for planar swimming, hopping, and walking, as well as simulated 3D humanoid running."

>	"In this paper, we show how trajectory optimization can guide the policy search away from poor local optima. Our guided policy search algorithm uses differential dynamic programming to generate “guiding samples”, which assist the policy search by exploring high-reward regions. An importance sampled variant of the likelihood ratio estimator is used to incorporate these guiding samples directly into the policy search. We show that DDP can be modified to sample from a distribution over high reward trajectories, making it particularly suitable for guiding policy search. Furthermore, by initializing DDP with example demonstrations, our method can perform learning from demonstration. The use of importance sampled policy search also allows us to optimize the policy with second order quasi-Newton methods for many gradient steps without requiring new on-policy samples, which can be crucial for complex, nonlinear policies. Our main contribution is a guided policy search algorithm that uses trajectory optimization to assist policy learning. We show how to obtain suitable guiding samples, and we present a regularized importance sampled policy optimization method that can utilize guiding samples and does not require a learning rate or new samples at every gradient step. We evaluate our method on planar swimming, hopping, and walking, as well as 3D humanoid running, using general-purpose neural network policies. We also show that both the proposed sampling scheme and regularizer are essential for good performance, and that the learned policies can generalize successfully to new environments."

>	"Standard likelihood ratio methods require new samples from the current policy at each gradient step, do not admit off-policy samples, and require the learning rate to be chosen carefully to ensure convergence. We discuss how importance sampling can be used to lift these constraints."

>	"Prior methods employed importance sampling to reuse samples from previous policies. However, when learning policies with hundreds of parameters, local optima make it very difficult to find a good solution. In this section, we show how differential dynamic programming can be used to supplement the sample set with off-policy guiding samples that guide the policy search to regions of high reward."

>	"We incorporate guiding samples into the policy search by building one or more initial DDP solutions and supplying the resulting samples to the importance sampled policy search algorithm. These solutions can be initialized with human demonstrations or with an offline planning algorithm. When learning from demonstrations, we can perform just one step of DDP starting from the example demonstration, thus constructing a Gaussian distribution around the example. If adaptive guiding distributions are used, they are constructed at each iteration of the policy search starting from the previous DDP solution. Although our policy search component is model-free, DDP requires a model of the system dynamics. Numerous recent methods have proposed to learn the model, and if we use initial examples, only local models are required. One might also wonder why the DDP policy is not itself a suitable controller. The issue is that this policy is time-varying and only valid around a single trajectory, while the final policy can be learned from many DDP solutions in many situations. Guided policy search can be viewed as transforming a collection of trajectories into a controller. This controller can adhere to any parameterization, reflecting constraints on computation or available sensors in partially observed domains. In our evaluation, we show that such a policy generalizes to situations where the DDP policy fail."

>	"Policy gradient methods often require on-policy samples at each gradient step, do not admit off-policy samples, and cannot use line searches or higher order optimization methods such as LBFGS, which makes them difficult to use with complex policy classes. Our approach follows prior methods that use importance sampling to address these challenges. While these methods recycle samples from previous policies, we also introduce guiding samples, which dramatically speed up learning and help avoid poor local optima. We also regularize the importance sampling estimator, which prevents the optimization from assigning low probabilities to all samples. The regularizer controls how far the policy deviates from the samples, serving a similar function to the natural gradient, which bounds the information loss at each iteration. Unlike Tang and Abbeel’s ESS constraint, our regularizer does not penalize reliance on a few samples, but does avoid policies that assign a low probability to all samples. Our evaluation shows that the regularizer can be crucial for learning effective policies."

>	"We presented a guided policy search algorithm that can learn complex policies with hundreds of parameters by incorporating guiding samples into the policy search. These samples are drawn from a distribution built around a DDP solution, which can be initialized from demonstrations. We evaluated our method using general-purpose neural networks on a range of challenging locomotion tasks, and showed that the learned policies generalize to new environments. While our policy search is model-free, it is guided by a model-based DDP algorithm. A promising avenue for future work is to build the guiding distributions with model-free methods that either build trajectory following policies or perform stochastic trajectory optimization. Our rough terrain results suggest that GPS can generalize by learning basic locomotion principles such as balance. Further investigation of generalization is an exciting avenue for future work. Generalization could be improved by training on multiple environments, or by using larger neural networks with multiple layers or recurrent connections. It would be interesting to see whether such extensions could learn more general and portable concepts, such as obstacle avoidance, perturbation recoveries, or even higher-level navigation skills."

----
>	"DAgger vs GPS:  
>	- DAgger does not require an adaptive expert  
>	  * Any expert will do, so long as states from learned policy can be labeled  
>	  * Assumes it is possible to match expert's behavior up to bounded loss (not always possible, e.g. in partially observed domains)  
>	- GPS adapts the expert behavior to learning agent  
>	  * Does not require bounded loss on initial expert (expert will change)"  

----
>	"Use (modification of) importance sampling to get policy gradient, where samples are obtained via trajectory optimization."

  - <https://graphics.stanford.edu/projects/gpspaper/index.htm> (demo)
  - <http://rll.berkeley.edu/gps/>
  - `video` <http://youtube.com/watch?v=o0Ebur3aNMo> (Levine)
  - `video` <http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/> (Abbeel, part 2)
  - `video` <http://youtube.com/watch?v=EtMyH_--vnU> (Levine)
  - `video` <https://video.seas.harvard.edu/media/ME+Sergey+Levine+2015+-04-01/1_gqqp9r3o/23375211> (Levine)
  - `video` <http://youtube.com/watch?v=xMHjkZBvnfU> (Abbeel)
  - `code` <https://github.com/cbfinn/gps>
  - `code` <https://github.com/nivwusquorum/guided-policy-search/>


#### ["Learning Neural Network Policies with Guided Policy Search under Unknown Dynamics"](https://papers.nips.cc/paper/5444-learning-neural-network-policies-with-guided-policy-search-under-unknown-dynamics) Levine, Abbeel
>	"We present a policy search method that uses iteratively refitted local linear models to optimize trajectory distributions for large, continuous problems. These trajectory distributions can be used within the framework of guided policy search to learn policies with an arbitrary parameterization. Our method fits time-varying linear dynamics models to speed up learning, but does not rely on learning a global model, which can be difficult when the dynamics are complex and discontinuous. We show that this hybrid approach requires many fewer samples than model-free methods, and can handle complex, nonsmooth dynamics that can pose a challenge for model-based techniques. We present experiments showing that our method can be used to learn complex neural network policies that successfully execute simulated robotic manipulation tasks in partially observed environments with numerous contact discontinuities and underactuation."

  - <http://rll.berkeley.edu/nips2014gps/> (demo)
  - `video` <http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/> (Abbeel, part 2)
  - `code` <https://github.com/nivwusquorum/guided-policy-search/>


#### ["Learning Contact-Rich Manipulation Skills with Guided Policy Search"](http://arxiv.org/abs/1501.05611) Levine, Wagener, Abbeel
>	"Autonomous learning of object manipulation skills can enable robots to acquire rich behavioral repertoires that scale to the variety of objects found in the real world. However, current motion skill learning methods typically restrict the behavior to a compact, low-dimensional representation, limiting its expressiveness and generality. In this paper, we extend a recently developed policy search method and use it to learn a range of dynamic manipulation behaviors with highly general policy representations, without using known models or example demonstrations. Our approach learns a set of trajectories for the desired motion skill by using iteratively refitted time-varying linear models, and then unifies these trajectories into a single control policy that can generalize to new situations. To enable this method to run on a real robot, we introduce several improvements that reduce the sample count and automate parameter selection. We show that our method can acquire fast, fluent behaviors after only minutes of interaction time, and can learn robust controllers for complex tasks, including stacking large lego blocks, putting together a plastic toy, placing wooden rings onto tight-fitting pegs, and screwing bottle caps onto bottles."

>	"The central idea behind guided policy search is to decompose the policy search problem into alternating trajectory optimization and supervised learning phases, where trajectory optimization is used to find a solution to the control problem and produce training data that is then used in the supervised learning phase to train a nonlinear, high-dimensional policy. By training a single policy from multiple trajectories, guided policy search can produce complex policies that generalize effectively to a range of initial states."

  - <http://rll.berkeley.edu/icra2015gps/> (demo)
  - `video` <http://youtube.com/watch?t=35&v=JeVppkoloXs> + <http://youtube.com/watch?v=oQasCj1X0e8> (demo)
  - `video` <http://videolectures.net/deeplearning2016_abbeel_deep_reinforcement/> (Abbeel, part 2)
  - `video` <http://youtube.com/watch?v=EtMyH_--vnU> (Levine)
  - `video` <https://video.seas.harvard.edu/media/ME+Sergey+Levine+2015+-04-01/1_gqqp9r3o/23375211> (Levine)
  - `video` <http://youtube.com/watch?v=xMHjkZBvnfU> (Abbeel)


#### ["End-to-End Training of Deep Visuomotor Policies"](http://arxiv.org/abs/1504.00702) Levine, Finn, Darrell, Abbeel
>	"Policy search methods based on reinforcement learning and optimal control can allow robots to automatically learn a wide range of tasks. However, practical applications of policy search tend to require the policy to be supported by hand-engineered components for perception, state estimation, and low-level control. We propose a method for learning policies that map raw, low-level observations, consisting of joint angles and camera images, directly to the torques at the robot's joints. The policies are represented as deep convolutional neural networks with 92,000 parameters. The high dimensionality of such policies poses a tremendous challenge for policy search. To address this challenge, we develop a sensorimotor guided policy search method that can handle high-dimensional policies and partially observed tasks. We use BADMM to decompose policy search into an optimal control phase and supervised learning phase, allowing CNN policies to be trained with standard supervised learning techniques. This method can learn a number of manipulation tasks that require close coordination between vision and control, including inserting a block into a shape sorting cube, screwing on a bottle cap, fitting the claw of a toy hammer under a nail with various grasps, and placing a coat hanger on a clothes rack."

  - <https://sites.google.com/site/visuomotorpolicy/home> (demo)
  - `video` <http://youtube.com/watch?v=EtMyH_--vnU> (Levine)
  - `video` <https://video.seas.harvard.edu/media/ME+Sergey+Levine+2015+-04-01/1_gqqp9r3o/23375211> (Levine)
  - `video` <http://youtube.com/watch?v=xMHjkZBvnfU> (Abbeel)
  - `code` <http://rll.berkeley.edu/gps/>



---
### interesting papers - inverse reinforcement learning

[**interesting recent papers**](https://github.com/brylevkirill/notes/blob/master/interesting%20recent%20papers.md#reinforcement-learning---imitation)

----
#### ["Maximum Entropy Deep Inverse Reinforcement Learning"](http://arxiv.org/abs/1507.04888) Wulfmeier, Ondruska, Posner
>	"This paper presents a general framework for employing deep architectures - in particular neural networks - to solve the inverse reinforcement learning (IRL) problem. Specifically, we propose to exploit the representational capacity and favourable computational complexity of deep networks to approximate complex, nonlinear reward functions. We show that the Maximum Entropy paradigm for IRL lends itself naturally to the efficient training of deep architectures. At test time, the approach leads to a computational complexity independent of the number of demonstrations. This makes it especially well-suited for applications in life-long learning scenarios commonly encountered in robotics. We demonstrate that our approach achieves performance commensurate to the state-of-the-art on existing benchmarks already with simple, comparatively shallow network architectures while significantly outperforming the state-of-the-art on an alternative benchmark based on more complex, highly varying reward structures representing strong interactions between features. Furthermore, we extend the approach to include convolutional layers in order to eliminate the dependency on precomputed features of current algorithms and to underline the substantial gain in flexibility in framing IRL in the context of deep learning."

  - `video` <https://youtu.be/d9DlQSJQAoI?t=7m16s> (Finn)
  - `code` <https://github.com/stormmax/irl-imitation>


#### ["Guided Cost Learning: Deep Inverse Optimal Control via Policy Optimization"](https://arxiv.org/abs/1603.00448) Finn, Levine, Abbeel
>	"Reinforcement learning can acquire complex behaviors from high-level specifications. However, defining a cost function that can be optimized effectively and encodes the correct task is challenging in practice. We explore how inverse optimal control can be used to learn behaviors from demonstrations, with applications to torque control of high-dimensional robotic systems. Our method addresses two key challenges in inverse optimal control: first, the need for informative features and effective regularization to impose structure on the cost, and second, the difficulty of learning the cost function under unknown dynamics for high-dimensional continuous systems. To address the former challenge, we present an algorithm capable of learning arbitrary nonlinear cost functions, such as neural networks, without meticulous feature engineering. To address the latter challenge, we formulate an efficient sample-based approximation for MaxEnt IOC. We evaluate our method on a series of simulated tasks and real-world robotic manipulation problems, demonstrating substantial improvement over prior methods both in terms of task complexity and sample efficiency."

----
>	"technique that lets one apply Maximum Entropy Inverse Optimal Control without the double-loop procedure and using policy gradient techniques"

  - `video` <https://youtube.com/watch?v=hXxaepw0zAw> (demo)
  - `video` <http://techtalks.tv/talks/guided-cost-learning-deep-inverse-optimal-control-via-policy-optimization/62472/> (Finn)
  - `video` <https://youtu.be/d9DlQSJQAoI?t=18m17s> (Finn)
  - `video` <https://channel9.msdn.com/Events/Neural-Information-Processing-Systems-Conference/Neural-Information-Processing-Systems-Conference-NIPS-2016/Deep-Learning-Symposium-Session-3> (22:48) (Levine)
  - `video` <https://youtu.be/0DkPUecLLpI?t=17m32s> (Ratnikov) `in russian`


#### ["Model-Free Imitation Learning with Policy Optimization"](http://arxiv.org/abs/1605.08478) Ho, Gupta, Ermon
>	"In imitation learning, an agent learns how to behave in an environment with an unknown cost function by mimicking expert demonstrations. Existing imitation learning algorithms typically involve solving a sequence of planning or reinforcement learning problems. Such algorithms are therefore not directly applicable to large, high-dimensional environments, and their performance can significantly degrade if the planning problems are not solved to optimality. Under the apprenticeship learning formalism, we develop alternative model-free algorithms for finding a parameterized stochastic policy that performs at least as well as an expert policy on an unknown cost function, based on sample trajectories from the expert. Our approach, based on policy gradients, scales to large continuous environments with guaranteed convergence to local minima."

>	"We showed that carefully blending state-of-the-art policy gradient algorithms for reinforcement learning with local cost function fitting lets us successfully train neural network policies for imitation in high-dimensional, continuous environments. Our method is able to identify a locally optimal solution, even in settings where optimal planning is out of reach. This is a significant advantage over competing algorithms that require repeatedly solving planning problems in an inner loop. In fact, when the inner planning problem is only approximately solved, competing algorithms do not even provide local optimality guarantees (Ermon et al., 2015). Our approach does not use expert interaction or reinforcement signal, fitting in a family of such approaches that includes apprenticeship learning and inverse reinforcement learning. When either of these additional resources is provided, alternative approaches (Kim et al., 2013; Daume III et al., 2009; Ross & Bagnell, 2010; Ross et al., 2011) may be more sample efficient, and investigating ways to combine these resources with our framework is an interesting research direction. We focused on the policy optimization component of apprenticeship learning, rather than the design of appropriate cost function classes. We believe this is an important area for future work. Nonlinear cost function classes have been successful in IRL (Ratliff et al., 2009; Levine et al., 2011) as well as in other machine learning problems reminiscent of ours, in particular that of training generative image models. In the language of generative adversarial networks (Goodfellow et al., 2014), the policy parameterizes a generative model of state-action pairs, and the cost function serves as an adversary. Apprenticeship learning with large cost function classes capable of distinguishing between arbitrary state-action visitation distributions would, enticingly, open up the possibility of exact imitation."

  - `video` <http://techtalks.tv/talks/model-free-imitation-learning-with-policy-optimization/62471/> (Ho)


#### ["Generative Adversarial Imitation Learning"](http://arxiv.org/abs/1606.03476) Ho, Ermon
  `GAIL`
>	"Consider learning a policy from example expert behavior, without interaction with the expert or access to reinforcement signal. One approach is to recover the expert’s cost function with inverse reinforcement learning, then extract a policy from that cost function with reinforcement learning. This approach is indirect and can be slow. We propose a new general framework for directly extracting a policy from data, as if it were obtained by reinforcement learning following inverse reinforcement learning. We show that a certain instantiation of our framework draws an analogy between imitation learning and generative adversarial networks, from which we derive a model-free imitation learning algorithm that obtains significant performance gains over existing model-free methods in imitating complex behaviors in large, high-dimensional environments."

>	"As we demonstrated, our method is generally quite sample efficient in terms of expert data. However, it is not particularly sample efficient in terms of environment interaction during training. The number of such samples required to estimate the imitation objective gradient was comparable to the number needed for TRPO to train the expert policies from reinforcement signals. We believe that we could significantly improve learning speed for our algorithm by initializing policy parameters with behavioral cloning, which requires no environment interaction at all. Fundamentally, our method is model free, so it will generally need more environment interaction than model-based methods. Guided cost learning, for instance, builds upon guided policy search and inherits its sample efficiency, but also inherits its requirement that the model is well-approximated by iteratively fitted time-varying linear dynamics. Interestingly, both our Algorithm 1 and guided cost learning alternate between policy optimization steps and cost fitting (which we called discriminator fitting), even though the two algorithms are derived completely differently. Our approach builds upon a vast line of work on IRL, and hence, just like IRL, our approach does not interact with the expert during training. Our method explores randomly to determine which actions bring a policy’s occupancy measure closer to the expert’s, whereas methods that do interact with the expert, like DAgger, can simply ask the expert for such actions. Ultimately, we believe that a method that combines well-chosen environment models with expert interaction will win in terms of sample complexity of both expert data and environment interaction."

>	"Authors showed that policies are uniquely characterised by their occupancies (visited state and action distributions) allowing IRL to be reduced to the problem of measure matching. With this insight they were able to use generative adversarial training to facilitate reward function learning in a more flexible manner."

  - `video` <https://youtube.com/watch?v=bcnCo9RxhB8> (Ermon)
  - `video` <https://youtu.be/d9DlQSJQAoI?t=22m12s> (Finn)
  - `video` <http://videolectures.net/deeplearning2017_de_freitas_deep_control/#t=4183> (de Freitas)
  - `notes` <http://tsong.me/blog/gail/>
  - `notes` <https://yobibyte.github.io/files/paper_notes/Generative_Adversarial_Imitation_Learning__Ho_Ermon__2017.pdf>
  - `code` <https://github.com/openai/imitation>


#### ["Inferring The Latent Structure of Human Decision-Making from Raw Visual Inputs"](https://arxiv.org/abs/1703.08840) Li, Song, Ermon
  `InfoGAIL`
>	"The goal of imitation learning is to match example expert behavior, without access to a reinforcement signal. Expert demonstrations provided by humans, however, often show signifi- cant variability due to latent factors that are not explicitly modeled. We introduce an extension to the Generative Adversarial Imitation Learning method that can infer the latent structure of human decision-making in an unsupervised way. Our method can not only imitate complex behaviors, but also learn interpretable and meaningful representations. We demonstrate that the approach is applicable to high-dimensional environments including raw visual inputs. In the highway driving domain, we show that a model learned from demonstrations is able to both produce different styles of human-like driving behaviors and accurately anticipate human actions. Our method surpasses various baselines in terms of performance and functionality."

>	"In imitation learning, example demonstrations are typically provided by human experts. These demonstrations can show significant variability. For example, they might be collected from multiple experts, each employing a different policy. External latent factors of variation that are not explicitly captured by the simulation environment can also significantly affect the observed behavior. For example, expert driving demonstrations might be collected from users with different skills and habits. The goal of this paper is to develop an imitation learning framework that is able to automatically discover and disentangle the latent factors of variation underlying human decision-making. Analogous to the goal of uncovering style, shape, and color in generative modeling of images (Chen et al., 2016), we aim to automatically learn concepts such as driver aggressiveness from human demonstrations."

>	"We propose a new method for learning a latent variable generative model of trajectories in a dynamic environment that not only accurately reproduce expert behavior, but also learns a latent space that is semantically meaningful. Our approach is an extension of GAIL, where the objective is augmented with a mutual information term between the latent variables and the observed state-action pairs. We demonstrate an application in autonomous driving, where we learn to imitate complex driving behaviors while learning semantically meaningful structure, without any supervision beyond the expert trajectories. Remarkably, our method performs directly on raw visual inputs, using raw pixels as the only source of perceptual information."

  - `video` <https://youtube.com/watch?v=YtNPBAW6h5k> (demo)
  - `notes` <https://github.com/DanielTakeshi/Paper_Notes/blob/master/reinforcement_learning/Inferring_The_Latent_Structure_of_Human_Decision-Making_from_Raw_Visual_Inputs.md>


#### ["Deep Reinforcement Learning from Human Preferences"](https://arxiv.org/abs/1706.03741) Christiano, Leike, Brown, Martic, Legg, Amodei
>	"For sophisticated reinforcement learning systems to interact usefully with real-world environments, we need to communicate complex goals to these systems. In this work, we explore goals defined in terms of (non-expert) human preferences between pairs of trajectory segments. We show that this approach can effectively solve complex RL tasks without access to the reward function, including Atari games and simulated robot locomotion, while providing feedback on less than one percent of our agent's interactions with the environment. This reduces the cost of human oversight far enough that it can be practically applied to state-of-the-art RL systems. To demonstrate the flexibility of our approach, we show that we can successfully train complex novel behaviors with about an hour of human time. These behaviors and environments are considerably more complex than any that have been previously learned from human feedback."

----
>	"Algorithm provides two possible solutions for task to human who indicates which one is better. The process is repeated and the algorithm learns from 900 bits of feedback how to solve the problem."

  - `post` <https://blog.openai.com/deep-reinforcement-learning-from-human-preferences/>
  - `post` <https://deepmind.com/blog/learning-through-human-feedback/>
  - `video` <https://youtu.be/0DkPUecLLpI?t=48m58s> (Ratnikov) `in russian`
  - `video` <https://youtube.com/watch?v=DekQm9pBbOE> (Shavkunov) `in russian`
  - `video` <https://youtube.com/watch?v=6h3_lTDFMb0> (Yagudin) `in russian`
