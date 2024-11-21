# second tidal cycles patch


## Progress from last week 

#### For this week, I added and changed the patch I created last week 

## Patch Breakdown

### tempo 
#### I changed the way of setting tempo from last week 
	Previous tempo 
		setcps (0.4)
	Current tempo
		setcps (120/60/4)
		
##### I realized when I tried to adjust the tempo that I have more precision and it's easier for me to understand in bpm than random number.
	
	
### Bass drum
	d1 $ rarely (# speed 2) 
	$ s "[808bd ~ ~ 808bd][[~ 808bd ~ ~ | ~ ~ 808bd ~]][808bd ~ ~ 808bd][[~ 808bd ~ ~ | ~ ~ 808bd ~]]" 
	# gain ("1.2")
	
### Hi-hat
	d2 $ s "[hh hh hh hh][hh hh hh hh][hh hh hh hh][hh hh hh hh]"
	  # hbrick sine
	  # pan ("0.5 0 1")
	  # room ("0.4")
	  # gain ("1.2")
	  # vowel "[a e i o u]/8"
	  # decay "[1 0.2]/4"
	  # hpf "500"
	  
##### I added more effect to the hi-hat and adjusting the amount of each effect
	
### Bass 1
	d3 $ n "[5][~][~ ~ 5 ~][~ [5|[~ 5]] ~ ~]"
	  # sound "bass1"
	  # lpf 400
	  # gain ("0.6")
	  # vowel "[a u o]/4"
	
### Bass 2
	d4 $ n "[0][~][~ ~ 0 ~][~ [0|[~ 0]] ~ ~]" 
	# sound "bass1" 
	# lpf 400 
	# gain ("1.0")
	
##### I added more effect to basses
	
### Sample
	d5 $ n "2 4 3 1" 
	# sound "seawolf" 
	# gain ("0.6")
	
### Drum 2
	d6 $ n "2 4 6 8 4 6 8 8 6 8 6 8" 
	# sound "voodoo"
	
### Drum 3
	d9 $ n "2 4 6 5 2 5 4 5 2 4 1 5 2 5 6 5"
    # sound "voodoo"
    # gain ("0.7")

##### I created another drum line to add complexity to the beat
	
### Sample 3
	I got rid of this sample
	
### Piano line
	d11 $ jux rev $ chunk 1 (fast 2 . (|+ n 24)) $ off 0.25 (|+ 14) $ struct (iter 4 "t(5,8)")
    $ n (scale "g phrygian" "0 .. 10") 
    # sound "<superpiano>"
    # gain ("0.7")
    # lpf "<1000 4000>"
    # lpq 0.2
##### I used chunk to divided the pattern and make it double the speed at the pitch that transposed down the octave. I give 0.25 delay for the trasnsposed note which is +14. I used struct so that those pattern happens 4 times in the cycle with 5 hits distributed by 8 steps.
	
## The entire patch
	setcps (120/60/4)
	d1 $ rarely (# speed 2)
	  $ s "[808bd ~ ~ 808bd][[~ 808bd ~ ~ | ~ ~ 808bd ~]][808bd ~ ~ 808bd][[~ 808bd ~ ~ | ~ ~ 808bd ~]]"
	  # gain ("1.2")
	d2 $ s "[hh hh hh hh][hh hh hh hh][hh hh hh hh][hh hh hh hh]"
	  # hbrick sine
	  # pan ("0.5 0 1")
	  # room ("0.4")
	  # gain ("1.2")
	  # vowel "[a e i o u]/8"
	  # decay "[1 0.2]/4"
	  # hpf "500"
	d3 $ n "[5][~][~ ~ 5 ~][~ [5|[~ 5]] ~ ~]"
	  # sound "bass1"
	  # lpf 400
	  # gain ("0.6")
	  # vowel "[a u o]/4"
	d4 $ n "[0][~][~ ~ 0 ~][~ [0|[~ 0]] ~ ~]"
	  # sound "bass1"
	  # lpf 400
	  # gain ("0.6")
	d5 $ n "2 4 3 1"
	  # sound "seawolf"
	  # gain ("0.4")
	d6 $ n "2 4 6 8 4 6 8 8 6 8 6 8 8 8 1 8"
	  # sound "voodoo"
	  #gain ("0.8")
	d7 $ n "[f][~][~ ~ f ~][~ [c|[~ c]] ~ ~]"
	  # sound "bass1"
	  # lpf 400
	  # gain ("0.8")
	d8 $ n "2 4 6 5 2 5 4 5 2 4 1 5 2 5 6 5"
	    # sound "voodoo"
	    # gain ("0.7")
	d9 $ jux rev $ chunk 1 (fast 2 . (|+ n 24)) $ off 0.25 (|+ 14) $ struct (iter 4 "t(5,8)")
	    $ n (scale "g phrygian" "0 .. 10") 
	    # sound "<superpiano>"
	    # gain ("0.7")
	    # lpf "<1000 4000>"
	    # lpq 0.2
	
	hush
	
	 
