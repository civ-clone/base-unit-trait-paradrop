# base-unit-trait-paradrop

The `Paradrop` unit trait: a unit type with it can be paradropped.

A unit type with this trait can be dropped onto a tile within range of a city or airbase it starts its turn in. The range is the game's rule.

For example: Civ2: flag 8 (Paratroopers).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(Paradrop)`:

```ts
import Paradrop from '@civ-clone/base-unit-trait-paradrop/Paradrop';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, Paradrop));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
