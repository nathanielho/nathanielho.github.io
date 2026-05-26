## Parents Power Plant - 01 Intro
_May 2026_

## The EPC C House

My parents purchased a bungalow to be their retirement home and on viewing the first video sent by them, it showed my biggest fear... a Gas Boiler in the second bedroom cupboard!

_Flashbacks/PTSD: remembering as a 5yo child using a small toilet cubicle with a gas boiler booming above the cistern_

When I saw that boiler, I knew that was going to be ripped out straight away. The Combi boiler looked pretty new, but I was keen on fully electrifying the house and removing all traces of gas; As my parents get older and (unfortunately) forgetful, it would be good to have a modern induction hob that is cold to touch, and auto shuts off. Unlike a gas hob that when unlit, can leak into the house. Let alone the carbon monoxide risk in the BEDROOM.

So stage 1 of the journey was actually getting the Heat Pump (which will be covered in another section), and although I knew that Octopus Agile would happily support the heat pump at the same price as gas (`18p/kWh divided by SCOP of 4`), it would make sense to go all in and proceed with stage 2 was to power that Heat Pump with Solar.

The house was built in 1996 and since it was a bungalow it had a 60 Amp fuse and a very early 90s looking consumer unit that was cracked. Yet somehow the seller's electrician managed to sign off an EICR for that... Anyway we decided _that had to go_ too for a modern metal consumer unit.


## How I approach Solar PV Systems choice

My Youtube history is basically Green Energy, Solar PV, and Cars. After years of following green energy, I generally research and know a product and then ask for that to be quoted. I was lucky enough to organise & oversee a GivEnergy 3-phase Solar PV installation for Church in March 2025 and now in August I was asking for GivEnergy & Sigenergy quotes. Both solar installers who came to quote basically dismissed GivEnergy and said Sigenergy would be in budget. They installers seemed to really rate Sigenergy and I already knew from first hand experience how poor GivEnergy software bugs were. (And now we know that GivEnergy has sadly gone into administration).


## Solar PV Panels

The wonderful south facing roof was going to be filled with around 7.2kW of panels and although Darroch who came to quote, asked me _what do you think about a north facing array?_ I loved the way he thought the same as me, but unfortunately the £2k premium for that was too much.

Although I mentioned I wanted good panels like Trina or REC bifacial, Darroch recommended AIKO (mono facial), and now that has turned out to be a great choice. It comes top for value and is only a little behind REC. The efficiency is 23% and has a great heat coefficient. I think we are fine without bifacial for since they are mounted so close to the roof.

Although the other quote came back with 16 panels, Darroch & Scott said that only 14 would fit (we are talking about the same dimensions). Therefore to compensate, Scott sourced 510W panels, giving me 7140W array which was close enough to the alternative 16 panel 7200W array. The flexibility from Scott was really great - he sadly had to accomodate all my different questions and scenarios! (moving old EV charger, North array, EVDC...)

I've actually seen the 7.1kW array generate at 8.3kW in May! (You always get your best production after a bit of cloud cover breaking into full sunshine).


## The Gateway

Since this is my parents retirement home, we have to make it ready for future eventualities. There are rarely any powercuts in the town but you never know if you will be running devices that need continuous power. My sister lived in a hamlet 5 miles away in old Workers Cottages where the neighbour who was on a respirator sadly passed away during an overnight powercut. We can solve this nowadays with Anker/EcoFlow batteries, but back then they weren't so prevalent. So for the ~£800 premium for the Sigenergy Gateway and especially since we were fully re-doing the consumer unit, it made sense to install it. 

So when there is a powercut, all Solar PV systems stop producing power, even if you have a battery and sunshine. This is to prevent electricity exporting out and electricuting anyone working on fixing the powercut. The way around this is using a Gateway that isolates you from the grid and you can be happily generating power. 

_I guess in a power cut we won't even know, the heat pump will still be running, the home battery will still charge from solar and we can run some long extension leads to the neighbours to share some juice_

The alternative is EPS (Emergency Power Supply), which are separate circuits sitting behind the inverter that supplies some sockets/lights that you designated to be protected. This might be fine if you have sockets next to the inverter, but can be a false economy as it might require a second consumer unit, lots of wiring around the house and therefore there could be a lot of labour cost.

Since we have the EVDC (see chapter below), I have found that it can also support the house in off-grid mode. And if we are low on home battery power, we could drive the EV to a public charger to juice up, and then bring back home to power the house. That's our strategy to avoid any petrol/diesel generator.


## EV Charging & V2G/V2H

Now I've been waiting since 2019 for V2G (Vehicle-to-Grid), we nearly signed up to the OVO Energy V2G with Nissan Leaf trial. And I've seen countless videos of it working in the Netherlands. So I decided the Signenergy EVDC was a toy I had to have. I also believe that EVs are likely to fail their MOTs from rust well before the battery loses useful life, so I failed MOT Renault Zoe could sit on the driveway to be a second battery.

So we specified for £2800, the 11kW EVDC since the inverter is only 8kW and went for the longer 10m cable option instead of 5m. We don't really need the 10m but the voltage drop over the extra 5m is negligible. It means that we don't have one "bay" for charging and it can stretch to the other side of the driveway.

Remember that the DC behaviour in a car is different to AC:
- Depending on the vehicle, when the target SoC is reached, the car simply sends a stop command and charging stops.
- It doesn't maintain a connection to allow taking power for e.g. preconditioning etc.
- So if you have a long journey in winter, you may wish to charge to 95% in off-peak hours, and then charge from Solar + Home Battery at T-1hr with preconditioning before you set off at time T.

We opted not to move the 4yo Ohme Home Charger 7.4kW from the old home. It was solid and worked really well. Although it would be nice to have, it was looking cracked and tired the electrician thought it would spoil the aesthetic of a clean house with a Sigestor. We left the Ohme behind to hopefully encourage the next tenant of that home to get an EV! So for AC charging, we depend on the 3-pin plug granny charger (2.3kW), or I may still ask electrician to come back to install a 32A Commando socket (think caravan hook-up) as I already have the 32A Commando adapter (7.4kW), but I am very aware I should really have a PEN device which we left behind with the Ohme.


## EVDC Limitations & Considerations

Sigenergy EVDC Charger sits on the DC Bus, behind the inverter. This has benefits in that the EVDC can take power from Solar + Battery + Grid to reach 11kW, however if you are heavily dependent on off-peak imports at night, you are limited by the inverter size. In our case our total 6hrs of Octopus Intelligent Go import is `6hrs x 8.8kw = 52.8 kWh` to share between the car & home battery. This might not be enough if you do a lot of mileage and have a big battery

Charging Off-Peak: The EVDC is currently higher priority than the home battery when it comes to charging and our 11kW charger will consume all 8.8kW and starve the home battery of any import. Therefore we generally limit the EVDC to 5.2kW to leave around 3kW for the 16kW home battery

Discharging V2G/V2H: We have found that most EVs seem to only discharge at around 3 to 5kW and depending on the EV may have a limit of 5kWh before it throws a hissy fit. The Sigenergy EVDC simply taps into the DC pins and instead of providing juice, it extracts it (unofficial operation without protocols). So right now, itt does not seem to be as dynamic as you would want. I envisaged it behaving like a home battery with instant response. The EV does discharge to match the house load, but the home battery is always faster and more precise. Although this is car-dependent, having to unplug and re-plug when you reach that ~5kWh limit to reset V2G/V2H is annoying. I originally wanted to have only 1x 8kWh Home Battery (4.6kW max output) and depend on the car to provide the 3.4kW to the inverter - but I'm glad Scott talked me into have 2x 8kWh Home Batteries.

How to use V2G/V2H Discharging:
- If the EV is at 80%, then you set the charge limit to +1% or greater, so that the EV is "ready to accept charge"
- EVDC handshakes CCS to "start charge" and then takes power out


## Tips & Lessons Learnt

- Scaffolding forms a huge part of the cost of installation. Therefore for the scaffolding you have up, you need to maximise what you get out of it. Install the BEST panels you can, as they only cost ~£80 per panel, and paying ~£100 instead is not a lot of premium when you talk about 14 to 16 panels.
- Warranties... they seem to be an indication of how well the manufacturer thinks it will perform, but if you're still liable to pay for the scaffolding to come up to change a single panel (covered under warranty), then I think a long warranty is not that important. So beware of anyone who is trying to sell you on long warranties and lifetime warranties
- For UK, make sure you choose a panel that is great for the grey weather
- EPS is probably not much cheaper if you have to have transfer switch, extra consumer units and rewiring. Gateway could be cost effective and much simpler
- Sigenergy EVDC sits on the DC bus behind the inverter
- Non-MCS routes exist, but make sure there is NAPIT or similar accrediation and that your utility will accept it. Octopus Energy accept NAPIT for signing up to export. This might mean I'm stuck with Octopus forever, but I don't mind that.

## Bugs

- When the home battery is on 0.1% and the solar priority is 1)House 2)Grid 3)Battery, then the home battery suddenly ramps up to discharge at 4kW. This is a known bug and should be fixed in future. Workarounds are to have battery higher priority than Grid, or to set a 1% SoC limit rather than 0%.


## Conclusion
The Sigenergy system has worked really well so far. The app is simply fantastic with so many ways to control what you want. The support has been good with responses within a few days and a thorough investigation / explanation.



