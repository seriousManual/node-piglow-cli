# node-piglow-cli

[![Build Status](https://travis-ci.org/zaphod1984/node-piglow-cli.png)](https://travis-ci.org/zaphod1984/node-piglow-cli)

[![NPM](https://nodei.co/npm/piglow-cli.png)](https://nodei.co/npm/piglow-cli/)

[![NPM](https://nodei.co/npm-dl/piglow-cli.png?months=3)](https://nodei.co/npm/piglow-cli/)

## Installation

````bash
npm install -g node-piglow-cli 
````

For more details see [node-piglow](https://github.com/zaphod1984/node-piglow).

## Invocation

````bash
$ piglow --leg_0 100 //lights up the 8 LEDs of the first piglow leg
````

Each parameter can be specified individually as a command line parameter. See the section [Adressing](https://github.com/zaphod1984/node-piglow#adressing) for a detailed overview.

When the parameter `mocked` is assigned, the parameters will not be passed to the piglow board but to a mocking backend. This is useful in a testing environment. (See the [Mocking](#mocking) section)

````bash
$ piglow --leg_1 100 --mocked

piglowConfiguration:
leg0    leg1    leg2
ring0  0       100     0
ring1  0       100     0
ring2  0       100     0
ring3  0       100     0
ring4  0       100     0
ring5  0       100     0
````

Example
````bash
piglow --mocked --ring_0 100 --leg_1 --l_2_5 10

piglowConfiguration:
leg0    leg1    leg2
ring0  100     255     100
ring1  0       255     0
ring2  0       255     0
ring3  0       255     0
ring4  0       255     0
ring5  0       255     10
````


The shorthand version can be used on the command line as well:

````bash
$ piglow --all --mocked

piglowConfiguration:
leg0    leg1    leg2
ring0  255     255     255
ring1  255     255     255
ring2  255     255     255
ring3  255     255     255
ring4  255     255     255
ring5  255     255     255
````
