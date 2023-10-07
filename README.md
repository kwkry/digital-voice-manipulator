
<div align="center">
  <img src="Group_Picture_Agripa_Magat_Popes.jpg" alt="Logo" width="300" height="400" />
  
  [![Open on YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&color=FF0000)](https://youtu.be/peSTb44w78U?si=aPRgcRD-2LU0DFw5)
  [![Open Google Drive](https://img.shields.io/badge/Google%20Drive-4285F4?style=for-the-badge&logo=googledrive&color=4285F4)](https://drive.google.com/drive/folders/1Os2Snu2mwzi4OKm8ulwivxAgM_ryU1Gw?usp=sharing)
  [![Open on Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://colab.research.google.com/drive/1NYzmnmK8G5PxIhz0wlRkENfYPl-z3vBz)

  # Digital Voice Manipulator
  Case Study: Development and Application of a Digital Voice Manipulator<br>
  Explore the development and practical applications of our innovative Digital Voice Manipulator in this case study. <br>

  Members:<br>
    Agripa, Vince Kurt C. <br>
    Magat, Pamela Mae G. <br>
    Popes, Mikaela Faye E. <br>
</div>

# Libraries

1. pydub (Install with `!pip install pydub`)
   - AudioSegment (Used for audio processing)
2. os
3. librosa
4. soundfile
5. IPython.display (Used for `Audio` and `display` functions)
6. matplotlib.pyplot
7. numpy
8. wave
9. sys

## Pitch Manipulation and Audio Plotting

In this section, we'll explore how to use the functions for pitch manipulation and audio plotting. These functions allow you to change audio pitch and visualize waveforms.

### How to Use

#### Pitch Manipulator Function

The `pitch_manipulator` function facilitates pitch manipulation of audio files. To use it:

```python
# Import the function and specify the filename and semitone change

input_path, output_path = pitch_manipulator('input_audio.wav', semitone_change)
```

- `filename`: Provide the name of the input audio file in your specified directory.
- `semitone_change`: Specify the number of semitones by which you want to change the pitch. Use positive values for higher pitch and negative values for lower pitch.

This function handles the conversion of M4A files to WAV (if necessary), manipulates pitch, and saves the modified audio.

#### Audio Plotter Function

The `plot_audio` function allows you to visualize audio waveforms. Here's how to use it:

```python
# Import the function and specify the audio file path and plot title

plot_audio('audio_file.wav', 'Plot Title')
```

- `audio_file.wav`: Enter the path to the audio file you want to plot.
- `Plot Title`: Define the title for the audio waveform plot.

This function displays original and manipulated audio waveforms in separate plots.

### How It Works

#### Pitch Manipulation

The `pitch_manipulator` function employs the following steps to modify pitch:

1. Converts M4A files to WAV format if necessary.
2. Manipulates the pitch of the audio file based on the provided semitone change. Positive values increase pitch, while negative values decrease it.
3. Saves the modified audio.

#### Audio Plotting

The `plot_audio` function works as follows:

1. Opens the specified audio file using the WAV format.
2. Extracts the raw audio signal and sample rate.
3. Plots the audio waveform using matplotlib.

### How to Change Tone (Parameters)

In the `librosa.effects.pitch_shift` function, the `n_steps` parameter represents the number of semitones by which you want to shift the pitch of the input audio. Each semitone corresponds to a specific musical note interval. 

- Positive values for `n_steps` will increase the pitch, making the audio sound higher in pitch.
- Negative values for `n_steps` will decrease the pitch, making the audio sound lower in pitch.

For example:

- Setting `n_steps=2` will shift the pitch up by 2 semitones, making the audio sound two semitones higher.
- Setting `n_steps=-3` will shift the pitch down by 3 semitones, making the audio sound three semitones lower.

You can adjust the `n_steps` parameter to achieve the desired pitch shift effect in your audio processing application.


Experiment with different values to achieve the desired pitch modification for your audio files.

Feel free to utilize these functions to explore pitch manipulation and visualize audio waveforms in your projects.
