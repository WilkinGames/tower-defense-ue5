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

## User Interface

#### `HUD_Widget`

Displays game/player stats, such as the current wave, enemies, lives, and money.

#### `HUD_Message`

UI element which is very modular and can be used for any game event (eg `Wave 1 Complete!`). Automatically fades in and out.

#### `InteractTooltip`

UI element which displays when the player touches something that can be interected with (eg `Press E to interact`). Used when a player touches a tower base that can be built.

#### `HealthBar_Widget`

Enemy health bars which actually exist in the world but rotate to face the player camera for a stylistic feel (as opposed to using a stricly UI element).

#### `ObjectIndicator`

UI element that can be applied to any actor and display a label (eg `Enemy Spawn`) and display the current distance in meters to the player.

#### Minimap

Simple minimap using an Orthographic camera above the map. A material is generated from this camera and is rendered as a texture.

#### Menus

Game menus which pause the game and blur the background. Used for the `BuyMenu` and `GameOverMenu`.
