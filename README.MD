## 命令列表

你可能需要在终端中运行 `java -jar grasscutter.jar -handbook` 它将会创建一个 `GM Handbook.txt` 以方便您查阅物品ID等

你可能需要在终端中运行 `java -jar grasscutter.jar -gachamap` 来使得祈愿历史记录系统正常显示物品信息。 这个命令生成一个配置文件到如下文件夹：`GRASSCUTTER_RESOURCE/gcstatic`。 不执行此命令，您的祈愿历史记录中将只会显示数字ID而非物品名称。（目前仅支持自动生成英文记录信息）

在每个玩家的朋友列表中都有一个名为“Server”的虚拟用户，你可以通过发送消息来使用命令。命令也适用于其他聊天室，例如私人/团队聊天。
要在游戏中使用命令，需要添加 `/` 或 `!` 前缀，如 `/pos`

| 命令            | 用法                                         | 权限节点                  | 可用性   | 注释                                       | 别名                                            |
| -------------- | -------------------------------------------- | ------------------------- | -------- | ------------------------------------------ | ----------------------------------------------- |
| account        | account <create\|delete> <用户名> [uid]      |                           | 仅服务端 | 通过指定用户名和uid增删账户                |                                                 |
| broadcast      | broadcast <消息内容>                         | server.broadcast          | 均可使用 | 给所有玩家发送公告                         | b                                               |
| coop           | coop \<uid> <目标uid>                 | server.coop               | 均可使用    | 强制某位玩家进入指定玩家的多人世界                  |                                                 |
| changescene    | changescene <场景ID>                         | player.changescene        | 仅客户端 | 切换到指定场景                             | scene                                           |
| clear          | clear <all\|wp\|art\|mat> [UID]                     | player.clearinv     | 仅客户端 | 删除所有未装备及未解锁的圣遗物(art)或武器(wp)或材料(mat)或者所有(all),包括五星    | clear         |
| drop           | drop <物品ID\|物品名称> [数量]               | server.drop               | 仅客户端 | 在指定玩家周围掉落指定物品                 | `d` `dropitem`                                  |
| enterdungeon   | enterdungeon <地牢ID>                        | player.enterdungeon       | 仅客户端 | 进入某个地牢                                |                                                 |
| give           | give [uid] <物品ID\|物品名称> [数量] [等级] [精炼等级]  | player.give      | 均可使用 | 给予指定玩家一定数量及等级的物品 (精炼等级仅适用于武器)  | `g` `item` `giveitem`                  |
| givechar       | givechar \<uid> <角色ID> [等级]               | player.givechar           | 均可使用 | 给予指定玩家对应角色                       | givec                                           |
| giveart        | giveart [uid] \<圣遗物ID> \<主属性ID> [\<副属性ID>[,<次数>]]... [等级] | player.giveart            | 均可使用 | 给予玩家指定属性的圣遗物                   | gart                                           |
| giveall        | giveall [uid] [数量]                         | player.giveall            | 均可使用 | 给予指定玩家全部物品                       | givea                                           |
| godmode        | godmode [uid]                                | player.godmode            | 仅客户端 | 保护你不受到任何伤害(依然会被击退)         |                                                 |
| heal           | heal                                         | player.heal               | 仅客户端 | 治疗队伍中所有角色                         | h                                               |
| help           | help [命令]                                  |                           | 均可使用 | 显示帮助或展示指定命令的帮助               |                                                 |
| join | join [多个角色id] | player.join | 仅客户端 | 强制入队角色，跟config.json中的avatarLimits有关（跟队内角色数量上限有关）。用法：`join 10000021 10000022` | |
| kick           | kick \<uid>                                   | server.kick               | 均可使用 | 从服务器中踢出指定玩家 (WIP)               | k                                               |
| killall        | killall [uid] [场景ID]                       | server.killall            | 均可使用 | 杀死指定玩家世界中所在或指定场景的全部生物 |                                                 |
| list           | list                                         |                           | 均可使用 | 列出在线玩家                               |                                                 |
| permission     | permission <add\|remove> <UID> <权限节点> | *                         | 均可使用 | 添加或移除玩家的权限                       |                                                 |
| position       | position                                     |                           | 仅客户端 | 获取当前坐标                               | pos                                             |
| remove | remove [多个角色在队伍中的序号] | player.remove | 仅客户端 | 强制将某个角色从当前队伍中移除。例如`remove 1 2`表示将1号和2号角色移除 |  |
| reload         | reload                                       | server.reload             | 均可使用 | 重载服务器配置                             |                                                 |
| resetconst     | resetconst [all]                             | player.resetconstellation | 仅客户端 | 重置当前角色的命座,重新登录即可生效        | resetconstellation                              |
| restart        | restart                                      |                           | 均可使用 | 重启服务端                                 |                                                 |
| say            | say \<uid> <消息>                             | server.sendmessage        | 均可使用 | 作为服务器发送消息给玩家                   | `sendservmsg` `sendservermessage` `sendmessage` |
| setfetterlevel | setfetterlevel <好感等级>                    | player.setfetterlevel     | 仅客户端 | 设置当前角色的好感等级                     | `setfetterlvl` `setfriendship`                  |
| setstats       | setstats <属性> <数值>                       | player.setstats           | 仅客户端 | 直接修改当前角色的面板                     | stats                                           |
| setworldlevel  | setworldlevel <世界等级>                     | player.setworldlevel      | 仅客户端 | 设置世界等级(重新登录即可生效)             | setworldlvl                                     |
| spawn          | spawn <实体ID> [数量] [等级]                  | server.spawn              | 仅客户端 | 在你周围生成实体                           |                                                 |
| stop           | stop                                         | server.stop               | 均可使用 | 停止服务器                                 |                                                 |
| talent         | talent <天赋ID> <等级>                       | player.settalent          | 仅客户端 | 设置当前角色的天赋等级                     |                                                 |
| teleport       | teleport [@playerUid] \<x> \<y> \<z> [sceneId] | player.teleport           | 均可使用 | 传送玩家到指定坐标                         | tp                                              |
| tpall          |                                                   | player.tpall              | 仅客户端  | 传送多人世界中所有的玩家到自身地点         |                                                 |
| unlocktower    |                               | player.tower                          | 仅客户端  | 解锁深渊全部层            | ut                                                                                                                              |
| weather        | weather <天气ID> <气候ID>                    | player.weather            | 仅客户端 | 改变天气                                   | w                                               |
