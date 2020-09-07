# FAQ

## Why does the switch face inwards?

I wanted to try ensure the switch was never unintentionally changed and one suggestion I got on a stream was to face it inwards. The switch will be toggled very very infreuently, most people will only change it once to match their power supply and then leave it as it is. The inward facing switch can be toggled without using any tools, but it is slightly awkward to do.

## What is the maximum power that can be supplied to the TS100 with a Flex-C-Friend?

*TL;DR*: ~48W

The TS100 is a 65W capable iron, but I think it is commonly misunderstood how it works.

The TS100 can operate between 12V and 24V, but it uses different amounts of current based on what voltage you supply it:

| Voltage Level  | Current Requirement | Power |
| ------------- | ------------- | ------- |
| 24V (not a PD standard) | 2.8A | 68W (is it really a 68W iron!?) |
| 20V (Max PD supports)  | 2.4A  | 48W |
| 15V  | 1.8A  | 27W |
| 12V  | 1.5A  | 18W | 

*This table is calculated using Ohms law (V=IR) and rounded up. The tip has a fixed resistance of roughly 8.5 Ohms.*

So given the max voltage that can be provided via PD is 20V, the max power that can be supplied is 48W.
