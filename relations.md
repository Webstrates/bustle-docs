# Relations

The relationships between entities are first-class entities themselves in BUSTLE.

All relationships are one-way. From an *origin* node to a *destination* node.

## Continues

*Continues* relates two activities in the sense the the origin is a continuation of the destination.

This relation can be used to orient an activity within a series and to provide a chronological view of past, current and future activities grounded in the given activity.

## Shares Themes With

The *sharesthemeswith* relation relates two activities in a weaker sense than *continues*. It should be used to indicate that there is a thematic overlap between two activites.

## Participates

The *participates* relation indicates that an individual is a participant in an activity. The individual is the origin node and the activity is the destination.

## Includes

*Includes* defines a relation between a resource and an activity. The origin is the activity and the destination is the resource.

## HasTag

The *hastag* releation is a catch-all relation between a random non-Tag node and a Tag-node. It should be used sparingly and replaced with a stronger typed variant if possible.


