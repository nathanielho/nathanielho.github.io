---
youtubeId: A2-DZb0vaq8 
---

## Pensioners Power Plant 01 - Intro

_May 2026_

{% include youtubePlayer.html id=page.youtubeId %}

## The EPC C House

In 2025 my parents purchased a bungalow to be their retirement home. The house is a 2-bed, 60 square metres, was built in 1996 and has an EPC of C. So my guestimation is a gas bill of £600 per year, especially the South facing aspect it has.

So stage 1 of the journey was actually getting the Heat Pump (which will be covered in another section), and although I knew that Octopus Agile would happily support the heat pump at the same price as gas (`18p/kWh divided by SCOP of 4`), it would make sense to go all in and proceed with stage 2 was to power that Heat Pump with Solar.

The house had a 60 Amp fuse and a very early 90s looking consumer unit that was cracked. Yet somehow the seller's electrician managed to sign off an EICR for that... Anyway we decided _that had to go_ too for a modern metal consumer unit as part of the whole solar project.


## How I approach Solar PV Systems choice

My Youtube history is basically Green Energy, Solar PV, and Cars. After years of following green energy, I generally research and know a product and then ask for that to be quoted. I was lucky enough to organise & oversee a GivEnergy 3-phase Solar PV installation for Church in March 2025 and now in August 2025 I was asking for GivEnergy & Sigenergy quotes. Both solar installers who came to quote basically dismissed GivEnergy and said Sigenergy would be in budget. The installers seemed to really rate Sigenergy and I already knew from first hand experience how poor GivEnergy software bugs were. (And now we know that GivEnergy has sadly gone into administration in 2026).


## Solar PV Panels

The wonderful south facing roof was going to be maxed out with 7.2kW of Solar PV panels and although Darroch who came to quote, asked me _what do you think about a north facing array?_ - he basically read my mind, but unfortunately the £2k premium for that was too much, so we only did the South facing array.

Although I mentioned I wanted panels like Trina or REC bifacial, Darroch recommended AIKO (mono facial), and now that has turned out to be a great choice. It comes top for value and is only a little behind REC. The efficiency is 23% and has a great heat coefficient. I think we are fine without bifacial for since they are mounted so close to the roof.

Although the other quote came back with 16 panels of 450W, Darroch & Scott said that only 14 would fit (we are talking about the same dimensions). Therefore to compensate, Scott sourced 510W panels, giving me 7140W array which was close enough to the alternative 16 panel 7200W array. The flexibility from Scott was really great throughout the quoting process, he had to accommodate all my different questions and scenarios! (moving old EV charger, North array, EVDC...)

Now I've actually seen the 7.14kW array generate at a peak of 8.3kW in May! (You always get your best production after a bit of cloud cover breaking into full sunshine).

## DNO Application

The DNO surprised me with permission for the full 8kW of our Sigenergy 8kW inverter! I thought we would get only 5kW given how many solar installations there are in the neighbourhood.


## The Gateway

Since this is my parents retirement home, it was prudent to make it ready for future eventualities. There are rarely any power cuts in the town but you never know if you will be running devices that need continuous power. Sidestory: In 2015, my sister lived in a hamlet 5 miles away in old Workers Cottages where the neighbour who was on a respirator sadly passed away during an overnight powercut. We can solve this nowadays with Anker/EcoFlow batteries, but back then they weren't so prevalent. So for the ~£800 premium for the Sigenergy Gateway and especially since we were fully rreplacing & relocating the consumer unit, it made sense to install it. 

So when there is a powercut, all non-gateway Solar PV systems stop producing power, even if you have a battery and blazing sunshine. This is to prevent electricity exporting out and electrocuting anyone working on fixing the powercut. The way around this is using a Gateway that isolates you from the grid in "islanding mode" and you can be happily generating power. 

_I guess in a power cut my parents won't even know, the heat pump will still be running, the home battery will still charge from solar and we can run some long extension leads to the neighbours to share some juice_

The alternative is EPS (Emergency Power Supply), which are separate circuits sitting behind the inverter that supplies some sockets/lights that you designated to be protected. This has a limit of a lower power rating (typically 3kW). This might be fine if you have sockets next to the inverter, but can be a false economy as it might require a second consumer unit, lots of wiring around the house and therefore there could be a lot of labour cost.

Since we also have the EVDC (see chapter below), I have found that the EV V2H can also support the house in off-grid mode. And if we are low on home battery power, we could drive the EV to a public charger to juice up, and then bring back home to power the house. That's our strategy to avoid any petrol/diesel generator.


## EV Charging & V2G/V2H

Now I've been waiting since 2019 for V2G (Vehicle-to-Grid) to be commercially available, we nearly signed up to the OVO Energy V2G with Nissan Leaf trial. And I've seen countless videos of it working in the Netherlands. So I decided the Signenergy EVDC was a toy I had to have. What about the health of the battery? A few extra charges won't stress the EV battery so much, especially if you keep it in the 20-70% SoC range. I also believe that EVs are likely to fail their MOTs from rust well before the battery loses useful life, so I failed MOT Renault Zoe could sit on the driveway to be a second battery.

So we specified the 11kW EVDC (£2800) since the inverter is only 8kW and went for the longer 10m cable option instead of 5m. We don't really need the 10m but the voltage drop over the extra 5m is negligible. It means that we don't have to be restricted to one "bay" for charging and it can stretch to the other side of the driveway.

How to use V2G/V2H Discharging:
- If the EV is at 80%, then you set the charge limit to +1% or greater, so that the EV is "ready to accept charge"
- EVDC handshakes CCS to "start charge" and then takes power out

We opted not to move our 4yo Ohme Home Charger 7.4kW from the old home. It was solid and worked really well. Although it would be nice to have, it was looking cracked and tired the electrician thought it would spoil the aesthetic of a clean house with a Sigestor. We left the Ohme behind to hopefully encourage the next tenant of that home to get an EV! So for AC charging, we depend on the 3-pin plug granny charger (2.3kW), or I may still ask electrician to come back to install a 32A Commando socket (think caravan hook-up) as I already have the 32A Commando adapter (7.4kW), but I am very aware I should really have a PEN device which we left behind with the Ohme.


## EVDC Limitations & Considerations

Sigenergy EVDC Charger sits on the DC Bus, behind the inverter. This has benefits in that the EVDC can take power from Solar + Battery + Grid to reach 11kW, however if you are heavily dependent on off-peak imports at night, you are limited by the inverter size. In our case our total 6hrs of Octopus Intelligent Go import is `6hrs x 8.8kw = 52.8 kWh` to share between the car & home battery. This might not be enough if you do a lot of mileage and have a big battery

Charging Off-Peak: The EVDC is currently higher priority than the home battery when it comes to charging and our 11kW charger will consume all 8.8kW and starve the home battery of any import. Therefore we generally limit the EVDC to 5.2kW to leave around 3kW for the 16kW home battery

Discharging V2G/V2H: We have found that most EVs seem to only discharge at around 3 to 5kW and depending on the EV may have a limit of 5kWh before it throws a hissy fit. The Sigenergy EVDC simply taps into the DC pins and instead of providing juice, it extracts it (unofficial operation without protocols). So right now, itt does not seem to be as dynamic as you would want. I envisaged it behaving like a home battery with instant response. The EV does discharge to match the house load, but the home battery is always faster and more precise. Although this is car-dependent, having to unplug and re-plug when you reach that ~5kWh limit to reset V2G/V2H is annoying. I originally wanted to have only 1x 8kWh Home Battery (4.6kW max output) and depend on the car to provide the 3.4kW to the inverter - but I'm glad Scott talked me into have 2x 8kWh Home Batteries.

Remember that the DC behaviour in a car is different to AC:
- Depending on the vehicle, when the target SoC is reached, the car simply sends a stop command and charging stops.
- It doesn't maintain a connection to allow taking power for e.g. preconditioning etc.
- So if you have a long journey in winter, you may wish to charge to 95% in off-peak hours, and then charge that final 5% from Solar + Home Battery at T-1hr with preconditioning before you set off at time T.


## Tips & Lessons Learnt

- Scaffolding forms a huge part of the cost of installation. Therefore for the scaffolding you have up, you need to maximise what you get out of it. Install the BEST panels you can, as they only cost ~£80 per panel, and paying ~£100 instead is not a lot of premium when you talk about 14 to 16 panels.
- Warranties... they seem to be an indication of how well the manufacturer thinks it will perform, but if you're still liable to pay for the scaffolding to come up to change a single panel (covered under warranty), then I think a long warranty is not that important. So beware of anyone who is trying to sell you on long warranties and lifetime warranties
- For UK, make sure you choose a panel that is great for the grey weather
- EPS is probably not much cheaper if you have to have transfer switch, extra consumer units and rewiring. Gateway could be cost effective and much simpler
- Sigenergy EVDC sits on the DC bus behind the inverter
- Non-MCS routes exist, but make sure there is NAPIT or similar accreditation and that your utility will accept it. Octopus Energy accept NAPIT for signing up to export. This might mean I'm stuck with Octopus forever, but I don't mind that.

## Bugs

- When the home battery is on 0.1% and the solar priority is 1)House 2)Grid 3)Battery, then the home battery suddenly ramps up to discharge at 4kW. This is a known bug and should be fixed in future. Workarounds are to have battery higher priority than Grid, or to set a 1% SoC limit rather than 0%.


## Conclusion

The Sigenergy system has worked really well and was definitely worth paying the premium for. The app is simply fantastic with so many ways to control what you want. The support has been good with responses within a few days and a thorough investigation / explanation.

The sizing of the battery was pretty much at fluke at 16kWh, we charge it up to 100% every night on off-peak 7p electricity. On most 5'C winter days it is sufficient to sustain the House & Heat Pump during the 18 hours of peak electricity hours. And when we are a bit short, we use the EV to provide a few kWh of its off-peak energy.

I can highly recommend the Sigenergy system and AIKO Solar PV panels. Thankfully we were in a position to buy the premium solution and I think its performance will give dividends over the next 30 years!

	



