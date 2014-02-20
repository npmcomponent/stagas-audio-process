*This repository is a mirror of the [component](http://component.io) module [stagas/audio-process](http://github.com/stagas/audio-process). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/stagas-audio-process`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# audio-process

creates a webaudio script process input node

## Example

```js
var process = require('audio-process');

var audio = new webkitAudioContext();

var node = process(audio, 1024, function(L, R){
  for(var i=0; i<L.length; i++){
    L[i] = Math.random()*0.5;
    R[i] = L[i];
  }
});

node.connect(audio.destination);
```

## License

MIT
