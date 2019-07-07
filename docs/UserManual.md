
# User Manual
Note:
Map movement(event command "Location move") during SRPG battle is not possible.
Go to the map for battle and use the plug-in command SRPGBattle Start.
Also, use the plugin command SRPGBattle End before moving to another map.

## Plugin Command:
| Command            | Function                 |
| -- | -- |
| `SRPGBattle Start` | Starting tactical battle |
| `SRPGBattle End`   | Ending tactical battle   |

## Event Notetag:
| Note                  | Function                                                                                                |
| -- | -- |
| `<type:actor>`        | set this event to actor(use this note with `<id:X>`)                                                    |
| `<type:enemy>`        | set this event to enemy(use this note with `<id:X>`)                                                    |
| `<id:X>`	        | set this event to ID X actor / enemy                                                                    |
| `<mode:normal>`       | set this unit's acting pattern 'normal'(if you don't set mode, set 'normal' automatically)              |
| `<mode:stand>`        | set this unit's acting pattern 'stand if enemy don't nearby                                             |
| `<mode:regionUp>`     | set this unit's acting pattern 'go to bigger region ID if enemy don't nearby                            |
| `<mode:regionDown>`   | set this unit's acting pattern 'go to smaller region ID if enemy don't near by                          |
| `<mode:absRegionUp>`  | set this unit's acting pattern 'always go to bigger region ID                                           |
| `<mode:absRegionDown>`| set this unit's acting pattern 'always go to smaller region ID                                          |
| `<mode:aimingEvent>`  | set this unit's acting pattern 'aim for event with the specified ID'(use this note with `<targetId:X>`) |
| `<mode:aimingActor>`  | set this unit's acting pattern 'aim for actor with the specified ID'(use this note with `<targetId:X>`) |
| `<targetId:X>`        | ID of target event or actor                                                                             |
| `<type:unitEvent>`    | set this event to event unit (event unit start when actor action or stand on it)                        |
| `<type:playerEvent>`  | set this event to player event (player event start when player push enter key on it)                    |
| `<type:object>`       | set this event to object that pleyer and enemy can't move(except for event has no graphic)              |
| `<type:battleStart>`  | start this event when only battle start                                                                 |
| `<type:actorTurn>`    | start this event when actor turn start                                                                  |
| `<type:enemyTurn>`    | start this event when enemy turn start                                                                  |
| `<type:turnEnd>`      | start this event when turn end                                                                          |
| `<type:afterAction>`  | start this event when actor or enemy action                                                             |

## Class Notetag:
| Note                 | Function                                                                          |
| -- | -- |
| `<srpgMove:X>`       | set move range X                                                                  |
| `<srpgThroughTag:X>` | unit can go through tiles with terrain tags less than X(except for terrain tag 0) |

## Skill or Item Notetags:
| Note               | Function                                                                            |
| -- | -- |
| `<srpgRange:X>`    | set attack range X |
|                    | when set 0, this skill targets the caster himself(set range 'user')                 |
|                    |when set -1, `<weaponMinRange:X>` on weapon or enemy's note set to this attack range |
| `<srpgMinRange:X>` | set attack minimum range X                                                          |

## Weapon Notetag:
| Note                  | Function                                                                          |
| -- | -- |
| `<weaponRange:X>`     | set attack range X                                                                |
| `<weaponMinRange:X>`  | set attack minimum range X                                                        |
| `<srpgWeaponSkill:X>` | set attack skill ID X. normal attack is skill ID 1                                |
| `<srpgCounter:false>` | set this weapon can't counter attack                                              |
| `<srpgMovePlus:X>`    | change move range X. you can set minus value                                      |
| `<srpgThroughTag:X>`  | unit can go through tiles with terrain tags less than X(except for terrain tag 0) |

## Armor Notetag:
| Note                 | Function                                                                          |
| -- | -- |
| `<srpgMovePlus:X>`   | change move range X. you can set minus value                                      |
| `<srpgThroughTag:X>` | unit can go through tiles with terrain tags less than X(except for terrain tag 0) |

## Enemy Notetag:
| Note                 | Function                                                                          |
| -- | -- |
| `<characterName:X>`  | set character graphic's file name to X                                            |
| `<characterIndex:X>` | set id in character graphic to X                                                  |
|                      | Index: 0 1 2 3                                                                    |
|                      |        4 5 6 7                                                                    |
| `<faceName:X>`       | set face graphic's file name to X                                                 |
| `<faceIndex:X>`      | set id in face graphic to X                                                       |
|                      | Index: 0 1 2 3                                                                    |
|                      |        4 5 6 7                                                                    |
| `<srpgClass:X>`      | set class name in SRPG status window. this name is dummy                          |
| `<srpgLevel:X>`      | set level in SRPG status window. this level is dummy                              |
| `<srpgMove:X>`       | set this enemy's move range                                                       |
| `<weaponRange:X>`    | set this enemy's attack range(when you don't set srpgWeapon)                      |
| `<weaponMinRange:X>` | set this enemy's attack minimum range(when you don't set srpgWeapon)              |
| `<srpgWeapon:X>`     | set this enemy's weapon. X is weapon id. this is NOT dummy                        |
| `<srpgThroughTag:X>` | unit can go through tiles with terrain tags less than X(except for terrain tag 0) |
 
## State Notetag:
| Note                 | Function                                                                          |
| -- | -- |
| `<srpgMovePlus:X>`   | change move range X.you can set minus value                                       |
| `<srpgThroughTag:X>` | unit can go through tiles with terrain tags less than X(except for terrain tag 0) |

## Script Call:
| Command                                               | Function                                                                                               |
| -- | -- |
| `this.EventDistance(VariableID, EventID, EventID);`   | Store the distance between events in a variable                                                        |
| `this.ActorDistance(VariableID, ActorID, ActorID);`   | Store the distance between actors in a variable                                                        |
| `this.playerMoveTo(X, Y);`                            | Move the cursor (player) to the coordinates (X, Y)                                                     |
| `this.addActor(EventID, ActorID);`                    | Make the event with the specified ID the actor                                                         |
| `this.addEnemy(EventID, EnemyID);`                    | Make the event with the specified ID the enemy                                                         |
| `this.setBattleMode(EventID, 'mode');`                | Change the acting pattern of the event with the specified ID                                           |
| `this.setTargetId(EventID, ID);`                      | Change the target ID of the event with the specified ID                                                |
| `this.fromActorMinimumDistance(VariableID, EventID);` | Stores the distance between the specified event and the nearest actor among all actors in the variable |
| `this.isUnitDead(SwitchID, EventID);`                 | Stores in the switch whether the event with the specified ID is dead or not                            |
| `this.isEventIdXy(VariableID, X, Y);`                 | Stores the event ID of the specified coordinates (X, Y) in the variable                                |
| `this.unitRecoverAll(EventID);`                       | Full recovery of the unit with the specified event ID (only when it is alive)                          |
| `this.unitAddState(EventId, StateId);`                | Add the state of the ID specified to the unit with the specified event ID                              |
| `this.turnEnd();`                                     | End player's turn(Same 'Turn End' in menu)                                                             |
| `this.isSubPhaseNormal(SwitchID);`                    | Whether the player selects the unit to be operated (ON is the same as when the menu can be opened)     |