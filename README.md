# WahWahWeenie

This project implements a simple adaptive filter to reduce noise in audio signals. The filter is based on the Delta Rule, which is a supervised learning algorithm that updates the weights of the filter based on the error between the desired output and the actual output.

The project uses the Pydub library to load and manipulate audio files. It also uses the SciPy library to compute the signal-to-noise ratio (SNR) of the audio signals.

To run the project, simply open the WahWahWeenie.ipynb notebook in Google Colab and click the "Run" button. The notebook will load the input and noise audio files, train the adaptive filter, and generate the output audio file.

The following is a brief overview of the steps involved in the project:

Load the input and noise audio files.
Convert the audio files to the same sample rate.
Merge the input and noise audio files to create a combined audio file.
Initialize the weights of the adaptive filter randomly.
Train the adaptive filter using the Delta Rule.
Generate the output audio file by filtering the combined audio file with the trained adaptive filter.
Plot the input, noise, combined, and output audio signals.
Compute the SNR of the output audio signal.
To test the project on a new audio file, simply replace the newinput.wav file with your own audio file. The project will then generate a new output audio file called newoutputfile.wav.

Results
The following are the results of the project on the pim.wav input file:

SNR of the input audio file: 13.37 dB
SNR of the noise audio file: -20.0 dB
SNR of the combined audio file: 4.14 dB
SNR of the output audio file: 12.91 dB
As you can see, the adaptive filter is able to significantly reduce the noise in the input audio signal. However, there is still some residual noise in the output audio signal. This is because the adaptive filter is a simple filter that is not able to perfectly remove all of the noise from the signal.

Conclusion
This project demonstrates how to use a simple adaptive filter to reduce noise in audio signals. The project can be used as a starting point for developing more sophisticated noise reduction algorithms.
