EEE Enemy/Projectile/Materials list

One of the main motivations of making this mod was making Down Record count player kills on renamed enemies :engilaugh:
MEV/DEA assets/rebuilds used with the permissions of the authors
Some MEV materials are added with different names so that they can be used in CD2 Material control (you can ask me if you want any specific mev enemy material to be introduced)
Some enemies were duplicated with new name so that "Down recorder" mod can correctly count kills done by enemy, because otherwise the counter breaks

Anything with (Nightmares) after descriptor has nightmares mode added to it. Which for anyone can be tested if you change difficulty such that it has "Nightmares" in the difficulty name.
    >>In "Nightmares" mode<< it will change some parts of the enemy (which may override some/all changes done to them by CD2), that i want for my difficulty but don't feel like a big enough change to introduce it into a mod as a separate enemy.
    The only exclusion to this rule are barrages. Since we don't have season 5 modkit and barrage dummies, i can only do so much about them. So most of their changes are behind "Nightmares" mode, because they are basically a "Hardcoded CD2 enemy"
    This was my original idea to do before CD2 b14 which improved networking and replication limit for CD2 significantly, in order to decrease file size, as of now its mostly not needed, but i still want to do and leave it that way.
    If you are intersted in exact changes done to enemy/projectile @me

Descriptors:
    ED_Empty - Empty descriptor
    Dwarves:
        Note: they dont do anything at all. they just stand in place, are immortal and pull agro.
        ED_DwarfDriller
        ED_DwarfEngi
        ED_DwarfGunner
        ED_DwarfScout

    Wardens:
        ED_Warden_Basic
            Spawns 6 - 8 Enemies, SpawnCount scales with difficulty
                60% chance for ED_Spider_Grunt,
                20% for ED_Spider_Grunt_Attacker, 
                20% for ED_Spider_Grunt_Guard

    Leeches:
        ED_CaveLeech_Camo: Normal leech who has materials changing based on biome it is in.

    Mactera & Menace Enemies:
        ED_Mactera_CircleJaw: Trijaw which shoots 72 projectiles in a circle.
        ED_Spider_RapidShooter_Rocket: Rocket menace.
        ED_Spider_RapidShooter_TCF: Menace that shoots PRJ_Spider_RapidShooter_TCF (modified EPC TCF PP) shots. Uses Donnie's fanatic/shotgunmenace AI.
        ED_TurboNuke: You won’t believe...
        ED_Spider_RapidShooter_Unstable: Teleporter menace. on hit applies "Dimensional Instability" which will teleport hit target randomly every 5 seconds

    Exploders & Bulk Variants:
        ED_Spider_Exploder_Radioactive: REZ exploder (because vanilla doesn't have ED).
        ED_Spider_Exploder_Camo(Nightmares) and ED_Spider_Exploder_Radioactive_Camo(Nightmares): Normal and radioactive camouflage variants of exploders
        ED_Spider_Exploder_Immortal: Immortal exploder with a 10m explosion radius.
        ED_Spider_ExploderTank_Multiplier (Nightmares): Exploder which spawns a copy of enem(y/ies) it hit
        ED_Spider_ExploderTank_Electrical (Nightmares): Electrical bulk, leaves an electrical field on death which slows players by 50% and disables shields.
        ED_Spider_ExploderTank_Fire (Nightmares): Fire bulk, 20m radius heat explosion, leaves magma floor and burning ground after death. On hit, spawns burning ground; projectiles spawn burning ground.
        ED_Spider_ExploderTank_Ice (Nightmares): Ice bulk, 20m radius cold explosion, leaves ice floor, and chilling zone on death and on projectile impact.
        ED_Spider_ExploderTank_Leadburster (Nightmares): Leadburster bulk, on death spreads PRJ_ExploderTankClusterBomb_leadburster, spawning leadbursters. Note: All kills and damage count as friendly fire.
        ED_Spider_ExploderTank_Elemental (Nightmares): Elemental bulk, spawns a random elemental field on death and from PRJ_ExploderTankClusterBomb_Elemental projectiles.
        ED_Spider_ExploderTank_Explosive (Nightmares): Explosive bulk, after getting hit, spawns a cluster of 20 bomblets (PRJ_ExploderTankExplosive) every 6 seconds.
        ED_Spider_ExploderTank_Goo (Nightmares): Goo bulk, on death explodes terrain into fungus goo.
        ED_Spider_Exploder_Multiplier (Nightmares): Same as above, but its an exploder
        ED_Spider_ExploderTank_Dystrum (Nightmares): Dystrum minibulk, 4 cluster bombs on death, 4m explosion radius, replaces terrain with Dystrum.
        ED_Spider_ExploderTank_Invis (Nightmares): Dystrum minibulk but invisible and without carve
        ED_Spider_Bulkonator (Nightmares): Very low HP Detonator that spawns 12-23 dystrum bulks after death.
        ED_Spider_ExploderTank_Kinetic (Nightmares): Normal bulk with no meatballs on death, 20m carve, immunity to elemental damage types and big weakness to non elemental damage types
        ED_Spider_ExploderTank_Repellant (Nightmares): On explosion replaces terrain with repellant platform variant in the carve radius, instead of destroying terrain
        ED_Spider_ExploderTank_Bedrock (Nightmares): Like above but bedrock.
        ED_Spider_ExploderTank_RandomReplace (Nightmares): Like above but random material.
        ED_Spider_ExploderTank_RandomCarve (Nightmares): Random, but carves like normal bulk
        ED_Spider_Exploder_Electrical (Nightmares): After death leaves electrical field
        ED_Spider_Exploder_Fire (Nightmares): same as above but burning ground
        ED_Spider_Exploder_Ice (Nightmares): same as above but chilling zone

    Oppressor/Praetorian Variants:
        ED_Spider_ShieldTank_Fire (Nightmares): Fire oppressor, spawns flames when hit and on death (Uses Mev materials).
        ED_Spider_ShieldTank_Ice (Nightmares): Ice oppressor, spawns frost flames when hit and an ice field on death (Uses Mev materials).
        ED_Spider_ShieldTank_Electric (Nightmares): Electrical oppressor, spawns an electric/stalker circle on death (Uses Mev materials).
        ED_Spider_ShieldTank_Bouncer (Nightmares): Normal oppressor with increased knockback on all of its attacks (Uses Mev materials).
        ED_Spider_Tank_Teleporter (Nightmares): Telepoter praetorian, who teleports and rotates hit target in 5m range. on death leaves field which applies STE_DimensionalInstability and will cause player to teleport randomly every 5 seconds (Ste has 15 seconds duration)

    Grabber Variants:
        ED_Grabber_Slow: Slow grabber, doesn't stop attacking/holding you when attacked, 25% less HP, 30% less speed.
        ED_Grabber_Invis: Invisible grabber. Half the speed, transparent material, hidden HP bar.
        ED_Dropper: Grabber with 0.5 grab time. 80% HP, slow start, very fast acceleration. Grabs player and instantly drops.
        ED_Telegrabber: Very fast grabber with a low grab time, effectively teleporting players after grabbing.

    Spitball Variants:
        ED_ShootingPlant_Wall: Spitwaller. Shoots PRJ_ShootingPlant_Wall (edited Lacerator stomp), which has 8 base kinetic damage and applies explosive and fire DoT (2s, 4 base damage).
        ED_ShootingPlant_Screen: Screenballer. Shoots PRJ_ShootingPlant_Screen (edited Nemesis shield attack), dealing 20 fire damage.
        ED_ShootingPlant_Inferno: Inferno. Shoots scorching tide attacks first in a 90-degree angle very fast, then in a full circle slowly.
        ED_ShootingPlant_Fireball: Spitball variant that shoots PRJ_Spider_Tank_Boss_C, recolored and renamed for Down Recorder mod.
        ED_ShootingPlant_NukeBurst: Copy of Mev's triple-shot nukeballer. Shoots PRJ_NukeBurstShot with an 8m radiation field, has better glowing weak points, and is renamed for Down Recorder mod (this was the only reason i did that tbh lol).
        ED_ShootingPlant_NukeSpread: Nukeballer variant that shoots 5 to 11 PRJ_NukeBurstShot in a 30-degree circle.
        ED_ShootingPlant_NukeBarrage: NukeBurst variant, which after each attack, increases projectile count by 1-5.
        ED_ShootingPlant_SmolSpawner: Spitball variant that spawns smollers.
        ED_ShootingPlant_Smoller: Smoller. has 1/4 hp of normal baller
        ED_ShootingPlant_Teleport: 
            1. On hit swaps hit target with anyone who it previously hit or self
            2. On miss teleports itself to a random ground location around projectile collision (in 2m radius), randomly scales itself (0.2x 2x; bounds: 0.1x; 5x) and rotates itself

    Lobber Variants:
        ED_Spider_Lobber_Fire: Fireball septic with modified og dread fireball (doesn't carve)
        ED_Spider_Lobber_Snow: Snowball septic with modified snowball projectile (doesn't isntafreeze players)
        ED_Spider_Lobber_Smoke: Gas septic, has different projectile variants that spawn different variation of praetorian gas. Default: PRJ_Lobber_SmokeDamage

    Miscellaneous Special Enemies:
        ED_BigShredder: Big shredder with 5x health and -176 freezing temperature. Note: "DieIfFrozen: false" doesn't work on shredders; set their freezing temperature to -99999 to make them unfreezable.
        ED_IceSprout: Ceiling sprout that shoots 3x PRJ_IceSprout (edited Bosco ice rockets). Does 0 damage but freezes players.
        ED_Bomber_Exploder_E: Exploder-spawning Foober (like DEA), with different materials, name, and changed dash attack to also spawn exploders compared to DEA’s.
        ED_GoldenLootbulk: Golden lootbug here, we’re rich.
        ED_Spider_Slasher_Dasher: Applies x11 speed for 0.75 seconds after hit
        ED_Bees: Bees

    Greg Variants & Unique Nightmares:
        ED_Greg: Giant high HP/damage/resistance Swarmer.
        ED_GregJunior: Greg, but junior.
        ED_Gabriel: Low, wide, high-speed, high-HP oppressor.
        ED_Gregomber: Spawner goober which spawns Greg.Jr
        ED_George: Very high HP, high delay between shots, Circlejaw.
        ED_Roadblock: Giant, transparent, immortal, stationary, pettable lootbug.
        ED_Speedbump: Small, transparent, immortal, fast, pettable lootbug.
        ED_Bomber_Exploder_Meme: No memes.

    Breeders & Spawners:
        ED_Sharknado: Shark breeder.
        ED_Shark_nado: Shark spawned by ED_Sharknado.
        ED_SentinelBreeder: Sentinel breeder.
        ED_Sentinel: Sentinel descriptor, spawned by Sentinel Breeder with a 1m spawn spread and max spawn count of 1.
        ED_GrabberBreeder: Grabber breeder, spawns slow grabbers.
        ED_StabberBreeder: Stabbervine breeder, spawns ED_Stabber.
        ED_ExploderBreeder: Exploder breeder, spawns ED_Exploder_Camo_spawn.
        ED_SpitterBreeder: Spitter breeder, spawns normal spitters.
        ED_ShredderBreeder: Shredder breeder, spawns ED_BigShredder
        ED_JellyNuker: boom
        ED_BattleBlimp (Nightmares): Breeder that shoots PRJ_Battleblimp (modified bot rockets).

    Barrages:
    Note: by default they are only renames
        ED_BarrageInfector_Exploder (Nightmares) : Normal renamed barrage at base. In nightmares mode has edited material and shoots with PRJ_Bomber_Exploder_Spawner 
        ED_BarrageInfector_Fire (Nightmares) : Normal renamed barrage at base. In nightmares mode has edited materials and shoots with PRJ_Spider_Boss_Twin_Mine
        ED_BarrageInfector_Nuke (Nightmares) : Normal renamed barrage at base. In nightmares mode has edited materials, shoots with PRJ_JellyNuke and has 0.5 time dilation
        ED_BeerrageInfector (Nightmares): Renamed barrage infector. normal barrage at base, with different descriptor values from vanilla and renamed for down recorder mod


    Nexus Variants:
    Note: For exact nexus configuration please ask me, its too long to explain here
        ED_Nexus_Bulk: Nexus variant that spawns dystrm bulks.
        ED_Nexus_Telegrabber: Nexus variant that spawns Telegrabbers.
        ED_Nexus_FireIce: Nexus variant that spawns Fire/Ice Septics.
        ED_Nexus_Invis: Nexus variant that spawns invisible bulks.
        ED_Nexus_Exploder: Nexus variant that spawns camouflaged normal and radioactive exploders

    Warden Variants:
        ED_Warden_Stalker: Warden variant that spawns stalkers and makes every buffed enemy have stalker material.        

    
Currently Not Configurable in CD2 (Expected Soon)

    ED_Nexus_Custom: Customizable Nexus, base descriptor for making custom Nexi.
    ED_Spider_Teleporter: Customizable Slasher Teleporter. Default: Teleports hit players randomly within a 50m radius
    ED_Spider_Swapper: Customizable Slasher Swapper. Default: Swaps hit players with another random player, exchanging position, scale, and rotation.
    ED_Spider_Puller: Customizable Slasher Puller. Default: Teleports every player to a random spot, on ground, within 10m radius of a hit player.
    ED_Spider_Morpher: Customizable Slasher Morpher. Default: Teleports hit player within 50m range, applies random scale between 0.5x and 2x with a cap of 0.33x and 3x.
    ED_Spider_Rotator: Customizable Slasher Rotator. Default: Randomly rotates hit player.
    ED_Spider_Scaler: Customizable Slasher Scaler. Default: Scales hit player randomly within 0.75x and 1.33x range, with a cap of 0.1x and 10x
    ED_Spider_ExploderTank_Teleport: Customizable Bulk Teleporter. On hit swaps rotation and location of everyone who it hit, with someone else who it didnt hit. If hit by death explosion, will apply dimensional instability
    ED_Spider_Slasher_DasherEX: On hit teleports hit target as much forward as it possibly can
    ED_Spider_Spitter_Dasher: Same as above but webspitter
    ED_Warden_Custom: Customizable Warden, base descriptor for custom Wardens.
    ED_Spider_Pitter: Digs a pit under hit target
    ED_CaveLeech_Friendly: Teleports single random player in 10m radius around grabbed player, every time grabbed player takes damage

Projectiles:

    PRJ_Inferno1; PRJ_Inferno2: Modified, weaker (by single hit damage) version of scorching tide projectile with extra width and damage particle count 
    PRJ_Spider_RapidShooter_Rocket: Modified rockets
    PRJ_NukeBurstShot: yet another nukeball projectile
    PRJ_ShootingPlant_Screen: Modified, 25% stronger variant of nemesis shield/screen attack, with fire/electrical damage types instead
    PRJ_ShootingPlant_Wall; PRJ_ShootingPlant_Wall_Fire: Modified variant of lacerator stomp, applies explosive/fire dot on player after hit, has 50% extra knockback but does 6 base damage instead of 20
    PRJ_Battleblimp: Modified rocket
    PRJ_(Exploder/Grabber/SentinelEgg/Sharknado/Spitter/Stabber): breeder egg variants
    PRJ_JellyNuke: :engithere:
    PRJ_BulkonatorSpawn: Projectile that bulkonator shoots after death
    PRJ_ExploderTankClusterBomb_(Elemental/Electric/Fire/Ice/leadburster): Projectile that elemental and leadburster bulks spawn after death
    PRJ_ExploderTankExplosive: Projectile that explosive bulk spawns after getting hit and on death
    PRJ_Bomber_(Exploder_DropSpawner/Exploder_Spawner/Gregomber_Spawner/Gregomber_DropSpawner): Projectiles that EEE exploder/greg spawning goobers use
    PRJ_Lobber_(Fire/Snow): Projectiles for fire and snow septics (modified fireballs and snowballs)
    PRJ_Spider_Shooter_Ice: Acid spitter projectile variant with ice damage type
    PRJ_IceSprout: Modified, weaker, bosco ice rocket
    PRJ_PlatformMaker_Fall;PRJ_PlatformMaker_Rep;PRJ_PlatformMaker_RepFall: platform projectiles with fall damage/repellant/both upgrades (untested)
    PRJ_PlatformMaker_Goo: platform projectile that spawns fungus goo
    PRJ_PlatformMaker_HotRock: platform projectile that spawns hot rock
    PRJ_Lobber_Smoke: Spitball projectile that spawns non damaging, non combustive gas cloud on impact
    PRJ_Lobber_SmokeCombustion: Spitball projectile that spawns non damaging, combustive gas cloud on impact
    PRJ_Lobber_SmokeDamage: Spitball projectile that spawns damaging, non combustive gas cloud on impact
    PRJ_Lobber_SmokeAll: Spitball projectile that spawns damaging, combustive gas cloud on impact
    PRJ_Lobber_SmokeAllRandom: Spitball projectile that spawns one of the above gas clouds, randomly chosen
    PRJ_ShootingPlant_MiniSpawn: Spitball projectile that spawns smoller on collision location
    PRJ_Spider_RapidShooter_Unstable: Menace projectile that on hit applies Dimensional Instability.
    PRJ_Bomber_Gregomber_DropSpawner: Gregomber projectile, spawns 1x ED_GregJunior
    PRJ_Bomber_Gregomber_Spawner: Same as above, but with different projectile speed 
    PRJ_Bomber_Exploder_DropSpawner: Spawns 2x (no more, no less, doesnt scale with difficulty) ED_Spider_Exploder_Camo_spawn
    PRJ_Bomber_Exploder_Spawner: Same as above but 6x
    PRJ_NukeShot: Projectile used by ED_TurboNuke
    PRJ_Spider_RapidShooter_TCF: Modified charged epc projectile, that can be popped like tcf, and does less damage
    PRJ_SpawnerRandom: spawns one random enemy
    PRJ_RandonatorSpawn: Same as above, but bulk meatball, with damage.

STEs:

    Dimensional instability is just a basic ste that has damage rate of once every 5 seconds. its basically same STE as any other damaging ste, it has nothing special to it except longer wait between damage to balance out teleporters

Materials:

M_BedrockArmor
M_BedrockWP
M_Brundlemat
M_BulkElemental
M_BulkElemental_electric
M_BulkElemental_fire
M_BulkElemental_Ice
M_Bulkonator_Body
M_DisconatorArmor
M_DisconatorBody
M_DystrumBulk
M_ElecBulkArmor
M_ElecBulk_body
M_ElectricField
M_ElemBulkBody
M_FireBulkArmor
M_FireBulk_body
M_Flier_HeavyVeteran01_CST
M_GooArmor
M_GooBulkBody
M_GooBulk_WP
M_GooWP
M_IceBulkArmor
M_IceBulk_body
M_IceWP
M_LeadBulker_Armor
M_Leadbulker_Body
M_NukeballBody
M_Nukeballwp25
M_Nukeballwp50
M_NukeMinigunWP
M_PitterArmor
M_PitterBody
M_Platforms_RepelNoPlat
M_RepelArmor
M_RepelWP
M_smokefire
M_SpiderShooter_Projectile_Ice1
M_Spider_Bulkonator_Weakpoint_
M_Spider_ExploderTank_Armor_Kinetic
M_Spider_ExploderTank_Body_Kinetic
M_Spider_Grunt_Armor_SlasherClaws_Dasher
M_Spider_Grunt_Armor_Slasher_Dasher
M_Spider_Grunt_Body_Dasher
M_Spider_Lobber_ArmorShell_Fire
M_Spider_Lobber_ArmorShell_Snow
M_Spider_Lobber_Body_Fire
M_Spider_Lobber_Body_Snow
M_Spider_Lobber_GlowBubbles_Fire
M_Spider_Lobber_GlowBubbles_Snow
M_Spider_Lobber_GlowButt_Fire
M_Spider_Lobber_GlowButt_Smoke
M_Spider_Lobber_GlowButt_Snow
M_Spider_Lobber_Projectile_Wobble_Fire
M_Spider_Lobber_Projectile_Wobble_Snow
M_Spider_Lobber_Teeth_Fire
M_Spider_Lobber_Teeth_Snow
M_Spider_Oppressor_Tank_Body_dummy
M_Spider_Oppressor_Tank_Body_fire
M_SpitwallerBody
M_SpitwallerWP
M_Telebulkarmor
M_Telebulkbody
M_TeleporterA
M_TeleporterA2
M_TeleporterA3
M_TeleporterA4
M_TeleporterBase
M_TeleporterBase2
M_TeleporterBase3
M_TeleporterBase4
M_TeleporterL
M_TeleporterL2
M_TeleporterL3
M_TeleporterL4
M_TeleporterLR
M_TeleporterLR2
M_TeleporterLR3
M_TeleporterLR4
M_TeleporterLS
M_TeleporterLS2
M_TeleporterLS3
M_TeleporterLS4
M_TeleporterR
M_TeleporterR2
M_TeleporterR3
M_TeleporterR4
M_TeleporterRS
M_TeleporterRS2
M_TeleporterRS3
M_TeleporterRS4
M_TeleporterS
M_TeleporterS2
M_TeleporterS3
M_TeleporterS4
M_TurboNukeArmor
M_TurboNukeBody
M_TurboNukeWP
M_VolatileArmor
M_VolatileWP


Special thanks to:
Modded community for: community modkit
PDRG for: existing
The Brain for: CD2, encouraging me to start modding, insane amount of help and stopping me from accidentally breaking game 
29 Phantom for: playing Nightmares long enough that there was a need to make a mod, testing, and materials
Yinny and Donnie for: MEV/DEA, allowing to use MEV/DEA assets and (yinny) being a reason customizable nexus became a thing
cookie, mercy, darth, nad, fresca, haust and possibly some other people who i forgot to mention, but everyone who i played modded with long enough to get here