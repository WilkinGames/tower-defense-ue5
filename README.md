# Tower Defense

Developed with Unreal Engine 5 (v5.5.1).

All custom Blueprints are located in the `TowerDefense` folder.

## Mechanics

- The player controls a 3rd person character with 2 default abilities: **Projectile** (Left Mouse) and **Stun** (Right Mouse)
- The player earns money by killing enemies and completing waves
- Defense tower bases are set in fixed points and be upgraded by pressing **E** near them (opens the `BuyMenu`)
- The player can select different tower types in the `BuyMenu`
- When an enemy reaches the player base, a life is lost
- Unlimited waves (endless survival) with 5 second intermission time between waves

Game properties (like intermission time) can easily be modified in the `TD_GameMode` class.

## Enemies

The total number of enemies and enemy health increases as the waves progress.

### Enemy Types

#### EnemySlow

A large, slow-moving enemy with increased health

#### EnemyFast

A small, fast-moving enemy

## Abilities

Abilities are handled using Unreal Engine's **Gameplay Ability System** (GAS). 

They are granted to the player by default and towers when they are purchased.

### Projectile

Fully automatic weapon that fires a projectile to deal damage

### Stun

Temporarily slows down any nearby enemies within the radius
