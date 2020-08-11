# ts100-flex-c-friend
Info and documentation for the TS100 Flex-C-Friend, an external add-on for TS-100 for adding USB-C Power Deliver (PD)


## Power Selector Switch

**Very Important!**

- If your power supply is > 48W (more specifically supports 20V @ 2.4A or greater), you should move the power selector switch to "20V"
- In any other case, you should move the power selector switch to "15V"

The TS100 will heat up faster using 20V, but it will not work if the supply does not support enough current!

#### More Details Around The Switch:

The TS100 uses different amounts of current based on what voltage it uses:

| Voltage Level  | Current Requirement |
| ------------- | ------------- |
| 20V  | 2.4A  |
| 15V  | 1.8A  |
| 12V  | 1.5A  |

This table is calculated using Ohms law (V=IR) and rounded up. The tip has a fixed resistance of roughly 8.5 Ohms.

The switch is not a gaurantee that you will get that voltage, the IP2721 (the IC used on the Flex-C-Friend for PD negotiating) will try request the selected voltage from the PSU, but it will accept the highest voltage under that. For Example, if you have the switch at "20V" and you plug it into a PSU that the highest voltage it supports is 15V, it will negotiate 15V.

## What Power Supply To Use

The Flex-C-Friend is designed to work with most USB-C PD supplies, it can be broken down as follows:

| Performance  | PSU Capablity |
| ------------- | ------------- |
| Best | <ul><li>48W or more</li><li>Supports 20V</li></ul>|
| Good  | <ul><li>28W or more</li><li>Supports 15V</li></ul>  |
| Poor (not designed for this)   | <ul><li>18W or more</li><li>Supports 12V</li><li>Does not supports 20V or 15V</li></ul>  |

For specific examples of Power Supplies to use:

#### RavPower 60W PD Portable Battery Bank

I have this exact supply and it works great.

- [Amazon.co.uk*](https://amzn.to/2XsIUzt)
- [Amazon.com*](https://amzn.to/31m7jb7)

#### Anker 60W PD Wall Charger

I do not own this supply, but have been happy with their products In the past.

- [Amazon.co.uk*](https://amzn.to/2DIDNnu)
- [Amazon.com*](https://amzn.to/2XylwAs)


\* = Affilate

#### Other Supplies

[Here is a list of chargers tested with the Flex-C-Friend](https://github.com/witnessmenow/ts100-flex-c-friend/blob/master/supplies.md), and feel free to add your own!





