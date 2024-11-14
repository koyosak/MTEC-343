# first tidal cycles patch

## difference between strudel and tidal cycles

#### While I was working on this week assignment, I realized that there are some difference between strudel and tidal cycles. I was a little confused and had to get used to it. 
##### For example, when I tried to control the tempo, I thought the scale of "setcps" was bpm. So when I first set it 60, it got so fast and caught me off guard. 
##### I also tried to use the name of the note (for example Eb6) by using the same syntax, but it didn't work. I need to do further research for this one.

## Patch Breakdown

### tempo 
	setcps (0.4)
	
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
	
### Bass 1
	d3 $ n "[5][~][~ ~ 5 ~][~ [5|[~ 5]] ~ ~]" 
	# sound "bass1" 
	# lpf 400 
	# gain ("1.2")
	
### Bass 2
	d4 $ n "[0][~][~ ~ 0 ~][~ [0|[~ 0]] ~ ~]" 
	# sound "bass1" 
	# lpf 400 
	# gain ("1.0")
	
### Sample
	d5 $ n "2 4 3 1" 
	# sound "seawolf" 
	# gain ("0.6")
	
### Drum 2
	d6 $ n "2 4 6 8 4 6 8 8 6 8 6 8" 
	# sound "voodoo"
	
### Sample 3
	d7 $ s "koy" 
	# gain ("0.7")
	
## The entire patch
	setcps (0.4)
	d1 $ rarely (# speed 2) $ s "[808bd ~ ~ 808bd][[~ 808bd ~ ~ | ~ ~ 808bd ~]][808bd ~ ~ 808bd][[~ 808bd ~ ~ | ~ ~ 808bd ~]]" # gain ("1.2")
	
	d2 $ s "[hh hh hh hh][hh hh hh hh][hh hh hh hh][hh hh hh hh]" # hbrick sine # pan ("0.5 0 1") # room ("0.4") # gain ("1.2")
	
	d3 $ n "[5][~][~ ~ 5 ~][~ [5|[~ 5]] ~ ~]" # sound "bass1" # lpf 400 # gain ("1.2")
	
	d4 $ n "[0][~][~ ~ 0 ~][~ [0|[~ 0]] ~ ~]" # sound "bass1" # lpf 400 # gain ("1.0")
	
	d5 $ n "2 4 3 1" # sound "seawolf" # gain ("0.6")
	
	d6 $ n "2 4 6 8 4 6 8 8 6 8 6 8" # sound "voodoo"
	
	d7 $ s "koy" # gain ("0.7")
	
	hushs
	
	 
