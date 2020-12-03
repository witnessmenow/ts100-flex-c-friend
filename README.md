# ts100-flex-c-friend
The Flex-C-Friend is an open source external module for the TS100 soldering iron that allows you to power the Iron from a USB-C Power Delivery PSU, including compatible battery banks.

![img](https://i.imgur.com/iFAO6KE.png?1)

Available on my [Tindie Store](https://www.tindie.com/products/21280/)!

I am very proud to say that it is the first OSHWA certified project from Ireland! - [OSHWA UID: IE000001](https://certification.oshwa.org/ie000001.html)

This repo contains [hardware files](hardware/README.md) for this project and also documentation for using the product.

## Help Support what I do!

My main contribution to the open source community to date has been my Arduino libraries for the ESP32 and ESP8266, but this is my first step into certified open source hardware. 

[If you enjoy my work, please consider becoming a Github sponsor!](https://github.com/sponsors/witnessmenow/)

## Required Hardware

To use the Flex-C-Friend, you will require the following hardware:

- TS100 Soldering Iron
    - [Aliexpress* (inc shipping from China, EU, US and Auz)](https://s.click.aliexpress.com/e/_dS5AyX4)
    - [Amazon.com*](https://amzn.to/2Ymc7fL)
    - [Amazon.co.uk*](https://amzn.to/31gFd1S)
- USB-C Power Delivery PSU - See below for more details
- XT60 to 5525 Cable - traditionally these would have been used for powering the TS100 via LiPO batteries. 
   - 45CM Miniware branded - Optional Add-on on the [Tindie listing](https://www.tindie.com/products/21280/)
   - [45CM Possibly Miniware branded (not sure, not the source of the above) Aliexpress](https://www.aliexpress.com/item/4000798024535.html)
   - [150CM RJXHobby Aliexpress*](https://s.click.aliexpress.com/e/_d6P4TaK)

\* = Affiliate

## Power Supply & Power Selection Switch

**Very Important!**

The Flex-C-Friend is designed to work with USB-C Power Delivery supplies. Power Delivery (PD) is a specific type of standard for USB-C PSUs, it will usually be labeled on the product listing and on the side/bottom of the PSU.

PD supplies can support a range of different voltage levels, and to ensure compatibility with most PD supplies, the Flex-C-Friend has a switch that allows you to configure what voltage is requested from the PSU.

To help illustrate what to do, here are some instructions that are sure to bring back some flat-pack related traumas in your life!

![img](https://i.imgur.com/AFrQpDM.png?1)

To put the above into words: 
- Look at the capabilities of your PD supply and do one of the following
- If it supports 20V with 2.4A or more, set the switch to **20V** 
- If it supports 15V with 1.8A or more, set the switch to **15V**

The TS100 will heat up faster using 20V, but it will not work if the supply does not support enough current!

If you still aren't sure, please reach out to me on [my discord](http://blough.ie/discord)

#### More Details Around The Switch:

The switch is not a guarantee that you will get the voltage it is set to. The IP2721 (the IC used on the Flex-C-Friend for PD negotiating) will try to request the selected voltage from the PSU, but it will accept the highest voltage under that. 

For Example, if you have the switch at "20V" and you plug it into a PSU that the highest voltage it supports is 15V, it will negotiate 15V.

## What Power Supply To Use

The Flex-C-Friend is designed to work with most USB-C PD supplies, it can be broken down as follows:

| Performance  | PSU Capability |
| ------------- | ------------- |
| Best | <ul><li>Supports 20V with at least 2.4A (48W+)</li></ul> |
| Good  | <ul><li>Supports 15V with at least 1.8A (27W+)</li></ul>  |
| Poor (will work, but not designed for this)   | <ul><li>Supports 12V with at least 1.5A</li><li>Does NOT support 20V or 15V</li></ul>  |

### Specific examples of Power Supplies to use

#### RavPower 60W PD Portable Battery Bank

I have this exact supply and it works great.

**Update:** *Some of the newer versions of this supply have an audible whine when being used with the decoy modules (including the Flex-C-Friend)*

- [Amazon.co.uk*](https://amzn.to/2XsIUzt)
- [Amazon.com*](https://amzn.to/31m7jb7)

#### Anker 60W PD Wall Charger

I do not own this supply, but have been happy with their products In the past.

- [Amazon.co.uk*](https://amzn.to/2DIDNnu)
- [Amazon.com*](https://amzn.to/2XylwAs)


\* = Affiliate

### Other Supplies

[Here is a list of chargers tested with the Flex-C-Friend](https://github.com/witnessmenow/ts100-flex-c-friend/blob/master/supplies.md), and feel free to add your own!

## More info/details

- [Hacakaday.io Flex-C-Friend Project page](https://hackaday.io/project/172187-ts100-flex-c-friend)
- [Frequently Asked Questions](FAQ.md) - Feel free to raise an issue if something isn't covered.


## Documentation License

Documentation licensed under the Creative Commons Attribution Share Alike 4.0 International License
