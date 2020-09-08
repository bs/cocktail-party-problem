# Cocktail Party Problem

## Background
The cocktail party problem (CPP) encompasses the problem of perceiving speech in noisy social settings. In human applications, the CPP has been well-characterized, and the fundamental question involves addressing how individuals recognize what another is saying even in the present of multiple overlapping speakers. Upon receiving a composite sound pressure waveform resulting from the acoustic interference of (1) multiple signalers, and (2) abiotic and (3) other biotic sources of noise, the human auditory system parses the incoming signal, integrating and segregating the stimulus into perceptually coherent and functional representations consisting of auditory objects, images, and/or streams via a complex neural circuitry. Acoustic cues that enable the human auditory system to solve the CPP include harmonicity of signals, temporal synchrony of overlapping signals, amplitude modulation rates, and spatial localization computed using interaural time differences (ITDs) and interaural level differences (ILDs). Numerous studies have aimed to address the cocktail party problem in human speech and music applications, typically employing deep machine learning (ML) techniques, often with reasonably high levels of success. Others have studied the CPP by focusing on multiple microphones (which is expressly unpragmatic for most bioacoustics applications) or by employing unsupervised methods, the most popular of which being the independent component analysis (ICA). While publications are available, a harder (and more relevant) challenge involves ‘single-channel source separation’ in which the dataset contains mixed audio signals recorded using a single microphone.

Contrarily, animal studies addressing the CPP remain comparatively understudied, with few conclusive attempts at offering solutions available in the literature. Similar to its human-related CPP counterpart, the fundamental non-human bioacoustics CPP question involves investigating how (1) animals detect and recognize conspecifics, (2) localize signalers, (3) discriminate among call types, and (4) extract meaningful information even when multiple conspecifics and heterospecifics are signaling simultaneously.
    
## Approach
In order to address the CPP in non-human applications, I propose a low-level approach consisting of two sequential phases:

    1. Understanding and implementing existing ML-based solutions designed to address human speech or music source separation
    2. Modifying the results from Phase 1 to address the non-human CPP

While numerous studies have explored the human CPP, yielding promising results, the non-human CPP has garnered relatively less interest and thus remains understudied. The difficulty of the non-human CPP is exacerbated by the challenges of procuring relevant datasets, especially since it is often unfeasible for trained experts to manually annotate recordings involving overlapping signals. This means that obtaining ground truth responses could be significantly harder in non-human studies as opposed to human CPP studies. Additionally, while the neural mechanisms in the human auditory system responsible for discriminating overlapping signals are well-understood, in animals, it remains to some degree unsolved whether non-human auditory processing systems involve similar mechanisms.

## Datasets

    1. WHAM! And WHAMR
    2. WSJ0-2mix and WSJ0-3mix
    3. LibriMix
    4. Microsoft DNS Challenge
    5. SMS_WSJ
    6. MUSDB18
    7. FUSS
    8. AVSpeech
    9. Kinect-WSJ
    
For Phase 2, a starting point could potentially require synthesizing artificial datasets by compiling multiple recordings of distinct individual signalers into a single audio stream. A possible data source could be the Gero sperm whale DTAG data, since it contains clear signals that are annotated with the identity of the vocalizing whale. As we progress, it would be important to evaluate the performance of our methods on real-world data (as opposed to manipulated artificial datasets). With this in mind, possible data sources could include:

    1. The Yossi Yovel Egyptian bat dataset, given that the annotations include ‘Emitters’ and ‘Addressees’
    2. The Diana Reiss, Marcelo Mancuso, and Andres Babino bow-riding data, since multi-modal learning could confer numerous advantages
    3. The Michelle Fournet and Fred Sharpe humpback whale data
    
## Problems 

Prior to tackling this projects, it is reasonable and appropriate to forecast a number of foreseeable problems (adapted from the ESP list of bioacoustics research questions). Some of these are biology-related, while others are ML-related, but all of the following will likely play some role in our exploration of the CPP.

    1. Representation of Bioacoustic Signals: some studies have indicated that employing Hilbert-Huang transforms (HHTs) and/or empirical mode decompositions (EMDs) could improve acoustic source separation
    2. Variable Time Scales in Vocal Behavior: given that animal sounds include a variety of vocalizations ranging from transient broadband click-like pulses to extended tonal “song”, it is likely that a solution to the non-human CPP will have to account for multiple time scales even within the context of a single species
    3. Neural Network Architectures: while CNNs have conventionally been used in speech and bioacoustics applications, it could be beneficial to investigate other architectures such as RNNs and/or transformers.

## Next Steps

The logical next step as we begin to address the non-human CPP is to become familiar with the existing techniques and approaches used to solve human speech and music acoustic source separation. A particularly relevant starting point might be the Asteroid PyTorch-based audio source separation toolkit. Several of the other key papers are listed on the Earth Species GitHub.

### 6-Week Agenda

Over the next six weeks, I propose that we focus our attention on understanding and implementing a number of existing techniques designed for human speech and music source separation. This will enable us both to develop a deeper understanding of ML-based audio source separation approaches as well as to gauge the performance of existing technologies. During this time, we can also aim to construct a number of bioacoustic source separation datasets using a variety of species and call types.

## More Information

More information for this project can be found at the project [homepage](https://github.com/orgs/earthspecies/projects/5)

   
    
    
    
    
    
    
