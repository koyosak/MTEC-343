# second strudel patch

## My patch

### In the second weeks, I had hard understand and using code for music. I usually am slow learner so I had to take all the information in and understand what I'm actually doing using strudel. I think I finally started understand and been able to enjoy this homework.

	stack (
	  ///Arpeggio 
	 n("[0 4 2 7]!2[0 5 3 6]!2").scale("c:minor").s("z_triangle").room("1.5"),
	 n("[9 7 4 0]!2[8 7 5 0]!2").scale("c:minor").s("z_triangle").room("1.5")
	 ).cmp(30)

##### I started the patch with two arpeggio line and trying to see what note goes well together. I also decided what scale I was going to use and what tempo sounds the best, and started building up this patch from it.

	stack (
	  ///Arpeggio 
	 n("[0 4 2 7]!2[0 5 3 6]!2").scale("c:minor").s("z_triangle").room("1.5"),
	 n("[9 7 4 0]!2[8 7 5 0]!2").scale("c:minor").s("z_triangle").room("1.5")
	  ///Bass
	 note("[C2]!2[[F2 G2 !|Ab2 F2!]!2]").s("gm_fretless_bass".gain("0.7")),
	  ///Drums
	 s("[MPC1000_hh MPC1000_hh MPC1000_hh MPC1000_hh]!4").gain("0.2"),
	 s("[MPC1000_bd ~ ~ ~][~ ~ MPC1000_bd ~][~ ~ MPC1000_bd ~][~ MPC1000_bd ~ MPC1000_bd]").gain("2"),
	 s("[~ ~ ~ ~][RolandCompurhythm8000_sd ~ ~ ~][~ ~ ~ ~][RolandCompurhythm8000_sd ~ ~ ~]").gain("0.5")
	 ).cmp(30)
	 
##### I added the bass and the drums and trying to see what I can add to this patch.



	stack (
	  ///Arpeggio 
	 n("[0 4 2 7]!2[0 5 3 6]!2").scale("c:minor").s("z_triangle").room("1.5"),
	 n("[9 7 4 0]!2[8 7 5 0]!2").scale("c:minor").s("z_triangle").room("1.5"),
	  /// Melody
	 note("[Eb6 ~ ~ ~][C6 ~ ~ ~][D6 ~ ~ ~][G5 ~ ~ ~]").s("gm_xylophone").room("2.5"),
	 note("[Eb6 D6 C6 Bb5][G5 F5 Eb5 C5][D6 C6 Bb5 G5][F5 Eb5 D5 Bb4]").s("zzfx").gain("0.7").room("2"),
	  ///Chords
	  note("[Eb4 ~ ~ ~][~ ~ ~ ~][D4 ~ ~ ~][~ ~ ~ ~]").s("gm_synth_choir").room("3"),
	  note("[C4 ~ ~ ~][~ ~ ~ ~][Ab3 ~ ~ ~][~ ~ ~ ~]").s("gm_synth_choir").room("3"),
	  note("[G3 ~ ~ ~][~ ~ ~ ~][F3 ~ ~ ~][~ ~ ~ ~]").s("gm_synth_choir").room("3"),
	  note("[C3 ~ ~ ~][~ ~ ~ ~][C3 ~ ~ ~][~ ~ ~ ~]").s("gm_synth_choir").room("3"),
	  ///Bass
	 note("[C2]!2[[F2 G2 !|Ab2 F2!]!2]").s("gm_fretless_bass".gain("0.7")),
	  ///Drums
	 s("[MPC1000_hh MPC1000_hh MPC1000_hh MPC1000_hh]!4").gain("0.2"),
	 s("[MPC1000_bd ~ ~ ~][~ ~ MPC1000_bd ~][~ ~ MPC1000_bd ~][~ MPC1000_bd ~ MPC1000_bd]").gain("2"),
	 s("[~ ~ ~ ~][RolandCompurhythm8000_sd ~ ~ ~][~ ~ ~ ~][RolandCompurhythm8000_sd ~ ~ ~]").gain("0.5")
	 
	).cpm(30) 
	
##### I ended up adding the melody and chords to the patch and this is my final patch. As I coding this patch, I had few moment when I thought there will be more efficient way to code this patch especially the repetitive part. Overall, I had so much fun building this code as I finally really understand what I'm doing!s
	
	
	 
