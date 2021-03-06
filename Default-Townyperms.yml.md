```
#############################################################################################
# This file contains custom permission sets which will be assigned to your players
# depending on their current status.
#
# This is all managed by towny and pushed directly to CraftBukkits SuperPerms.
# These will be in addition to any you manually assign in your specific permission plugin.
#
# You may assign any Permission nodes here, including those from other plugins.
# You may also create any custom ranks you require.
# You may change the names of any of the ranks except: nomad, default, mayor, king.
#############################################################################################
 
 
# The 'nomad' permissions are given to all players in all Towny worlds, townless and players who are part of a town.
nomad:
- towny.command.towny.map
- towny.command.towny.prices
- towny.command.towny.tree
- towny.command.towny.time
- towny.command.towny.universe
- towny.command.towny.version
- towny.command.towny.war
- towny.command.town.online
- towny.command.town.here
- towny.command.town.new
- towny.command.town.join
- towny.command.town.list.*
- towny.command.town.reslist
- towny.command.plot.group.*
- towny.command.plot.perm
- towny.command.plot.perm.hud
- towny.command.plot.trust
- towny.command.nation.list.*
- towny.command.nation.townlist
- towny.command.nation.allylist
- towny.command.nation.enemylist
- towny.town.resident
- towny.town.spawn.public
- towny.chat.general
- towny.command.towny.war.hud
 
# This section of permissions covers players who are members of a town.
towns:
 
  # 'default' is the permission set which is auto assigned to any normal town member.
  default:
  - towny.command.resident.*
  - towny.command.plot.claim
  - towny.command.plot.unclaim
  - towny.command.plot.forsale
  - towny.command.plot.notforsale
  - towny.command.plot.toggle.*
  - towny.command.plot.set.perm
  - towny.command.plot.set.reset
  - towny.command.town.online
  - towny.command.town.leave
  - towny.command.town.deposit
  - towny.command.town.reclaim
  - towny.town.spawn.town
  - towny.chat.town
 
  # Mayors get these permissions in addition to the default set.
  mayor:
  - towny.tax_exempt
  - towny.command.towny.top
  - towny.command.town.*
  - towny.command.plot.*
  - towny.claimed.owntown.*
  - towny.command.nation.new
  - towny.outlaw.jailer
  - towny.command.nation.join
  - towny.command.nation.leave
 
  # Ranks contain additional permissions residents will be
  # granted if they are assigned that specific rank.
  ranks:
 
    # assistants are able to grant VIP and helper rank.
    assistant:
    - towny.tax_exempt
    - towny.command.town.claim.*
    - towny.command.town.invite.add
    - towny.command.plot.*
    - towny.command.town.toggle.public
    - towny.claimed.owntown.switch.*
    - towny.command.town.rank.vip
    - towny.command.town.rank.helper
    - towny.outlaw.jailer
    helper:
    - towny.claimed.townowned.switch.*
 
    # Currently only an example rank holder with no extra permissions.
    donator:
    - foo.bar
 
    # Currently only an example rank holder with no extra permissions.
    vip:
    - foo.bar
 
    # Sheriff rank is able to jail other town members.
    sheriff:
    - towny.command.town.toggle.jail
    - towny.outlaw.jailer
 
# This section of permissions covers players who are members of any town in a nation.
nations:
 
  # All nation members get these permissions.
  default:
  - towny.command.nation.online
  - towny.command.nation.deposit
  - towny.command.nation.spawn
  - towny.nation.spawn.nation
  - towny.nation.spawn.ally
  - towny.town.spawn.nation
  - towny.town.spawn.ally
  - towny.chat.nation
  - towny.chat.alliance
 
  # Kings get these permissions in addition to the default set.
  king:
  - towny.command.nation.*
  - towny.command.nation.deposit.other
  ranks:
    assistant:
    - towny.command.nation.rank.helper
    - towny.command.nation.invite.add
    - towny.command.nation.ally.*
    - towny.command.nation.enemy
    - towny.command.nation.deposit.other
    helper:
    - towny.command.nation.add

```