
# WahWahWeenie

This project implements a simple adaptive filter to reduce noise in audio signals. The filter is based on the Delta Rule, which is a supervised learning algorithm that updates the weights of the filter based on the error between the desired output and the actual output.

The project uses the Pydub library to load and manipulate audio files. It also uses the SciPy library to compute the signal-to-noise ratio (SNR) of the audio signals.

## Table of Contents

- [Introduction](#introduction)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [File Descriptions](#file-descriptions)
- [Results](#results)
- [Waveform Visualization](#waveform-visualization)
- [Testing with New Audio](#testing-with-new-audio)
- [Conclusion](#conclusion)

## Introduction

This project is designed to reduce noise in audio signals using a simple adaptive filter. Key features and components include:

- Loading and processing input and noise audio files.
- Converting audio files to the same sample rate for compatibility.
- Merging the input and noise audio to create a combined audio file.
- Initializing the adaptive filter's weights randomly.
- Training the adaptive filter using the Delta Rule algorithm.
- Generating an output audio file by filtering the combined audio with the trained adaptive filter.
- Visualizing the input, noise, combined, and output audio signals.
- Computing the SNR (Signal-to-Noise Ratio) of the audio signals.

## Requirements

Ensure you have the following Python libraries installed before running the project:

- `numpy`
- `pydub`
- `soundfile`
- `scipy`
- `matplotlib`

You can install these libraries using the following command:
```
bash
pip install numpy pydub soundfile scipy matplotlib
```


## Installation
To get started with the WahWahWeenie project, follow these steps:

1.Clone the Repository:
First, clone this repository to your local machine using the following command:
```
git clone https://github.com/yourusername/WahWahWeenie.git
```
2.Navigate to the Project Directory:
Change your current directory to the project folder by running:
```
cd WahWahWeenie
```

3.Install Required Python Libraries:
Make sure you have the necessary Python libraries installed. You can do this by running the following command:
```
pip install -r requirements.txt
```
This command will install all the required libraries listed in the requirements.txt file.

You're now ready to use the WahWahWeenie project for audio processing and noise reduction.


## Usage
To use the WahWahWeenie project for audio processing and noise reduction, follow these steps:

1. **Open the Notebook**:
    - Open the WahWahWeenie.ipynb Jupyter Notebook in Google Colab.

2. **Run the Notebook**:
    - Within the notebook, click the "Run" button to execute the code cells.

3. **Notebook Functionality**:
  The notebook will guide you through the following steps:

    - _Loading Audio Files_:
      - The notebook will load the input and noise audio files for processing.
    - _Sample Rate Conversion_:
      - Audio files are converted to the same sample rate for compatibility.
    - _Audio Combination_:
      - The input and noise audio files are merged to create a combined audio file.
    - _Filter Initializatio_n:
      - The adaptive filter's weights are initialized randomly.
    - _Filter Training_:
      - The adaptive filter is trained using the Delta Rule algorithm.
    - _Output Generation_:
      - An output audio file is generated by filtering the combined audio with the trained adaptive filter.
    - _Visualization_:
        - The notebook includes plots of the input, noise, combined, and output audio signals for analysis.
    - _Signal-to-Noise Ratio (SNR) Calculation_:
        - The SNR of the output audio signal is computed.
        
By following these steps, you can effectively utilize the WahWahWeenie project to enhance audio quality and reduce noise in audio signals.

## File Descriptions

- `WahWahWeenie.ipynb`: Jupyter Notebook containing the project code.
- `inputfile.wav`: Sample input audio file.
- `noise.wav`: Sample noise audio file.
- `combine.wav`: Result of combining input and noise.
- `outputfile.wav`: Enhanced output audio file.
- `newinput.wav`: Sample new input audio file.
- `newcombine.wav`: Result of combining new input and noise.
- `newoutputfile.wav`: Enhanced output of the new audio file.

## Results

The project's results on the `pim.wav` input file are as follows:

- SNR of the input audio file: 13.37 dB
- SNR of the noise audio file: -20.0 dB
- SNR of the combined audio file: 4.14 dB
- SNR of the output audio file: 12.91 dB

While the adaptive filter significantly reduces noise, some residual noise may remain in the output audio due to the filter's simplicity.

Certainly, here's a "Waveform Visualization" section added to the README:

## Waveform Visualization

You can visualize the audio waveforms at various stages of the processing using 3D plots in the project. These visualizations provide insights into the input, noise, combined, and output audio signals.

### Input Audio Waveform

The input audio waveform represents the original audio signal before any processing. It's depicted in green in the 3D plots.

![input](https://github.com/yashrajtarte/WahWahWeenie/assets/91187090/e2fb79a2-c6a0-4b88-aed3-4e1488908e43)


### Noise Audio Waveform

The noise audio waveform shows the noise component that needs to be removed from the input signal. It's visualized in red in the 3D plots.

![noice](https://github.com/yashrajtarte/WahWahWeenie/assets/91187090/176f512e-4f8e-4965-94a4-d88cb1bf465e)


### Combined Audio Waveform

The combined audio waveform is the result of merging the input and noise signals. It provides a view of the audio with added noise. It's represented in blue in the 3D plots.

![comb](https://github.com/yashrajtarte/WahWahWeenie/assets/91187090/989434a2-f1b7-4ec4-ba7b-229250d21e71)


### Output Audio Waveform

The output audio waveform illustrates the result of the noise reduction process. It's the enhanced audio signal after adaptive filtering. You can observe it in magenta in the 3D plots.

![op](https://github.com/yashrajtarte/WahWahWeenie/assets/91187090/7cd8d530-5b36-40bd-b70b-f0f2f04ab53a)


These visualizations offer a clear representation of the audio signals at each stage, helping you understand the impact of noise reduction on the audio quality.

## Testing with New Audio

To test the project with a new audio file, follow these steps:

1. Replace the `newinput.wav` file in the project directory with your own audio file.
2. Run the notebook again.
3. The project will generate a new output audio file called `newoutputfile.wav`.

## Conclusion

This project demonstrates how to use a simple adaptive filter to reduce noise in audio signals. While the filter can significantly improve audio quality, it may not remove all noise entirely. This project serves as a starting point for developing more advanced noise reduction algorithms.
