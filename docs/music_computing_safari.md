# Music Computing Safari

[@hughrawlinson](https://twitter.com/hughrawlinson)

Musicians need computers. Software has opened up a huge variety of musical
possibilities, ranging from instrumentation and synthesis - the building blocks
of modern music, to generative composition - several layers of abstraction above
where musicians and composers usually sit. Musicians are taking advantage of
these new possibilities, whether they realise it or not.

We’re going to take a look at four major uses of computation in music, examining
the variety of problems that exist in this space, and the perspectives of the
artist.

## Why are hugh telling me this?

* This is what I went to school for
* The point was never to become a developer, the point was to become a musician
* Things have changed a little
* But I still know this stuff

## Is there more?

Yes, of course, there’s lots lots more.

* Faust
* Pure Data
* Tidal
* Overtone
* VST
* Demoscene
* Chiptune
* MIDI
* CSound

## But first: What is music?

* Every single academic computer music related paper/class ever asks this
  question
* Audio relates to signals and array math
* Music relates to melody, harmony, and timbre

Audio - Low level

Music - High level

## ChucK

### Overview

* Developed by Ge Wang at Princeton (now Stanford)
* Been around since 2003
* “Strongly Timed”
* “Multi-shred”
* “On-the-fly”
  * Live Coding
  * Algorave
* Dedicated programming language for music
* Handles both signal processing and higher level composition
* Particularly academic

### Demo

#### Beep

_I’ll do this example in all of the languages_

```ChucK
SinOsc a => dac;

while( true ) {
    1::ms => now;
}
```


#### Frequency Modulation Synthesis

```ChucK
// FM synthesis by hand

// carrier
SinOsc c => dac;
// modulator
SinOsc m => blackhole;

// carrier frequency
220 => float cf;
// modulator frequency
550 => float mf => m.freq;
// index of modulation
200 => float index;

// time-loop
while( true ) {
    // modulate
    cf + (index * m.last()) => c.freq;
    // advance time by 1 samp
    1::samp => now;
}
```


#### Music Modelling, IO

```ChucK
[
   [0, 2, 4, 5, 7, 9, 11], // Major
   [0, 2, 3, 5, 7, 9, 11]  // Minor
] @=> int scales[][];

fun int[] scale ( int root, int kind ) {
    root - 4 * 12 => int base;
    10 * scales[kind].size() => int length;
    int out[length];
    0 => int counter;

    for (0 => int octave; octave < 10; octave++ ) {
        for ( 0 => int scaleIndex;
        scaleIndex < scales[kind].size();
        scaleIndex++) {
            base + 12 * octave + scales[kind][scaleIndex] => int note;
            if (note > 127) {
                break;
            }
            note => out[counter];
            counter++;
        }
    }
    return out;
}

MidiOut mout;
// check if port is open
if( !mout.open( 0 ) ) me.exit();

fun void sendNote ( int note, int velocity, dur duration ) {
    MidiMsg msg;
    0x90 => int noteOn;
    0x80 => int noteOff;
    0 => int channel;
    noteOn + channel => msg.data1;
    note => msg.data2;
    velocity => msg.data3;
    mout.send(msg);
    duration => now;
    noteOff + channel => msg.data1;
    mout.send(msg);
}

scale(60, 0) @=> int cMajor[];
for ( 8 => int i; i < cMajor.size() - 10; i++) {
    <<< "Number " + i + ": " +cMajor[i] >>>;
    spork ~ sendNote(cMajor[i], 100, 333::ms);
    250::ms => now;
}

```


### More Info

* [Official Website](http://chuck.cs.princeton.edu/)
* [Wang, G., P. R. Cook, S. Salazar. 2015. "ChucK: A Strongly-timed Computer
    Music Language." Computer Music Journal. 39(4):10-29.](
    http://www.gewang.com/publish/files/2015-cmj-chuck.pdf)


### Further reading
* [Algorave](https://algorave.com/)
* [Live coding](https://en.wikipedia.org/wiki/Live_coding)
* [Tidal](https://slab.org/tidal/)
  * Haskell Live Coding environment
* [Overtone](http://overtone.github.io/)
  * Clojure live coding environment
* [Gibber](http://gibber.mat.ucsb.edu/)
  * Web audio live coding environment
* [Lissajous](http://lissajousjs.com/)
  * Web audio live coding environment


## Web Audio

### Overview

* On the W3C standards track
* 2011
* Audio Programming for the web
* Graph based signal path
* Generally focused on audio level programming rather than music level
* JS-SDK

### Demo

#### Beep

```javascript
const ctx = new AudioContext();
const osc = ctx.createOscillator();
osc.connect(ctx.destination);
osc.start();
```


#### AudioCrawl
* [Birdman](http://audiocrawl.co/crawl/birdman-0760)



### More Info

* [Spec](https://webaudio.github.io/web-audio-api/)
* [GitHub Issue Tracker](https://github.com/webaudio/web-audio-api/issues)
* [Demos](http://audiocrawl.co/)


### Further Reading

* [Meyda](http://hughrawlinson.github.io/meyda)
  * Realtime audio feature extraction
  * Disclaimer: I helped write it
* [DAW Plugins for Web Browsers](https://mediatech.aalto.fi/publications/webservices/dawplugins/)
  * Someone made VSTs run in web browsers
  * This is the paper I had to follow at the First Web Audio Conference
* [Web Audio Conference 2017](http://wac.eecs.qmul.ac.uk/)
  * The third (sort-of) Annual Web Audio Conference


## Max/MSP

### Overview

* Proprietary software based on an academic research project by Miller Puckette at IRCAM
* Been around since the 1980s
* Graphical programming
* Aimed at technical musicians
* Used in production by Radiohead (and many many more artists)
* Both for studio and live use


### Demo


#### Beep

```
----------begin_max5_patcher----------
316.3ocqREsSCCCC74zuhn7bA0tV1l3WAgPYIVaYJKoJIczwz12NsNMPGLIf
IdwU9p8cmsywLBaksC7L5izmnDxwLBAgF.Hi4D1NdmPy8XYL3MIWblkG+koc
msMng.9yhQzFdPrQYV+hCDgH40U2WjSKKqG9T+PJRedrEkDY2tZ6cUIx8gCZ
.gmHmxjTa1.1orrgP9uz8F30dIRzEfNzdLwAgFNSqqKt9fU9SC17EXb4Pb1r
qOWkItiDGNz.QJXd0ZCWy9no+vfi8vzJyWuhnUGvuba3ssNQR2QWQ+ztRvGT
FdPYMSpo5hZ1njRvL8dKUd9JMHmhYcRvg6tqdl9usW4sZuhusL4MM6AmeTCz
Y8Oh1ZwxWjioJSLsBScvdUp9HB20+NIz+Ho0EOjcKmyhsZ6E1zpFWM8JeJ6c
7Zhy7.
-----------end_max5_patcher-----------

```

(There’s also a weird json format, but it’s weird and doesn’t matter)

Let’s open the GUI


#### Generative Percussion

```
----------begin_max5_patcher----------
1310.3oc4asrjahCEcs6uBJ1NdRo2RLqmrJalplkSMUJrsR2jX.WfblNUp7u
OVRPRmNF6K9g.i2.ABFtm68niN5Q+0GlEun7YccbzeD8OQyl80GlMycK6Ml0
b8r37zmWtNs18XwKKyy0El349+Oi9Yi69u8YSUZzeoqVtstNqrn8AJ1lWt0r
Vab+bTyc2jZV9TVwiuuRuz3+7bD9Mn4QXdyIj8DY2wn+s4Gksx8kJW7weOQ0
99qMeYs1c+W7EyJZ+fX6891COXOL+Lg3eWjVo6MtHJTOvkX.v06xV9on+rZa
d+qYDGlXffF6JBsB8+s6a7KHKWapJivhNXi3tQFS3vDiYOJ3NfQ5.Xj12t+U
a9xFs+kDuHs3w3u+aNBtIWNb+aQTd+gLW4JiDo8DkcPLi6DyY6XXC.jWUss3
S63fmJrUN7xkGD0nKBpoWZBNo+7aBsoX6n49TPWvVkLBI3x9WnSZzm703j2v
6FxR4vwu2luPWsezQNdqWoSRtQJtKzo5DcwyecQcSZU5NZlt585hzEdzhthJ
4mF74ROh8.+HvOY7B+bccc5i5egvSU8luyYBuPdxwSIptU1FijctvwxoJI.n
gmfjcWacFlC.9jQL72u3dQoQuKX6uaTOgm4Ms48a2YZgFG7NqWoWGgQHzI2R
FwOtGEEa.6r9r55hhD.ny7IWqYljAWLSL8fu2VFLwL4ciXVSiBXhYpvKlcJN
vIR3NvE7aMG3sCoBhCbwzqcLkC2AtPdW3.mRf6.WntobfSYvcfKRlfjc3Nvk
n6lNsZH7f5zRhugbf21RFhCbI4lyAdSWWfbfKoStVyDNbG3R1zC9R3Nvk76F
wrlFEvDyDWQwLS4iOtV2e21JpawqbwMq83d6flAyq83nd5WyC1IrlGpeTHO7
JdHFeKomoJsndSYUG73jixCXtiXD8P.moNHSX92O8g0koc7O12SsuL1t3bQ5
UOskkq2TlUX5MaAS8YJunXxAyZxKCcAOrCOW.ez4T0M2nygO3b5zaNFwL3CN
mntAGbtn+suwvGbNQbSM3bLE9fyIjIHYG9fyIz6F+rMDdP9YIrqne1EaMlxS
09VB.+rX0nq+3SdlGZkofLyC3au09i.ehGvSuExmAedGldygp.9rNHtelzA3
y4voHQ6dOwqyJd8l91EJ16+yPstba0x1bc6lcM5GgyJcsIqH0X2v2u3gP+zC
8T1pU5hWB7UY01RiCKn8lzgFO1ot33wCoOwSKUqZ0NR8YGf1cJ6QCP6FxKPI
rWUa5HggGWEP6NP8zKfjyJ.e02d+Anc8bCTBytGHNdByRnHgIdDPiGbXhGNz
3YnHTPTDr6OsPkvHPiGxHp.h5S94xJoqPPSXgQQPBQgxtu.CEghAs.hFQDJ1
4nHfOuBnBhGA4vYhAT.9pzbXyfxKd.ddwCDJmcQCCjlpjAMdBiDgjBMdFnNo
EPzTsagkPkvPPiGx3o.JTCWmzBEzDVfFmCDEJ6VGJTDJBzBHZDoHPFttXDPF
mifObcRCJ.kzALCxu3A30epGDmEkid8CPlZ.qnPDQvgSDACQzmFNafTHwCNb
cBQ4W734xRn.EfT0vIxhgL4M3AbrjXHZFjvMckDEzDVX78PfzKIgENIKLz50
.YjlPglvByHOHDnwCd7T.YC2HYS.FdgIaI.FMmBWxu3loa17YcUcyqzEHw4o
erzkJkycWlU3uj5trR+4r1m2emzpkOkYzKMaq7Kr5yM+g2FmWtqnTrMqQnd2
W9aO7+HFSxKM
-----------end_max5_patcher-----------
```


### More Info
* [Miller Puckette PD Paper](https://ipsj.ixsq.nii.ac.jp/ej/index.php?action=pages_view_main&active_action=repository_action_common_download&item_id=56450&item_no=1&attribute_id=1&file_no=1&page_id=13&block_id=8)
* [Cycling ‘74 Max/MSP Website](https://cycling74.com/products/max/)


### Further Reading
* [Johnny Greenwood Interview](https://cycling74.com/2014/01/02/mini-interview-jonny-greenwood/#.WMViAxLyuAw)
* [PureData](https://puredata.info/)
  * A free alternative to Max/MSP
  * Looks AWFUL


## Maximillian


### Overview

* Low level, signal-focussed, single-sample-at-a-time audio.
* Developed by Mick Grierson at Goldsmiths (where I studied)
* There’s lots of similar libraries, usually focussing on buffers rather than
  single samples.
* I chose this one because it’s illustrative of the general technique, not
  because it’s popular
* Similar: PortAudio, RTAudio, piping to `/dev/audio`

This is the sort of stuff you need to know to work with eSDK

### Demo

Examples from [the GitHub repo](
https://github.com/micknoise/Maximilian/tree/master/maximilian_examples). Mick
absolutely refuses to observe literally any code conventions, sorry.

#### Beep

```cpp
// Demo code here
#include "maximilian.h"

//This shows how the fundamental building block of digital audio - the sine wave.
maxiOsc mySine;//One oscillator - can be called anything. Can be any of the available waveforms.
void setup() {//some inits
    //nothing to go here this time
}

void play(double *output) {
    output[0]=mySine.sinewave(440);
    output[1]=output[0];
}
```


#### Replicant

```cpp
#include "maximilian.h"

// Bizarelly, this sounds a little bit like Kraftwerk's 'Metropolis', although
// it isn't. Funny that.

// here are the synth bits
maxiOsc sound, bass, timer, mod, lead, lead2, leadmod;
// some envelopes
maxiEnv envelope, leadenvelope;
// some filters
maxiFilter filter, filter2;
// a delay
maxiDelayline delay;
// a method for converting midi notes to frequency
convert mtof;
// some variables to hold the data and pass it around
double bassout,leadout, delayout;
// some control variables
int trigger, trigger2, newnote;
// some other control variables
int currentCount,lastCount,playHead=0, currentChord=0;
// the bassline for the arpeggio
int pitch[8]={57,57,59,60};
// the root chords for the arpeggio
int chord[8]={0,0,7,2,5,5,0,0};
// the final pitch variables
float currentPitch,leadPitch;

// here's the lead line trigger array, followed by the pitches
int leadLineTrigger[256] = {
    1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1,0,0,0,0,0,0,0,1,0,0,0,0,0,0,0,
    1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,
    1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1,0,0,0,0,0,0,0,1,0,0,0,0,0,0,0,
    1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,
    1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1,0,0,0,0,0,0,0,1,0,0,0,0,0,0,0,
    1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1,0,0,0,1,0,0,0,
    1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,
    0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0
};
int leadLinePitch[15] = {
    69,67,65,64,67,66,64,62,65,64,62,57,55,60,57
};



void setup() {
   //some inits
}

// this is where the magic happens. Very slow magic.
void play(double *output) {
    // this sets up a metronome that ticks every so often
    currentCount = (int) timer.phasor(9);

    // if we have a new timer int this sample, play the sound
    if (lastCount!=currentCount) {
        //play the arpeggiator line
        trigger = 1;
        //play the lead line
        trigger2 = leadLineTrigger[playHead%256];
        //if we are going to play a note
        if (trigger2 == 1) {
            // get the next pitch val
            leadPitch = mtof.mtof(leadLinePitch[newnote]);
            //and iterate
            newnote++;
            if (newnote > 14) {
                //make sure we don't go over the edge of the array
                newnote = 0;
            }
        }
        // write the frequency val into currentPitch
        currentPitch = mtof.mtof(pitch[(playHead%4)]+chord[currentChord%8]);
        // iterate the playhead
        playHead++;
        // wrap every 4 bars
        if (playHead % 32 == 0) {
            // change the chord
            currentChord++;
        }
        // cout << "tick\n";//the clock ticks
        // set lastCount to 0
        lastCount=0;
    }

    // new, simple ADSR.
    bassout=filter2.lores(
        envelope.adsr(
            bass.saw(currentPitch*0.5) + sound.pulse(
                currentPitch * 0.5,
                mod.phasor(1)
            ), 1, 0.9995, 0.25, 0.9995, 1, trigger
        ),
        9250,
        2
   );

    // leadline
    leadout=filter.lores(
        leadenvelope.ar(
            lead2.saw(
                leadPitch*4) +
                lead.pulse(
                    leadPitch +
                    (leadmod.sinebuf(1.9) * 1.5),
                    0.6
                ),
                0.00005, 0.999975, 50000, trigger2
        ),
        5900,
        10
    );

    // add some delay
    delayout = (leadout+(delay.dl(leadout, 14000, 0.8)*0.5))/2;

    // set the trigger to off if you want it to trigger immediately next time.
    if(trigger != 0) trigger = 0;

    // sum output
    output[0] = (bassout+delayout)/2;
    output[1] = (bassout+delayout)/2;
}
```



### More Info

* [GitHub Repo Page](https://github.com/micknoise/Maximilian)
* [Website](http://maximilian.strangeloop.co.uk/)


## Summary

* Many different approaches to Music Computing
* I hope you’ve enjoyed your tour

_Bonus: [here's how far we've come](http://www.doornbusch.net/CSIRAC/)_

