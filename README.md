# Ratatouille.lv2

![Ratatouille](https://github.com/brummer10/Ratatouille.lv2/blob/main/Ratatouille.png?raw=true)

Ratatouille is a Neural Model loader and mixer for Linux/Windows.

It can load two models, which can be [*.nam files](https://tonehunt.org/all) with the
[Neural Amp Modeler](https://github.com/sdatkinson/NeuralAmpModelerCore) module, or 
[*.json or .aidax files](https://cloud.aida-x.cc/all) with the 
[RTNeural](https://github.com/jatinchowdhury18/RTNeural) module.

You can also load just a single model file, in that case the "Blend" control will do nothing.
When you've loaded a second model, the "Blend" control will blend between the two models and
mix them to simulate your specific tone.

Ratatouille using parallel processing for the neural models,
so, loading a second neural model wouldn't be remarkable on the dsp load.

The "Delay" control could add a small delay to the second model to overcome phasing issues,
or to add some color/reverb to the sound. 

To round up your sound you can load two Impulse Response Files and mix them to your needs.
IR-files could be normalised on load, so that they didn't influence the loudness. 

Ratatouille.lv2 supports resampling when needed to match the expected sample rate of the 
loaded models. Both models and the IR Files may have different expectations regarding the sample rate.

## MOD Desktop
You could find a Ratatouille GUI made by David Germain [here](https://github.com/Riebeck-one/ratatouille-modgui)
for using it on the [MOD Desktop](https://github.com/moddevices/mod-desktop)


## Dependencies

- libsndfile1-dev
- libcairo2-dev
- libx11-dev
- lv2-dev

[![build](https://github.com/brummer10/Ratatouille.lv2/actions/workflows/build.yml/badge.svg)](https://github.com/brummer10/Ratatouille.lv2/actions/workflows/build.yml)

## Building from source code

- git clone https://github.com/brummer10//Ratatouille.lv2.git
- cd Ratatouille.lv2
- git submodule update --init --recursive
- make
- make install # will install into ~/.lv2 ... AND/OR....
- sudo make install # will install into /usr/lib/lv2
