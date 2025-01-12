# Neuromorphic audio source localization
 Proof of concept for a neuromorphic audio source localization in LabView

The project is a proof of concept for the Neuromorphic Engineering exam at university of Scuola Superiore Sant'Anna of Pisa.
The aim of the project is to develop a metod that mimic the auditory system of the human body for the localization of an audio source in the 2D space, simulating the work done by the olivary nucleus using the Jeffres model.

There are three main section of the work:
- Encoding of the ears in two different computers:
    Decoding of the sound recived: the code is capable of decoding multifrequency sounds in the human auditory range. Each neuron, 8 in total, code a different range of frequencies
- Modelling of the neural activation:
    The neural activity is modelled using the Izhikevich model with a phasic behaviour. When the sound pressure reach a predifined value, a spike is produced
- Communication between devices:
    The two computers that simulates the ears communicate with a third one mimicking the olivary nucleus usig a UDP protocol
- Decoding of the spikes train:
    The third computer receives the spike trains from the other pc and, using the delay between the spikes, compute the position in the 2D plane.
    There are two implementation of the decoding: an analitic one, that take the difference in ms between the two spike trains, and a dicrete one, that uses two sliding array for the detection

There are many issues that have to be resolved, first of all the communication delay between devices, that affects a lot the results obtained, since the time scale of the delay and the spikes activity are comparable 