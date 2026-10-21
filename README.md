# Graduate Papers

A collection of papers I wrote during my graduate coursework at Penn State. Each one is a PDF in this folder. Below is a short description of what each paper covers.

## Papers

### Artificial Intelligence in Cars: A Detailed Study Analyzing General Public Reception
File: `Artificial Intelligence in Cars - Sourajit Karmakar.pdf`

A survey-based study of how people feel about AI features in cars, such as lane departure warnings, distance-based automatic braking, and self-driving. I put together a Google Forms survey and sent it to classmates, friends, and family, including people living outside the United States. It got 32 responses. The questions covered whether people know where AI is used in cars, how much they trust it, and whether price affects their willingness to adopt it. The paper also compares opinions across countries. For example, some respondents in India were doubtful that self-driving cars could cope with mixed, unpredictable traffic. Overall, most respondents were aware of AI in cars and thought it would reduce accidents.

### From Theory to Practice: Oblivious RAM and Its Role in Modern Secure Memory Systems
File: `CSE 530 - Final Project Paper - Sourajit Karmakar.pdf`

Written for CSE 530. This is a survey of Oblivious RAM (ORAM), a technique that hides memory access patterns, because encrypting data alone does not stop an observer from learning things from which locations get touched and when. The paper goes through threat models and formal definitions, then follows the progression from the early hierarchical constructions to tree-based designs like Path ORAM and Ring ORAM. It also looks at how ORAM is used with trusted execution environments, secure processors, and privacy-preserving computation, and where it falls short in practice (latency and energy costs, mainly). I also built a working Path ORAM prototype and measured its bandwidth and latency overhead, and checked that access patterns were indistinguishable.

### RECAP: Reaction Completion and Prediction for Biochemical Reactions with Incomplete Inputs
File: `CSE 587 - NLP - RECAP_final.pdf`

A group project for CSE 587 (NLP), done with Haixing Piao and Somtirtha Santra. Language models trained on organic chemistry tend to do poorly on metabolic reactions, which involve cofactors, charged species, and varying protonation states. We tried three ways of adapting ReactionT5 to the MetaNetX dataset (roughly 19,000 valid reactions): plain supervised fine-tuning, fine-tuning guided by a functional-group knowledge graph, and a LongT5-based long-context model. Supervised fine-tuning gave the biggest gain, lifting all-product accuracy from 0.003 to 0.173 and any-product accuracy from 0.025 to 0.586. The knowledge graph and LongT5 did not beat it. Stoichiometric balance stayed low even in the best model, with H, O, and C causing most of the imbalance. We conclude that a larger tuning dataset is needed.

### CSE 586 Project: Body Pose Forecasting
File: `CSE 586 - Computer Vision - Project 1 - Report.pdf`

A group project for CSE 586 (Computer Vision), with Pradyumna Kunchala, Mayuravarsha Peethambara Swamy, and Prithvi Pandaala. The task is to predict a person's future body poses from a sequence of past ones. We used the CMU portion of the AMASS motion capture dataset, downsampled from 120 to 30 fps, and worked with SMPL pose parameters (63 rotation values across 21 joints) instead of raw 3D joint positions, which avoids bone-stretching artifacts. Poses are compressed into a 32-dimensional latent space with the pretrained VPoser autoencoder, and an autoregressive Transformer predicts the change from one latent pose to the next. At inference each prediction is fed back in to forecast further out. It beat simple deterministic baselines on MPJPE, especially at longer horizons, though errors build up over long rollouts.

### Marine Detect: AI-Powered Marine Species Detection
File: `CMPSC 497 - Marine Detect AI.pdf`

A group project for CMPSC 497, with Adithi Gollakota, Ann Zezyus, and Samuel Baxter. The paper looks at using YOLOv8 object detection to identify marine species in underwater images and video, building on the open-source Marine-Detect pipeline. Underwater footage is hard for standard detectors because of poor lighting, turbidity, and species that look alike. The system uses two separate models, one for fish and invertebrates and one for megafauna, which lets it reuse existing labeled datasets instead of re-annotating everything. The target species are bioindicators of coral reef health, focused on the Indo-Pacific and Malaysian regions. The goal is to make large-scale ecological monitoring practical for researchers who are not machine learning experts.
