# Strudel purcussion patch

#### I started building patch by referencing the stack example on the class GitHub.

### The stack Patch reference

	stack( 
	 "[bd ~ ~ bd] [~ ~ ~ bd] [~ bd bd ~] [~ ~ ~ ~] ",
	 "[~ ~ ~ ~] [sd ~ ~ ~] [~ ~ ~ ~] [sd ~ ~ ~] ", 
	 "[hh ~ hh ~] [hh ~ hh ~] [hh ~ ~ ~] [hh ~ hh ~] ", 
	 "[~ ~ ~ ~] [ho ~ ~ ~] [~ ~ ho ~] [~ ~ ~ ~] ", 
	 ).s()
 
#### From there, I started experiment by changing the beat and sound

	stack(
	  "[KorgDDM110_bd ~ ~ ~] [~ ~ KorgDDM110_bd ~] [~ bd ~ ~] [bd ~ ~ ~] ",
	  "[~ ~ ~ ~] [MPC1000_sd ~ ~ ~] [~ ~ MPC1000_sd ~] [~ ~ ~ MPC1000_sd] ",
	  "[hh hh hh ~] [hh ~ hh hh] [~ hh ~ hh] [~ ~ hh hh] ",
	  "[ho ~ ~ ~] [ho ~ ~ ~] [ho ~ ~ ~] [ho ~ ~ ~] ",
	).s()

#### Once I get the beat I wanted I added another instruments as well as adding random syntax to make the beat slight different each cycle

	stack(
	  "[KorgDDM110_bd ~ ~ ~] [~ ~ KorgDDM110_bd ~] [~ bd ~ ~] [bd ~ ~ ~] ",
	  "[~ ~ ~ ~] [MPC1000_sd ~ ~ ~] [~ ~ MPC1000_sd ~] [~ ~ ~ MPC1000_sd] ",
	  "[[hh!|hh!3|hh!4] hh hh ~] [hh ~ hh hh] [~ hh ~ hh] [~ ~ hh hh] ",
	  "[ho ~ ~ ~] [ho ~ ~ ~] [ho ~ ~ ~] [ho ~ ~ ~] ",
	  "[BossDR55_sd ~ ~ BossDR55_sd][BossDR55_sd ~ ~ BossDR55_sd][~ ~ ~ BossDR55_sd][BossDR55_sd ~ ~ BossDR55_sd]",
	  "[gm_guitar_fret_noise ~ ~ ~][gm_guitar_fret_noise ~ ~ ~][~ ~ gm_guitar_fret_noise ~][gm_guitar_fret_noise! ~ ~ ~]",
	).s()
	
#### For this time, I used Strudel more as a drum machine. I would like to experiment more and use pitch instrument and keep playing with it!