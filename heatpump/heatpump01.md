---
layout: page
title: "Pensioners Power Plant 01 — Intro"
---

_May 2026_



My parents purchased a 2-bedroom 60 square metre bungalow to be their retirement home and on viewing the first video sent by them, it showed my biggest fear… a Gas Boiler in the second bedroom cupboard!

_Flashbacks/PTSD: remembering as a 5yo child using a small toilet cubicle with a gas boiler firing up and booming above my head_

When I saw that boiler, I knew that was going to be ripped out straight away. The Combi boiler looked pretty new, but I was keen on fully electrifying the house and removing all traces of gas; As my parents get older and (unfortunately) forgetful, it would be good to have a modern induction hob that is cold to touch, and auto shuts off. Unlike a gas hob that when unlit, can leak into the house. Let alone the carbon monoxide risk in the BEDROOM.

Another benefit of removing all gas appliances is that we could have the gas supply removed saving ~£100 of standing charge per year. So making sure the gas hob was replaced with an electric induction made sense to be performed at the same time.

So stage 1 of the journey was actually getting the Heat Pump, and although I knew that Octopus Agile would happily support the heat pump at the same price as gas (~18p/kWh divided by SCOP of 4), it would make sense to go all in and proceed with stage 2 was to power that Heat Pump with Solar.

Unfortunately in the town there were no Heat Pump installers and I had to look at the nearby cities 1 hour away. The first installer came and quoted a great price, however I broke my rule as I was up against time and by the time a second installer had time to quote, the first guy was already starting work. 


## Retrofit
I knew that with an EPC C house it was going to be relatively good canvas to start with. It’s not too leaky and we can constantly pump heat in to deal with the heat loss. It is also has some big south facing windows so the passive solar gain is also very good.

My original plan was to keep the existing radiators and operate the Heat Pump at high temperature - with the intention that it would be good to prove that works - however the radiators were all fed with microbore pipes. These pipes have a diameter of a pencil! So the installer said by the time he starts changing out the pipes and a few radiators, it would be pretty cost comparable to installing underfloor heating. Fortunately we were able to afford a 2 month window where all the Heat Pump & Solar works could be carried out in the empty house, before we had to move in.

## Overlay Underfloor Heating (UFH)
According to Building Regulations, underfloor heating should be done with high levels of insulation. Think 100mm cotex, with pipes laid on top, finished with a nice 30-50mm concrete screed.

However this would involve digging up the very nice concrete floor and take ages. There is now the availability of overlay systems which are polystyrene boards of 20-30mm thick, which have grooves to put in the UFH pipes and finished with silver foil. These boards sit directly on to the existing concrete floor and shouldn't heat the concrete up too much. You top this off with 20mm of self-levelling screed for a nice smooth finish. 

Unfortunately the job done by the installer was horrendous, it wasn’t level with some pipes still exposed. Frankly there wasn’t enough used and with the sinking of the screed into pits and grooves, it looked spottier than a teenagers face. It frankly looked like the first time he'd ever done screeding... The opinion of the flooring installer was that it was really unacceptable and would lead to the vinyl tearing over the imperfect pits and dips.

Our builder came to save the day by adding more of the same self-levelling screed and although not fully level, the smoothness was much improved which meant that luxury vinyl could be put on without fear of it tearing. It has been saved but due to height changes you can catch yourself on the odd high point.

Vinyl was chosen for the practical purpose of it being quite grippy - useful for the elderly. If I had known the Heat Pump installer would not be able to do a good job, I would have opted for laminate floorboards. As this does not require screed but rather an intermediate plastic grid. _But how was I to know?_


## Vaillant aroTherm 5kW

A Vaillant aroTherm 5kW was quoted by the installer, along with the Vaillant 150L slimline tank. We opted for remote app connectivity with the myVAILLANT Connect, so that I could control and diagnose it from anywhere in the world.

The only connection possible is via 2.4GHz WiFi and I originally found the app to be very “buggy” and new settings would only be set 25% of the time. This turned out to be caused by WiFi connectivity & congestion issues. Once I offloaded all the home computers/tablets/phones to 5GHz band, the Vaillant app left alone on 2.4GHz WiFi band has been working very well.

I have also connected it to Home Assistant which allows me to track things like water pressure and have more historic information of issues like pressure loss.

## Domestic Hot Water

When the Hot Water cylinder is recharged/heated, the space heating is not in operation. This means that the temperature in the home can drop. You can choose whether to perform the hot water recharge in:

1. Eco Mode - slowest and most efficient
2. [Mick Wall's Sweet Spot] (https://energy-stats.uk/vaillant-arotherm-hot-water-modes-performance/) (Normal mode with quiet operation)
3. Normal Mode - Fastest but least efficient

We have left it only in Eco mode, even in winter.


## Winter Operation

In winter, we have the thermostat set at 20.5°C space heating and we find it overshoots to 22°C. The system runs space heating 24/7 except for when Hot Water is being recharged.  

- We are performing Domestic Hot Water recharging at 13:00 as this is the _hottest_ part of the day (for higher efficiency) whilst balancing the fact that the grid usually has less load at this time
- In Eco Mode, we hope it finishes by 15:30 to allow space heating to resume before the peak grid time of 16:00
- However in Dec/Jan we do add 1 hour of Hot Water recharging at 01:00 at night during off-peak times. This allows the house to cool a bit for a comfortable sleeping temperature. I originally did this because the target temperature would not be reached in the 120 minute maximum time. However I have since removed all limits entirely and next Winter may not perform a night time “boost” 
- Usually the tank is depleted to 12°C (probe is in the bottom 1/3)
- We heat hot water up to 55 to 58°C
- We do not run legionella cycle since a full tank is depleted per day
- I’m chasing efficiency by recharging during the day, even though it means using the Home Battery which is a bit precious on certain days - therefore we end up leaning on the EV V2H to provide extra power. Some people choose to do a full recharge during off-peak electricity hours.


## Summer Operation
 In summer with the abundance of solar, we don’t change the thermostat from Winter. 20.5°C during the day, with a cooler 19.5°C for night. That’s the benefit of Heat Pumps, is that you never really touch the thermostat!

The system will switch off the space heating at a (configurable) outdoor temperature of 19°C.

- We are performing Domestic Hot Water recharging at 13:00 as this is the _hottest_ part of the day (for higher efficiency) whilst balancing the fact that the grid usually has less load at this time and usually does not want so much solar export
- In Eco Mode, we hope it finishes by 15:00 to allow space heating to resume before the peak grid time of 16:00
- Usually the tank is depleted to 18°C  (probe is in the bottom 1/3)
- We heat hot water up to 50 to 52°C
- We do not run legionella cycle since a full tank is depleted per day
- There is an abundance of Solar Power in summer and although it is more cost effective to operate Hot Water recharging in the night time off-peak hours (at 7p import), I'm chasing efficiency instead at the detriment of not exporting a couple of kWh at 12p.


## The Comfort

You have to understand that my parents barely used the gas boiler for space heating in their previous home in order to save money/carbon. I believe that EPC C home had an annual gas bill of only £400 per year which means they must have been cold a lot of the time. As they get older, this is not good for their health. One main motivation of embarking on this whole green energy Net Zero bills project was that I did not want them to worry about switching on the heating at all. With the efficient heat pump + Underfloor Heating setup + home batteries, they are now super warm, all year round, with quite dry humidity.

So we originally planned to simply keep the Heat Pump's thermostat in manual mode and set it to 20.5°C and forget it. It would generally be 22°C inside and 45% humidity. The issue was that it was too hot at night and hence we had to switch to timer mode with 19.5C at night.

Underfloor heating operates the water flow at 30°C which is frankly glorious. I have no idea why all flooring (vinyl, wood laminate) all seem to state the maximum temperature permitted is 27°C. This is quite an annoyingly low figure! Since the flow temperature is weather compensated, you can see it operate anywhere from 28 to 35°C (the latter when it is sub-zero ambient). However the luxury vinyl hasn’t deteriorated… yet…

The kitchen has UFH pipes only on the walkable areas, but not under the cabinets. I would have liked to have it under the cabinets as we just have the raw concrete under there. But then that might remove any "Cool Dry Place" for foods...

The bathroom is south facing, so when the sun shines it is very warm, but when it is cold & windy we can definitely feel cold draughts from behind the toilet and under the bath. It just means the bath needs topping up with hot water more often. The warm floor always feels great but the space can feel cold. If we ever renovate the bathroom, we will definitely seal the wall up and put UFH pipes under the bath too. This gives the benefit of:
- A larger emitter space
- Warmer Bath for longer

But we'll see how the Towel Radiator replacement goes (see below)


## Heating Curve

Pretty much from day 1 in Oct, we started on a heating curve of 0.55 and slowly found that once the house warmed up (it was empty for months)

0.45 seems to be the best compromise to deal with the cold North of England whilst balancing the 27°C maximum for the flooring. 0.40 could be used, but I’ve erred on the safer side just in case. I don’t want my parents to be cold on a windy night.


## Towel Radiator 

We kept the towel radiator in the bathroom to hang towels on. The downside of operating at low temperature of 30°C (heating curve at 0.45 to "protect the flooring") is that the radiator doesn’t really seem to be that effective. It’s basically a mild towel conduction heater, than a convection radiator. However I have plans to change it to a large T21 or T22 radiator so that we can see if convection does better at drying towels. Failing that, we'll have a large surface area for conduction.

I am not a fan of towel radiators - I prefer regular radiators. And don't get me started on the new trendy style floor to ceiling ones...


## Temporary Operation on Octopus Agile

When the Sigenergy system was not commissioned, we operated for 1.5 months on Octopus Agile. 
- We had the space heating off at 16:00 - 19:00 when Agile electricity was the most expensive.
- We would recharge the cylinder at the cheapest times, which was usually the early hours of the morning 01:00
- November/December 2025, the average price seemed to be 18p/kWh, so with a SCOP of 4 or 5, you are matching gas prices.


## Tips & Lessons Learned

- They always say get multiple quotes, but I was balancing getting the house ready within 3 months of purchase. So I went with the one and only person who came to quote. Being a heat pump installer I simply assumed he knew how to do Underfloor Heating Screeding. 
- It’s quite possible that even if I had a second quote I might still have chosen the same installer.
- I might have gone for a method without screeding. So that would have been laminate floorboards
- It is all about the emitters and it is even more critical when you are using low temperature heat pumps. You want the most amount of UFH pipes down as possible. If you can, to get them under your kitchen cabinets and bath tub etc.


## Conclusion

The Heat Pump has definitely achieved the desired ambition to avoid having a cold house to save pennies & carbon emissions. It is pretty much set and forget and when my parents said to me that on sunny days it is 24°C+ and what should they do to reduce the temperature? I just simple said "open the window" - you also feel less wasteful (money, energy, carbon) when operating a heat pump.

Fortunately we were in a position to support this Heat Pump installation with a Solar + Home Battery setup to allow the home to operate on 100% off-peak energy, which helps reduce the pay back periods.
