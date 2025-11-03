# RetroDIMM

This is documentation for the RetroDIMM specification. For boards, see [Boards and Designs](#boards-and-designs).

## Table of Contents

1. [Pinout](#pinout)
1. [Signal Descriptions](#signal-descriptions)
1. [Detailed Signal Descriptions](#detailed-signal-descriptions)
1. [Boards and Designs](#boards-and-designs)

## Pinout

| Pin | Description | \| | Pin | Description | \| | Pin | Description | \| | Pin | Description |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | GND |

## Signal Descriptions

| Signal | Description | Source | Unused - Module | Unused - Controller |
| --- | ----------- | ---- | ------------- | ----------------- |
| CLOCK | Clock for RAM, typically the main system clock. The controller should always provide some sort of clock if possible for maximum compatibility. | Controller | Leave floating | Pull up or down |
| DIR | Direction control for bus transceivers. High = write to module. | Controller | Leave floating | Required |
| SLEEP | Puts module components into a low power state. High = sleep mode. | Controller | Leave floating | Pull down |
| <span style="text-decoration:overline">DOEH</span> & <span style="text-decoration:overline">DOEL</span> | Output enables for bus transceivers. | Controller | Leave floating | Required |
| <span style="text-decoration:overline">DTACK</span> | Active low signal to complete a bus transaction. | Controller/Module | Leave floating | Pull up |
| <span style="text-decoration:overline">EXT_DTACK</span> | | Module | Leave floating | Leave floating |
| <span style="text-decoration:overline">LW</span> & <span style="text-decoration:overline">UW</span> | | Controller |
| <span style="text-decoration:overline">RAM_SENSE</span> | Identifies the module as RAM | Module |
| <span style="text-decoration:overline">ROM_SENSE</span> | Identifies the module as ROM | Module |
| SLEEP | Puts module components into a low power state | Controller | Leave floating | Pull down |
| <span style="text-decoration:overline">RAM_SIZE[N]</span> | | Module | Leave floating | Leave floating |
| <span style="text-decoration:overline">RAM_[2/4]CHIP</span> | | Module | Leave floating | Leave floating |
| <span style="text-decoration:overline">RAM_[1/2]WS</span> | Number of wait states when accessing RAM | Module | Leave floating/Pull down | Leave floating |
| <span style="text-decoration:overline">RAM_CS[1/2/3/4]</span> | Chip select for up to four chips. | Controller | | Required/Pull up |
| VCC | Supply voltage, typically +5V | Controller | Required | Required |
| VPP | Future use for programming | Controller | Leave floating | Pull up |
| NC | Not connected |

## Detailed Signal Descriptions

## Boards and Designs
