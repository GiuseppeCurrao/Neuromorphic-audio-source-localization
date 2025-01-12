Audio trasformation setted frequency

-v001: Simplest version, trasformation with gabor, one frequency, one neuron, curent setted at 15 A. Izikevich primitive v001
-v002: Added a filtering on the input, the signal smaller than a 0.9 the max value of the trasformation do not pass. Izikevich primitive v001
-v003: Probably tried a filtring of the signal to see if the peak changed. It didn't. Izikevich primitive v001
-v004: Added the possibility to spike at different frequency interval with 8 different neurons. Izikevich primitive v001
-v005: This version attempt is to create a control over the noise, setting a minimum threshold of 0.15 for each before spiking. The problem observed is that different devices reached higly different values, with differences by 2 order of 	magnitude. So the threshold value cannot be defined well. Izikevich primitive v001
-v006: No difference with v004 if not the treshold value. Izikevich primitive v001
-v007: Add an initial sampling of noise, to see if the spike happen by chance or if there is actually a sound at that frequency higher than the noise sampled. Izikevich primitive v001
-v008: Optimization of the code with the two possible values of the current outside the blocks. Izikevich primitive v001
-v009: Version that stores all the values of the current. Probably to tell which neuron was spiking. There is no need to do so, is an orrible implementation (non so che mi ero fumato, si può fare in un altro modo estremamente più facile). Izikevich primitive v002
-v010: Changed the Izhikevich subVI version from 1 to 3. Izikevich primitive v003
-v011: Added an initial message to sinchronize the comunication. The neuron here send the time of spiking. Izikevich primitive v001
-v012: Same as v011 for the other port. Izikevich primitive v003
-v013: Returned to the single neuron and one interval spiking to reduce the delay. Izikevich primitive v001
-v014: Same as v013 but for the other port. Izikevich primitive v003
-v015: Readded the multiple interval spiking, signalling which neuron is sending the message. Izikevich primitive v007
-v016: Readded the multiple interval spiking, signalling which neuron is sending the message. Izikevich primitive v008

Izhikevich prmitive

-v001: Send the neuron ID or 0. NeuronID_UDP v002
-v002: Send a message only if the spike happen, sending the neuron ID. NeuronID_UDP v006
-v003: Same structure as v001, probably created to send time and not the neuron ID. NeuronID_UDP v006
-v004: NOT USED Send a costant 1 as message only when spiking; if not spiking do not send anything. NeuronID_UDP v006 
-v005: NOT USED Mi da errore ad aprirla, probabilmente l'ho salvata con la versione 21
-v006: Same structure of v001. NeuronID_UDP v007
-v007: Version used to send also the information on the frequency interval. NeuronID_UDP v009
-v008: Version used to send also the information on the frequency interval. NeuronID_UDP v010

NeuronID UDP

-v001: NOT USED Initial version, array of addresses, sending the neural id to 8001
-v002: Fixed address, sending neuron ID, or time, to 8001
-v003: NOT USED Same structure of v001, Do not spotted any signitive change
-v006: Fixed address, sending neuron ID, or time, to 8002
-v007: Same structure of v002, but with the possibility to send numeric or string. Useless. Port 8001
-v008: NOT USED Same structure of v002, but with the possibility to send numeric or string. Useless. Port 8002
-v009: Version to send both interval and time of arrival at port 8002
-v010: Version to send both interval and time of arrival at port 8001


Jeffress model

-v001: First attempt, if the signal arriving is "Right" or "Left", start a timer. When a message from the other ear arrive, calculate the difference between the two times. One connection used
-v002: One connection used; when a signal arrives checks if is 1 or 2 and start a timer. When both timer are greater than 0 compute and plot the position
-v003: Same as before but two connection used
-v004: The signal is inserted in a array, that slides in different direction in respect to the ear. The position of the sound is found seeing in which position the coincidence is found
-v005: Same code as v004 but optimized without a for
-v006: Same model, but after the coincidence is found the array is resetted but the graph manteined
-v007: Temporal code again, this time is used one timer for both messagges, computing the difference between the two moments considered
-v008: Version used to estimate the time delay from the connection. It used time and sine
-v009: Version that code the different intervals with different color
-v010: Version based on v006, using the time of arrival as input
-v011: Use of the initial shift to adjust the delay due to connection 

