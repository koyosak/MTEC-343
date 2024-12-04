# Final tidal cycles patch



## Patch Breakdown

### tempo 

		setcps (120/60/4)
		
	
	
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
	  
## Changes from the last patch I submitted
	
### Snare
	d3 $ s "[~ ~ ~ sd][sd ~ ~ sd][~][sd ~ ~ sd]"
  	# gain ("0.6")
  	# room ("0.4")
	
### Sample
	d4 $ n "2 4 3 1"
  	# sound "seawolf"
  	# gain ("0.4")
	
### Percussion 1
	d5 $ n "2 4 6 8 4 6 8 8 6 8 6 1 8 7 8 6"
  	# sound "voodoo"
  	#gain ("0.8")
	
### Percussion 2
	d6 $ n "2 4 6 5 2 5 4 5 2 4 1 5 2 5 6 5"
    # sound "voodoo"
    # gain ("0.7")
	
### Random piano line 1
	d7 $ jux rev $ chunk 2 (fast 2 . (|+ n 12)) $ off 0.5 (|+ 7) $ struct (iter 4 "t(5,8)")
    $ n (scale "e minor" "0 .. 10")
    # sound "<superpiano>"
    # gain ("0.6")
    # lpf "<5000 10000>"
    # hpf "<1000 2000>"
    # room "<0.4>"
    # lpq 0.2

	
### Random piano line 2
	d8 $ jux rev $ chunk 1 (fast 2 . (|- n 12)) $ off 0.5 (|+ 14) $ struct (iter 4 "t(5,8)")
    $ n (scale "e minor" "0 .. 10")
    # sound "<superpiano>"
    # gain ("0.6")
    # lpf "<10000>"
    # hpf "<1000>"
    # room "<0.8>"
    # lpq 0.2
	
### Random piano line 3
	d9 $ jux rev $ chunk 2 (fast 2 . (|+ n 12)) $ off 0.5 (|+ 10) $ struct (iter 4 "t(5,8)")
    $ n (scale "g minor" "0 .. 10")
    # sound "<superpiano>"
    # gain ("0.6")
    # lpf "<10000>"
    # hpf "<1000>"
    # room "<0.4>"
    # lpq 0.2
    
### Original sample 1
	d10 $ s "sample"
    # gain ("0.95")
    # lpf "<10000 40000>"
    
### Original sample 2
	d11 $ s "sample1"
    # gain ("1.2")
    # room "<0.2>"
    # lpf "<5000 10000>"
    
##### I decided to use my own sample for this patch since I had some drum samples in the same BPM.
	
## The entire patch
	setcps (120/60/4)
	d1 $ rarely (# speed 2)
	  $ s "[808bd ~ ~ 808bd][[~ ~ 808bd ~ | ~ ~ 808bd ~]][808bd ~ ~ 808bd][[~ ~ 808bd ~ | ~ ~ 808bd ~]]"
	  # gain ("1.2")
	d2 $ s "[hh hh hh hh][hh hh hh hh][hh hh hh hh][hh hh hh hh]"
	  # hbrick sine
	  # pan ("0.5 0 1")
	  # room ("0.4")
	  # gain ("0.95")
	  # decay "[1 0.2]/4"
	  # hpf "500"
	  # vowel "[a e i o u]/8"
	d3 $ s "[~ ~ ~ sd][sd ~ ~ sd][~][sd ~ ~ sd]"
	  # gain ("0.6")
	  # room ("0.4")
	d4 $ n "2 4 3 1"
	  # sound "seawolf"
	  # gain ("0.4")
	d5 $ n "2 4 6 8 4 6 8 8 6 8 6 1 8 7 8 6"
	  # sound "voodoo"
	  #gain ("0.8")
	d6 $ n "2 4 6 5 2 5 4 5 2 4 1 5 2 5 6 5"
	    # sound "voodoo"
	    # gain ("0.7")
	d7 $ jux rev $ chunk 2 (fast 2 . (|+ n 12)) $ off 0.5 (|+ 7) $ struct (iter 4 "t(5,8)")
	    $ n (scale "e minor" "0 .. 10")
	    # sound "<superpiano>"
	    # gain ("0.6")
	    # lpf "<5000 10000>"
	    # hpf "<1000 2000>"
	    # room "<0.4>"
	    # lpq 0.2
	d8 $ jux rev $ chunk 1 (fast 2 . (|- n 12)) $ off 0.5 (|+ 14) $ struct (iter 4 "t(5,8)")
	    $ n (scale "e minor" "0 .. 10")
	    # sound "<superpiano>"
	    # gain ("0.6")
	    # lpf "<10000>"
	    # hpf "<1000>"
	    # room "<0.8>"
	    # lpq 0.2
	d9 $ jux rev $ chunk 2 (fast 2 . (|+ n 12)) $ off 0.5 (|+ 10) $ struct (iter 4 "t(5,8)")
	    $ n (scale "g minor" "0 .. 10")
	    # sound "<superpiano>"
	    # gain ("0.6")
	    # lpf "<10000>"
	    # hpf "<1000>"
	    # room "<0.4>"
	    # lpq 0.2
	d10 $ s "sample"
	    # gain ("0.95")
	    # lpf "<10000 40000>"
	d11 $ s "sample1"
	    # gain ("1.2")
	    # room "<0.2>"
	    # lpf "<5000 10000>"
	
	hush
	
## Visual element

#### Since I can't use Hydra in Pulsar, I decided to use Strudel for the visual.

	await initHydra({feedStrudel:1})

	shape(60,.8)
	 .modulatePixelate(osc(20,.8))
	  .out()
	  
##### it is a very simple patch, but I like the simple and monotone visual for the Tidal Cycle patch that I created.
