# 🌊WavCraft

Generate and edit the audio with a simple sentence.

This repo currently support:

* text-guided audio editing: edit the content of given audio clip(s) conditioned on text input
* text-guided audio generation: create an audio clip given text input
* audio scriptwriting: get more inspiration from WavCraft by prompting a script setting and let the model do the scriptwriting and create the sound for you.

## Content

- [Usage](##usage)
  - [Installation](###installation)
  - [Audio edition using a single line](###audio-edition-using-a-single-line)
  - [Audio edition via interaction](###audio-edition-via-interaction)
  - [Check if an audio file is generated/modified by WavCraft](###check_if_an_audio_file_is_generated/modified_by_wavcraft)
- [Approach](##approach)
- [Acknowledgments](##acknowledgments)
- [Citing](##citing)

## Usage

### Installation

```
source scripts/setup_envs.sh
```

### Audio edition using a single line

```
python3 WavCraft.py basic -f \
--input-wav assets/duck_quacking_in_water.wav \
--input-text "Add dog barking."
```

### Audio edition via interaction

```
python3 WavCraft-chat.py basic -f -c
[New session is create]
Add audio files(s) (each file starts with '+'): +assets/duck_quacking_in_water.wav
Enter your instruction (input `EXIT` to exit the process): "Add dog barking"

```

### Check if an audio file is generated/modified by WavCraft

```
python3 check_watermark.py --wav-path /path/to/audio/file
```

## Approach

WavCraft is an LLM-driven agent for audio content creation and editing. It applies LLM to connect various audio expert models and DSP function together. An overview of WavCraft architecture can be found bellow:

\[overview](assets/overview.png)

## Acknowledgments

We appreciate [WavJourney](https://github.com/Audio-AGI/WavJourney), [AudioCraft](https://github.com/facebookresearch/audiocraft), [AudioSep](https://github.com/Audio-AGI/AudioSep), [AudioSR](https://github.com/haoheliu/versatile_audio_super_resolution), [AudioLDM](https://github.com/haoheliu/AudioLDM), [WavMark](https://github.com/wavmark/wavmark) for their amazing code work.

## Citing

If you found our work is helpful, please cite our work: