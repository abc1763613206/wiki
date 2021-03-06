# Changelog

喵窝的更新记录。

!> **此页尚需完善。**因原 Wiki 记录遗失，且维护者精力有限，本页或未记录所有事件。

!> 除管理组公告、服务器重大变动之外，其余内容会逐步迁移至[喵窝历史事件](misc/history/events.md)。<br>关于「无尽地狱世界」本体的更新记录，请见 [Infinite Infernal](inf/index#历史) 页面。

## 2021
### 2021-3-3 Mod 服务器运营始动

- 在简单筹划之后，管理组开始试水 Mod 服务器，并[公之于众](https://bbs.nyaa.cat/d/1826-nyaacat-flourish-moment-202133-alpha)。  
该服务器挂靠于 `hana`，详情见[服务器列表](wiki/server-network#hana)。
- 服务器前端由 Waterfall 更换为 Velocity。
  - 该变动导致 `/glist` 命令不再可用。

## 2020
### 2020-11-24 Minecraft 1.16.4
- 喵窝主服务器**升级至 1.16.4 版本。**
  - PvP、NFS 等子服务器也基本已升级。UBW 等非公开服务器尚未跟进。
  - 三个非原版维度 `EpicWorld` `EpicNether` `EpicEnd` 再度被重置。
- **经济系统大改：**
  - 经济系统基础插件——HamsterEcoHelper 被重构，其中多个命令用法发生改变，并增加了 `/h` 命令以替代 `/heh`（后者仍可用）。[详见](space/plugins/hamsterecohelper)
  - 现在开设商店木牌需通过命令，而非编辑告示牌。
  - 新增展示框商店，可以展示店内随机物品，并允许玩家直接购买展示框中的物品（一次购买一个）。
  - 天喵商城费率上调：
    + 上架手续费 39 → 100 节
    + 消费税 8% → 10%
  - 天喵商城托管费用将进行调整，目前暂时免费。请密切关注管理组的通知。
  - ~~现在商店（含天喵商城）不再优先展示最近上架的物品了。~~<sup>（已恢复）</sup>
  - 商店搜索结果中不再显示商店木牌坐标。
- **部分细节变更**<sup>（待完善）</sup>：
  - NyaaUtils 展示框保护功能被重写，利用了原版新增的 `Fixed` 属性。
  - 由于 API 限制，**旧版动力燃料胶囊和经验瓶全部失效。**请等待管理组的补偿方案。
  - 聊天新增 **RGB 彩色文本**支持，支持 HTML 表记的颜色代码，如 `&#66ccff好喝的水`。<br>11 月 29 日，支持范围扩展到**自定义前后缀、告示牌及物品重命名**（后两者均需要通过 NyaaUtils 设置才可生效）。
  - 铁砧不再会清除物品名称中原有的多彩样式。
  - 暂时离开（AFK）状态提醒由中文变为英文。
  - ~~告示牌不再支持多彩样式，即便是通过 `/nu se sign` 编辑的。~~<sup>（已修复）</sup>

### 2020-09-04 服务器物理架构更新
- 喵窝主服务器迁移至一台新机器，采用了 Core i9-9900K CPU。
- 活动专用服务器 `act` 也迁移至另一新机器，采用了 Core i5-10600K CPU。
- PvP、NFS、美羽实验室迁移到了主服务器原先的平台上。该平台由 Xeon E3-1280 v5 CPU 驱动。
- [Terraria 游戏服务器](terraria/server) 迁移到了活动专用服务器原先的，基于 Xeon E3-1271 v3 CPU 的平台上。

### 2020-07-18 权限表更新
- 喵窝主服务器进行了权限表更新。  
玩家发现的变化：
  * 玩家不再拥有默认前缀 `[喵]`。
  * **所有玩家的自定义前后缀均被重置**，玩家需要重新进行设置。
  * `/help`、`/mvlist` 命令不再可用。
  * `/home` 命令支持补全功能了。
  * 玩家**不再被允许欠债**。
  * 玩家的私人传送点数量上限 6 → 2。  
各玩家超过 2 个传送点的原有设置不受影响，但必须在删除多余的传送点以后才能设置新的传送点。
  * 玩家在天喵商城的占用槽位上限 12 → 6。
  * 在告示牌编辑界面，不再能使用样式码。<sup>（请以 `/nu se sign` 替代）</sup>
  * 传送冷却时间提升至 10 秒。
- 如果发现有任何权限异常的情况，请直接与管理组联系。
- 领域提示文本得到了大幅简化；玩家村落会直接在副标题显示所有者。

### 2020-03-20 实物货币更新
- 多种中间兑换物发生了变化：
  + 「一元大钱」、「喵爪银币」即日起**发行新版**，材质和原型均已更换。「喵爪银币」的**消失诅咒附魔被删除**~~，同时解决了易于被误食的问题~~。
  + 「一两银票」**被「一元钞票」取代**。
  + **新增中间兑换物「一张银行卡」**，可用 64 个「一元钞票」兑换。
  + 喵窝主世界的相关 NPC 也已更新，改为需要上述新版物品。
  + 可以在 `inf` 世界各大城镇的 ATM **自助更换**旧版物品。
- 「通用纳米子弹」即日起**发行新版**，可以在月耀城的**火狐弹药库**自助更换旧版物品；已经装在「子弹袋」的子弹则无需处理。


### 2020-03-12 服务器资源包上线
- 通过资源包，道具的材质开始可以定制了。
  + 目前已知覆盖了其它资源包的 **木制工具、木棍、弓、弩、纸、铁粒、金粒、羽毛、火把等**材质。
  + <span class="nw-spoiler">于是我们的 MC 世界开始《泰拉瑞亚》化了</span>
- 所有玩家自此日起，将被要求使用服务器资源包。~~由于某些缘故，下载过程时有卡顿，期间无法控制人物。开发组已给出[临时解决方案](https://bbs.nyaa.cat/d/1574)。~~<sup>（13日中午起，资源包改从大陆节点分发，下载表现趋于正常）</sup>
- 插件Resource-pack Over The Air [(ROTA)](https://github.com/NyaaCat/ROTA)启用，允许在不退出服务器的情况下更新资源包。
  + 当服务端资源包更新后，将向玩家推送更新提示。
  + 玩家可以用 `/rota accept`强制更新；或者`/rota ignore`忽略更新提醒。


### 2020-03-02 服务器设定小改
- 性能问题基本缓解之后，2日晚间，游戏规则 `maxEntityCramming` 恢复为 24。
- 1日，经济系统变更：
  + PTT 签到奖励大幅上调。先前，`daily` `eco-up` `week` `activator`奖励上限分别为 45、1024、10240、25600，此次分别上调至 450、2048、15000、80000 节操。
    * 只有`month`被小幅下调了（20480 → 20000）。
    * 「樱花辦」物品 `Quest_Serrakura` 不再发放。
  + 高级装备回收服务开放。
  + 搬迁服务已被确认下线。
  + **商店木牌**数目上限从 12 下调至 8。
- 主世界边境范围由圆形（半径 15360 格）改为**正方形**（边长 30720 格）。

### 2020-02-15 Minecraft 1.15.2
服务器主体升级至 1.15.2 版本。
- 为 `inf` 维度恢复了「死亡箱」，以保护掉落物。
- RPGItem 插件增加了新特性。
- 修复了 InfiniteInfernal 插件的若干 bug。
- **樱华町**属地扩大了超过三倍。原属地范围为 (-84, 12) 至 (547, 481)。
- 像素画粘贴服务开放。

### 2020-01 黑化世界回归 & 若干小更新
- 据多人报告，NyaaUtils 附魔命令不再可用。
  + 所有（在旧版产生的）超原版附魔书几乎丧失价值。
  + 基于 `Inf` 世界附魔台的附魔功能，取代了该指令。若干新型附魔书（称“魔法书”或「贤者の石」）出现，可在新装备上使用。
- 31 日，自定义昵称命令 `/nick` 开始支持非 ASCII 字符。~~颜文字使用可能~~
- 29 日，出于性能考虑，游戏规则 `maxEntityCramming` （生物可挤压数）[调降至 4](https://github.com/NyaaCat/wiki/commit/1e7cbac5ad5000c8ff5821156a8ec6f13584ea72)。
  + 高密度养殖场受影响较大。
  + 有玩家报告，兔圈及蜜蜂机器受损严重。因为一些特性，兔子、蜜蜂偏好于挤在同一角落/花，5 只以上的种群很快出现死亡。


- 27 日，子服务器 *Infinite Infernal* `inf` 关闭。
- 取而代之的是，隶属于主服务器的同名**维度** `inf`。
  + 当日，地形（含月耀城）被原样迁移，其它内容暂缺。有玩家在此发现了上古时期（2016年重建前）的阿库亚斯地图。
  + 次日，**黑化怪物回归**。
  + 此后数日，各种武器装备陆续复刻。自此，“去 RPG 化”进程终止。
  + 2 月 6 日，作为*Infinite Infernal* 2.2 版本[正式开放](https://bbs.nyaa.cat/d/1521-infinite-infernal-v2-2 "Infinite Infernal v2.2 开放公告")。
  + 因其带来的海量“肝黑”需求，加上版本升级的debuff，服务器压力甚巨。~~据粗略观察，当十人以上同时“肝黑”，主世界生物（除怪物外）行动会大幅放缓；甚至每秒随机刻数（TPS）会被削减。~~

## 2019
### 2019-12-30 Minecraft 1.15.1
服务器主体升级至 1.15.1 版本（子服务器 `inf` 除外）。  
**EpicWorld、二号下界、二号末地维度被重置**，其余不变。

### 2019-12-1 聚落群组计划
- 管理组成员*凤凰卷* [建议各聚落成立居委会](https://bbs.nyaa.cat/d/1497)，以便内部沟通、接纳新进居民。
- 当日有 13 个聚落响应倡议，成立居委会12个。

### 2019-12 随机宝箱
- 现在「万华街」多处角落放置了固定宝箱，每隔一定时间刷新战利品。已知其内容选自普通**地牢**的战利品表。
- 现在 EpicWorld 维度的海边藏宝箱，**清空后**隔一定时间刷新战利品。

### 2019-10-？ 幻翼临时禁制令 & 细微变动
- 通过设置于大神殿某处的命令方块，一切幻翼生成后即消灭。
  + 据悉，其为管理组某成员投放；后者还透露，其未指定作用范围，且所在区块强制加载——也即**整个主世界**皆实时禁止幻翼存在。他指出，“等装备的 NPC 普及了就关掉了”。
  + 当月 27 日，命令方块被撤下。幻翼不再被限制。
- 现在「樱华神树」树冠下，会随机落下粉色粒子。
- 现在 `brainhole` 维度永久和平了。

### 2019-10 十月更新
*相关[公告帖](https://bbs.nyaa.cat/d/1478-2019)*  
<span class="nw-spoiler">一句话：不忘初心，返璞归真</span>

- [游戏规则](wiki/rules.md) 更新
  + **建筑要求**简化：
    * 公共交通用建筑，须有底座、桥墩（对于桥梁）、照明、防护等合理结构。
    * 建筑（公共交通以外）的硬性要求，仅保留「禁止“擎天柱”、“豆腐块”存在」「禁止建设测试用建筑」。  
    其余要求将仅作建议/指导。
    * 自动化生产装置本身不限制，但应选择于「科技特区」、地下或专用建筑内部署。
    * 如聚落内有建筑规划及风格要求，应遵守。
- **城市规划更新**
  + 取消「主城」概念，各主城（除樱华町外）更名：
    * 东方主城 → **阿库亚斯**
    * 南方主城 → **浪花町**
    * 西方主城 → **柚子小镇**
    * 北方主城 → **北风城**
    * *（※各地相关标识将在随后陆续跟进修改。）*
    * *（注意： 将出生点设为以上主城者，需重新选择出生点，否则`/spawn`将回到位于`(0,0)`的密闭洞穴中。）*
  + [樱华町](nyaa/realms/sakurakacho.md)扩建，设置自建区。
  + 建立村落（景观区）不再要求常驻人口及规划内容。新村落在[城镇村落列表](nyaa/realms.md)登记后，即视为有效。
- **经济规则调整**
  + ~变更出生点~ 村落间传送命令`/town select` 之费用，降至 45 节操/次。
- **维度功能调整**
  + 脑洞世界 `brainhole` 保留，作为像素画专用托管区域。其余内容转移至子服务器 `miu`（美羽实验室）。
- **内容调整**
  + RPGItem即将适配新版：
    * 大部分原基于RPGItem的**道具、武器装备**不再恢复功能。
    * 然而，部分**实用道具**仍将~恢复~ 重制。
    * 后续将添加新型道具（如玩具、工具）。相应地，会新设一些NPC，以便兑换。
    * 22日起[征集新型道具之灵感](https://bbs.nyaa.cat/d/1482)。

### 2019-09-20 Minecraft 1.14.4
- 服务器主体升级至1.14.4版本。以下服务器除外：
  + 因相关插件有待跟进，子服务器`inf`暂时停留于1.13.2版本。
  + 子服务器`Freebuild`关闭。
- 主服务器三个非原版维度`EpicWorld` `EpicNether` `EpicEnd`同步重置。
- CE（CustomEnchantment）插件移除，相关附魔不再有效。
- RPGItem、Capcat（即传送牌）与NPC暂停服务。其中：
  + RPGItem相关插件仍在为升级准备；<sup>*（10月26日起已恢复）*</sup>
  + **移除所有NPC。**  
10月中旬起，可重新放置商店NPC；其余NPC陆续添加。
  + 因原告示牌升级为“橡木告示牌”，Capcat需跟进更新相关逻辑。<sup>*（9月21日修复）*</sup>
- 高级玩家（Advanced）用户组取消，并入玩家（Player）组。
  + 原Advanced权限下放，如木牌商店空间额度。详见《经济设定》。
- HEH（HamsterEcoHelper）增加若干短命令，以便交易顺畅。
- 主服务器备份方式完全改为「增量备份」。  
因此，玩家不会再收到以下定时备份的消息：

```
[公告] Time now 2019/09/20 Sun 18:00 CST
[公告] 正在备份服务器喵~可能会有点卡喵~

[公告] 备份成功了喵~撒花~
```

### 2019-08-17 → 08-30 the *REAL* Aquatic Update
- 主世界水域“升级”至1.13+版本风格。包括水底方块、冰山、生态群系等。
- 期间，建立一个与主世界使用相同种子的镜像世界；对比两个世界相应水域的海拔Y=63及以下方块，在主世界是水方块、水流的，替换为镜像世界对应的方块。
- 以下为令人惊喜的成果：
  + 东城海星城正下方、小鱼塘以西海面，猹湾以南海面，皆发现珊瑚群。
  + QQ村港湾以西，海面上冒出大量冰山。为已知距离樱华町最近的冰山群。
- 过程中出现了一些副作用：
  + 由于未采取“重生成”方式，除水以外的一切皆予保留。你可以在新海床下发现曾经遍布旧海底的砂砾层。
  + 海床下依靠水工作的人工装置（守卫者渔场、自动化瓜菜生产装置等）遭到大面积破坏。水几乎为岩石取代，鱼类、瓜果等无法输送。
  + 世界多地出现怪异海滩、海岛、沉船，其在海平面以上本应出现的新方块被削去。
    * 冰山群因被单独处理，而免于削顶。
  + ~~所有新出现的海泡菜未自动“开灯”，需人工干预。~~

### 2019-07-17 NyaaWiki 架构变更
- 由 BookStackApp 迁移至 [Docsify](https://docsify.js.org)。
  + 因无任何迁移工具支持，所有文档均须以 Markdown 语言重写；
  + 现知识库基于 [GitHub 仓库](https://github.com/NyaaCat/wiki)；
  + 因此，编辑者需掌握基本的 Git 操作与 Markdown 语法。详见 [参与贡献 Wiki](wiki/contribute.md)。
- 原 BookStackApp 知识库于 7 月 21 日下线，数据不再保留。

### 2019-05 服务器设定变更
- [经济规则调整](https://bbs.nyaa.cat/d/1410-20190514)
  + **死亡惩罚取消。**但保留“死亡掉落”。
  + Capcat 传送木牌最低传送费用降低为 1 节。
  + 改变出生点 `/town select` 费用降低为 450 节每次。
  + 前后缀更改费用降低为 42 节
  + `/sethome` 的费用范围变为 45 - 450，每 100 格降低 20，其他不变。
  + `/home` 基础费用变为 9，单位 100 格增量改为 1，其他不变。
  + `/back` 基础费用变为 9，单位 100 格增量改为 1，其他不变。
- **维度调整**
  + 新增 资源末地 `EpicEnd`；
  + 新增 资源下界 `EpicNether`；
  + 同步恢复使用跨维度传送命令 `/mvtp` `/goto`。
- NyaaUtils 经验存储瓶[更新](https://bbs.nyaa.cat/d/1408-20190514-nyaautils)
  + 现在有存储经验的*附魔之瓶* 被砸碎后，所存经验会分散到经验球中。
- 服务器登录地址[变更](https://bbs.nyaa.cat/d/1409)。

### 2019-03-04 出生点更新
- 现在 `/espawn` 目的地重归大神殿。

### 2019-03-02 白名单申请方式变更
- 即日起开放申请，不再要求是否有邀请人。
  + 不过，有邀请人可**增加**些许的过审可能性。
- 开放“迎新群”供申请人初步了解社区情况，并接受审视。
- 移除对 Google+ 个人主页的要求（因其即将停止服务）。

### 2019-02-01 用户组改革
- 现仅保留三个用户组（含“管理组”）。以下用户组撤销，不再保留相应权限：
  + 建筑师（Builder）
  + 创造组（Creator）
  + 城主（Moderator）
- 原隶属于上述用户组的玩家，按活跃度<sup>*（需要验证）*</sup>划归“高级玩家”或“玩家”组。

- - -

## 更早年份的更新

* [2018](changelogs/2018.md) :sweat_drops:
* [2017](changelogs/2017.md) :rainbow:
* [2016](changelogs/2016.md) :cat:
* [2015](changelogs/2015.md) :heart:
* [2014](changelogs/2014.md) :cyclone:
