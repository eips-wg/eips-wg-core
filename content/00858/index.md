---
eip: 858
title: Reduce block reward and delay difficulty bomb
author: Carl Larson <cslarson@gmail.com>
type: Standards Track
category: Core
status: Stagnant
created: 2018-01-29
---

## Simple Summary
Reduce the block reward to 1 ETH and delay the difficulty bomb.

## Abstract
The current public Ethereum network has a hashrate that corresponds to a tremendous level of energy consumption. As this energy consumption has a correlated environmental cost the network participants have an ethical obligation to ensure this cost is not higher than necessary. At this time, the most direct way to reduce this cost is to lower the block reward in order to limit the appeal of ETH mining. Unchecked growth in hashrate is also counterproductive from a security standpoint.
Recent research developments also now time the switch to POS as sometime in 2019 and as a result there is need to further delay the difficulty bomb so the network doesn't grind to a halt.


## Motivation
The current public Ethereum network has a hashrate of 296 TH/s. This hashrate corresponds to a power usage of roughly [1 TW](./assets/calculations.md) and yearly energy consumption of 8.8 TWh (roughly 0.04% of [total](https://en.wikipedia.org/wiki/List_of_countries_by_electricity_consumption) global electricity consumption). A future switch to full Proof of Stake will solve this issue entirely. Yet that switch remains enough in the future that action should be taken in the interim to limit excess harmful side affects of the present network.

## Specification

Delay difficulty bomb by 2,000,000 blocks
Adjust block, uncle, and nephew rewards to reflect a new block reward of 1 ETH.

## Rationale
This will delay the difficulty bomb by roughly a year. The difficulty bomb remains a community supported mechanism to aid a future transition to POS.

The network hashrate provides security by reducing the likelihood that an adversary could mount a 51% attack. A static block reward means that factors (price) may be such that participation in mining grows unchecked. This growth may be counterproductive and work to also grow and potential pool of adversaries. The means we have to arrest this growth is to reduce the appeal of mining and the most direct way to do that is to reduce the block reward.

## Backwards Compatibility
This EIP is consensus incompatible with the current public Ethereum chain and would cause a hard fork when enacted. The resulting fork would allow users to chose between two chains: a chain with a block reward of 1 ETH/block and another with a block reward of 3 ETH/block. This is a good choice to allow users to make. In addition, the difficulty bomb would be delayed - ensuring the network would not grind to a halt.

## Test Cases
Tests have, as yet, not been completed.

## Implementation
No implementation including both block reward and difficulty adjustment is currently available.

## Copyright
Copyright and related rights waived via [CC0](/LICENSE.md).
