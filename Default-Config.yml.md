```
version:
  # This is the current version of Towny.  Please do not edit.
  version: 0.94.0.0
  # This is for showing the changelog on updates.  Please do not edit.
  last_run_version: 0.94.0.0
# The language file you wish to use
language: english.yml
 
############################################################
# +------------------------------------------------------+ #
# |                   Permission nodes                   | #
# +------------------------------------------------------+ #
############################################################
 
#  Possible permission nodes
#
#    for a full list of permission nodes visit: 
#    http://palmergames.com/towny/towny-permission-nodes/ 
permissions: ''
 
############################################################
# +------------------------------------------------------+ #
# |                Town and Nation levels                | #
# +------------------------------------------------------+ #
############################################################
 
levels:
  # default Town levels.
  town_level:
  - numResidents: 0
    namePostfix: ' Ruins'
    mayorPrefix: 'Spirit '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 1
    upkeepModifier: 1.0
    townOutpostLimit: 0
  - numResidents: 1
    namePostfix: ' (Settlement)'
    mayorPrefix: 'Hermit '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 16
    upkeepModifier: 1.0
    townOutpostLimit: 0
  - numResidents: 2
    namePostfix: ' (Hamlet)'
    mayorPrefix: 'Chief '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 32
    upkeepModifier: 1.0
    townOutpostLimit: 1
  - numResidents: 6
    namePostfix: ' (Village)'
    mayorPrefix: 'Baron Von '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 96
    upkeepModifier: 1.0
    townOutpostLimit: 1
  - numResidents: 10
    namePostfix: ' (Town)'
    mayorPrefix: 'Viscount '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 160
    upkeepModifier: 1.0
    townOutpostLimit: 2
  - numResidents: 14
    namePostfix: ' (Large Town)'
    mayorPrefix: 'Count Von '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 224
    upkeepModifier: 1.0
    townOutpostLimit: 2
  - numResidents: 20
    namePostfix: ' (City)'
    mayorPrefix: 'Earl '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 320
    upkeepModifier: 1.0
    townOutpostLimit: 3
  - numResidents: 24
    namePostfix: ' (Large City)'
    mayorPrefix: 'Duke '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 384
    upkeepModifier: 1.0
    townOutpostLimit: 3
  - numResidents: 28
    namePostfix: ' (Metropolis)'
    mayorPrefix: 'Lord '
    namePrefix: ''
    mayorPostfix: ''
    townBlockLimit: 448
    upkeepModifier: 1.0
    townOutpostLimit: 4
  # default Nation levels.
  nation_level:
  - kingPostfix: ''
    capitalPostfix: ''
    upkeepModifier: 1.0
    kingPrefix: 'Leader '
    capitalPrefix: ''
    numResidents: 0
    nationBonusOutpostLimit: 0
    namePostfix: ' (Nation)'
    townBlockLimitBonus: 10
    namePrefix: 'Land of '
    nationZonesSize: 1
    nationTownUpkeepModifier: 1.0
  - kingPostfix: ''
    capitalPostfix: ''
    upkeepModifier: 1.0
    kingPrefix: 'Count '
    capitalPrefix: ''
    numResidents: 10
    nationBonusOutpostLimit: 1
    namePostfix: ' (Nation)'
    townBlockLimitBonus: 20
    namePrefix: 'Federation of '
    nationZonesSize: 1
    nationTownUpkeepModifier: 1.0
  - kingPostfix: ''
    capitalPostfix: ''
    upkeepModifier: 1.0
    kingPrefix: 'Duke '
    capitalPrefix: ''
    numResidents: 20
    nationBonusOutpostLimit: 2
    namePostfix: ' (Nation)'
    townBlockLimitBonus: 40
    namePrefix: 'Dominion of '
    nationZonesSize: 1
    nationTownUpkeepModifier: 1.0
  - kingPostfix: ''
    capitalPostfix: ''
    upkeepModifier: 1.0
    kingPrefix: 'King '
    capitalPrefix: ''
    numResidents: 30
    nationBonusOutpostLimit: 3
    namePostfix: ' (Nation)'
    townBlockLimitBonus: 60
    namePrefix: 'Kingdom of '
    nationZonesSize: 2
    nationTownUpkeepModifier: 1.0
  - kingPostfix: ''
    capitalPostfix: ''
    upkeepModifier: 1.0
    kingPrefix: 'Emperor '
    capitalPrefix: ''
    numResidents: 40
    nationBonusOutpostLimit: 4
    namePostfix: ' Empire'
    townBlockLimitBonus: 100
    namePrefix: 'The '
    nationZonesSize: 2
    nationTownUpkeepModifier: 1.0
  - kingPostfix: ''
    capitalPostfix: ''
    upkeepModifier: 1.0
    kingPrefix: 'God Emperor '
    capitalPrefix: ''
    numResidents: 60
    nationBonusOutpostLimit: 5
    namePostfix: ' Realm'
    townBlockLimitBonus: 140
    namePrefix: 'The '
    nationZonesSize: 3
    nationTownUpkeepModifier: 1.0
 
############################################################
# +------------------------------------------------------+ #
# |               Town Claim/new defaults                | #
# +------------------------------------------------------+ #
############################################################
 
town:
  # Default public status of the town (used for /town spawn)
  default_public: 'true'
  # Default Open status of the town (are new towns open and joinable by anyone at creation?)
  default_open: 'false'
  # Default tax settings for new towns.
  default_taxes:
    # Default amount of tax of a new town. This must be lower than the economy.daily_taxes.max_tax_percent setting.
    tax: '0.0'
    # Default amount of shop tax of a new town.
    shop_tax: '0.0'
    # Default amount of embassy tax of a new town.
    embassy_tax: '0.0'
    # Default amount for town's plottax costs.
    plot_tax: '0.0'
    # Default status of new town's taxpercentage. True means that the default_tax is treated as a percentage instead of a fixed amount.
    taxpercentage: 'false'
    # A required minimum tax amount for the default_tax, will not change any towns which already have a tax set.
    # Do not forget to set the default_tax to more than 0 or new towns will still begin with a tax of zero.
    minimumtax: '0.0'
  # Limits the maximum amount of bonus blocks a town can buy.
  max_purchased_blocks: '0'
  # maximum number of plots any single resident can own
  max_plots_per_resident: '100'
  # maximum number used in /town claim/unclaim # commands.
  # set to 0 to disable limiting of claim radius value check.
  # keep in mind that the default value of 4 is a radius, 
  # and it will allow claiming 9x9 (80 plots) at once.
  max_claim_radius_value: '4'
  # Maximum number of towns allowed on the server.
  town_limit: '3000'
 
  # Minimum number of plots any towns plot must be from the next town's own plots.
  # This will prevent town encasement to a certain degree.
  min_plot_distance_from_town_plot: '5'
 
  # Minimum number of plots any towns home plot must be from the next town.
  # This will prevent someone founding a town right on your doorstep
  min_distance_from_town_homeblock: '5'
 
  # Minimum number of plots an outpost must be from any other town's plots.
  # Useful when min_plot_distance_from_town_plot is set to near-zero to allow towns to have claims
  # near to each other, but want to keep outposts away from towns.
  min_distance_for_outpost_from_plot: '5'
 
  # Maximum distance between homeblocks.
  # This will force players to build close together.
  max_distance_between_homeblocks: '0'
 
  # The maximum townblocks available to a town is (numResidents * ratio).
  # Setting this value to 0 will instead use the level based jump values determined in the town level config.
  town_block_ratio: '8'
  # The size of the square grid cell. Changing this value is suggested only when you first install Towny.
  # Doing so after entering data will shift things unwantedly. Using smaller value will allow higher precision,
  # at the cost of more work setting up. Also, extremely small values will render the caching done useless.
  # Each cell is (town_block_size * town_block_size * 128) in size, with 128 being from bedrock to clouds.
  town_block_size: '16'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |             Default new world settings               | #
  # +------------------------------------------------------+ #
  ############################################################
 
  # These flags are only used at the initial setup of a new world.
 
  # Once Towny is running each world can be altered from within game
  # using '/townyworld toggle'
 
new_world_settings:
  # Default for new worlds to have towny enabled.
  using_towny: 'true'
 
  pvp:
    # Set if PVP is enabled in this world
    world_pvp: 'true'
    # force_pvp_on is a global flag and overrides any towns flag setting
    force_pvp_on: 'false'
 
  mobs:
    # world_monsters_on is a global flag setting per world.
    world_monsters_on: 'true'
    # force_town_monsters_on is a global flag and overrides any towns flag setting
    force_town_monsters_on: 'false'
 
  explosions:
    # Allow explosions in this world
    world_explosions_enabled: 'true'
    # force_explosions_on is a global flag and overrides any towns flag setting
    force_explosions_on: 'false'
 
  fire:
    # Allow fire to be lit and spread in this world.
    world_firespread_enabled: 'true'
    # force_fire_on is a global flag and overrides any towns flag setting
    force_fire_on: 'false'
 
  # Prevent Endermen from picking up and placing blocks.
  enderman_protect: 'true'
  # Disable players trampling crops
  disable_player_crop_trampling: 'true'
  # Disable creatures trampling crops
  disable_creature_crop_trampling: 'true'
 
  # World management settings to deal with un/claiming plots
  plot_management:
 
    block_delete:
      enabled: 'true'
      # These items will be deleted upon a plot being unclaimed
      unclaim_delete: BED_BLOCK,TORCH,REDSTONE_WIRE,SIGN_POST,WOODEN_DOOR,WALL_SIGN,STONE_PLATE,IRON_DOOR_BLOCK,WOOD_PLATE,REDSTONE_TORCH_OFF,REDSTONE_TORCH_ON,DIODE_BLOCK_OFF,DIODE_BLOCK_ON
 
    mayor_plotblock_delete:
      enabled: 'true'
      # These items will be deleted upon a mayor using /plot clear
      # To disable deleting replace the current entries with NONE.
      mayor_plot_delete: WALL_SIGN,SIGN_POST
 
    revert_on_unclaim:
      # *** WARNING***
      # If this is enabled any town plots which become unclaimed will
      # slowly be reverted to a snapshot taken before the plot was claimed.
      #
      # Regeneration will only work if the plot was
      # claimed under version 0.76.2, or
      # later with this feature enabled
      # Unlike the rest of this config section, the speed setting is not
      # set per-world. What you set for speed will be used in all worlds.
      #
      # If you allow players to break/build in the wild the snapshot will
      # include any changes made before the plot was claimed.
      enabled: 'true'
      speed: 1s
      # These block types will NOT be regenerated
      block_ignore: GOLD_ORE,LAPIS_ORE,LAPIS_BLOCK,GOLD_BLOCK,IRON_BLOCK,MOSSY_COBBLESTONE,TORCH,MOB_SPAWNER,DIAMOND_ORE,DIAMOND_BLOCK,SIGN_POST,WALL_SIGN,GLOWSTONE
 
    wild_revert_on_mob_explosion:
      # Enabling this will slowly regenerate holes created in the
      # wilderness by monsters exploding.
      enabled: 'true'
      entities: Creeper,EnderCrystal,EnderDragon,Fireball,SmallFireball,LargeFireball,TNTPrimed,ExplosiveMinecart
      delay: 20s
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                Global town settings                  | #
  # +------------------------------------------------------+ #
  ############################################################
 
global_town_settings:
  # can residents/Allies harm other residents when in an area with pvp enabled? Other than an Arena plot.
  friendly_fire: 'true'
  # Players within their town or allied towns will regenerate half a heart after every health_regen_speed seconds.
  health_regen:
    speed: 3s
    enable: 'true'
  # Allow towns to claim outposts (a townblock not connected to town).
  allow_outposts: 'true'
  # When set to true outposts can be limited by the townOutpostLimit value of the Town Levels and
  # the nationBonusOutpostLimit value in the Nation Levels. In this way nations can be made to be
  # the only way of receiving outposts, or as an incentive to receive more outposts. Towns which are
  # larger can have more outposts.
  # When activated, this setting will not cause towns who already have higher than their limit
  # to lose outposts. They will not be able to start new outposts until they have unclaimed outposts
  # to become under their limit. Likewise, towns that join a nation and receive bonus outposts will
  # be over their limit if they leave the nation.
  limit_outposts_using_town_and_nation_levels: 'false'
  # When limit_outposts_using_town_and_nation_levels is also true, towns which are over their outpost
  # limit will not be able to use their /town outpost teleports for the outpost #'s higher than their limit,
  # until they have dropped below their limit.
  # eg: If their limit is 3 then they cannot use /t outpost 4
  over_outpost_limits_stops_teleports: 'false'
  # Allow the use of /town spawn
  # Valid values are: true, false, war, peace
  # When war or peace is set, it is only possible to teleport to the town,
  # when there is a war or peace.
  allow_town_spawn: 'true'
  # Allow regular residents to use /town spawn [town] (TP to other towns if they are public).
  # Valid values are: true, false, war, peace
  # When war or peace is set, it is only possible to teleport to the town,
  # when there is a war or peace.
  allow_town_spawn_travel: 'true'
  # Allow regular residents to use /town spawn [town] to other towns in your nation.
  # Valid values are: true, false, war, peace
  # When war or peace is set, it is only possible to teleport to the town,
  # when there is a war or peace.
  allow_town_spawn_travel_nation: 'true'
  # Allow regular residents to use /town spawn [town] to other towns in a nation allied with your nation.
  # Valid values are: true, false, war, peace
  # When war or peace is set, it is only possible to teleport to the town,
  # when there is a war or peace.
  allow_town_spawn_travel_ally: 'true'
  # When set to true both nation and ally spawn travel will also require the target town to have their status set to public.
  is_nation_ally_spawning_requiring_public_status: 'false'
  # If non zero it delays any spawn request by x seconds.
  teleport_warmup_time: '0'
  # Respawn the player at his town spawn point when he/she dies
  town_respawn: 'false'
  # Town respawn only happens when the player dies in the same world as the town's spawn point.
  town_respawn_same_world_only: 'false'
  # Prevent players from using /town spawn while within unclaimed areas and/or enemy/neutral towns.
  # Allowed options: unclaimed,enemy,neutral
  prevent_town_spawn_in: enemy
  # Enables the [~Home] message.
  # If false it will make it harder for enemies to find the home block during a war
  show_town_notifications: 'true'
  # The required number of residents in a town to join a nation
  # If the number is 0, towns will not require a certain amount of residents to join a nation
  required_number_residents_join_nation: '0'
  # The required number of residents in a town to create a nation
  # If the number is 0, towns will not require a certain amount of residents to create a nation
  required_number_residents_create_nation: '0'
  # If set to true, if a nation is disbanded due to a lack of residents, the capital will be refunded the cost of nation creation.
  refund_disband_low_residents: 'true'
  # The maximum number of townblocks a town can be away from a nation capital,
  # Automatically precludes towns from one world joining a nation in another world.
  # If the number is 0, towns will not a proximity to a nation.
  nation_requires_proximity: '0.0'
  # List of blocks which can be modified on farm plots, as long as player is also allowed in the plot's '/plot perm' line.
  # Not included by default but some servers add GRASS_BLOCK,FARMLAND,DIRT to their list.
  farm_plot_allow_blocks: BAMBOO,BAMBOO_SAPLING,JUNGLE_LOG,JUNGLE_SAPLING,JUNGLE_LEAVES,OAK_LOG,OAK_SAPLING,OAK_LEAVES,BIRCH_LOG,BIRCH_SAPLING,BIRCH_LEAVES,ACACIA_LOG,ACACIA_SAPLING,ACACIA_LEAVES,DARK_OAK_LOG,DARK_OAK_SAPLING,DARK_OAK_LEAVES,SPRUCE_LOG,SPRUCE_SAPLING,SPRUCE_LEAVES,BEETROOTS,COCOA,CHORUS_PLANT,CHORUS_FLOWER,SWEET_BERRY_BUSH,KELP,SEAGRASS,TALL_SEAGRASS,GRASS,TALL_GRASS,FERN,LARGE_FERN,CARROTS,WHEAT,POTATOES,PUMPKIN,PUMPKIN_STEM,ATTACHED_PUMPKIN_STEM,NETHER_WART,COCOA,VINE,MELON,MELON_STEM,ATTACHED_MELON_STEM,SUGAR_CANE,CACTUS,ALLIUM,AZURE_BLUET,BLUE_ORCHID,CORNFLOWER,DANDELION,LILAC,LILY_OF_THE_VALLEY,ORANGE_TULIP,OXEYE_DAISY,PEONY,PINK_TULIP,POPPY,RED_TULIP,ROSE_BUSH,SUNFLOWER,WHITE_TULIP,WITHER_ROSE
  # List of animals which can be kiled on farm plots by town residents.
  farm_animals: PIG,COW,CHICKEN,SHEEP,MOOSHROOM
  # The maximum number of residents that can be joined to a town. Setting to 0 disables this feature.
  max_residents_per_town: '0'
  # If Towny should show players the townboard when they login
  display_board_onlogin: 'true'
  # If set to true, Towny will prevent a town from toggling PVP while an outsider is within the town's boundaries.
  # When active this feature can cause a bit of lag when the /t toggle pvp command is used, depending on how many players are online.
  outsiders_prevent_pvp_toggle: 'false'
  # If set to true, when a world has forcepvp set to true, homeblocks of towns will not be affected and have PVP set to off.
  homeblocks_prevent_forcepvp: 'false'
  # The amount of residents a town needs to claim an outpost,
  # Setting this value to 0, means a town can claim outposts no matter how many residents
  minimum_amount_of_residents_in_town_for_outpost: '0'
  # If People should keep their inventories on death in a town
  # Is not guaranteed to work with other keep inventory plugins!
  keep_inventory_on_death_in_town: 'false'
  # If People should keep their experience on death in a town
  # Is not guaranteed to work with other keep experience plugins!
  keep_experience_on_death_in_town: 'false'
  # Maximum amount that a town can set their plot, embassy, shop, etc plots' prices to.
  # Setting this higher can be dangerous if you use Towny in a mysql database. Large numbers can become shortened to scientific notation. 
  maximum_plot_price_cost: '1000000.0'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |              Global nation settings                  | #
  # +------------------------------------------------------+ #
  ############################################################
 
global_nation_settings:
 
  # Nation Zones are a special type of wilderness surrounding Capitals of Nations or Nation Capitals and their Towns.
  # When it is enabled players who are members of the nation can use the wilderness surrounding the town like normal.
  # Players who are not part of that nation will find themselves unable to break/build/switch/itemuse in this part of the wilderness.
  # The amount of townblocks used for the zone is determined by the size of the nation and configured in the nation levels.
  # Because these zones are still wilderness anyone can claim these townblocks.
  # It is recommended that whatever size you choose, these numbers should be less than the min_plot_distance_from_town_plot otherwise
  # someone might not be able to build/destroy in the wilderness outside their town.
  nationzone:
 
    # Nation zone feature is disabled by default. This is because it can cause a higher server load for servers with a large player count.
    enable: 'false'
 
    # When set to true, only the capital town of a nation will be surrounded by a nation zone type of wilderness.
    only_capitals: 'true'
 
    # Amount of buffer added to nation zone width surrounding capitals only. Creates a larger buffer around nation capitals.
    capital_bonus_size: '0'
 
    # When set to true, nation zones are disabled during the the Towny war types.
    war_disables: 'true'
  # If Towny should show players the nationboard when they login.
  display_board_onlogin: 'true'
  # If enabled, only allow the nation spawn to be set in the capital city.
  capital_spawn: 'true'
  # Allow the use of /nation spawn
  # Valid values are: true, false, war, peace
  # When war or peace is set, it is only possible to teleport to the nation,
  # when there is a war or peace.
  allow_nation_spawn: 'true'
  # Allow regular residents to use /nation spawn [nation] (TP to other nations if they are public).
  # Valid values are: true, false, war, peace
  # When war or peace is set, it is only possible to teleport to the nation,
  # when there is a war or peace.
  allow_nation_spawn_travel: 'true'
  # Allow regular residents to use /nation spawn [nation] to other nations allied with your nation.
  # Valid values are: true, false, war, peace
  # When war or peace is set, it is only possible to teleport to the nations,
  # when there is a war or peace.
  allow_nation_spawn_travel_ally: 'true'
  # If higher than 0, it will limit how many towns can be joined into a nation.
  # Does not affect existing nations that are already over the limit.
  max_towns_per_nation: '0'
  default:
    # If set to true, any newly made nation will have their spawn set to public.
    public: 'false'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                 Plugin interfacing                   | #
  # +------------------------------------------------------+ #
  ############################################################
 
plugin:
 
  # Valid load and save types are: flatfile, mysql, h2.
  database:
    database_load: flatfile
    database_save: flatfile
 
    # SQL database connection details (IF set to use SQL).
    sql:
      hostname: localhost
      port: '3306'
      dbname: towny
      table_prefix: towny_
      username: root
      password: ''
      ssl: 'false'
 
    # Flatfile backup settings.
    daily_backups: 'true'
    backups_are_deleted_after: 90d
 
    # Valid entries are: zip, none.
    flatfile_backup: zip
 
  interfacing:
 
    tekkit:
      # Add any fake players for client/server mods (aka Tekkit) here
      fake_residents: '[IndustrialCraft],[BuildCraft],[Redpower],[Forestry],[Turtle]'
 
    # Enable using_essentials if you are using cooldowns in essentials for teleports.
    using_essentials: 'false'
 
    # This enables/disables all the economy functions of Towny.
    # This will first attempt to use Vault or Reserve to bridge your economy plugin with Towny.
    # If Reserve/Vault is not present it will attempt to find a supported economy plugin.
    # If neither Vault/Reserve or supported economy are present it will not be possible to create towns or do any operations that require money.
    using_economy: 'true'
 
  day_timer:
    # The number of hours in each "day".
    # You can configure for 10 hour days. Default is 24 hours.
    day_interval: 1d
    # The time each "day", when taxes will be collected.
    # MUST be less than day_interval. Default is 12h (midday).
    new_day_time: 12h
 
  # Lots of messages to tell you what's going on in the server with time taken for events.
  debug_mode: 'false'
 
  # Info tool for server admins to use to query in game blocks and entities.
  info_tool: BRICK
 
  # Spams the player named in dev_name with all messages related to towny.
  dev_mode:
    enable: 'false'
    dev_name: ElgarL
 
  # Record all messages to the towny.log
  logging: 'true'
  # If true this will cause the log to be wiped at every startup.
  reset_log_on_boot: 'true'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |               Filters colour and chat                | #
  # +------------------------------------------------------+ #
  ############################################################
 
filters_colour_chat:
  # This is the name given to any NPC assigned mayor.
  npc_prefix: NPC
  # Regex fields used in validating inputs.
  regex:
    name_filter_regex: '[ /]'
    name_check_regex: ^[a-zA-Z0-9._\[\]-]*$
    string_check_regex: ^[a-zA-Z0-9\s._\[\]\#\?\!\@\$\%\^\&\*\-\,\*\(\)\{\}]*$
    name_remove_regex: '[^a-zA-Z0-9._\[\]-]'
 
  modify_chat:
    # Maximum length of Town and Nation names.
    max_name_length: '20'
    # Maximum length of titles and surnames.
    max_title_length: '10'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |             block/item/mob protection                | #
  # +------------------------------------------------------+ #
  ############################################################
 
protection:
 
  # Items that can be blocked within towns via town/plot flags
  # 259 - flint and steel
  # 325 - bucket
  # 326 - water bucket
  # 327 - lava bucket
  # 351 - bone/bonemeal
  # 359 - shears
  # 368 - ender pearl
  # 374 - glass bottle
  # 385 - fire charge
  item_use_ids: BONE_MEAL,FLINT_AND_STEEL,BUCKET,WATER_BUCKET,LAVA_BUCKET,MINECART,STORAGE_MINECART,INK_SACK,SHEARS,ENDER_PEARL,GLASS_BOTTLE,FIREBALL,ARMOR_STAND,SKULL_ITEM,BIRCH_BOAT,ACACIA_BOAT,DARK_OAK_BOAT,JUNGLE_BOAT,OAK_BOAT,SPRUCE_BOAT,END_CRYSTAL,POWERED_MINECART,COMMAND_MINECART,EXPLOSIVE_MINECART,HOPPER_MINECART,CHORUS_FRUIT
 
  # Items which can be blocked or enabled via town/plot flags
  # 25 - noteblock
  # 54 - chest ...etc
  switch_ids: JUKEBOX,NOTE_BLOCK,BEACON,CHEST,TRAPPED_CHEST,FURNACE,DISPENSER,HOPPER,DROPPER,LEVER,COMPARATOR,REPEATER,STONE_PRESSURE_PLATE,ACACIA_PRESSURE_PLATE,BIRCH_PRESSURE_PLATE,DARK_OAK_PRESSURE_PLATE,JUNGLE_PRESSURE_PLATE,OAK_PRESSURE_PLATE,SPRUCE_PRESSURE_PLATE,HEAVY_WEIGHTED_PRESSURE_PLATE,LIGHT_WEIGHTED_PRESSURE_PLATE,STONE_BUTTON,ACACIA_BUTTON,BIRCH_BUTTON,DARK_OAK_BUTTON,JUNGLE_BUTTON,OAK_BUTTON,SPRUCE_BUTTON,ACACIA_DOOR,BIRCH_DOOR,DARK_OAK_DOOR,JUNGLE_DOOR,OAK_DOOR,SPRUCE_DOOR,ACACIA_FENCE_GATE,BIRCH_FENCE_GATE,DARK_OAK_FENCE_GATE,OAK_FENCE_GATE,JUNGLE_FENCE_GATE,SPRUCE_FENCE_GATE,ACACIA_TRAPDOOR,BIRCH_TRAPDOOR,DARK_OAK_TRAPDOOR,JUNGLE_TRAPDOOR,OAK_TRAPDOOR,SPRUCE_TRAPDOOR,MINECART,COMMAND_BLOCK_MINECART,CHEST_MINECART,FURNACE_MINECART,HOPPER_MINECART,TNT_MINECART,SHULKER_BOX,WHITE_SHULKER_BOX,ORANGE_SHULKER_BOX,MAGENTA_SHULKER_BOX,LIGHT_BLUE_SHULKER_BOX,YELLOW_SHULKER_BOX,LIME_SHULKER_BOX,PINK_SHULKER_BOX,GRAY_SHULKER_BOX,CYAN_SHULKER_BOX,PURPLE_SHULKER_BOX,BLUE_SHULKER_BOX,BROWN_SHULKER_BOX,GREEN_SHULKER_BOX,RED_SHULKER_BOX,BLACK_SHULKER_BOX,CARROT_STICK,DAYLIGHT_DETECTOR,STONECUTTER,SMITHING_TABLE,FLETCHING_TABLE,SMOKER,LOOM,LECTERN,GRINDSTONE,COMPOSTER,CARTOGRAPHY_TABLE,BLAST_FURNACE,BELL,BARREL,DRAGON_EGG,ITEM_FRAME,POTTED_ACACIA_SAPLING,POTTED_ALLIUM,POTTED_AZURE_BLUET,POTTED_BAMBOO,POTTED_BIRCH_SAPLING,POTTED_BLUE_ORCHID,POTTED_BROWN_MUSHROOM,POTTED_CACTUS,POTTED_CORNFLOWER,POTTED_DANDELION,POTTED_DARK_OAK_SAPLING,POTTED_DEAD_BUSH,POTTED_FERN,POTTED_JUNGLE_SAPLING,POTTED_LILY_OF_THE_VALLEY,POTTED_OAK_SAPLING,POTTED_ORANGE_TULIP,POTTED_OXEYE_DAISY,POTTED_PINK_TULIP,POTTED_POPPY,POTTED_RED_MUSHROOM,POTTED_RED_TULIP,POTTED_SPRUCE_SAPLING,POTTED_WHITE_TULIP,POTTED_WITHER_ROSE
 
  # permitted entities https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/entity/LivingEntity.html
  # Animals, Chicken, Cow, Creature, Creeper, Flying, Ghast, Giant, Monster, Pig, 
  # PigZombie, Sheep, Skeleton, Slime, Spider, Squid, WaterMob, Wolf, Zombie, Shulker
  # Husk, Stray, SkeletonHorse, ZombieHorse, Vex, Vindicator, Evoker, Endermite, PolarBear
 
  # Remove living entities within a town's boundaries, if the town has the mob removal flag set.
  town_mob_removal_entities: Monster,Flying,Slime,Shulker,SkeletonHorse,ZombieHorse
 
  # Prevent the spawning of villager babies in towns.
  town_prevent_villager_breeding: 'false'
  # Disable creatures triggering stone pressure plates
  disable_creature_pressureplate_stone: 'true'
 
  # Globally remove living entities in all worlds that have their flag set.
  world_mob_removal_entities: Monster,Flying,Slime,Shulker,SkeletonHorse,ZombieHorse
 
  # Prevent the spawning of villager babies in the world.
  world_prevent_villager_breeding: 'false'
 
  # The maximum amount of time a mob could be inside a town's boundaries before being sent to the void.
  # Lower values will check all entities more often at the risk of heavier burden and resource use.
  # NEVER set below 1.
  mob_removal_speed: 5s
 
  # permitted entities https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/entity/package-summary.html
  # Animals, Chicken, Cow, Creature, Creeper, Flying, Ghast, Giant, Monster, Pig, 
  # PigZombie, Sheep, Skeleton, Slime, Spider, Squid, WaterMob, Wolf, Zombie
 
  # Protect living entities within a town's boundaries from being killed by players.
  mob_types: Animals,WaterMob,NPC,Snowman,ArmorStand
 
  # permitted Potion Types https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/potion/PotionType.html
  # ABSORPTION, BLINDNESS, CONFUSION, DAMAGE_RESISTANCE, FAST_DIGGING, FIRE_RESISTANCE, HARM, HEAL, HEALTH_BOOST, HUNGER, 
  # INCREASE_DAMAGE, INVISIBILITY, JUMP, NIGHT_VISION, POISON, REGENERATION, SATURATION, SLOW , SLOW_DIGGING, 
  # SPEED, WATER_BREATHING, WEAKNESS, WITHER.
 
  # When preventing PVP prevent the use of these potions.
  potion_types: BLINDNESS,CONFUSION,HARM,HUNGER,POISON,SLOW,SLOW_DIGGING,WEAKNESS,WITHER
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                Wilderness settings                   | #
  # +------------------------------------------------------+ #
  ############################################################
 
  # These Settings defaults only. They are copied to each worlds data files upon first detection
  # To make changes for each world edit the settings in the relevant worlds data file 'plugins/Towny/data/worlds/'
 
unclaimed:
  unclaimed_zone_build: 'false'
  unclaimed_zone_destroy: 'false'
  unclaimed_zone_item_use: 'false'
  unclaimed_zone_ignore: SAPLING,GOLD_ORE,IRON_ORE,COAL_ORE,LOG,LEAVES,LAPIS_ORE,LONG_GRASS,YELLOW_FLOWER,RED_ROSE,BROWN_MUSHROOM,RED_MUSHROOM,TORCH,DIAMOND_ORE,LADDER,RAILS,REDSTONE_ORE,GLOWING_REDSTONE_ORE,CACTUS,CLAY,SUGAR_CANE_BLOCK,PUMPKIN,GLOWSTONE,LOG_2,VINE,NETHER_WARTS,COCOA
  unclaimed_zone_switch: 'false'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                 Town Notifications                   | #
  # +------------------------------------------------------+ #
  ############################################################
 
  # This is the format for the notifications sent as players move between plots.
  # Empty a particular format for it to be ignored.
 
  # Example:
  # [notification.format]
  # ~ [notification.area_[wilderness/town]][notification.splitter][notification.[no_]owner][notification.splitter][notification.plot.format]
  # ... [notification.plot.format]
  # ... [notification.plot.homeblock][notification.plot.splitter][notification.plot.forsale][notification.plot.splitter][notification.plot.type]
  # ~ Wak Town - Lord Jebus - [Home] [For Sale: 50 Beli] [Shop]
 
notification:
  format: '&6 ~ %s'
  splitter: '&7 - '
  area_wilderness: '&2%s'
  area_wilderness_pvp: '%s'
  area_town: '&6%s'
  area_town_pvp: '%s'
  owner: '&a%s'
  no_owner: '&a%s'
  plot:
    splitter: ' '
    format: '%s'
    homeblock: '&b[Home]'
    outpostblock: '&b[Outpost]'
    forsale: '&e[For Sale: %s]'
    type: '&6[%s]'
  # If set to true MC's Title and Subtitle feature will be used when crossing into a town.
  # Could be seen as intrusive/distracting, so false by default.
  using_titles: 'false'
 
  # Requires the above using_titles to be set to true.
  # Title and Subtitle shown when entering a town or the wilderness. By default 1st line is blank, the 2nd line shows {townname} or {wilderness}.
  # You may use colour codes &f, &c and so on.
  titles:
    # Entering Town Upper Title Line
    town_title: ''
    # Entering Town Lower Subtitle line.
    town_subtitle: '&b{townname}'
    # Entering Wilderness Upper Title Line
    wilderness_title: ''
    # Entering Wilderness Lower Subtitle line.
    wilderness_subtitle: '&2{wilderness}'
  # If the notification.owner option should show name or {title} name.
  # Titles are the ones granted by nation kings.
  owner_shows_nation_title: 'false'
 
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |             Default Town/Plot flags                  | #
  # +------------------------------------------------------+ #
  ############################################################
 
 
default_perm_flags:
 
  # Default permission flags for residents plots within a town
  #
  # Can allies/friends/outsiders perform certain actions in the town
  #
  # build - place blocks and other items
  # destroy - break blocks and other items
  # itemuse - use items such as furnaces (as defined in item_use_ids)
  # switch - trigger or activate switches (as defined in switch_ids)
  resident:
    friend:
      build: 'true'
      destroy: 'true'
      item_use: 'true'
      switch: 'true'
    ally:
      build: 'false'
      destroy: 'false'
      item_use: 'false'
      switch: 'false'
    outsider:
      build: 'false'
      destroy: 'false'
      item_use: 'false'
      switch: 'false'
 
  # Default permission flags for towns
  # These are copied into the town data file at creation
  #
  # Can allies/outsiders/residents perform certain actions in the town
  #
  # build - place blocks and other items
  # destroy - break blocks and other items
  # itemuse - use items such as flint and steel or buckets (as defined in item_use_ids)
  # switch - trigger or activate switches (as defined in switch_ids)
  town:
    default:
      pvp: 'true'
      fire: 'false'
      explosion: 'false'
      mobs: 'false'
    resident:
      build: 'true'
      destroy: 'true'
      item_use: 'true'
      switch: 'true'
    ally:
      build: 'false'
      destroy: 'false'
      item_use: 'false'
      switch: 'false'
    outsider:
      build: 'false'
      destroy: 'false'
      item_use: 'false'
      switch: 'false'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                 Towny Invite System                  | #
  # +------------------------------------------------------+ #
  ############################################################
 
invite_system:
  # Command used to accept towny invites)
  #e.g Player join town invite.
  accept_command: accept
  # Command used to deny towny invites
  #e.g Player join town invite.
  deny_command: deny
  # Command used to confirm some towny actions/tasks)
  #e.g Purging database or removing a large amount of townblocks
  confirm_command: confirm
  # Command used to cancel some towny actions/tasks
  #e.g Purging database or removing a large amount of townblocks
  cancel_command: cancel
  # When set for more than 0m, the amount of time (in minutes) which must have passed between
  # a player's first log in and when they can be invited to a town.
  cooldowntime: 0m
  # You can increase these limits but it is not recommended. Invites/requests are not saved between server reloads/stops.
  maximum_invites_sent:
    # How many invites a town can send out to players, to join the town.
    town_toplayer: '35'
    # How many invites a nation can send out to towns, to join the nation.
    nation_totown: '35'
    # How many requests a nation can send out to other nations, to ally with the nation.
    # Only used when war.disallow_one_way_alliance is set to true.
    nation_tonation: '35'
  # You can increase these limits but it is not recommended. Invites/requests are not saved between server reloads/stops.
  maximum_invites_received:
    # How many invites can one player have from towns.
    player: '10'
    # How many invites can one town have from nations.
    town: '10'
    # How many requests can one nation have from other nations for an alliance.
    nation: '10'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                  Resident settings                   | #
  # +------------------------------------------------------+ #
  ############################################################
 
resident_settings:
  # player is flagged as inactive after 1 hour (default)
  inactive_after_time: 1h
  # if enabled old residents will be kicked and deleted from a town
  # after Two months (default) of not logging in
  delete_old_residents:
    enable: 'false'
    deleted_after_time: 60d
    delete_economy_account: 'true'
  # The name of the town a resident will automatically join when he first registers.
  default_town_name: ''
  # If true, players can only use beds in plots they personally own.
  deny_bed_use: 'false'
  # If true, players who join the server for the first time will cause the msg_registration message in the language files to be shown server-wide.
  is_showing_welcome_message: 'true'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                  Economy settings                    | #
  # +------------------------------------------------------+ #
  ############################################################
 
economy:
  # By default it is set to true.
  # Rarely set to false. Set to false if you get concurrent modification errors on timers for daily tax collections.
  use_async: 'true'
  # Prefix to apply to all town economy accounts.
  town_prefix: town-
  # Prefix to apply to all nation economy accounts.
  nation_prefix: nation-
  # The cost of renaming a town.
  town_rename_cost: '0'
  # The cost of renaming a nation.
  nation_rename_cost: '0'
 
  spawn_travel:
    # Cost to use /town spawn
    price_town_spawn_travel: '0.0'
    # Cost to use '/town spawn [town]' to another town in your nation.
    price_town_nation_spawn_travel: '5.0'
    # Cost to use '/town spawn [town]' to another town in a nation that is allied with your nation.
    price_town_ally_spawn_travel: '10.0'
    # Cost to use /town spawn [town]
    # This is paid to the town you goto.
    price_town_public_spawn_travel: '10.0'
    # When set to true, any cost paid by a player to use any variant of '/town spawn' will be paid to the town bank.
    # When false the amount will be paid to the server account whose name is set in the closed economy setting below..
    town_spawn_cost_paid_to_town: 'true'
 
  # The daily upkeep to remain neutral during a war. Neutrality will exclude you from a war event, as well as deterring enemies.
  price_nation_neutrality: '100.0'
 
  new_expand:
    # How much it costs to start a nation.
    price_new_nation: '1000.0'
    # How much it costs to start a town.
    price_new_town: '250.0'
    # How much it costs to make an outpost. An outpost isn't limited to being on the edge of town.
    price_outpost: '500.0'
    # The price for a town to expand one townblock.
    price_claim_townblock: '25.0'
    # How much it costs a player to buy extra blocks.
    price_purchased_bonus_townblock: '25.0'
    # How much every extra bonus block costs more. Set to 1 to deactivate this. 1.2 means +20% to every bonus claim block cost.
    price_purchased_bonus_townblock_increase: '1.0'
 
  death:
    # Either fixed or percentage.
    # For percentage 1.0 would be 100%. 0.01 would be 1%.
    price_death_type: fixed
    # A maximum amount paid out by a resident from their personal holdings for percentage deaths.
    # Set to 0 to have no cap.
    percentage_cap: '0.0'
    # If True, only charge death prices for pvp kills. Not monsters/environmental deaths.
    price_death_pvp_only: 'false'
 
    price_death: '1.0'
 
    price_death_town: '0.0'
 
    price_death_nation: '0.0'
 
  banks:
    # Maximum amount of money allowed in town bank
    # Use 0 for no limit
    town_bank_cap: '0.0'
    # Set to true to allow withdrawls from town banks
    town_allow_withdrawls: 'true'
    # Maximum amount of money allowed in nation bank
    # Use 0 for no limit
    nation_bank_cap: '0.0'
    # Set to true to allow withdrawls from nation banks
    nation_allow_withdrawls: 'true'
    # When set to true, players can only use their town withdraw/deposit commands while inside of their own town.
    # Likewise, nation banks can only be withdrawn/deposited to while in the capital city.
    disallow_bank_actions_outside_town: 'false'
  closed_economy:
    # The name of the account that all money that normally disappears goes into.
    server_account: towny-server
    # Turn on/off whether all transactions that normally don't have a second party are to be done with a certain account.
    # Eg: The money taken during Daily Taxes is just removed. With this on, the amount taken would be funneled into an account.
    #     This also applies when a player collects money, like when the player is refunded money when a delayed teleport fails.
    enabled: 'false'
 
  daily_taxes:
    # Enables taxes to be collected daily by town/nation
    # If a town can't pay it's tax then it is kicked from the nation.
    # if a resident can't pay his plot tax he loses his plot.
    # if a resident can't pay his town tax then he is kicked from the town.
    # if a town or nation fails to pay it's upkeep it is deleted.
    enabled: 'true'
    # Maximum tax amount allowed when using flat taxes
    max_tax_amount: '1000.0'
    # maximum tax percentage allowed when taxing by percentages
    max_tax_percent: '25'
    # The server's daily charge on each nation. If a nation fails to pay this upkeep
    # all of it's member town are kicked and the Nation is removed.
    price_nation_upkeep: '100.0'
    # The server's daily charge on each town. If a town fails to pay this upkeep
    # all of it's residents are kicked and the town is removed.
    price_town_upkeep: '10.0'
    # Uses total amount of owned plots to determine upkeep instead of the town level (Number of residents)
    # calculated by (number of claimed plots X price_town_upkeep).
    town_plotbased_upkeep: 'false'
    # If set to true, the plot-based-upkeep system will be modified by the Town Levels' upkeep modifiers.
    town_plotbased_upkeep_affected_by_town_level_modifier: 'false'
    # If enabled and you set a negative upkeep for the town
    # any funds the town gains via upkeep at a new day
    # will be shared out between the plot owners.
    use_plot_payments: 'false'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                 Jail Plot settings                   | #
  # +------------------------------------------------------+ #
  ############################################################
 
jail:
  #If true attacking players who die on enemy-town land will be placed into the defending town's jail if it exists.
  #Requires town_respawn to be true in order to work.
  is_jailing_attacking_enemies: 'false'
  #If true attacking players who are considered an outlaw, that are killed inside town land will be placed into the defending town's jail if it exists.
  #Requires town_respawn to be true in order to work.
  is_jailing_attacking_outlaws: 'false'
  #If true jailed players can use Ender Pearls but are still barred from using other methods of teleporting.
  jail_allows_ender_pearls: 'false'
  #If false jailed players can use /town leave, and escape a jail.
  jail_denies_town_leave: 'false'
 
  bail:
    #If true players can pay a bail amount to be unjailed.
    is_allowing_bail: 'false'
    #Amount that bail costs.
    bail_amount: '10'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                 Bank Plot settings                   | #
  # +------------------------------------------------------+ #
  ############################################################
  # Bank plots may be used by other economy plugins using the Towny API.
 
bank:
  # If true players will only be able to use /t deposit, /t withdraw, /n deposit & /n withdraw while inside bank plots belonging to the town or nation capital respectively.
  # Home plots will also allow deposit and withdraw commands.
  is_banking_limited_to_bank_plots: 'false'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                     War settings                     | #
  # +------------------------------------------------------+ #
  ############################################################
 
war:
  #This setting allows you disable the ability for a nation to pay to remain neutral during a war.
  nation_can_be_neutral: 'true'
  #By setting this to true, nations will receive a prompt for alliances and alliances will show on both nations.
  disallow_one_way_alliance: 'false'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |         Economy Transfers During War settings        | #
  # +------------------------------------------------------+ #
  ############################################################
 
  economy:
    enemy:
      # Amount charged to place a warflag (payed to server).
      place_flag: '10'
      # Amount payed from the flagbearer to the defender after defending the area.
      defended_attack: '10'
    # Defending town pays attaking flagbearer. If a negative (attacker pays defending town),
    # and the attacker can't pay, the attack is canceled.
    townblock_won: '10'
    # Same as townblock_won but for the special case of winning the homeblock.
    homeblock_won: '100'
 
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                 War Event settings                   | #
  # +------------------------------------------------------+ #
  ############################################################
 
  # This is started with /townyadmnin toggle war
 
  # In peace time War spoils are accumulated from towns and nations being
  # deleted with any money left in the bank.
  #
  # These funds are increased during a war event upon a player death.
  # An additional bonus to the war chest is set in base_spoils.
  #
  # During the event a town losing a townblock pays the wartime_town_block_loss_price to the attacking town.
  # The war is won when the only nations left in the battle are allies, or only a single nation.
  #
  # The winning nations share half of the war spoils.
  # The remaining half is paid to the town which took the most town blocks, and lost the least.
 
  event:
    warning_delay: '30'
    #If false all towns not in nations can be attacked during a war event.
    towns_are_neutral: 'true'
    enemy:
      # If true, enemy's can only attack the edge plots of a town in war.
      only_attack_borders: 'true'
    plots:
      # If true, nation members and allies can regen health on plots during war.
      healable: 'true'
      # If true, fireworks will be launched at plots being attacked or healed in war every war tick.
      firework_on_attacked: 'true'
 
    # If true and the monarch/king dies the nation is removed from the war.
    remove_on_monarch_death: 'false'
    # If enabled players will be able to break/place any blocks in enemy plots during a war.
    # This setting SHOULD NOT BE USED unless you want the most chaotic war possible.
    # The editable_materials list in the Warzone Block Permission section should be used instead.
    allow_block_griefing: 'false'
 
    # A townblock takes damage every 5 seconds that an enemy is stood in it.
    block_hp:
      town_block_hp: '60'
      home_block_hp: '120'
 
    eco:
      # This amount is new money injected into the economy with a war event.
      base_spoils: '100.0'
      # This amount is taken from the losing town for each plot lost.
      wartime_town_block_loss_price: '100.0'
      # This amount is taken from the player if they die during the event
      price_death_wartime: '200.0'
    # If set to true when a town drops an enemy townblock's HP to 0, the attacking town gains a bonus townblock,
    # and the losing town gains a negative (-1) bonus townblock.
    costs_townblocks: 'false'
 
    points:
      points_townblock: '1'
      points_town: '10'
      points_nation: '100'
      points_kill: '1'
 
    # The minimum height at which a player must stand to count as an attacker.
    min_height: '60'
 
  ############################################################
  # +------------------------------------------------------+ #
  # |                   Flag war settings                  | #
  # |                                                      | #
  # |               Separate from Event War                | #
  # |                 Unsupported / Buggy                  | #
  # +------------------------------------------------------+ #
  ############################################################
 
  enemy:
    # If false, players won't be able to place war flags, effectively disabling warzones.
    allow_attacks: 'false'
    # If true, enemy's can only attack the edge plots of a town with war flags.
    only_attack_borders: 'true'
    # This many people must be online in target town in order to place a war flag in their domain.
    min_players_online_in_town: '2'
    # This many people must be online in target nation in order to place a war flag in their domain.
    min_players_online_in_nation: '3'
    max_active_flags_per_player: '1'
    flag:
      waiting_time: 1m
      # This is the block a player must place to trigger the attack event.
      base_block: fence
      # This is the block a player must place to trigger the attack event.
      light_block: torch
    beacon:
      # Must be smaller than half the size of town_block_size.
      radius: '3'
      # The range the beacon will be drawn in. It's flexibility is in case the flag is close to the height limit.
      # If a flag is too close to the height limit (lower than the minimum), it will not be drawn.
      height_above_flag:
        min: '3'
        max: '64'
      draw: 'true'
      wireframe_block: glowstone
  ############################################################
  # +------------------------------------------------------+ #
  # |              Warzone Block Permissions               | #
  # |                                                      | #
  # |              Used in Flag & Event Wars               | #
  # +------------------------------------------------------+ #
  ############################################################
 
  warzone:
    # List of materaials that can be modified in a warzone.
    # '*' = Allow all materials.
    # Prepend a '-' in front of a material to remove it. Used in conjunction with when you use '*'.
    # Eg: '*,-chest,-furnace'
    editable_materials: tnt,fence,ladder,wood_door,iron_door,fire
    item_use: 'true'
    switch: 'true'
    # Add '-fire' to editable materials for complete protection when setting is false. This prevents fire to be created and spread.
    fire: 'true'
    explosions: 'true'
    explosions_break_blocks: 'true'
    # Only under affect when explosions_break_blocks is true.
    explosions_regen_blocks: 'true'
    # A list of blocks that will not be exploded, mostly because they won't regenerate properly.
    # These blocks will also protect the block below them, so that blocks like doors do not dupe themselves.
    # Only under affect when explosions_break_blocks is true.
    explosions_ignore_list: WOODEN_DOOR,ACACIA_DOOR,DARK_OAK_DOOR,JUNGLE_DOOR,BIRCH_DOOR,SPRUCE_DOOR,IRON_DOOR,CHEST,TRAPPED_CHEST,FURNACE,BURNING_FURNACE,DROPPER,DISPENSER,HOPPER,ENDER_CHEST,WHITE_SHULKER_BOX,ORANGE_SHULKER_BOX,MAGENTA_SHULKER_BOX,LIGHT_BLUE_SHULKER_BOX,YELLOW_SHULKER_BOX,LIME_SHULKER_BOX,PINK_SHULKER_BOX,GRAY_SHULKER_BOX,SILVER_SHULKER_BOX,CYAN_SHULKER_BOX,PURPLE_SHULKER_BOX,BLUE_SHULKER_BOX,BROWN_SHULKER_BOX,GREEN_SHULKER_BOX,RED_SHULKER_BOX,BLACK_SHULKER_BOX,NOTE_BLOCK,LEVER,STONE_PLATE,IRON_DOOR_BLOCK,WOOD_PLATE,JUKEBOX,DIODE_BLOCK_OFF,DIODE_BLOCK_ON,FENCE_GATE,GOLD_PLATE,IRON_PLATE,REDSTONE_COMPARATOR_OFF,REDSTONE_COMPARATOR_ON,BEACON
```