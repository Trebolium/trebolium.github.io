---
layout: default
---

I am Brendan O'Connor, a PhD candidate at the [Centre for Digital Music](http://c4dm.eecs.qmul.ac.uk/) at Queen Mary University of London. I am interested in all things related to MIR, instrument modelling, audio analysis and synthesis, music classification, disentanglement, and ML.

## Voice Work

Our most recent work focuses on generating a voice timbre encoder designed specifically for the singing voice. [Previous work](https://program.ismir2020.net/poster_1-08.html) exploring voice conversion in the singing domain have used encoder's trained on speech data to achieve the task of singing voice conversion. We have used a similar architecture proposed by [Wan et al. 2018](https://ieeexplore.ieee.org/abstract/document/8462665) and implemented by [CorentinJ](https://github.com/CorentinJ/Real-Time-Voice-Cloning) for this task, and trained it on a number of features and combinations of datasets. The implementation of this network is featured [here](https://github.com/Trebolium/singer_id_encoder).


**Commented on 2022.02.22 -> Please note that documentation and formatting for the public eye is underway. Links to _some_ of the repos below have been temporarily disabled**

Our published work on [Zero-shot Singing Voice Conversion](https://cmmr2021.github.io/proceedings/pdffiles/cmmr2021_26.pdf) describes a process for converting the perceived singing technique of a sung passage to a target technique, without affecting any other vocal attributes. The framework involves using the AutoVC framework (a repository for this has kindly supplied by the author [Kaizhi Qian/Auspicious3000](https://github.com/auspicious3000/autovc)) which is conditioned on the output embeddings of a pretrained singing technique classifier (the code of which is available [here](https://github.com/Trebolium/VocalTechClass) The presentation can be found on the CMMR2021 Youtube channel [here](https://www.youtube.com/watch?v=3SpzDQKQ3O0&t=3283s), the code at my [singing technique converter repository](), and the conversions can be found [here](https:).

Current research (and most likely not yet ready for public consumption if you are reading this) explores using the [WORLD vocoder](https:) for its voice-specific features and pitch-invariant properties. The WORLD vocoder is used to train a _singer-identity_ encoder, which captures the most important features of the vocal timbre and provides these as embeddings. This will be used to train an autoVC, the bottleneck embeddings of which we look forward to using as input to a VAE.

To ensure our models' latent space is reflecting something similar to that of human perception, we derived dissimilarity ratings by publishing a listening test, where users rated how different vocal sounds were from one another. The setup, analysis and conclusions are all documented in our paper, [An Exploratory Study on Perceptual Spaces of the Singing Voice](https://boblsturm.github.io/aimusic2020/papers/CSMC__MuMe_2020_paper_38.pdf) and illustrated at the Joint AI in Music Creativity conference [presentation](https://www.youtube.com/watch?v=DAZZ_ChbfSo). Results and analysis are presented [here](https://github.com/Trebolium/VoicePerception)!


## MIR Tasks

I also have experience in DSP, which has been made applicable in my studies on music information retrieval. An example of this can be found in the [Shazam imitator repo](https://github.com/Trebolium/shazam_Imitator), were recorded clips of a song in a noisey environment can be submitted as a query and compared with a song database. The algorithm returns the top three most likely matches for the given query. Results were evaluated using a subset of classical and pop songs from the GTZAN dataset. The algorithm is inspired from [Fundamentals of Music Processing](https://link.springer.com/book/10.1007/978-3-319-21945-5) (Muller, 2015).

I have also designed a basic beat-tracker that estimates tempo and follows the beat of music, using a combination of techniques from multiple researchers. Results were evaluated using the [Ballroom dataset](http://mtg.upf.edu/ismir2004/contest/tempoContest/node5.html). The repository for this can be found [here](https://github.com/Trebolium/beat_tracker).

Separate documentation providing further referencing and context for these applications for these repositories are available on request.