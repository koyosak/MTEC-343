# Midterm

## about my patch

#### I wanted to create the patch which I can build up as I perform, so I made patch which I can add line (instrument) one by one. For hydra, I referenced the example from strudel + Hydra site and tweaked around for my patch as well.

## Hydra part

#### Because my patch is buildable and I can control how many sound I play at the moment, I wanted to express the difference of the layer of sound. So I referece the patch from the strudel + Hydra website which you can visualize the sound using Hydra.

	///the original
	 
	await initHydra({feedStrudel:1})
	src(s0).kaleid(H("<4 5 6>"))
	  .diff(osc(1,0.5,5))
	  .modulateScale(osc(2,-0.25,1))
	  .out()
	  
	  all(x=>x.fft(2).scope({pos:0,smear:.80}))
	
	 
	 ///Visual
	await initHydra({feedStrudel:1})
	
	src(s0).kaleid(H("<5 6 7>"))
	  .diff(osc(1,-0.5,5))
	  .modulateScale(osc(-2,-500,1))
	  .out()
	  
	 all(x=>x.fft(2).scope({pos:0,smear:.80}))
	 
#### I adjusted the amount of line and how fast the color changes. I tried to make the line looks like flower as well.

## Patch

#### Like I said in the beginning, I made patch that I can add line while I'm performing. All of the line can be subtracted or added any time.

	stack (
	  ///Arpeggio  
	 n("[0 4 2 7]!4[0 5 3 6]!4").scale("c:minor").s("z_triangle").room("1.5").gain("1.1").lpf(perlin.range(500,3000)),
	 n("[9 7 4 0]!4[8 7 5 0]!4").scale("c:minor").s("z_triangle").room("1.5").gain("1.1").lpf(perlin.range(500,3000)),
	 
	  /// Melody
	 note("[Eb6 ~ ~ ~][C6 ~ ~ ~][G6 ~ ~ ~][Eb6 ~ ~ ~][D6 ~ ~ ~][G5 ~ ~ ~][F6 ~ ~ ~][D6 ~ ~ ~]").s("gm_xylophone").room("2.5"),
	 note("[G6 ~ ~ ~][C7 ~ ~ ~][Eb6 ~ ~ ~][G6 ~ C7 ~][F6 ~ ~ ~][Bb6 ~ ~ ~][D6 ~ ~ ~][F6 ~ Bb6 ~]").s("gm_music_box").room("2.5").gain("0.4"),
	 note("[Eb5 ~ F5 ~][G5 ~ Eb5 ~][C5 ~ ~ ~][G4 ~ ~ ~][D5 ~ Eb5 ~][F5 ~ D5 ~][Bb4 ~ ~ ~][G4 ~ ~ ~]").s("gm_xylophone").room("2.5").gain("0.5"),
	 note("[Eb7 D7 C7 Bb6][G6 F6 Eb6 C6][Eb6 D6 C6 Bb5][G5 F5 Eb5 C5][D7 C7 Bb6 G6][F6 Eb6 D6 Bb5][D6 C6 Bb5 G5][F5 Eb5 D5 Bb4]").s("zzfx").gain("0.7").room("2").pan("<0 .5 1>").lpf(perlin.range(500, 3000)),
	 note("[G7 F7 Eb7 D7][Eb7 D7 C7 F6][G6 F6 Eb6 D6][Eb6 D6 C6 Eb6][F7 Eb7 D7 C7][D7 C7 Bb6 F6][F6 Eb6 D6 C6][D6 C6 Bb5 D5]").s("zzfx").gain("0.7").room("2").pan("<1 .5 0>").lpf(perlin.range(500, 3000)),
	  
	  ///Chords
	  note("[Eb4 ~ ~ ~][~ ~ ~ ~][Eb4 ~ ~ ~][~ ~ ~ ~][D4 ~ ~ ~][~ ~ ~ ~][D4 ~ ~ ~][~ ~ ~ ~]").s("gm_synth_choir").room("5").decay(perlin.range(0.1, 0.5).slow(4)).gain("1.1"), note("[C4 ~ ~ ~][~ ~ ~ ~][C4 ~ ~ ~][~ ~ ~ ~][Ab3 ~ ~ ~][~ ~ ~ ~][Ab3 ~ ~ ~][~ ~ ~ ~]").s("gm_synth_choir").room("5").decay(perlin.range(0.1, 0.5).slow(4)).gain("1.1"), note("[G3 ~ ~ ~][~ ~ ~ ~][G3 ~ ~ ~][~ ~ ~ ~][F3 ~ ~ ~][~ ~ ~ ~][F3 ~ ~ ~][~ ~ ~ ~]").s("gm_synth_choir").room("5").decay(perlin.range(0.1, 0.5).slow(4)).gain("1.1"), note("[C3 ~ ~ ~][~ ~ ~ ~][C3 ~ ~ ~][~ ~ ~ ~][C3 ~ ~ ~][~ ~ ~ ~][C3 ~ ~ ~][~ ~ ~ ~]").s("gm_synth_choir").room("5").decay(perlin.range(0.1, 0.5).slow(4)).gain("1.1"),
	  note("[C2 ~ ~ ~][C2 ~ ~ ~][C2 ~ ~ ~][C2 ~ ~ ~][C2 ~ ~ ~][C2 ~ ~ ~][C2 ~ ~ ~][C2 ~ ~ ~]").s("gm_church_organ").room("3").gain("0.8"), note("[G2 ~ ~ ~][~ ~ ~ ~][C3 ~ ~ ~][Eb3 ~ ~ ~][Bb2 ~ ~ ~][~ ~ ~ ~][D3 ~ ~ ~][F3 ~ ~ ~]").s("gm_church_organ").room("3").gain("0.8"), note("[Eb3 ~ ~ ~][~ ~ ~ ~][G3 ~ ~ ~][C4 ~ ~ ~][F3 ~ ~ ~][~ ~ ~ ~][Bb3 ~ ~ ~][D4 ~ ~ ~]").s("gm_church_organ").room("3").gain("0.8"), note("[C4 ~ ~ ~][~ ~ ~ ~][Eb4 ~ ~ ~][G4 ~ ~ ~][D4 ~ ~ ~][~ ~ ~ ~][F4 ~ ~ ~][Bb4 ~ ~ ~]").s("gm_church_organ").room("3").gain("0.8"),
	 
	  ///Bass
	 note("[C2]!4[[F2 G2 !|Ab2 F2!]!2]").s("gm_fretless_bass".gain("0.8")),
	 note("[C1]!4[[F1 G1 !|Ab1 F1!]!2]").s("gm_church_organ".gain("0.7")),
	 
	  ///Drums
	 s("[MPC1000_hh MPC1000_hh MPC1000_hh MPC1000_hh]!4").gain("0.2"),
	 s("[MPC1000_bd ~ ~ ~][~ ~ MPC1000_bd ~][~ ~ MPC1000_bd ~][~ MPC1000_bd ~ MPC1000_bd]").gain("2"),
	 s("[~ ~ ~ ~][RolandCompurhythm8000_sd ~ ~ ~][~ ~ ~ ~][RolandCompurhythm8000_sd ~ ~ ~]").gain("0.5")
	 
	).cpm(15)
	
#### I made two chords but made it in one line so that I can add and subtract any time. I personally really like the lpf on Arpegio using perlin to modify the amount of filter. In order to listen to the filter, I'll put arpegio as the first thing to play in the performance.
	 

 
