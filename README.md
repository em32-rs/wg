# Rust support for EM32 microprocessors

This document describes the EM32 Rust group's purpose, scope and workings.

## Purpose

The group exists to pool efforts to facilitate developing Rust applications on the chips in scope
by maintaining Peripheral Access Crates (PACs) and suitable Hardware Abstraction Layer (HAL) implementations for the chips,
as well as board support crates for selected devices built from those.

## Scope

Chips in scope are the Silicon Labs EFM32 family and related or newer families,
as long as they share architectural components to the extent of warranting shared HAL components.

This encompasses the original EFM32 generations
(EFM32 Gecko, EFM32 Tiny Gecko, EFM32 Giant Gecko, EFM32 Happy Gecko)
as well as newer generations with and without on-board radio
(EZR32 Wonder, Leopard and Happy Gecko; EFR32 Blue, Flex and Mighty Gecko).

Note that some names resurface in newer series
(e.g. there are now EFM32GG12 family that bears little resemblance with the original EFM32GG series);
check the individual PACs for details on which ordering codes they relate to.
Features of the HAL that are limited to a particular series will often refer to the PACs they require.

## Workings

follow embedded-wg best practice

## Crates

This group will, eventually, try to maintain:

* PACs:
  * [EFM32GG](https://github.com/maximeborges/svd2rust_efm32gg990)
  * [EFR32xG1](https://github.com/em32-rs/efr32xg1-pac)
  * [EFM32HG](https://github.com/em32-rs/efm32hg-pac)
  * EFM32G, EFM32TG (at least there's hardware around to test it)
  * all the others (as soon as someone gets the hardware to test them)

* A single HAL crate: em32-hal (to be merged from [efm32gg-hal](https://github.com/chrysn/efm32gg-hal) and [imtomu-rs](https://github.com/fudanchii/imtomu-rs))

* yet indeterminate selected Board Support Crates

## Related projects

* [Silicon Labs software](http://devtools.silabs.com/dl/documentation/doxygen/5.7/index.html<Paste>):
  Various C libraries maintained by the chips' manufacturer, including emlib (their hardware abstraction) and board support packages
* [RustyGecko](https://github.com/RustyGecko): Wrapping emlib via the FFI to Rust. Last updated 2015.
