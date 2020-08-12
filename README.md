# MawsonLakes.Org SkyWater Shuttle

This repository contains the files and documentation for production of as ASIC
via the Google and Skywater shuttle program.

# Tools / Installation

These files were created using software installed on Ubuntu (most recent -
20.04.1).

For more information, see: https://opencircuitdesign.com

## Open PDKS

The Open-PDKs project aims to collect the technology data for open and freely
available Process Development Kits for ASIC development.

It contains the technology and configuration files required to design an ASICS
for a particular fabrication process.

Download with:

    git clone git://opencircuitdesign.com/open_pdks

Hosted by 'efabless'.

## Magic VLSI

Magic allows VLSI designs to be drawn by hand and exported to GDS format. It
does a lot more though, and can be used to check designs created by other means
against design rule constraints (DRC)

Install with the following (version 8.2.157)

    sudo apt install magic

## Electric

Electric is similar to Magic. Originally written in 'C' it has been ported to
Java and is available on other operating systems.

It also provides a 3D visualization option.

To install

    sudo apt install electric

## klayout

VLSI Layout software written in KDE

To install

    sudo apt install klayout

# Examples

## Editing gds with Magic

    magic -T ../open_pdks/sky130/magic/sky130gds.tech gds/mawson-lakes-org.gds

or, to load the sky130 technology file separately, at the prompt in the magic
console, use:

    tech load ../open_pdks/sky130/magic/sky130gds.tech
