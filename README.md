# vinyl-scrobbler
Listen to vinyl, identify the songs, and scrobble to last.fm

## Plan of attack
- Have some sort of client listening all the time somehow. This might be a hard part because I imagine this client being an old phone or something. I suppose you could also split the audio output into some sort of computer which would save you having to listen to audio. This would also make it a lot easier to identify the music because there wouldn't be any background noise (talking or whatever). I imagine the audio source for this should be interchangable, the components here should be modular.
- Maybe try and identify each track and then scrobble that or identify an entire album and then scrobble that. The first one is clearly preferable and probably possible, the latter is sort of just like how http://vinylscrobbler.com works.
- To do this probably take 20 second samples (what about really small tracks???) and over the course of a song keep checking what song it is and then take the majority. This way you're not relying on a single sample. It'd be good if the library for this had a confidence metric, we'll see what we've got.
- For the audio identification I'll probably use acoustid: https://acoustid.org.
- Once the audio has been identified I need to scrobble it to last.fm, I'll read the documentation for their scrobbling API.
