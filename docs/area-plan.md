# Area Plan

## Final area model

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

## Key design decisions

- kitchen exists as its own Home Assistant area even without smart devices today
- winter garden is its own area and climate zone
- boiler room is a separate small second-floor nook for equipment
- entrance hall and toilet room lights should be grouped in Home Assistant because they are always intended to act together

## Grouping rule

When a room has multiple lights that should always act together:

1. expose individual bulbs to Home Assistant if possible
2. create a Home Assistant group or helper entity for room-level control
3. use the room-level group in dashboards, automations, and Alexa exposure

This gives the cleanest long-term setup.
