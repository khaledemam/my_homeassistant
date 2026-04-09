# House Layout

This is a Home Assistant-oriented view of the house, based on the floor plans and room mapping we agreed on.

## Mermaid Layout

```mermaid
flowchart TB
  subgraph GF["Ground Floor"]
    EH["Entrance Hall"]
    WC["Toilet Room"]
    LR["Living Room"]
    K["Kitchen"]
    WG["Winter Garden"]
  end

  subgraph FF["First Floor"]
    O["Office Room"]
    B["Bedroom"]
    LB["Leila's Bedroom"]
    BA["Bathroom"]
  end

  subgraph SF["Second Floor"]
    A["Attic"]
    BR["Boiler Room"]
  end

  subgraph OUT["Outside"]
    BY["Backyard"]
    SH["Shed"]
  end

  EH --- WC
  EH --- LR
  LR --- K
  K --- WG
  WG --- BY
  BY --- SH

  EH -. "stairs" .- O
  EH -. "stairs" .- B
  EH -. "stairs" .- LB
  EH -. "stairs" .- BA
  EH -. "stairs" .- A
  A --- BR
```

## Ground Floor

```text
+-------------------------------------------+
|               Winter Garden               |
+----------------------+--------------------+
|       Kitchen        |    Living Room     |
|                      |                    |
|                      |                    |
+-----------+----------+--------------------+
| Toilet    |       Entrance Hall           |
| Room      |                               |
+-----------+-------------------------------+
```

Outside related areas:

```text
+---------------------------+
|         Backyard          |
|                           |
|   +-------------------+   |
|   |       Shed        |   |
|   +-------------------+   |
+---------------------------+
```

## First Floor

```text
+--------------------+----------------------+
|    Office Room     |       Bedroom        |
|                    |                      |
+----------+---------+----------------------+
| Bathroom |      Leila's Bedroom           |
|          |                                |
+----------+--------------------------------+
```

## Second Floor

```text
+-------------------------------------------+
|                   Attic                   |
|                                           |
|  +-------------------+                    |
|  |   Boiler Room     |                    |
|  |   small nook      |                    |
|  +-------------------+                    |
+-------------------------------------------+
```

## Final Home Assistant Areas

- entrance hall
- living room
- kitchen
- winter garden
- backyard
- shed
- toilet room
- office room
- bedroom
- Leila's bedroom
- bathroom
- attic
- boiler room

## Notes

- kitchen exists as its own area even though it has no smart devices yet
- winter garden is its own climate zone
- entrance hall and toilet room lights should be grouped in Home Assistant for room-level control
- the boiler room is a small equipment area within the second floor attic layout
- this is an automation-oriented map, not a precise architectural drawing
