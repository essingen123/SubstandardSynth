# SubstandardSynth

Ugly and powerful web audio api based synth. Polyphonic, multiple oscillators, bugs, filters and noise generators. No dependency and easily exportable

#### Add the script to your project. 
```html
<script src="scripts/substandardSynth.min.js"></script>
```
#### Add containers in your HTML
```html
<div id="synth"></div>

```

#### Create a synth object
```javascript
let context = new AudioContext
let basicSynth = new SubstandardSynth({context:context,id:'synth'})
	
//Plug it to your keyboard or desired input method with the following methods:
//	.playNote(frequency,time)
//	.stopyNote(frequency,time)
//	.remotePlayNote(notes,time,duration)

//Example with a keyboard set up:
keyboard.pressNote = function(frequency){
	basicSynth.playNote(frequency,0);
}
keyboard.releaseNote = function(frequency){
	basicSynth.stopNote(frequency,0);
}
//Or with the console:
//this will play a C major triad in 2 seconds, for 5 seconds
basicSynth.remotePlayNote(['C3','E3','G3'],2,5);

//this will play a A3 and A4, now, for 0.5 seconds
basicSynth.remotePlayNote([440,880],2,0.5);

```


Visit the [SubstandardSynth page](https://atactionpark.github.io/SubstandardSynth/) for more info.