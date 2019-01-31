# Rust support for EM32 microprocessors

This document describes the EM32 Rust group's purpose, scope and workings.

## Purpose

The group exists to pool efforts to facilitate developing Rust applications on the chips in scope
by maintaining device crates and suitable hardware abstraction for the chips,
as well as board support crates for selected devices built from those.

## Scope

Chips in scope are the Silicon Labs EFM32 family and related or newer families,
as long as they share architectural components to the extent of warranting shared Hardware Abstraction Layer (HAL) components.

This encompasses the original EFM32 generations
(EFM32 Gecko, EFM32 Tiny Gecko, EFM32 Giant Gecko, EFM32 Happy Gecko)
as well as newer generations with and without on-board radio
(EZR32 Wonder, Leopard and Happy Gecko; EFR32 Blue, Flex and Mighty Gecko).

Note that some names resurface in newer series
(e.g. there are now EFM32GG12 family that bears little resemblance with the original EFM32GG series);
check the individual device support crates for details on which ordering codes they relate to.
Features of the HAL that are limited to a particular series will often refer to the device support crates they require.

## Workings

follow embedded-wg best practice

## Crates

This group will, eventually, try to maintain:

* Device support crates:
  * EFM32GG (working; named efm32gg990)
  * EFR32xG1 (working)
  * EFM32HG (working; named efm32hg309f64-pac)
  * EFM32G, EFM32TG (at least there's hardware around to test it)
  * all the others (as soon as someone gets the hardware to test them)

* A single HAL crate: em32-hal (to be merged from efm32gg-hal and imtomu-rs)

* yet indeterminate Board Support Crates
