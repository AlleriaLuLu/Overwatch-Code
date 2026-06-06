变量
{
	全局:
		0: HeroRoster
		1: LavaLocations
		2: LavaRadius
		3: CheckpointLocations
		4: ZoneLocations
		5: ZoneText
		6: PortalLocations
		7: PortalDestinations
		8: PortalUnlockDefaults
		9: PortalText
		10: HeroLocations
		11: UnlockLocations
		12: SpeedrunLocation
		13: SpecialPortalLocation
		14: SpecialPortalRadius
		15: MaxObjectIndex
		16: LoadingObjectIndex
		17: LoadingElementIndex
		18: MaxZones
		19: MaxHeroes
		20: SpawnFaceDirection
		21: DJlocation
		22: weihelocation
		25: MatchTime
		26: EasterEggLocations
		27: EasterEggHeroes
		28: EasterEggMaxCount
		29: ExtraHero
		30: ExtraHeroLocation
		31: Point
		32: LavaLocations_1
		33: LavaLocations_2
		34: LavaLocations_3
		35: LavaRadius_1
		36: LavaRadius_2
		37: LavaRadius_3
		38: LavaLoop
		39: ExtraHeroSwapLocation
		41: EffectSwitchLocation
		42: chat
		43: maomao
		44: tiaozhanzhe
		45: zhongjuloction
		64: chatLocation
		65: ExtraHeroEggLocation
		66: playname
		67: playdata
		68: fileText
		70: SpecialPortalHero
		71: no_pass
		73: aishi_tanqiu
		74: yuanshigod
		88: settingLocation
		89: EffectHUDText
		90: cangsuLocation
		91: cangsuRadius
		99: blacklist
		100: Hero_
		101: Type_
		102: Location
		103: Color_
		104: Index
		105: Hero_Used
		106: MaxSkillsCount
		107: tiequanLocation
		108: heiyingLocation
		109: administrator
		111: map_text
		113: texiao12
		114: jingsu_text
		116: cheng_hao_Location
		125: debug
		126: SpecialHeroes
		127: Arr

	玩家:
		0: Victory
		1: TutorialMode
		2: ZonesReached
		3: HeroesUnlocked
		4: ZoneCount
		5: HeroCount
		6: FoundSecretHero
		7: Respawn
		8: AlternativeRespawn
		9: SpeedRunMode
		10: Timer
		11: Deaths
		12: MyHUD
		13: CanDie
		14: LoopCounter
		15: PortalUnlocked
		16: data
		17: weihezhe
		21: IsInAnimation
		26: EasterEggsFound
		27: EasterEggCount
		28: ExtraHeroLoop
		29: Destination
		32: Switch
		33: Cam
		34: Effect_Choice
		35: Effect__
		36: Watch
		37: sanduan
		65: chatstart
		66: chatcount
		67: daxiao
		68: chat1count
		69: fileIndex
		70: file
		87: settingCount
		88: settingIndex
		89: setting
		90: shenying
		92: quiet
		93: er_wai_jing_su
		94: jingsu_Sel
		95: cheng_hao
		96: lang
		100: Abi_1
		101: Abi_2
		102: R_Click
		103: Hero
		104: Index
		105: SkillsFound
		107: play_date
		108: play
		109: playset
		110: played
		111: pengzhuang
		112: tiequanlevel
		113: only_maker
		115: tiaozhanpanding
		116: mianban
		117: maomao
		118: tiaozhanzhe
		119: zhongju
}

子程序
{
	0: ResetProgress
	1: UpdateCount
	2: ResetCoolDown
	3: Camera
	4: Creat_Effect
	67: tiequanskill
	100: Skill_SetUp
	101: Skill_Init
}

规则("Initialize global variables")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		禁用 全局.debug = 真;
	}
}

规则("界面文本")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		If(全局.debug != 真);
			禁用查看器录制;
		End;
		关闭游戏预设计分模式;
		关闭游戏预设完成条件;
		"Center HUD"
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.Victory == 真 && 当前数组元素.SpeedRunMode == 假 && 当前数组元素.only_maker[9] == 0), 自定义字符串("END"), 空, 空, 顶部,
			0, 颜色(紫色), 空, 空, 可见和字符串, 默认可见度);
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.only_maker[9] == 0), 本地玩家.TutorialMode ? 自定义字符串(
			"                     教学模式\r\n{0}读点 {1}存点  F互动  {2}提示（长按）", 输入绑定字符串(按钮(终极技能)), 输入绑定字符串(按钮(装填)), 输入绑定字符串(按钮(近身攻击))) : 自定义字符串(
			"长按R进入教学模式"), 空, 空, 顶部, 3, 颜色(黄色), 颜色(白色), 颜色(黄色), 可见和字符串, 默认可见度);
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.only_maker[9] == 0), 空, 空, 本地玩家.Switch ? 自定义字符串("长 第三人称：{0}+{1}\r\n按 开关观战：{2}", 输入绑定字符串(按钮(蹲下)),
			输入绑定字符串(按钮(跳跃)), 输入绑定字符串(按钮(技能2))) : 自定义字符串("长按:  第三人称：{0}  开关观战：{1}", 输入绑定字符串(按钮(互动)), 输入绑定字符串(按钮(技能2))), 右边, 1, 颜色(绿色), 颜色(
			绿色), 颜色(绿色), 可见和字符串, 默认可见度);
		等待(1, 无视条件);
		"Left-Side HUD"
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.only_maker[9] == 0), 空, 空, 自定义字符串("按住{0}重置游戏", 输入绑定字符串(按钮(终极技能))), 左边, 0, 空, 空, 颜色(黄色), 可见和字符串,
			默认可见度);
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.only_maker[9] == 0 && 当前数组元素.chat1count < 5), 自定义字符串("游戏进度:"), 空, 空, 左边, 1, 颜色(紫色), 空, 空, 可见和字符串,
			默认可见度);
		等待(1, 无视条件);
		"Right-Side HUD"
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.only_maker[9] == 0), 自定义字符串("代码: rkjtj（雷姆原版）\r\n         GGJ6T（简化版）"), 空, 自定义字符串(
			"作者:城维大队\r\nQQ 群：769015485\r\n“卡关请入群求救”"), 右边, 0, 颜色(蓝色), 颜色(蓝色), 颜色(白色), 可见和字符串, 默认可见度);
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.only_maker[9] == 0), 空, 空, 自定义字符串("||        B站教程：“漓江塔简化版”         ||"), 顶部, -1, 颜色(白色), 颜色(白色),
			颜色(橙色), 可见和字符串, 默认可见度);
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.only_maker[9] == 0 && 当前数组元素.chat1count < 5), 空, 空, 本地玩家.Victory ? 自定义字符串("{0}\r\n{1}", 自定义字符串(
			"复活节彩蛋\r\n{0} / 5", 本地玩家.EasterEggCount), 自定义字符串("找到其他英雄\r\n{0} / 5", 数量(已过滤的数组(本地玩家.FoundSecretHero, 当前数组元素)))) : 自定义字符串(""),
			左边, 3, 空, 空, 颜色(水绿色), 可见和字符串, 始终不可见);
	}
}

规则("玩家设置")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	动作
	{
		事件玩家.lang = 数组值的索引(数组(自定义字符串("Practice Range"), 自定义字符串("训练靶场")), 自定义字符串("{0}", 地图(训练靶场)));
		If(事件玩家.lang < 0);
			"默认语言：中文"
			事件玩家.lang = 1;
		End;
		"初始化称号变量"
		事件玩家.cheng_hao[0] = 0;
		事件玩家.cheng_hao[1] = 数组(数组(自定义字符串("No title or no title used"), 自定义字符串("无称号或不使用称号 "))[事件玩家.lang]);
		事件玩家.cheng_hao[2] = 数组(颜色(白色));
		事件玩家.data[7] = 随机实数(0.600, 1);
		事件玩家.play = 空数组;
		事件玩家.CanDie = 假;
		开始强制玩家选择英雄(事件玩家, 首个(全局.HeroRoster));
		设置最大复生时间(事件玩家, 9999);
		事件玩家.shenying = 1;
		开始修改英雄语音(事件玩家, 事件玩家.shenying, 真);
		启用死亡回放时目标的HUD(事件玩家);
		取消与玩家的移动碰撞(事件玩家);
		事件玩家.SpeedRunMode = 假;
		事件玩家.quiet = 假;
		事件玩家.only_maker[6] = 事件玩家.quiet;
		设置造成伤害(事件玩家, 0.100);
		调用子程序(ResetProgress);
		等待(0.300, 无视条件);
		创建HUD文本(已过滤的数组(事件玩家, !事件玩家.IsInAnimation && 当前数组元素.only_maker[9] == 0 && 当前数组元素.chat1count < 5), 空, 空, 自定义字符串(
			"解锁区域\r\n{0}\r\n解锁英雄\r\n{1}\r\n解锁技能\r\n{2}", 自定义字符串("{0} / {1}", 事件玩家.ZoneCount, 全局.MaxZones), 自定义字符串("{0} / {1}",
			事件玩家.HeroCount, 全局.MaxHeroes), 自定义字符串("{0} / {1}", 数量(已过滤的数组(事件玩家.SkillsFound, 当前数组元素)), 全局.MaxSkillsCount)), 左边, 2, 空, 空, 颜色(
			蓝色), 可见和字符串, 默认可见度);
		禁用 设置目标点描述(事件玩家, 自定义字符串("B站搜索“漓江塔简化版”"), 字符串);
		"称号"
		创建地图文本(事件玩家.cheng_hao[0] > 0 ? 所有玩家(所有队伍) : 空数组, 事件玩家.cheng_hao[1][事件玩家.cheng_hao[0]], 事件玩家, 2, 不要截取, 可见，位置，字符串和颜色,
			事件玩家.cheng_hao[2][事件玩家.cheng_hao[0]], 默认可见度);
		创建效果(所有玩家(所有队伍), 有益光环, 颜色(黄色), 矢量(0, 130.790, 190.200), 1, 可见，位置和半径);
		创建地图文本(所有玩家(所有队伍), 自定义字符串("这能上去"), 矢量(0, 130.790, 190.200), 1, 根据表面截取, 可见，位置和字符串, 颜色(白色), 默认可见度);
		事件玩家.CanDie = 真;
		事件玩家.TutorialMode = 真;
		事件玩家.play_date[2] = 空数组;
		事件玩家.play_date[3] = 空数组;
		事件玩家.play_date[5] = 5;
		事件玩家.weihezhe = 0;
		隐藏游戏模式HUD(事件玩家);
	}
}

规则("Global Variable")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.MatchTime = 16200;
		"Lava | Checkpoints | Zones | Portals | Heroes | Unlocks | Speedrun | Bouncepads"
		全局.MaxObjectIndex = 数组(86, 2, 4, 15, 5, 3, 0);
		全局.jingsu_text = 数组(数组(自定义字符串("Racing Mode"), 自定义字符串("竞速模式")), 数组(自定义字符串(" Cripple's race mode"), 自定义字符串("腿瘸模式")), 数组(自定义字符串(
			"  Unstoppable racing mode"), 自定义字符串("炫迈模式")), 数组(自定义字符串("  Blind race mode"), 自定义字符串("盲人模式")));
	}
}

规则("区域数量")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.MaxZones = 4;
		全局.MaxHeroes = 4;
	}
}

规则("初始英雄变量")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"Spawning Hero - Yellow"
		全局.HeroRoster[0] = 英雄(卡西迪);
		"Unlockable Hero 1 - Green"
		全局.HeroRoster[1] = 英雄(布丽吉塔);
		"Unlockable Hero 2 - Blue"
		全局.HeroRoster[2] = 英雄(艾什);
		"Unlockable Hero 3 - Purple"
		全局.HeroRoster[3] = 英雄(源氏);
		"Unlockable Hero 4 - Red"
		全局.HeroRoster[4] = 英雄(卢西奥);
		"SpecialHeroes"
		全局.SpecialHeroes[0] = 全部英雄[8];
	}
}

规则("更换英雄坐标")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.HeroLocations = 数组(矢量(6, 0, -55.800), 矢量(3.500, 0, -55.800), 矢量(1, 0, -55.800), 矢量(-1.500, 0, -55.800), 矢量(-4, 0, -55.800), 矢量(
			39.932, 7.380, -41.168));
	}
}

规则("初始英雄解锁坐标")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"Unlockable Hero 1 - Green"
		全局.UnlockLocations[0] = 矢量(0.976, 3.425, -77.656);
		"Unlockable Hero 2 - Blue"
		全局.UnlockLocations[1] = 矢量(-50.936, 96.580, 132.461);
		"Unlockable Hero 3 - Purple"
		全局.UnlockLocations[2] = 矢量(12.775, 271.529, 327.059);
		"Unlockable Hero 4 - Red"
		全局.UnlockLocations[3] = 矢量(-0.080, 164, 149.890);
	}
}

规则("球位置")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.LavaLocations[0] = 矢量(-59.030, -17.880, -28.380);
		全局.LavaLocations[1] = 矢量(-59.010, -19.070, -16.980);
		全局.LavaLocations[2] = 矢量(-61.710, 2.700, -4.630);
		全局.LavaLocations[3] = 矢量(-46.900, 5.650, -37.250);
		全局.LavaLocations[4] = 矢量(-35, -0.140, -24.740);
		全局.LavaLocations[5] = 矢量(-18.450, 3.200, -21.550);
		全局.LavaLocations[6] = 矢量(-12.130, -15.570, -26.700);
		全局.LavaLocations[7] = 矢量(-40.620, 0.440, -15.800);
		全局.LavaLocations[11] = 矢量(-22.400, -1.050, -55.270);
		全局.LavaLocations[13] = 矢量(-14.690, -6.380, -45.510);
		全局.LavaLocations[14] = 矢量(7.170, 0.010, -11.810);
		全局.LavaLocations[16] = 矢量(21.100, -8.070, -42.500);
		全局.LavaLocations[18] = 矢量(20.420, -26.400, -52.500);
		全局.LavaLocations[20] = 矢量(17.740, -16.270, -28.500);
		全局.LavaLocations[22] = 矢量(28.110, -12.750, -23.160);
		全局.LavaLocations[23] = 矢量(33.450, -0.140, -30.510);
		全局.LavaLocations[26] = 矢量(37.510, 7.530, -46.010);
		全局.LavaLocations[27] = 矢量(66.430, -6.200, -23.330);
		全局.LavaLocations[28] = 矢量(48.890, -3.250, -18);
		全局.LavaLocations[29] = 矢量(24.950, 8.020, -22.790);
		全局.LavaLocations[31] = 矢量(35.750, 101.390, 176.420);
		全局.LavaLocations[32] = 矢量(-14.620, 76.770, 167.930);
		全局.LavaLocations[33] = 矢量(-29.480, 94.050, 176.460);
		全局.LavaLocations[34] = 矢量(-35, 94.690, 156.300);
		全局.LavaLocations[35] = 矢量(-59.690, 60.600, 154.900);
		全局.LavaLocations[36] = 矢量(23.260, 94, 152.300);
		全局.LavaLocations[39] = 矢量(-9.600, 93.800, 124.200);
		全局.LavaLocations[40] = 矢量(12.090, 95, 122);
		全局.LavaLocations[41] = 矢量(-26.060, 94, 142.730);
		全局.LavaLocations[42] = 矢量(-47.100, 99.200, 163.870);
		全局.LavaLocations[43] = 矢量(-48.930, 105.540, 135.780);
		全局.LavaLocations[44] = 矢量(-46.520, 100.740, 149.400);
		全局.LavaLocations[45] = 矢量(-68, 75.700, 139.250);
		全局.LavaLocations[46] = 矢量(-12.300, 92.140, 159);
		全局.LavaLocations[47] = 矢量(5, 85, 170.500);
		全局.LavaLocations[48] = 矢量(26.510, 96.120, 126.670);
		全局.LavaLocations[49] = 矢量(25.180, 98.100, 136.150);
		全局.LavaLocations[50] = 矢量(45.230, 82.100, 152.660);
		全局.LavaLocations[51] = 矢量(69.430, 94.500, 152.190);
		全局.LavaLocations[52] = 矢量(82.580, 60, 148.450);
		全局.LavaLocations[53] = 矢量(79.020, 96.100, 132.070);
		全局.LavaLocations[54] = 矢量(-2.700, 269.430, 274.610);
		全局.LavaLocations[55] = 矢量(-8.300, 281.800, 290.200);
		全局.LavaLocations[56] = 矢量(18.230, 267, 270.420);
		全局.LavaLocations[58] = 矢量(57.580, 269.690, 339.450);
		全局.LavaLocations[59] = 矢量(41.320, 264.080, 344.950);
		全局.LavaLocations[60] = 矢量(33.290, 254, 343.510);
		全局.LavaLocations[61] = 矢量(14.230, 269.950, 319.330);
		全局.LavaLocations[62] = 矢量(41.800, 267, 317.250);
		全局.LavaLocations[63] = 矢量(34.500, 268.650, 328);
		全局.LavaLocations[65] = 矢量(22.180, 254.320, 285.820);
		全局.LavaLocations[66] = 矢量(32, 255.640, 299);
		全局.LavaLocations[67] = 矢量(16.070, 269.700, 297.330);
		全局.LavaLocations[68] = 矢量(1.970, 268.050, 259.600);
		全局.LavaLocations[69] = 矢量(5.750, 281.500, 266.780);
		全局.LavaLocations[70] = 矢量(6.920, 243.110, 278.100);
		全局.LavaLocations[71] = 矢量(4.540, 270, 295.380);
		全局.LavaLocations[72] = 矢量(-8, 270.300, 286.800);
		全局.LavaLocations[73] = 矢量(-6.650, 276.260, 280.250);
		全局.LavaLocations[74] = 矢量(-20.710, 270.830, 270.460);
		全局.LavaLocations[75] = 矢量(-10.950, 271.850, 321.280);
		全局.LavaLocations[76] = 矢量(-0.020, 243.450, 320.310);
		全局.LavaLocations[77] = 矢量(-5.360, 270.270, 304.210);
		全局.LavaLocations[78] = 矢量(-10.160, 263.040, 273.130);
		全局.LavaLocations[80] = 矢量(-24.580, 271.270, 339.020);
		全局.LavaLocations[81] = 矢量(-45.080, 265, 313.700);
		全局.LavaLocations[82] = 矢量(-37.590, 270, 341.720);
		全局.LavaLocations[84] = 矢量(20.080, 269.950, 337.280);
		全局.LavaLocations[85] = 矢量(-28.710, 267, 295.630);
		全局.LavaLocations[86] = 矢量(-4.100, 277.700, 309.200);
		全局.LavaLocations[87] = 矢量(-66.150, 8.620, -45.300);
		全局.LavaLocations[88] = 矢量(-59.470, 9.340, -47.860);
	}
}

规则("球大小")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.LavaRadius[0] = 24.650;
		全局.LavaRadius[1] = 26.900;
		全局.LavaRadius[2] = 5.750;
		全局.LavaRadius[3] = 10.020;
		全局.LavaRadius[4] = 8;
		全局.LavaRadius[5] = 7;
		全局.LavaRadius[6] = 20;
		全局.LavaRadius[7] = 7.320;
		全局.LavaRadius[11] = 5.900;
		全局.LavaRadius[13] = 8.230;
		全局.LavaRadius[14] = 3.050;
		全局.LavaRadius[16] = 10.430;
		全局.LavaRadius[18] = 28.020;
		全局.LavaRadius[20] = 18.950;
		全局.LavaRadius[22] = 13.770;
		全局.LavaRadius[23] = 7.320;
		全局.LavaRadius[26] = 4.470;
		全局.LavaRadius[27] = 18.130;
		全局.LavaRadius[28] = 12.130;
		全局.LavaRadius[29] = 2.830;
		全局.LavaRadius[31] = 18.130;
		全局.LavaRadius[32] = 19.630;
		全局.LavaRadius[33] = 8.820;
		全局.LavaRadius[34] = 9.500;
		全局.LavaRadius[35] = 37.780;
		全局.LavaRadius[36] = 15.500;
		全局.LavaRadius[39] = 10.100;
		全局.LavaRadius[40] = 9.200;
		全局.LavaRadius[41] = 6.950;
		全局.LavaRadius[42] = 2.750;
		全局.LavaRadius[43] = 8;
		全局.LavaRadius[44] = 8.070;
		全局.LavaRadius[45] = 23.380;
		全局.LavaRadius[46] = 8.400;
		全局.LavaRadius[47] = 13;
		全局.LavaRadius[48] = 8.680;
		全局.LavaRadius[49] = 3.050;
		全局.LavaRadius[50] = 17.600;
		全局.LavaRadius[51] = 11.820;
		全局.LavaRadius[52] = 37.050;
		全局.LavaRadius[53] = 4.780;
		全局.LavaRadius[54] = 7.250;
		全局.LavaRadius[55] = 9.230;
		全局.LavaRadius[56] = 6.350;
		全局.LavaRadius[58] = 5.450;
		全局.LavaRadius[59] = 7.470;
		全局.LavaRadius[60] = 18.050;
		全局.LavaRadius[61] = 6.650;
		全局.LavaRadius[62] = 8.200;
		全局.LavaRadius[63] = 8.520;
		全局.LavaRadius[65] = 15.880;
		全局.LavaRadius[66] = 15.270;
		全局.LavaRadius[67] = 2;
		全局.LavaRadius[68] = 10;
		全局.LavaRadius[69] = 7.470;
		全局.LavaRadius[70] = 27.080;
		全局.LavaRadius[71] = 8.980;
		全局.LavaRadius[72] = 7.600;
		全局.LavaRadius[73] = 4.470;
		全局.LavaRadius[74] = 7.630;
		全局.LavaRadius[75] = 3.800;
		全局.LavaRadius[76] = 28.850;
		全局.LavaRadius[77] = 5.450;
		全局.LavaRadius[78] = 8.230;
		全局.LavaRadius[80] = 2;
		全局.LavaRadius[81] = 9.250;
		全局.LavaRadius[82] = 11;
		全局.LavaRadius[84] = 4.850;
		全局.LavaRadius[85] = 11.980;
		全局.LavaRadius[86] = 1.700;
		全局.LavaRadius[87] = 4;
		全局.LavaRadius[88] = 3;
	}
}

规则("区域坐标")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.ZoneLocations = 数组(矢量(-51.364, 6, -5.088), 矢量(1, -1, -60.816), 矢量(0, 94, 183.690), 矢量(49, 265, 330), 矢量(-49, 265, 330));
	}
}

规则("传送门坐标")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.PortalLocations = 数组(矢量(-2.009, 0, -63.956), 矢量(0.990, 0, -64.765), 矢量(3.991, 0, -63.966), 矢量(-2.992, 95, 180.143), 矢量(0.009,
			95, 179.342), 矢量(3.008, 95, 180.148), 矢量(44.441, 266, 329.939), 矢量(45.997, 266, 327.252), 矢量(48.689, 266, 325.702), 矢量(-48.419,
			266, 325.462), 矢量(-45.740, 266, 327.034), 矢量(-44.206, 266, 329.734), 矢量(59.828, 10.572, -8.472), 矢量(18.187, 99.830, 184.241),
			矢量(77.345, 105.450, 117.253), 矢量(13.780, 271.580, 263.758));
	}
}

规则("检查点坐标")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.CheckpointLocations[0] = 矢量(15.972, 0, -17.537);
		全局.CheckpointLocations[1] = 矢量(29.781, 94.851, 136.760);
		全局.CheckpointLocations[2] = 矢量(-0.071, 277.925, 292.723);
	}
}

规则("竞速模式坐标")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.SpeedrunLocation = 矢量(-46.940, 7.300, -4.934);
	}
}

规则("区域文本")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"Spawn - Cannot Edit"
		全局.ZoneText[0] = 空;
		"Zone 1"
		全局.ZoneText[1] = 数组(自定义字符串("开始区域"), 自定义字符串("开始区域"));
		"Zone 2"
		全局.ZoneText[2] = 数组(自定义字符串("夺取区域"), 自定义字符串("夺取区域"));
		"Zone 3"
		全局.ZoneText[3] = 数组(自定义字符串("进攻区域"), 自定义字符串("进攻区域"));
		"Zone 4"
		全局.ZoneText[4] = 数组(自定义字符串("最终区域"), 自定义字符串("最终区域"));
	}
}

规则("传送门文本t")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.PortalText[0] = 全局.ZoneText[2];
		全局.PortalText[1] = 全局.ZoneText[3];
		全局.PortalText[2] = 全局.ZoneText[4];
		全局.PortalText[3] = 全局.ZoneText[1];
		全局.PortalText[4] = 全局.ZoneText[3];
		全局.PortalText[5] = 全局.ZoneText[4];
		全局.PortalText[6] = 全局.ZoneText[1];
		全局.PortalText[7] = 全局.ZoneText[2];
		全局.PortalText[8] = 全局.ZoneText[4];
		全局.PortalText[9] = 全局.ZoneText[1];
		全局.PortalText[10] = 全局.ZoneText[2];
		全局.PortalText[11] = 全局.ZoneText[3];
		全局.PortalText[12] = 数组(自定义字符串("go to Start Area"), 自定义字符串("去夺取区域"));
		全局.PortalText[13] = 数组(自定义字符串("go to Advanced Area"), 自定义字符串("去开始区域"));
		全局.PortalText[14] = 数组(自定义字符串("go to Difficult Area"), 自定义字符串("去进攻区域"));
		全局.PortalText[15] = 数组(自定义字符串("go to END Area"), 自定义字符串("去夺取区域"));
	}
}

规则("传送目的地设置")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.PortalDestinations[0] = 全局.ZoneLocations[2];
		全局.PortalDestinations[1] = 全局.ZoneLocations[3];
		全局.PortalDestinations[2] = 全局.ZoneLocations[4];
		全局.PortalDestinations[3] = 全局.ZoneLocations[1];
		全局.PortalDestinations[4] = 全局.ZoneLocations[3];
		全局.PortalDestinations[5] = 全局.ZoneLocations[4];
		全局.PortalDestinations[6] = 全局.ZoneLocations[1];
		全局.PortalDestinations[7] = 全局.ZoneLocations[2];
		全局.PortalDestinations[8] = 全局.ZoneLocations[4];
		全局.PortalDestinations[9] = 全局.ZoneLocations[1];
		全局.PortalDestinations[10] = 全局.ZoneLocations[2];
		全局.PortalDestinations[11] = 全局.ZoneLocations[3];
		全局.PortalDestinations[12] = 矢量(18.188, 98.330, 184.241);
		全局.PortalDestinations[13] = 矢量(59.828, 9.072, -8.473);
		全局.PortalDestinations[14] = 矢量(13.779, 270.080, 263.757);
		全局.PortalDestinations[15] = 矢量(77.345, 103.950, 117.253);
	}
}

规则("Portal Unlock Defaults")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"True = Usable from Start | False = Locked until destination is reached"
		全局.PortalUnlockDefaults[0] = 假;
		全局.PortalUnlockDefaults[1] = 假;
		全局.PortalUnlockDefaults[2] = 假;
		全局.PortalUnlockDefaults[3] = 假;
		全局.PortalUnlockDefaults[4] = 假;
		全局.PortalUnlockDefaults[5] = 假;
		全局.PortalUnlockDefaults[6] = 假;
		全局.PortalUnlockDefaults[7] = 假;
		全局.PortalUnlockDefaults[8] = 假;
		全局.PortalUnlockDefaults[9] = 假;
		全局.PortalUnlockDefaults[10] = 假;
		全局.PortalUnlockDefaults[11] = 假;
		全局.PortalUnlockDefaults[12] = 真;
		全局.PortalUnlockDefaults[13] = 真;
		全局.PortalUnlockDefaults[14] = 真;
		全局.PortalUnlockDefaults[15] = 真;
	}
}

规则("Spawn Face Direction")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"First time spawn direction"
		全局.SpawnFaceDirection = 矢量(1000, 0, 0);
	}
}

规则("V键指引")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.TutorialMode == 真;
		按钮被按下(事件玩家, 按钮(近身攻击)) == 真;
	}

	动作
	{
		等待(1, 当为“假”时中止);
		If(首个(事件玩家.SkillsFound) == 假);
			小字体信息(事件玩家, 自定义字符串("提示：找到{0}的{1}", 英雄图标字符串(英雄(卡西迪)), 技能图标字符串(英雄(卡西迪), 按钮(技能1))));
		Else If(首个(事件玩家.ZonesReached) == 假);
			小字体信息(事件玩家, 自定义字符串("提示：用{0}去{1}", 英雄图标字符串(首个(全局.HeroRoster)), 全局.ZoneText[1][事件玩家.lang]));
		Else If(事件玩家.SkillsFound[1] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：找到{0}的{1}", 英雄图标字符串(英雄(卡西迪)), 技能图标字符串(英雄(卡西迪), 按钮(技能2))));
		Else If(首个(事件玩家.HeroesUnlocked) == 假);
			小字体信息(事件玩家, 自定义字符串("提示：在{0}上使用{1}找到{2}\r\n{1}它可以提供一个向上的推力", 全局.ZoneText[1][事件玩家.lang], 英雄图标字符串(首个(全局.HeroRoster)), 英雄图标字符串(
				全局.HeroRoster[1])));
		Else If(事件玩家.SkillsFound[2] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：使用{0}找到的{1}", 英雄图标字符串(英雄(布丽吉塔)), 技能图标字符串(英雄(布丽吉塔), 按钮(辅助攻击模式))));
		Else If(事件玩家.ZonesReached[1] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：用{0}去{1}", 英雄图标字符串(全局.HeroRoster[1]), 全局.ZoneText[2][事件玩家.lang]));
		Else If(事件玩家.SkillsFound[3] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：找到{0}的{1}", 英雄图标字符串(英雄(布丽吉塔)), 技能图标字符串(英雄(布丽吉塔), 按钮(技能1))));
		Else If(事件玩家.HeroesUnlocked[1] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：用{0}的{1}找到{2}\r\n{0}有一个类似于后坐力的推力", 英雄图标字符串(全局.HeroRoster[1]), 全局.ZoneText[2][事件玩家.lang], 英雄图标字符串(
				全局.HeroRoster[2])));
		Else If(事件玩家.SkillsFound[4] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：使用{0}找到的{1}", 英雄图标字符串(英雄(艾什)), 技能图标字符串(英雄(艾什), 按钮(技能1))));
		Else If(事件玩家.ZonesReached[2] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：用{0}去{1}", 英雄图标字符串(全局.HeroRoster[2]), 全局.ZoneText[3][事件玩家.lang]));
		Else If(事件玩家.HeroesUnlocked[2] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：在{0}中使用{1}找到{2}", 全局.ZoneText[3][事件玩家.lang], 英雄图标字符串(全局.HeroRoster[2]), 英雄图标字符串(全局.HeroRoster[3])));
		Else If(事件玩家.ZonesReached[3] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：使用{0}快落地按跳使用并刷新二段跳，从而有两个二段跳", 英雄图标字符串(全局.HeroRoster[3]), 全局.ZoneText[4][事件玩家.lang]));
		Else If(事件玩家.SkillsFound[5] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：找到{0}的{1}", 英雄图标字符串(英雄(源氏)), 技能图标字符串(英雄(源氏), 按钮(技能1))));
		Else If(事件玩家.HeroesUnlocked[3] == 假);
			小字体信息(事件玩家, 自定义字符串("提示：在{0}中使用{1}找到{2}", 全局.ZoneText[2][事件玩家.lang], 英雄图标字符串(全局.HeroRoster[3]), 英雄图标字符串(全局.HeroRoster[4])));
		Else If(数量(已过滤的数组(事件玩家.FoundSecretHero, 当前数组元素)) < 5);
			小字体信息(事件玩家, 自定义字符串("提示： 找到所有隐藏的秘密英雄，建议查看B站教学"));
		Else If(事件玩家.EasterEggsFound[5] == 假);
			小字体信息(事件玩家, 自定义字符串("提示： 收集复活节彩蛋找到彩蛋英雄!建议查看B站教学"));
		Else If(事件玩家.chatcount < 5);
			小字体信息(事件玩家, 自定义字符串("提示：搜集额外彩蛋，建议查看B站教学"));
		Else If(事件玩家.chat1count < 5);
			小字体信息(事件玩家, 自定义字符串("提示：搜集额外彩蛋，建议查看B站教学"));
		Else;
			小字体信息(事件玩家, 自定义字符串("提示：结束？这才刚刚开始！"));
		End;
		根据条件中止(事件玩家.Victory);
		事件玩家.data[1] = (事件玩家.data[1] + 1) % 2;
		开始镜头(事件玩家, 射线命中位置(全局.Point[数量(事件玩家.Destination)], 全局.Point[数量(事件玩家.Destination)] - 面朝方向(事件玩家) * 6, 空, 空, 假), 全局.Point[数量(
			事件玩家.Destination)], 60);
		等待直到 (!按钮被按下(事件玩家, 按钮(近身攻击)), 99999);
		停止镜头(事件玩家);
		If(事件玩家.only_maker[5] == 0);
			事件玩家.data[1] = (事件玩家.data[1] + 1) % 2;
		End;
		Else;
		小字体信息(事件玩家, 数组(自定义字符串("You are a blind person, don't look if you can't see."), 自定义字符串("你是一个盲人，看不见就不要看了。"))[本地玩家.lang]);
		End;
		等待(0.750, 无视条件);
	}
}

规则("Loading Data")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		If(全局.LoadingElementIndex > 全局.MaxObjectIndex[全局.LoadingObjectIndex]);
			全局.LoadingObjectIndex += 1;
			全局.LoadingElementIndex = 0;
		End;
		"Load Lava"
		If(全局.LoadingObjectIndex == 0);
			If(全局.LavaLocations[全局.LoadingElementIndex] != 矢量(0, 0, 0) && 全局.LavaLocations[全局.LoadingElementIndex] != 空);
			End;
			等待(0.030, 无视条件);
			全局.LoadingElementIndex += 1;
			循环;
		Else If(全局.LoadingObjectIndex == 1);
			If(全局.CheckpointLocations[全局.LoadingElementIndex] != 矢量(0, 0, 0) && 全局.CheckpointLocations[全局.LoadingElementIndex] != 空);
				创建效果(所有玩家(所有队伍), 光柱, 颜色(灰绿色), 全局.CheckpointLocations[全局.LoadingElementIndex], 1, 可见);
			End;
			等待(0.030, 无视条件);
			全局.LoadingElementIndex += 1;
			循环;
		Else If(全局.LoadingObjectIndex == 2);
			If(全局.ZoneLocations[全局.LoadingElementIndex] != 矢量(0, 0, 0) && 全局.ZoneLocations[全局.LoadingElementIndex] != 空);
				"Zones"
				If(全局.LoadingElementIndex > 0);
					创建地图文本(所有玩家(所有队伍), 全局.ZoneText[单次赋值(全局.LoadingElementIndex)][本地玩家.lang], 全局.ZoneLocations[全局.LoadingElementIndex] + 矢量(0, 3, 0), 3,
						根据表面截取, 可见和字符串, 颜色(白色), 默认可见度);
					等待(0.030, 无视条件);
					创建效果(所有玩家(所有队伍), 光柱, 颜色(绿色), 全局.ZoneLocations[全局.LoadingElementIndex], 2, 可见);
				End;
			End;
			等待(0.030, 无视条件);
			全局.LoadingElementIndex += 1;
			循环;
		Else If(全局.LoadingObjectIndex == 3);
			If(全局.PortalLocations[全局.LoadingElementIndex] != 矢量(0, 0, 0) && 全局.PortalLocations[全局.LoadingElementIndex] != 空);
				创建地图文本(所有玩家(所有队伍), 全局.PortalText[单次赋值(全局.LoadingElementIndex)][本地玩家.lang], 全局.PortalLocations[全局.LoadingElementIndex], 1.500,
					根据表面截取, 可见和字符串, 颜色(白色), 默认可见度);
				等待(0.030, 无视条件);
				创建效果(所有玩家(所有队伍), 有益光环, 颜色(天蓝色), 全局.PortalLocations[全局.LoadingElementIndex], 1, 可见);
			End;
			等待(0.030, 无视条件);
			全局.LoadingElementIndex += 1;
			循环;
		Else If(全局.LoadingObjectIndex == 4);
			If(全局.HeroLocations[全局.LoadingElementIndex] != 矢量(0, 0, 0) && 全局.HeroLocations[全局.LoadingElementIndex] != 空);
				If(全局.LoadingElementIndex <= 4);
					创建地图文本(所有玩家(所有队伍), 英雄图标字符串(全局.HeroRoster[全局.LoadingElementIndex]), 全局.HeroLocations[全局.LoadingElementIndex] + 矢量(0, -0.300, 0), 2,
						根据表面截取, 可见, 颜色(白色), 默认可见度);
				End;
				等待(0.030, 无视条件);
				If(全局.LoadingElementIndex == 0);
					创建效果(所有玩家(所有队伍), 有害光环, 颜色(黄色), 首个(全局.HeroLocations), 1, 可见);
				Else If(全局.LoadingElementIndex == 1);
					创建效果(所有玩家(所有队伍), 有害光环, 颜色(绿色), 全局.HeroLocations[1], 1, 可见);
				Else If(全局.LoadingElementIndex == 2);
					创建效果(所有玩家(所有队伍), 有害光环, 颜色(蓝色), 全局.HeroLocations[2], 1, 可见);
				Else If(全局.LoadingElementIndex == 3);
					创建效果(所有玩家(所有队伍), 有害光环, 颜色(紫色), 全局.HeroLocations[3], 1, 可见);
				Else If(全局.LoadingElementIndex == 4);
					创建效果(所有玩家(所有队伍), 有害光环, 颜色(红色), 全局.HeroLocations[4], 1, 可见);
				End;
			End;
			等待(0.030, 无视条件);
			全局.LoadingElementIndex += 1;
			循环;
		Else If(全局.LoadingObjectIndex == 5);
			If(全局.UnlockLocations[全局.LoadingElementIndex] != 矢量(0, 0, 0) && 全局.UnlockLocations[全局.LoadingElementIndex] != 空);
				创建地图文本(所有玩家(所有队伍), 英雄图标字符串(全局.HeroRoster[全局.LoadingElementIndex + 1]), 全局.UnlockLocations[全局.LoadingElementIndex], 2, 根据表面截取, 可见,
					颜色(白色), 默认可见度);
				等待(0.030, 无视条件);
				If(全局.LoadingElementIndex == 0);
					创建效果(所有玩家(所有队伍), 火花, 颜色(绿色), 首个(全局.UnlockLocations), 1, 可见);
				Else If(全局.LoadingElementIndex == 1);
					创建效果(所有玩家(所有队伍), 火花, 颜色(蓝色), 全局.UnlockLocations[1], 1, 可见);
				Else If(全局.LoadingElementIndex == 2);
					创建效果(所有玩家(所有队伍), 火花, 颜色(紫色), 全局.UnlockLocations[2], 1, 可见);
				Else If(全局.LoadingElementIndex == 3);
					创建效果(所有玩家(所有队伍), 火花, 颜色(红色), 全局.UnlockLocations[3], 1, 可见);
				End;
			End;
			等待(0.030, 无视条件);
			全局.LoadingElementIndex += 1;
			循环;
		Else If(全局.LoadingObjectIndex == 6);
			If(全局.SpeedrunLocation != 矢量(0, 0, 0) && 全局.SpeedrunLocation != 空);
				创建地图文本(所有玩家(所有队伍), 自定义字符串("竞速模式"), 全局.SpeedrunLocation, 1, 根据表面截取, 可见，字符串和颜色, 本地玩家.SpeedRunMode ? 颜色(灰绿色) : 颜色(红色), 默认可见度);
				等待(0.030, 无视条件);
				创建效果(所有玩家(所有队伍), 有益光环, 本地玩家.SpeedRunMode ? 颜色(灰绿色) : 颜色(红色), 全局.SpeedrunLocation, 1, 可见和颜色);
			End;
			等待(0.030, 无视条件);
			全局.LoadingElementIndex += 1;
			循环;
	}
}

规则("Locked Text Effects")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"Portals"
		If(首个(全局.PortalLocations) == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 首个(当前数组元素.PortalUnlocked) == 假), 自定义字符串("已锁定"), 首个(全局.PortalLocations) + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.PortalLocations[1] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[1] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[1] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.PortalLocations[2] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[2] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[2] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		等待(0.510, 无视条件);
		If(全局.PortalLocations[3] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[3] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[3] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.PortalLocations[4] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[4] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[4] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.PortalLocations[5] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[5] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[5] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		等待(0.510, 无视条件);
		If(全局.PortalLocations[6] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[6] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[6] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.PortalLocations[7] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[7] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[7] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.PortalLocations[8] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[8] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[8] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		等待(0.510, 无视条件);
		If(全局.PortalLocations[9] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[9] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[9] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.PortalLocations[10] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[10] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[10] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.PortalLocations[11] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.PortalUnlocked[11] == 假), 自定义字符串("已锁定"), 全局.PortalLocations[11] + 矢量(0, -0.500, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		等待(0.510, 无视条件);
		"Heroes"
		If(全局.HeroLocations[1] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 首个(当前数组元素.HeroesUnlocked) == 假), 自定义字符串("已锁定"), 全局.HeroLocations[1] + 矢量(0, -0.750, 0), 1.250, 根据表面截取,
				可见, 颜色(橙色), 默认可见度);
		End;
		If(全局.HeroLocations[2] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.HeroesUnlocked[1] == 假), 自定义字符串("已锁定"), 全局.HeroLocations[2] + 矢量(0, -0.750, 0), 1.250, 根据表面截取, 可见,
				颜色(橙色), 默认可见度);
		End;
		等待(0.510, 无视条件);
		If(全局.HeroLocations[3] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.HeroesUnlocked[2] == 假), 自定义字符串("已锁定"), 全局.HeroLocations[3] + 矢量(0, -0.750, 0), 1.250, 根据表面截取, 可见,
				颜色(橙色), 默认可见度);
		End;
		If(全局.HeroLocations[4] == 真);
			创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.HeroesUnlocked[3] == 假), 自定义字符串("已锁定"), 全局.HeroLocations[4] + 矢量(0, -0.750, 0), 1.250, 根据表面截取, 可见,
				颜色(橙色), 默认可见度);
	}
}

规则("Lava Death")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		已重生(事件玩家) == 真;
		存活(事件玩家) == 真;
		事件玩家.CanDie == 真;
		所用英雄(事件玩家) != 全局.EasterEggHeroes[5];
		数组包含(全局.ExtraHero, 所用英雄(事件玩家)) == 假;
	}

	动作
	{
		If(对任意为“真”(全局.LavaLocations, 相距距离(所选位置(事件玩家) + 矢量(0, 0.300, 0), 当前数组元素) < 全局.LavaRadius[数组值的索引(全局.LavaLocations, 当前数组元素)]));
			If(数组包含(数组(英雄(死神), 英雄(美), 英雄(莫伊拉)), 所用英雄(事件玩家)) && 正在使用技能 1(事件玩家));
				等待(0.100, 无视条件);
				如条件为“真”则循环;
			End;
			设置玩家生命值(事件玩家, 1);
			If(生命值(事件玩家) == 1);
				If(!具有状态(事件玩家, 无法杀死));
					击杀(事件玩家, 空);
				End;
			End;
		Else;
			设置玩家生命值(事件玩家, 最大生命值(事件玩家) - 1);
		End;
		等待(0.100, 无视条件);
		如条件为“真”则循环;
	}
}

规则("R 存点")
{
	事件
	{
		玩家阵亡;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Watch != 真;
	}

	动作
	{
		If(事件玩家.setting[7] == 1);
			等待(0.400, 无视条件);
			传送(事件玩家, 事件玩家.setting[8] ? 全局.cangsuLocation[事件玩家.setting[8] - 1] : 全局.EffectSwitchLocation);
			等待(0.400, 无视条件);
			复活(事件玩家);
		Else If(事件玩家.data[5] == 1);
			取消主要动作(事件玩家);
			开始强制设置玩家位置(事件玩家, 所选位置(事件玩家), 假);
			等待(0.200, 无视条件);
			停止强制设置玩家位置(事件玩家);
			If(全局.tiequanLocation[事件玩家.tiequanlevel] != 0);
				传送(事件玩家, 全局.tiequanLocation[事件玩家.tiequanlevel]);
			Else;
				传送(事件玩家, 全局.tiequanLocation[事件玩家.tiequanlevel - 1]);
			End;
			等待(0.200, 无视条件);
			复活(事件玩家);
		Else;
			If(事件玩家.Victory == 假);
				事件玩家.Deaths += 1;
			End;
			停止限制阈值(事件玩家);
			等待(0.400, 无视条件);
			传送(事件玩家, 事件玩家.Respawn);
			等待(0.400, 无视条件);
			复活(事件玩家);
			If(事件玩家.jingsu_Sel == 2);
				开始强制设置玩家位置(事件玩家, 所选位置(事件玩家), 假);
			End;
			If(事件玩家.Respawn == 首个(全局.ZoneLocations));
				If(数量(已过滤的数组(事件玩家.HeroesUnlocked, 当前数组元素 == 真)) == 0);
					事件玩家.Timer = 0;
					事件玩家.Deaths = 0;
				End;
			End;
			If(事件玩家.jingsu_Sel == 2);
				等待(0.500, 无视条件);
				开始限制阈值(事件玩家, 1, 1, 0, 0, 0, 1);
				停止强制设置玩家位置(事件玩家);
			End;
		End;
		设置技能冷却(事件玩家, 按钮(主要攻击模式), 0);
		设置技能冷却(事件玩家, 按钮(辅助攻击模式), 0);
		设置技能冷却(事件玩家, 按钮(技能1), 0);
		设置技能冷却(事件玩家, 按钮(技能2), 0);
		设置技能冷却(事件玩家, 按钮(蹲下), 0);
		设置技能冷却(事件玩家, 按钮(跳跃), 0);
		设置技能充能(事件玩家, 按钮(技能1), 3);
	}
}

规则("Checkpoint")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		已重生(事件玩家) == 真;
		事件玩家.CanDie == 真;
		所用英雄(事件玩家) != 全局.EasterEggHeroes[5];
		数组包含(全局.ExtraHero, 所用英雄(事件玩家)) == 假;
		事件玩家.Watch != 真;
	}

	动作
	{
		If(首个(全局.CheckpointLocations) != 矢量(0, 0, 0));
			If(事件玩家.Respawn != 首个(全局.CheckpointLocations) && 相距距离(所选位置(事件玩家), 首个(全局.CheckpointLocations)) <= 1);
				事件玩家.Respawn = 首个(全局.CheckpointLocations);
				事件玩家.AlternativeRespawn = 首个(全局.CheckpointLocations);
				小字体信息(事件玩家, 自定义字符串("Checkpoints！"));
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
			End;
		End;
		If(全局.CheckpointLocations[1] != 矢量(0, 0, 0));
			If(事件玩家.Respawn != 全局.CheckpointLocations[1] && 相距距离(所选位置(事件玩家), 全局.CheckpointLocations[1]) <= 1);
				事件玩家.Respawn = 全局.CheckpointLocations[1];
				事件玩家.AlternativeRespawn = 全局.CheckpointLocations[1];
				小字体信息(事件玩家, 自定义字符串("Checkpoints！"));
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
			End;
		End;
		If(全局.CheckpointLocations[2] != 矢量(0, 0, 0));
			If(事件玩家.Respawn != 全局.CheckpointLocations[2] && 相距距离(所选位置(事件玩家), 全局.CheckpointLocations[2]) <= 1);
				事件玩家.Respawn = 全局.CheckpointLocations[2];
				事件玩家.AlternativeRespawn = 全局.CheckpointLocations[2];
				小字体信息(事件玩家, 自定义字符串("Checkpoints！"));
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
			End;
		End;
		等待(0.100, 无视条件);
		如条件为“真”则循环;
	}
}

规则("Zones")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory != 真;
		事件玩家.ZoneCount < 4;
		已重生(事件玩家) == 真;
		所用英雄(事件玩家) != 全局.EasterEggHeroes[5];
		数组包含(全局.ExtraHero, 所用英雄(事件玩家)) == 假;
		事件玩家.Watch != 真;
	}

	动作
	{
		If(全局.ZoneLocations[1] != 矢量(0, 0, 0));
			If(事件玩家.Respawn != 全局.ZoneLocations[1] && 相距距离(所选位置(事件玩家), 全局.ZoneLocations[1]) <= 2);
				事件玩家.Respawn = 全局.ZoneLocations[1];
				小字体信息(事件玩家, 自定义字符串("Checkpoints！"));
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
				If(首个(事件玩家.ZonesReached) == 假);
					事件玩家.ZonesReached[0] = 真;
					大字体信息(所有玩家(所有队伍), 自定义字符串(" \r\n{0} {1} {2}", 事件玩家, 自定义字符串("Arrived"), 全局.ZoneText[1][本地玩家.lang]));
					调用子程序(UpdateCount);
				End;
			End;
		End;
		If(全局.ZoneLocations[2] != 矢量(0, 0, 0));
			If(事件玩家.Respawn != 全局.ZoneLocations[2] && 相距距离(所选位置(事件玩家), 全局.ZoneLocations[2]) <= 2);
				事件玩家.Respawn = 全局.ZoneLocations[2];
				事件玩家.AlternativeRespawn = 全局.ZoneLocations[2];
				小字体信息(事件玩家, 自定义字符串("Checkpoints！"));
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
				If(事件玩家.ZonesReached[1] == 假);
					事件玩家.ZonesReached[1] = 真;
					大字体信息(所有玩家(所有队伍), 自定义字符串(" \r\n{0} {1} {2}", 事件玩家, 自定义字符串("Arrived"), 全局.ZoneText[2][本地玩家.lang]));
					调用子程序(UpdateCount);
				End;
			End;
		End;
		If(全局.ZoneLocations[3] != 矢量(0, 0, 0));
			If(事件玩家.Respawn != 全局.ZoneLocations[3] && 相距距离(所选位置(事件玩家), 全局.ZoneLocations[3]) <= 2);
				事件玩家.Respawn = 全局.ZoneLocations[3];
				事件玩家.AlternativeRespawn = 全局.ZoneLocations[3];
				小字体信息(事件玩家, 自定义字符串("Checkpoints！"));
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
				If(事件玩家.ZonesReached[2] == 假);
					事件玩家.ZonesReached[2] = 真;
					大字体信息(所有玩家(所有队伍), 自定义字符串(" \r\n{0} {1} {2}", 事件玩家, 自定义字符串("Arrived"), 全局.ZoneText[3][本地玩家.lang]));
					调用子程序(UpdateCount);
				End;
			End;
		End;
		If(全局.ZoneLocations[4] != 矢量(0, 0, 0));
			If(事件玩家.Respawn != 全局.ZoneLocations[4] && 相距距离(所选位置(事件玩家), 全局.ZoneLocations[4]) <= 2);
				事件玩家.Respawn = 全局.ZoneLocations[4];
				事件玩家.AlternativeRespawn = 全局.ZoneLocations[4];
				小字体信息(事件玩家, 自定义字符串("Checkpoints！"));
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
				If(事件玩家.ZonesReached[3] == 假);
					事件玩家.ZonesReached[3] = 真;
					大字体信息(所有玩家(所有队伍), 自定义字符串(" \r\n{0} {1} {2}", 事件玩家, 自定义字符串("Arrived"), 全局.ZoneText[4][本地玩家.lang]));
					调用子程序(UpdateCount);
				End;
			End;
		End;
		等待(0.100, 无视条件);
		如条件为“真”则循环;
	}
}

规则("Hero Swap")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		事件玩家.setting[7] == 0;
		事件玩家.data[5] == 0;
		对任意为“真”(从数组中移除(全局.HeroLocations, 矢量(0, 0, 0)), 相距距离(眼睛位置(事件玩家), 当前数组元素) < 1.500) == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		For 玩家变量(事件玩家, LoopCounter, 0, 全局.MaxObjectIndex[4] + 1, 1);
			If(全局.HeroLocations[事件玩家.LoopCounter] != 矢量(0, 0, 0) && 全局.HeroLocations[事件玩家.LoopCounter] != 0);
				If(事件玩家.HeroesUnlocked[事件玩家.LoopCounter - 1] == 真 || 事件玩家.LoopCounter == 0);
					If(相距距离(眼睛位置(事件玩家), 全局.HeroLocations[事件玩家.LoopCounter]) <= 1.500);
						开始强制玩家选择英雄(事件玩家, 全局.HeroRoster[事件玩家.LoopCounter]);
						事件玩家.Respawn = 全局.ZoneLocations[1];
						If(事件玩家.Respawn == 全局.ZoneLocations[1]);
							事件玩家.AlternativeRespawn = 空;
						End;
						中断;
					End;
				End;
			End;
		End;
		等待(0.250, 无视条件);
	}
}

规则("Hero Swap Tip")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		已重生(事件玩家) == 真;
		对任意为“真”(从数组中移除(全局.HeroLocations, 矢量(0, 0, 0)), 相距距离(眼睛位置(事件玩家), 当前数组元素) < 1.500) == 真;
	}

	动作
	{
		等待(2, 当为“假”时中止);
		小字体信息(事件玩家, 数组(自定义字符串("Press the interaction key [{0}] to switch heroes", 输入绑定字符串(按钮(互动))), 自定义字符串("按[{0}]切换英雄", 输入绑定字符串(按钮(互动))))
			[本地玩家.lang]);
	}
}

规则("英雄解锁")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory != 真;
		已重生(事件玩家) == 真;
		事件玩家.HeroCount < 全局.MaxHeroes;
		所用英雄(事件玩家) != 全局.EasterEggHeroes[5];
		对任意为“真”(从数组中移除(全局.UnlockLocations, 矢量(0, 0, 0)), 相距距离(眼睛位置(事件玩家), 当前数组元素) < 1.500) == 真;
		数组包含(全局.ExtraHero, 所用英雄(事件玩家)) == 假;
		事件玩家.Watch != 真;
	}

	动作
	{
		For 玩家变量(事件玩家, LoopCounter, 0, 全局.MaxObjectIndex[5] + 1, 1);
			If(全局.UnlockLocations[事件玩家.LoopCounter] != 矢量(0, 0, 0) && 全局.UnlockLocations[事件玩家.LoopCounter] != 0);
				If(事件玩家.HeroesUnlocked[事件玩家.LoopCounter] == 假);
					If(相距距离(眼睛位置(事件玩家), 全局.UnlockLocations[事件玩家.LoopCounter]) <= 1.500);
						大字体信息(所有玩家(所有队伍), 自定义字符串(" \r\n{0} {1} {2}", 事件玩家, 自定义字符串("Unlocked"), 英雄图标字符串(全局.HeroRoster[事件玩家.LoopCounter + 1])));
						事件玩家.HeroesUnlocked[事件玩家.LoopCounter] = 真;
						播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
						调用子程序(UpdateCount);
						中断;
					End;
				End;
			End;
		End;
	}
}

规则("传送门交互")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		对任意为“真”(从数组中移除(全局.PortalLocations, 矢量(0, 0, 0)), 相距距离(眼睛位置(事件玩家), 当前数组元素) < 1.500) == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		For 玩家变量(事件玩家, LoopCounter, 0, 全局.MaxObjectIndex[3] + 1, 1);
			If(事件玩家.PortalUnlocked[事件玩家.LoopCounter] == 真);
				If(全局.PortalLocations[事件玩家.LoopCounter] != 矢量(0, 0, 0) && 全局.PortalLocations[事件玩家.LoopCounter] != 0);
					If(全局.PortalDestinations[事件玩家.LoopCounter] != 矢量(0, 0, 0) && 全局.PortalDestinations[事件玩家.LoopCounter] != 0);
						If(相距距离(眼睛位置(事件玩家), 全局.PortalLocations[事件玩家.LoopCounter]) <= 1.500);
							传送(事件玩家, 全局.PortalDestinations[事件玩家.LoopCounter]);
							事件玩家.Respawn = 全局.PortalDestinations[事件玩家.LoopCounter];
							事件玩家.AlternativeRespawn = 全局.PortalDestinations[事件玩家.LoopCounter];
							等待(0.100, 无视条件);
							播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
							小字体信息(事件玩家, 自定义字符串("{0}!", 自定义字符串("Checkpoints")));
							中断;
						End;
					End;
				End;
			End;
		End;
		等待(0.250, 无视条件);
	}
}

规则("传送点解锁")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory != 真;
		所用英雄(事件玩家) != 全局.EasterEggHeroes[5];
		对任意为“真”(从数组中移除(全局.PortalDestinations, 矢量(0, 0, 0)), 相距距离(当前数组元素, 所选位置(事件玩家)) < 2) == 真;
		数组包含(全局.ExtraHero, 所用英雄(事件玩家)) == 假;
		事件玩家.Watch != 真;
	}

	动作
	{
		For 玩家变量(事件玩家, LoopCounter, 0, 全局.MaxObjectIndex[3] + 1, 1);
			If(全局.PortalDestinations[事件玩家.LoopCounter] != 矢量(0, 0, 0) && 全局.PortalDestinations[事件玩家.LoopCounter] != 0);
				If(事件玩家.PortalUnlocked[事件玩家.LoopCounter] == 假);
					If(相距距离(所选位置(事件玩家), 全局.PortalDestinations[事件玩家.LoopCounter]) <= 2);
						事件玩家.PortalUnlocked[事件玩家.LoopCounter] = 真;
					End;
				End;
			End;
		End;
	}
}

规则("Q回点")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(终极技能)) == 真;
		按钮被按下(事件玩家, 按钮(蹲下)) == 假;
		所用英雄(事件玩家) != 全局.EasterEggHeroes[5];
		数组包含(全局.ExtraHero, 所用英雄(事件玩家)) == 假;
		事件玩家.Watch != 真;
	}

	动作
	{
		If(事件玩家.setting[7] == 1);
			If(事件玩家.setting[8] > 6);
				传送(事件玩家, 全局.cangsuLocation[事件玩家.setting[8] - 1]);
			End;
		Else If(事件玩家.data[5] == 1);
			击杀(事件玩家, 空);
		Else;
			If(相距距离(所选位置(事件玩家), 事件玩家.Respawn) > 1);
				传送(事件玩家, 事件玩家.Respawn);
				开始强制设置玩家位置(事件玩家, 所选位置(事件玩家), 假);
				调用子程序(ResetCoolDown);
				停止强制设置玩家位置(事件玩家);
				等待(0.050, 无视条件);
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
			Else;
				If(事件玩家.AlternativeRespawn != 空);
					If(相距距离(所选位置(事件玩家), 事件玩家.AlternativeRespawn) > 1);
						传送(事件玩家, 事件玩家.AlternativeRespawn);
						调用子程序(ResetCoolDown);
						事件玩家.Respawn = 事件玩家.AlternativeRespawn;
					Else;
						If(首个(事件玩家.ZonesReached) == 真);
							传送(事件玩家, 全局.ZoneLocations[1]);
						End;
					End;
				End;
			End;
		End;
		等待(0.250, 无视条件);
	}
}

规则("原版完成判定")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory == 假;
		事件玩家.ZoneCount == 全局.MaxZones;
		事件玩家.HeroCount == 全局.MaxHeroes;
		数量(已过滤的数组(事件玩家.SkillsFound, 当前数组元素)) == 全局.MaxSkillsCount;
	}

	动作
	{
		事件玩家.Victory = 真;
		事件玩家.setting[10] = 0;
		If(!数组包含(全局.playname, 自定义字符串("{0}", 事件玩家)));
			修改全局变量(playname, 添加至数组, 自定义字符串("{0}", 事件玩家));
		End;
		事件玩家.fileIndex = 数组值的索引(全局.playname, 自定义字符串("{0}", 事件玩家));
		大字体信息(事件玩家, 自定义字符串("Autoarchived: Ended"));
		全局.playdata[事件玩家.fileIndex] = 1;
		If(事件玩家.SpeedRunMode == 真);
			消除HUD文本(事件玩家.MyHUD[1]);
			创建HUD文本(事件玩家.IsInAnimation ? 空数组 : 事件玩家, 自定义字符串("Ended"), 自定义字符串("death: {0}", 事件玩家.Deaths), 自定义字符串("time: {0}:{1}", 取整(
				事件玩家.Timer / 60, 下), 取整(事件玩家.Timer % 60, 下)), 顶部, 1, 颜色(紫色), 颜色(绿色), 颜色(绿色), 可见和字符串, 默认可见度);
			事件玩家.MyHUD[0] = 上一个文本ID;
			大字体信息(所有玩家(所有队伍), 自定义字符串("\r\n{0} Ended time {1}:{2}!!!", 事件玩家, 取整(事件玩家.Timer / 60, 下), 取整(事件玩家.Timer % 60, 下)));
			If(事件玩家.Timer < 600);
				小字体信息(事件玩家, 自定义字符串(
					"The clearance time of racing mode is less than 10 minutes,\r\n and special effect rewards have been obtained!"));
				If(事件玩家.TutorialMode == 假);
					事件玩家.data[3] = 1;
				End;
			End;
			If(事件玩家.jingsu_Sel == 2);
				事件玩家.data[23] = 1;
				事件玩家.jingsu_Sel = 0;
				停止限制阈值(事件玩家);
			End;
		Else;
			大字体信息(所有玩家(所有队伍), 自定义字符串(" \r\n{0} {1}!", 事件玩家, 自定义字符串("恭喜完成教学关卡，请开始额外彩蛋探索吧！")));
	}
}

规则("长按Q重置")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.IsInAnimation == 假;
		按钮被按下(事件玩家, 按钮(终极技能)) == 真;
		按钮被按下(事件玩家, 按钮(蹲下)) == 假;
		事件玩家.Watch != 真;
	}

	动作
	{
		等待(0.750, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("正在重置... 3"));
		等待(0.750, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("正在重置... 2"));
		等待(0.750, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("正在重置... 1"));
		等待(0.750, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("重置成功!"));
		等待(0.050, 无视条件);
		调用子程序(ResetProgress);
	}
}

规则("竞速模式启用")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		全局.SpeedrunLocation != 矢量(0, 0, 0);
		相距距离(眼睛位置(事件玩家), 全局.SpeedrunLocation) < 1.500;
		事件玩家.Watch != 真;
		事件玩家.SpeedRunMode == 假;
	}

	动作
	{
		等待(0.250, 无视条件);
		If(!按钮被按下(事件玩家, 按钮(互动)));
			小字体信息(事件玩家, 自定义字符串("警告：启用竞速将重置所有进度\r\n按住[{0}]启用竞速模式", 输入绑定字符串(按钮(互动))));
		End;
		等待(1, 无视条件);
		If(!按钮被按下(事件玩家, 按钮(互动)));
			小字体信息(事件玩家, 自定义字符串("提示：近战+互动，打开特殊竞速模式"));
		Else;
			事件玩家.SpeedRunMode = 真;
			事件玩家.Victory = 假;
			调用子程序(ResetProgress);
			创建HUD文本(事件玩家.IsInAnimation ? 空数组 : 事件玩家, 全局.jingsu_text[事件玩家.jingsu_Sel][事件玩家.lang], 自定义字符串("死亡: {0}", 事件玩家.Deaths), 自定义字符串(
				"耗时: {0}:{1}", 取整(事件玩家.Timer / 60, 下), 取整(事件玩家.Timer % 60, 下)), 顶部, 1, 颜色(橙色), 颜色(红色), 颜色(橙色), 可见和字符串, 默认可见度);
			事件玩家.MyHUD[1] = 上一个文本ID;
			小字体信息(事件玩家, 自定义字符串("在规定时间内通关竞速模式可以获得额外奖励"));
			If(按钮被按下(事件玩家, 按钮(近身攻击)));
				事件玩家.jingsu_Sel = 2;
				开始限制阈值(事件玩家, 1, 1, 0, 0, 0, 1);
				事件玩家.quiet = 真;
			End;
		End;
	}
}

规则("竞速模式关闭")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		全局.SpeedrunLocation != 矢量(0, 0, 0);
		相距距离(眼睛位置(事件玩家), 全局.SpeedrunLocation) < 1.500;
		事件玩家.Watch != 真;
		事件玩家.SpeedRunMode == 真;
	}

	动作
	{
		等待(1, 当为“假”时中止);
		事件玩家.SpeedRunMode = 假;
		消除HUD文本(首个(事件玩家.MyHUD));
		消除HUD文本(事件玩家.MyHUD[1]);
		事件玩家.er_wai_jing_su[0] = 0;
		停止限制阈值(事件玩家);
		事件玩家.jingsu_Sel = 0;
		设置移动速度(事件玩家, 100);
		事件玩家.SpeedRunMode = 假;
		小字体信息(事件玩家, 自定义字符串("退出竞速模式"));
	}
}

规则("Speed Run Timer Increase")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory == 假;
		事件玩家.IsInAnimation == 假;
		事件玩家.SpeedRunMode == 真;
		相距距离(所选位置(事件玩家), 首个(全局.ZoneLocations)) > 1;
	}

	动作
	{
		等待(0.992, 当为“假”时中止);
		事件玩家.Timer += 1;
		循环;
	}
}

规则("长按R教学模式")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.TutorialMode == 假;
		事件玩家.IsInAnimation == 假;
		按钮被按下(事件玩家, 按钮(装填)) == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		等待(0.250, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("进入教学模式... 3"));
		等待(0.750, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("进入教学模式... 2"));
		等待(0.750, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("进入教学模式... 1"));
		等待(0.750, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("教学模式!"));
		事件玩家.TutorialMode = 真;
	}
}

规则("R存点")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		垂直速度(事件玩家) == 0;
		水平速度(事件玩家) == 0;
		事件玩家.TutorialMode == 真;
		事件玩家.IsInAnimation == 假;
		按钮被按下(事件玩家, 按钮(装填)) == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		If(事件玩家.jingsu_Sel == 2 && 事件玩家.Victory == 假);
			小字体信息(事件玩家, 自定义字符串("当你存点时，“根本停不下来”在你耳边响起"));
		Else;
			等待(0.500, 当为“假”时中止);
			小字体信息(事件玩家, 自定义字符串("已存点!"));
			事件玩家.Respawn = 所选位置(事件玩家);
			事件玩家.AlternativeRespawn = 所选位置(事件玩家);
			播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
	}
}

规则("长按q重置")
{
	事件
	{
		子程序;
		ResetProgress;
	}

	动作
	{
		开始强制玩家选择英雄(事件玩家, 首个(全局.HeroRoster));
		事件玩家.daxiao = 1;
		开始调整玩家大小(事件玩家, 事件玩家.daxiao, 真);
		If(事件玩家.SpeedRunMode == 真 && 事件玩家.Victory == 真);
			消除HUD文本(事件玩家.MyHUD[1]);
			创建HUD文本(事件玩家, 自定义字符串("竞速模式"), 自定义字符串("死亡: {0}", 事件玩家.Deaths), 自定义字符串("耗时: {0}:{1}", 取整(事件玩家.Timer / 60, 下), 取整(事件玩家.Timer % 60,
				下)), 顶部, 1, 颜色(橙色), 颜色(红色), 颜色(橙色), 可见和字符串, 默认可见度);
			事件玩家.MyHUD[1] = 上一个文本ID;
		End;
		全局.Arr[0] = 截取字符串(自定义字符串("{0}", 事件玩家), 1, 3) == 自定义字符串("{0}{1}{2}", 截取字符串(自定义字符串("队伍"), 0, 1), 截取字符串(自定义字符串("盟友"), 1, 1), 截取字符串(
			自定义字符串("不受限"), 0, 1)) ? 自定义字符串("{0}", 事件玩家) : 首个(全局.Arr);
		消除HUD文本(首个(事件玩家.MyHUD));
		消除HUD文本(事件玩家.MyHUD[5]);
		事件玩家.PortalUnlocked = 全局.PortalUnlockDefaults;
		事件玩家.Victory = 假;
		事件玩家.setting[10] = 1;
		事件玩家.ZonesReached[0] = 假;
		事件玩家.ZonesReached[1] = 假;
		事件玩家.ZonesReached[2] = 假;
		事件玩家.ZonesReached[3] = 假;
		事件玩家.HeroesUnlocked[0] = 假;
		事件玩家.HeroesUnlocked[1] = 假;
		事件玩家.HeroesUnlocked[2] = 假;
		事件玩家.HeroesUnlocked[3] = 假;
		If(首个(全局.ZoneLocations) != 矢量(0, 0, 0));
			事件玩家.Respawn = 首个(全局.ZoneLocations);
		End;
		事件玩家.Deaths = 0;
		事件玩家.Timer = 0;
		事件玩家.ZoneCount = 0;
		事件玩家.HeroCount = 0;
		事件玩家.AlternativeRespawn = 空;
		传送(事件玩家, 事件玩家.Respawn);
		等待(0.100, 无视条件);
		播放效果(所有玩家(所有队伍), 环状爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
		事件玩家.TutorialMode = 假;
		事件玩家.FoundSecretHero = 假;
		事件玩家.EasterEggsFound = 空数组;
		事件玩家.EasterEggCount = 0;
		设置朝向(事件玩家, 全局.SpawnFaceDirection, 至地图);
		调用子程序(Skill_Init);
		调用子程序(Skill_SetUp);
		事件玩家.SkillsFound = 空数组;
		事件玩家.Destination = 空数组;
		事件玩家.chatcount = 0;
		事件玩家.chat1count = 0;
		事件玩家.chatstart = 0;
		事件玩家.pengzhuang = 真;
		事件玩家.maomao = 0;
		事件玩家.tiaozhanzhe = 0;
		事件玩家.zhongju = 假;
		开启与环境的移动碰撞(事件玩家);
		消除效果(事件玩家.Effect__);
		事件玩家.CanDie = 真;
		事件玩家.data[0] = 0;
		事件玩家.er_wai_jing_su[0] = 0;
		事件玩家.jingsu_Sel = 0;
		停止限制阈值(事件玩家);
		设置移动速度(事件玩家, 100);
	}
}

规则("Update Count | Subroutine")
{
	事件
	{
		子程序;
		UpdateCount;
	}

	动作
	{
		事件玩家.ZoneCount = 数量(已过滤的数组(事件玩家.ZonesReached, 当前数组元素 == 真));
		事件玩家.HeroCount = 数量(已过滤的数组(事件玩家.HeroesUnlocked, 当前数组元素 == 真));
		If(事件玩家.HeroCount > 4);
			事件玩家.HeroCount = 4;
		End;
	}
}

规则("Reset CoolDown | Subroutine")
{
	事件
	{
		子程序;
		ResetCoolDown;
	}

	动作
	{
		设置技能冷却(事件玩家, 按钮(主要攻击模式), 0);
		设置技能冷却(事件玩家, 按钮(技能1), 0);
		设置技能冷却(事件玩家, 按钮(技能2), 0);
		设置技能充能(事件玩家, 按钮(技能1), 3);
	}
}

规则("游戏倒计时文本")
{
	事件
	{
		持续 - 全局;
	}

	条件
	{
		正在集结英雄 == 假;
		游戏正在进行中 == 真;
	}

	动作
	{
		创建HUD文本(所有玩家(所有队伍), 空, 空, 自定义字符串("剩余游戏时间 - {0}:{1}", 取整(全局.MatchTime / 60, 下), 取整(全局.MatchTime % 60, 下)), 顶部, -10, 空, 空, 颜色(白色),
			可见和字符串, 默认可见度);
		设置比赛时间(3599);
		等待(5, 无视条件);
		比赛时间暂停;
	}
}

规则("炸房警告")
{
	事件
	{
		持续 - 全局;
	}

	条件
	{
		"10 Min Warning"
		全局.MatchTime < 600;
	}

	动作
	{
		大字体信息(所有玩家(所有队伍), 自定义字符串("10 分钟结束本局游戏"));
		等待(240, 无视条件);
		大字体信息(所有玩家(所有队伍), 自定义字符串("5 分钟结束本局游戏"));
		等待(240, 无视条件);
		大字体信息(所有玩家(所有队伍), 自定义字符串("1 分钟结束本局游戏"));
		等待(60, 无视条件);
		大字体信息(所有玩家(所有队伍), 自定义字符串("正在重新启动房间!"));
		开启游戏预设完成条件;
		显示游戏模式地图UI(所有玩家(所有队伍));
		显示游戏模式HUD(所有玩家(所有队伍));
		设置比赛时间(0);
		等待(0.250, 无视条件);
		比赛时间继续;
	}
}

规则("比赛时间显示")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		等待(0.980, 无视条件);
		全局.MatchTime -= 1;
		根据条件中止(全局.MatchTime <= 0);
		循环;
	}
}

规则("Skip Assembling Heroes")
{
	事件
	{
		持续 - 全局;
	}

	条件
	{
		正在集结英雄 == 真;
	}

	动作
	{
		设置比赛时间(1);
	}
}

规则("Heroes Used")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"Heroes used to find easter eggs"
		全局.EasterEggHeroes[0] = 英雄(卡西迪);
		全局.EasterEggHeroes[1] = 英雄(布丽吉塔);
		全局.EasterEggHeroes[2] = 英雄(艾什);
		全局.EasterEggHeroes[3] = 英雄(源氏);
		全局.EasterEggHeroes[4] = 英雄(卢西奥);
		"Easter Egg Hero"
		全局.EasterEggHeroes[5] = 英雄(西格玛);
	}
}

规则("Locations")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"Make sure index of location matches index of hero"
		全局.EasterEggLocations[0] = 矢量(7.971, 95.572, 159.126);
		"Make sure index of location matches index of hero"
		全局.EasterEggLocations[1] = 矢量(77.475, 101.916, 117.847);
		"Make sure index of location matches index of hero"
		全局.EasterEggLocations[2] = 矢量(-15.656, 7.445, -9.529);
		"Make sure index of location matches index of hero"
		全局.EasterEggLocations[3] = 矢量(-42.030, 30.586, -14.501);
		"Make sure index of location matches index of hero"
		全局.EasterEggLocations[4] = 矢量(9.394, 271.175, 306.418);
		"Location to swap to Easter Egg hero"
		全局.EasterEggLocations[5] = 矢量(-52.605, 266.689, 333.422);
	}
}

规则("Max Count")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.EasterEggMaxCount = 5;
	}
}

规则("Effect")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.Victory && 首个(全局.EasterEggLocations) && !首个(当前数组元素.EasterEggsFound) && 所用英雄(当前数组元素) == 首个(
			全局.EasterEggHeroes)), 火花, 颜色(黄色), 首个(全局.EasterEggLocations), 1, 可见);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.Victory && 全局.EasterEggLocations[1] && !当前数组元素.EasterEggsFound[1] && 所用英雄(当前数组元素)
			== 全局.EasterEggHeroes[1]), 火花, 颜色(绿色), 全局.EasterEggLocations[1], 1, 可见);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.Victory && 全局.EasterEggLocations[2] && !当前数组元素.EasterEggsFound[2] && 所用英雄(当前数组元素)
			== 全局.EasterEggHeroes[2]), 火花, 颜色(蓝色), 全局.EasterEggLocations[2], 1, 可见);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.Victory && 全局.EasterEggLocations[3] && !当前数组元素.EasterEggsFound[3] && 所用英雄(当前数组元素)
			== 全局.EasterEggHeroes[3]), 火花, 颜色(紫色), 全局.EasterEggLocations[3], 1, 可见);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.Victory && 全局.EasterEggLocations[4] && !当前数组元素.EasterEggsFound[4] && 所用英雄(当前数组元素)
			== 全局.EasterEggHeroes[4]), 火花, 颜色(红色), 全局.EasterEggLocations[4], 1, 可见);
		"Easter Egg hero - Orange"
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.EasterEggCount >= 全局.EasterEggMaxCount), 有害光环, 颜色(橙色), 全局.EasterEggLocations[5], 1, 可见);
		创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.EasterEggCount >= 全局.EasterEggMaxCount), 英雄图标字符串(全局.EasterEggHeroes[5]),
			全局.EasterEggLocations[5] + 矢量(0, -0.300, 0), 2, 根据表面截取, 可见, 颜色(白色), 默认可见度);
	}
}

规则("彩蛋拾取")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory == 真;
		已重生(事件玩家) == 真;
		事件玩家.EasterEggCount < 全局.EasterEggMaxCount;
		对任意为“真”(全局.EasterEggLocations, 相距距离(眼睛位置(事件玩家), 当前数组元素) < 1.500) == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		For 玩家变量(事件玩家, LoopCounter, 0, 全局.EasterEggMaxCount, 1);
			If(事件玩家.EasterEggsFound[事件玩家.LoopCounter] == 假);
				If(所用英雄(事件玩家) == 全局.EasterEggHeroes[事件玩家.LoopCounter]);
					If(相距距离(眼睛位置(事件玩家), 全局.EasterEggLocations[事件玩家.LoopCounter]) <= 1.500);
						If(全局.EasterEggLocations[事件玩家.LoopCounter]);
							事件玩家.EasterEggsFound[事件玩家.LoopCounter] = 真;
							事件玩家.EasterEggCount += 1;
							调用子程序(Skill_SetUp);
							播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
							小字体信息(事件玩家, 自定义字符串("你找到了一个万圣节彩蛋"));
							中断;
						End;
					End;
				End;
			End;
		End;
	}
}

规则("Hero Swap")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		事件玩家.data[5] == 0;
		所用英雄(事件玩家) != 全局.EasterEggHeroes[5];
		相距距离(眼睛位置(事件玩家), 全局.EasterEggLocations[5]) < 1.500;
		事件玩家.Watch != 真;
	}

	动作
	{
		If(事件玩家.EasterEggCount >= 全局.EasterEggMaxCount);
			开始强制玩家选择英雄(事件玩家, 数组包含(全局.Arr, 自定义字符串("{0}", 事件玩家)) && 按钮被按下(事件玩家, 按钮(蹲下)) ? 全局.SpecialHeroes[数组值的索引(全局.Arr, 自定义字符串("{0}", 事件玩家))
				] : 全局.EasterEggHeroes[5]);
			If(事件玩家.Respawn == 全局.ZoneLocations[1]);
				事件玩家.AlternativeRespawn = 空;
			End;
			等待(0.250, 无视条件);
			If(事件玩家.EasterEggsFound[5] == 假);
				大字体信息(所有玩家(所有队伍), 自定义字符串(" \r\n{0} {1} {2}", 事件玩家, 自定义字符串("找到"), 英雄图标字符串(所用英雄(事件玩家))));
				事件玩家.EasterEggsFound[5] = 真;
	}
}

规则("Easter Egg Uit")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		西格玛;
	}

	条件
	{
		终极技能充能百分比(事件玩家) != 100;
	}

	动作
	{
		设置终极技能充能(事件玩家, 100);
		等待(0.250, 无视条件);
		如条件为“真”则循环;
	}
}

规则("麦克雷e推力")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		卡西迪;
	}

	条件
	{
		正在使用技能 2(事件玩家) == 真;
	}

	动作
	{
		施加推力(事件玩家, 上, 5, 至地图, 取消相反运动);
	}
}

规则("McCree_R_Click")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		所用英雄(事件玩家) == 首个(全局.HeroRoster);
	}

	动作
	{
		禁用按钮(事件玩家, 按钮(辅助攻击模式));
		等待直到 (所用英雄(事件玩家) != 首个(全局.HeroRoster), 99999);
		可用按钮(事件玩家, 按钮(辅助攻击模式));
	}
}

规则("小锤s推力")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		布丽吉塔;
	}

	条件
	{
		正在使用技能 1(事件玩家) == 真;
		(事件玩家.chatcount == 1 && 事件玩家.play_date[0] == 0) == 假;
	}

	动作
	{
		施加推力(事件玩家, 面朝方向(事件玩家), -10, 至地图, 取消相反运动);
	}
}

规则("锤妹额外彩蛋解锁shift")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount > 0;
		事件玩家.chatcount == 真;
		事件玩家.Victory == 真;
		所用英雄(事件玩家) == 英雄(布丽吉塔);
		相距距离(所选位置(事件玩家), 矢量(-44.372, 9.627, -25.979)) < 2;
		事件玩家.play_date[0] == 0;
	}

	动作
	{
		等待(0.500, 当为“假”时中止);
		事件玩家.play_date[0] = 1;
		大字体信息(事件玩家, 自定义字符串("已解锁shft能力"));
	}
}

规则("穿墙位置存储")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.SpecialPortalHero = 数组(英雄(卡西迪), 英雄(布丽吉塔), 英雄(艾什), 英雄(源氏));
		全局.SpecialPortalLocation = 数组(矢量(-59.250, 17.750, -3.939), 矢量(-59.250, 17.750, -3.939), 矢量(-16.559, 276.999, 347.337), 矢量(21.791,
			23.368, -32.889));
		全局.SpecialPortalRadius = 数组(3.250, 3.250, 1.500, 1.500);
		创建效果(已过滤的数组(所有玩家(所有队伍), 数组包含(全局.SpecialPortalHero, 所用英雄(当前数组元素))), 有益光环, 颜色(黑色), 全局.SpecialPortalLocation[数组值的索引(
			全局.SpecialPortalHero, 所用英雄(本地玩家))], 全局.SpecialPortalRadius[数组值的索引(全局.SpecialPortalHero, 所用英雄(本地玩家))], 可见，位置和半径);
	}
}

规则("穿墙程序")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		全局.SpecialPortalLocation == 真;
		数组包含(全局.SpecialPortalHero, 所用英雄(事件玩家)) == 真;
		相距距离(眼睛位置(事件玩家), 全局.SpecialPortalLocation[数组值的索引(全局.SpecialPortalHero, 所用英雄(事件玩家))]) <= 全局.SpecialPortalRadius[数组值的索引(
			全局.SpecialPortalHero, 所用英雄(事件玩家))];
	}

	动作
	{
		取消与环境的移动碰撞(事件玩家, 假);
		等待直到 (!数组包含(全局.SpecialPortalHero, 所用英雄(事件玩家)) || 相距距离(眼睛位置(事件玩家), 全局.SpecialPortalLocation[数组值的索引(全局.SpecialPortalHero, 所用英雄(事件玩家))
			]) > 全局.SpecialPortalRadius[数组值的索引(全局.SpecialPortalHero, 所用英雄(事件玩家))], 99999);
		根据条件中止(事件玩家.pengzhuang == 假);
		开启与环境的移动碰撞(事件玩家);
	}
}

规则("Lava Locations")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.LavaLocations_1 = 数组分割(全局.LavaLocations, 0, 30);
		全局.LavaRadius_1 = 数组分割(全局.LavaRadius, 0, 30);
		全局.LavaLocations_2 = 数组分割(全局.LavaLocations, 30, 24);
		全局.LavaRadius_2 = 数组分割(全局.LavaRadius, 30, 24);
		全局.LavaLocations_3 = 数组分割(全局.LavaLocations, 54, 33);
		全局.LavaRadius_3 = 数组分割(全局.LavaRadius, 54, 33);
	}
}

规则("Hero")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.Hero_ = 数组(英雄(卡西迪), 英雄(布丽吉塔), 英雄(艾什), 英雄(源氏));
	}
}

规则("MaxSkillsCount")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.MaxSkillsCount = 6;
	}
}

规则("技能坐标")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.Location[0] = 矢量(-65.581, 7.425, 0.351);
		全局.Location[1] = 矢量(30.700, 1.600, -50.756);
		全局.Location[2] = 矢量(-37.892, 3.425, -42.698);
		全局.Location[3] = 矢量(-41.749, 97.299, 140.771);
		全局.Location[4] = 矢量(17.158, 96.675, 114.813);
		全局.Location[5] = 矢量(-30.359, 272.838, 358.506);
	}
}

规则("Hero_Used")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.Hero_Used = 数组(0, 0, 1, 1, 2, 3);
	}
}

规则("Color")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.Color_ = 数组(颜色(黄色), 颜色(黄色), 颜色(绿色), 颜色(绿色), 颜色(蓝色), 颜色(紫色));
	}
}

规则("Type")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.Type_ = 数组(0, 1, 2, 0, 0, 0);
	}
}

规则("Skill_Init| Subroutine")
{
	事件
	{
		子程序;
		Skill_Init;
	}

	动作
	{
		事件玩家.SkillsFound = 空数组;
		事件玩家.Abi_1 = 数组(假, 假, 假, 假);
		事件玩家.Abi_2 = 数组(假, 假, 假, 假);
		事件玩家.R_Click = 数组(假, 假, 真, 真);
	}
}

规则("Effect")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		等待(2, 无视条件);
		For 全局变量(Index, 0, 全局.MaxSkillsCount, 1);
			创建效果(已过滤的数组(所有玩家(所有队伍), 所用英雄(当前数组元素) == 全局.Hero_[全局.Hero_Used[单次赋值(全局.Index)]] && !当前数组元素.SkillsFound[单次赋值(全局.Index)]), 火花,
				全局.Color_[单次赋值(全局.Index)], 全局.Location[单次赋值(全局.Index)], 1, 可见);
			等待(0.050, 无视条件);
		End;
	}
}

规则("Pickup")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory != 真;
		对任意为“真”(已过滤的数组(全局.Location, 当前数组元素 && 已重生(事件玩家)), 相距距离(眼睛位置(事件玩家), 当前数组元素) <= 1.500) == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		For 玩家变量(事件玩家, Index, 0, 全局.MaxSkillsCount, 1);
			If(相距距离(眼睛位置(事件玩家), 全局.Location[事件玩家.Index]) <= 1.500);
				If(!事件玩家.SkillsFound[事件玩家.Index]);
					If(全局.Hero_Used[事件玩家.Index] == 数组值的索引(全局.Hero_, 所用英雄(事件玩家)));
						If(全局.Type_[事件玩家.Index] == 0);
							事件玩家.Abi_1[数组值的索引(全局.Hero_, 所用英雄(事件玩家))] = 真;
						Else If(全局.Type_[事件玩家.Index] == 1);
							事件玩家.Abi_2[数组值的索引(全局.Hero_, 所用英雄(事件玩家))] = 真;
						Else If(全局.Type_[事件玩家.Index] == 2);
							事件玩家.R_Click[数组值的索引(全局.Hero_, 所用英雄(事件玩家))] = 真;
						End;
						小字体信息(事件玩家, 自定义字符串("你找到 {0} 的 {1}", 英雄图标字符串(所用英雄(事件玩家)), 技能图标字符串(所用英雄(事件玩家), 数组(按钮(技能1), 按钮(技能2), 按钮(辅助攻击模式))
							[全局.Type_[事件玩家.Index]])));
						播放效果(事件玩家, 状态爆炸声音, 颜色(白色), 事件玩家, 200);
						事件玩家.SkillsFound[事件玩家.Index] = 真;
						调用子程序(Skill_SetUp);
						中断;
					End;
				End;
			End;
		End;
	}
}

规则("Skill_SetUp")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		所用英雄(事件玩家) != 事件玩家.Hero;
	}

	动作
	{
		调用子程序(Skill_SetUp);
		事件玩家.Hero = 所用英雄(事件玩家);
		If(首个(事件玩家.er_wai_jing_su) == 0);
			设置移动速度(事件玩家, 事件玩家.only_maker[8] == 1 ? 300 : 100);
	}
}

规则("Skill_SetUp | Subroutine")
{
	事件
	{
		子程序;
		Skill_SetUp;
	}

	动作
	{
		设置辅助攻击模式启用(事件玩家, 数组包含(全局.Hero_, 所用英雄(事件玩家)) ? 事件玩家.R_Click[数组值的索引(全局.Hero_, 所用英雄(事件玩家))] : 真);
		设置启用技能 1(事件玩家, 数组包含(全局.Hero_, 所用英雄(事件玩家)) ? 事件玩家.Abi_1[数组值的索引(全局.Hero_, 所用英雄(事件玩家))] : 真);
		设置启用技能 2(事件玩家, 数组包含(全局.Hero_, 所用英雄(事件玩家)) ? 事件玩家.Abi_2[数组值的索引(全局.Hero_, 所用英雄(事件玩家))] : 真);
		设置启用终极技能(事件玩家, 数组包含(全局.Hero_, 所用英雄(事件玩家)) ? 事件玩家.Abi_2[数组值的索引(全局.Hero_, 所用英雄(事件玩家))] : 真);
		等待(0.250, 无视条件);
		设置辅助攻击模式启用(事件玩家, 数组包含(全局.Hero_, 所用英雄(事件玩家)) ? 事件玩家.R_Click[数组值的索引(全局.Hero_, 所用英雄(事件玩家))] : 真);
	}
}

规则("额外英雄")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.ExtraHero[0] = 英雄(回声);
		全局.ExtraHero[1] = 英雄(天使);
		全局.ExtraHero[2] = 英雄(黑影);
		全局.ExtraHero[3] = 英雄(半藏);
		全局.ExtraHero[4] = 英雄(秩序之光);
	}
}

规则("额外英雄无碰撞")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		数组包含(全局.ExtraHero, 所用英雄(事件玩家)) == 真;
	}

	动作
	{
		取消与环境的移动碰撞(事件玩家, 假);
		等待直到 (!数组包含(全局.ExtraHero, 所用英雄(事件玩家)), 99999);
		根据条件中止(事件玩家.pengzhuang == 假);
		开启与环境的移动碰撞(事件玩家);
	}
}

规则("额外英雄位置")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.ExtraHeroLocation[0] = 矢量(-11.092, 92.517, 134.837);
		全局.ExtraHeroLocation[1] = 矢量(-0.016, 279.588, 292.725);
		全局.ExtraHeroLocation[2] = 矢量(15.675, 252.482, 347.951);
		全局.ExtraHeroLocation[3] = 矢量(-72.390, 15.280, -49.210);
		全局.ExtraHeroLocation[4] = 矢量(-0.080, 162, 149.890);
	}
}

规则("Effect")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.Victory && 数组包含(全局.HeroRoster, 所用英雄(当前数组元素))), 有害光环, 颜色(白色), 全局.ExtraHeroLocation[数组值的索引(
			全局.HeroRoster, 所用英雄(本地玩家))], 1, 可见，位置和半径);
	}
}

规则("Pickup")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory == 真;
		事件玩家.chatstart != 真;
		对任意为“真”(已过滤的数组(全局.ExtraHeroLocation, 当前数组元素 && 已重生(事件玩家)), 相距距离(眼睛位置(事件玩家), 当前数组元素) <= 1.500) == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		For 玩家变量(事件玩家, ExtraHeroLoop, 0, 数量(全局.ExtraHeroLocation), 1);
			If(相距距离(眼睛位置(事件玩家), 全局.ExtraHeroLocation[事件玩家.ExtraHeroLoop]) <= 1.500);
				If(事件玩家.ExtraHeroLoop == 数组值的索引(全局.HeroRoster, 所用英雄(事件玩家)));
					开始强制玩家选择英雄(事件玩家, 全局.ExtraHero[事件玩家.ExtraHeroLoop]);
					等待(0.250, 无视条件);
					If(!事件玩家.FoundSecretHero[事件玩家.ExtraHeroLoop]);
						大字体信息(所有玩家(所有队伍), 自定义字符串("{0} {1} {2}", 自定义字符串("{0}{1}", 英雄图标字符串(全局.HeroRoster[事件玩家.ExtraHeroLoop]), 事件玩家), 自定义字符串("find"),
							英雄图标字符串(全局.ExtraHero[事件玩家.ExtraHeroLoop])));
						事件玩家.FoundSecretHero[事件玩家.ExtraHeroLoop] = 真;
					End;
					传送(事件玩家, 全局.ZoneLocations[1]);
					事件玩家.Respawn = 全局.ZoneLocations[1];
					中断;
				End;
			End;
		End;
	}
}

规则("Extra Hero Swap Effect")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.ExtraHeroSwapLocation = 矢量(1, 0, -73.600);
		创建效果(已过滤的数组(所有玩家(所有队伍), 数组包含(全局.HeroRoster, 所用英雄(当前数组元素)) && 当前数组元素.FoundSecretHero[数组值的索引(全局.HeroRoster, 所用英雄(当前数组元素))]), 有害光环,
			颜色(白色), 全局.ExtraHeroSwapLocation, 1, 可见);
		创建地图文本(已过滤的数组(所有玩家(所有队伍), 数组包含(全局.HeroRoster, 所用英雄(当前数组元素)) && 当前数组元素.FoundSecretHero[数组值的索引(全局.HeroRoster, 所用英雄(当前数组元素))]),
			英雄图标字符串(全局.ExtraHero[数组值的索引(全局.HeroRoster, 所用英雄(本地玩家))]), 全局.ExtraHeroSwapLocation, 2, 根据表面截取, 可见和字符串, 颜色(白色), 始终不可见);
	}
}

规则("Extra Hero Swap")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		全局.ExtraHeroSwapLocation == 真;
		数组包含(全局.HeroRoster, 所用英雄(事件玩家)) == 真;
		相距距离(眼睛位置(事件玩家), 全局.ExtraHeroSwapLocation) <= 2;
		事件玩家.FoundSecretHero[数组值的索引(全局.HeroRoster, 所用英雄(事件玩家))] == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		开始强制玩家选择英雄(事件玩家, 全局.ExtraHero[数组值的索引(全局.HeroRoster, 所用英雄(事件玩家))]);
		传送(事件玩家, 全局.ZoneLocations[1]);
		事件玩家.Respawn = 全局.ZoneLocations[1];
		等待(0.250, 无视条件);
	}
}

规则("指引点记录")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.Point[0] = 首个(全局.Location);
		全局.Point[1] = 全局.ZoneLocations[1];
		全局.Point[2] = 全局.Location[1];
		全局.Point[3] = 首个(全局.UnlockLocations);
		全局.Point[4] = 全局.Location[2];
		全局.Point[5] = 首个(全局.CheckpointLocations);
		全局.Point[6] = 全局.PortalLocations[12];
		全局.Point[7] = 全局.ZoneLocations[2];
		全局.Point[8] = 全局.Location[3];
		全局.Point[9] = 全局.UnlockLocations[1];
		全局.Point[10] = 全局.Location[4];
		全局.Point[11] = 全局.CheckpointLocations[1];
		全局.Point[12] = 全局.PortalLocations[14];
		全局.Point[13] = 全局.ZoneLocations[3];
		全局.Point[14] = 全局.UnlockLocations[2];
		全局.Point[15] = 全局.CheckpointLocations[2];
		全局.Point[16] = 全局.ZoneLocations[4];
		全局.Point[17] = 全局.Location[5];
		全局.Point[18] = 全局.UnlockLocations[3];
	}
}

规则("Effect")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建图标(已过滤的数组(所有玩家(所有队伍), 当前数组元素.TutorialMode == 真 && 当前数组元素.setting[10] == 1), 全局.Point[数量(本地玩家.Destination)], 旗帜, 可见和位置, 颜色(绿色),
			真);
	}
}

规则("For")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Victory == 假;
		事件玩家.TutorialMode == 真;
		相距距离(眼睛位置(事件玩家), 全局.Point[数量(已过滤的数组(事件玩家.Destination, 当前数组元素 == 真))]) <= 2;
	}

	动作
	{
		事件玩家.Destination[数量(已过滤的数组(事件玩家.Destination, 当前数组元素 == 真))] = 真;
	}
}

规则("卢西奥切歌")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		所用英雄(事件玩家) == 英雄(卢西奥);
	}

	动作
	{
		If(事件玩家.chatcount != 5);
			开始按下按钮(事件玩家, 按钮(技能1));
			等待直到 (!处于非初始状态(事件玩家), 99999);
			禁用按钮(事件玩家, 按钮(技能1));
			设置启用技能 1(事件玩家, 假);
			设置移动速度(事件玩家, 125);
			停止按下按钮(事件玩家, 按钮(技能1));
			等待直到 (所用英雄(事件玩家) != 英雄(卢西奥), 99999);
			设置移动速度(事件玩家, 事件玩家.only_maker[8] == 1 ? 300 : 100);
			可用按钮(事件玩家, 按钮(技能1));
			设置启用技能 1(事件玩家, 真);
			停止按下按钮(事件玩家, 按钮(技能1));
	}
}

规则("Lúcio SPD")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		卢西奥;
	}

	条件
	{
		正在使用技能 2(事件玩家) == 真;
	}

	动作
	{
		If(事件玩家.chatcount != 5);
			设置移动速度(事件玩家, 185);
			等待直到 (!正在使用技能 2(事件玩家), 99999);
			设置移动速度(事件玩家, 所用英雄(事件玩家) == 英雄(卢西奥) ? 125 : 100);
	}
}

规则("Lúcio SPD")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		卢西奥;
	}

	条件
	{
		事件玩家.chatcount < 5;
		处于非初始状态(事件玩家) == 真;
	}

	动作
	{
		等待(2, 当为“假”时中止);
		取消主要动作(事件玩家);
		击杀(事件玩家, 事件玩家);
		事件玩家.play_date[5] -= 1;
		大字体信息(事件玩家, 自定义字符串("再使用{0}次绿圈将T出游戏", 事件玩家.play_date[5]));
		If(事件玩家.play_date[5] <= 0);
			移除玩家(事件玩家);
		End;
		等待(1, 无视条件);
		If(处于非初始状态(事件玩家) == 真);
			可用按钮(事件玩家, 按钮(技能1));
			设置启用技能 1(事件玩家, 真);
			等待(0.100, 无视条件);
			开始按下按钮(事件玩家, 按钮(技能1));
			等待直到 (!处于非初始状态(事件玩家), 1);
			If(处于非初始状态(事件玩家) == 真);
				循环;
			Else;
				禁用按钮(事件玩家, 按钮(技能1));
				设置启用技能 1(事件玩家, 假);
				停止按下按钮(事件玩家, 按钮(技能1));
			End;
		End;
	}
}

规则("第三人称开启")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		按钮被按下(事件玩家, 按钮(装填)) == 假;
		按钮被按下(事件玩家, 按钮(蹲下)) == 假;
		事件玩家.Watch != 真;
	}

	动作
	{
		等待(3, 当为“假”时中止);
		事件玩家.Switch = (事件玩家.Switch + 1) % 2;
		If(!事件玩家.Switch);
			事件玩家.Cam = 0;
			调用子程序(Camera);
			小字体信息(事件玩家, 自定义字符串("第三人称视角已关闭"));
		End;
		小字体信息(事件玩家, 自定义字符串("切换成功"));
		播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 事件玩家, 200);
	}
}

规则("第三人称切换")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Switch == 真;
		按钮被按下(事件玩家, 按钮(蹲下)) == 真;
		按钮被按下(事件玩家, 按钮(跳跃)) == 真;
		事件玩家.Watch != 真;
	}

	动作
	{
		事件玩家.Cam = (事件玩家.Cam + 1) % 2;
		调用子程序(Camera);
		等待(0.250, 无视条件);
	}
}

规则("Camera | Subroutine")
{
	事件
	{
		子程序;
		Camera;
	}

	动作
	{
		If(事件玩家.Cam);
			开始镜头(事件玩家, 射线命中位置(事件玩家 + 上 * (相距距离(眼睛位置(事件玩家), 事件玩家) + 0.500), 射线命中位置(事件玩家 + 上 * (相距距离(眼睛位置(事件玩家), 事件玩家) + 0.500), 事件玩家 + 上 * (
				相距距离(眼睛位置(事件玩家), 事件玩家) + 0.500) + 面朝方向(事件玩家) * -3, 空, 事件玩家, 真), 空, 事件玩家, 真), 事件玩家 + 面朝方向(事件玩家) * 100, 100);
		Else;
			停止镜头(事件玩家);
		End;
	}
}

规则("特效选择文本")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.EffectHUDText = 数组(数组(自定义字符串("◆ No special effects"), 自定义字符串("◆1: complete the competition"), 自定义字符串("◆2: Find the egg hero"),
			自定义字符串("◆3: Find all hidden heroes"), 自定义字符串("◆4: Pass in 10 minutes in race mode"), 自定义字符串("◆5: Find all the extra eggs"),
			自定义字符串("◆6: Find all the air eggs"), 自定义字符串("◆7: Complete the hamster challenge"), 自定义字符串(
			"◆8: Do not use the Tutorial, and pass the customs in 10 minutes in the racing mode"), 自定义字符串(
			"◆9: Complete Anna Super Jump Challenge(impossible,Applicable to ow1)"), 自定义字符串("◆10：？？？"), 自定义字符串("◆11：？？？"), 自定义字符串(
			"◆12：？？？"), 自定义字符串("◆13：Complete the Amazing Race"), 自定义字符串("◆14：Full fire"), 自定义字符串("◆15：Complete the blind race")), 数组(
			自定义字符串("◆无特效"), 自定义字符串("◆1：完成教学关卡到“已结束”"), 自定义字符串("◆2：找到彩蛋英雄（西格玛）"), 自定义字符串("◆3：找到全部隐藏英雄"), 自定义字符串("◆4：10分钟内通关竞速模式"), 自定义字符串(
			"◆5：找到全部额外彩蛋"), 自定义字符串("◆6：找到全部空气彩蛋"), 自定义字符串("◆7：完成仓鼠挑战"), 自定义字符串("◆8：不开教学模式10分钟内通关竞速模式"), 自定义字符串("◆9：通关安娜娜超级跳挑战"), 自定义字符串(
			"◆10：DJ科目二"), 自定义字符串("◆11：维和者试炼"), 自定义字符串("◆12：神秘的隐藏特效Ⅲ"), 自定义字符串("◆13：通关炫迈竞速"), 自定义字符串("◆14：触发火力全开"), 自定义字符串(
			"◆15：神秘的隐藏特效Ⅳ")));
		全局.EffectSwitchLocation = 矢量(-7.134, -0.576, -83.097);
		创建图标(所有玩家(所有队伍), 全局.EffectSwitchLocation, 感叹号, 可见, 颜色(黄色), 假);
		全局.zhongjuloction = 矢量(0.760, 0, -83);
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 首个(当前数组元素.mianban) == 1), 自定义字符串("{0}", 数组(自定义字符串(
			"                    Special Effect Selection                    \r\n{0}\r\n\r\n\r\n{1}", 自定义字符串(
			"{0} or {1}Toggle Selection\r\n<{2}>Confirm special effects", 输入绑定字符串(按钮(主要攻击模式)), 输入绑定字符串(按钮(辅助攻击模式)), 输入绑定字符串(按钮(互动))),
			全局.EffectHUDText[本地玩家.lang][本地玩家.Effect_Choice]), 自定义字符串(
			"                    特效选择/挑战开启                    \r\n{0}\r\n\r\n\r\n{1}", 自定义字符串("{0}或{1}切换选择\r\n<{2}>选择特效", 输入绑定字符串(按钮(
			主要攻击模式)), 输入绑定字符串(按钮(辅助攻击模式)), 输入绑定字符串(按钮(互动))), 全局.EffectHUDText[本地玩家.lang][本地玩家.Effect_Choice]))[本地玩家.lang]), 空, 空, 顶部, 127,
			颜色(橙色), 空, 空, 可见和字符串, 始终不可见);
	}
}

规则("Effect Choice")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		(按钮被按下(事件玩家, 按钮(主要攻击模式)) || 按钮被按下(事件玩家, 按钮(辅助攻击模式))) == 真;
		相距距离(事件玩家, 全局.EffectSwitchLocation) <= 3;
		事件玩家.Watch != 真;
	}

	动作
	{
		If(按钮被按下(事件玩家, 按钮(主要攻击模式)));
			事件玩家.Effect_Choice = (事件玩家.Effect_Choice + 1) % 数量(全局.EffectHUDText[事件玩家.lang]);
		Else;
			If(事件玩家.Effect_Choice == 0);
				事件玩家.Effect_Choice = 数量(全局.EffectHUDText[事件玩家.lang]) - 1;
			Else;
				事件玩家.Effect_Choice -= 1;
			End;
		End;
		等待(0.250, 无视条件);
	}
}

规则("称号选择栏")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		(相距距离(事件玩家, 全局.EffectSwitchLocation) <= 3 || 相距距离(事件玩家, 全局.cheng_hao_Location) <= 3) == 真;
	}

	动作
	{
		禁用按钮(事件玩家, 按钮(主要攻击模式));
		禁用按钮(事件玩家, 按钮(辅助攻击模式));
		If(相距距离(事件玩家, 全局.EffectSwitchLocation) <= 3);
			事件玩家.mianban[0] = 1;
		Else;
			事件玩家.mianban[1] = 1;
		End;
		等待直到 (相距距离(事件玩家, 全局.EffectSwitchLocation) > 3 && 相距距离(事件玩家, 全局.cheng_hao_Location) > 3, 99999);
		事件玩家.mianban[0] = 0;
		事件玩家.mianban[1] = 0;
		可用按钮(事件玩家, 按钮(主要攻击模式));
		If(所用英雄(事件玩家) != 英雄(卡西迪));
			可用按钮(事件玩家, 按钮(辅助攻击模式));
	}
}

规则("Create Effect")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		相距距离(事件玩家, 全局.EffectSwitchLocation) <= 3;
		事件玩家.Watch != 真;
	}

	动作
	{
		调用子程序(Creat_Effect);
		等待(1, 无视条件);
	}
}

规则("Leave")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		相距距离(事件玩家, 全局.EffectSwitchLocation) > 3;
	}

	动作
	{
		事件玩家.Effect_Choice = 0;
	}
}

规则("特效选择及挑战开启")
{
	事件
	{
		子程序;
		Creat_Effect;
	}

	动作
	{
		设置不可见(事件玩家, 无);
		事件玩家.data[13] = 0;
		事件玩家.data[15] = 0;
		事件玩家.data[17] = 0;
		If(!事件玩家.Effect_Choice);
			消除效果(事件玩家.Effect__);
			小字体信息(事件玩家, 自定义字符串("已选择 不使用效果"));
		Else If(事件玩家.Effect_Choice == 1);
			If(事件玩家.Victory != 真);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), 温斯顿原始暴怒效果, 队伍2, 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效一"));
			End;
		Else If(事件玩家.Effect_Choice == 2);
			If(事件玩家.EasterEggsFound != 真);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), 安娜纳米激素强化效果, 队伍1, 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效二"));
			End;
		Else If(事件玩家.Effect_Choice == 3);
			If(数量(已过滤的数组(事件玩家.FoundSecretHero, 当前数组元素)) < 5);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), “回声”复制效果, 队伍1, 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效三"));
			End;
		Else If(事件玩家.Effect_Choice == 4);
			If(!(事件玩家.Victory && 事件玩家.SpeedRunMode && 事件玩家.Timer < 600));
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), “破坏球”重力坠击火焰效果, 队伍1, 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效四"));
			End;
		Else If(事件玩家.Effect_Choice == 5);
			If(事件玩家.chat1count < 5);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), “破坏球”感应护盾目标效果, 队伍1, 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效五"));
			End;
		Else If(事件玩家.Effect_Choice == 6);
			If(首个(事件玩家.setting) != 520);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), 巴蒂斯特维生力场保护效果, 队伍1, 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效六"));
			End;
		Else If(事件玩家.Effect_Choice == 7);
			If(事件玩家.setting[6] != 1);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!\r\n按住互动来开始挑战"));
				等待(1, 无视条件);
				If(事件玩家.Victory == 假);
					大字体信息(事件玩家, 自定义字符串("请先完成原版内容"));
				Else;
					If(按钮被按下(事件玩家, 按钮(互动)));
						事件玩家.setting[7] = 1;
						事件玩家.setting[8] = 0;
						事件玩家.setting[9] = 0;
						事件玩家.setting[10] = 1;
						开始强制玩家选择英雄(事件玩家, 英雄(破坏球));
						事件玩家.Destination = 数组(真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真);
						事件玩家.data[0] = 0;
						事件玩家.daxiao = 1;
						事件玩家.pengzhuang = 真;
						事件玩家.TutorialMode = 真;
						开启与环境的移动碰撞(事件玩家);
						事件玩家.CanDie = 真;
						等待直到 (所用英雄(事件玩家) == 英雄(破坏球), 99999);
						等待(0.500, 无视条件);
						设置启用技能 2(事件玩家, 假);
						设置辅助攻击模式启用(事件玩家, 假);
						禁用按钮(事件玩家, 按钮(蹲下));
						大字体信息(事件玩家, 自定义字符串("开始仓鼠挑战"));
					End;
				End;
			Else;
				消除效果(事件玩家.Effect__);
				设置不可见(事件玩家, 全部);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效七"));
			End;
		Else If(事件玩家.Effect_Choice == 8);
			If(事件玩家.data[3] == 0);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				事件玩家.data[4] = 1;
				创建效果(所有玩家(所有队伍), 卢西奥音障保护效果, 队伍1, 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 空数组;
				小字体信息(事件玩家, 自定义字符串("已选择 特效八"));
			End;
		Else If(事件玩家.Effect_Choice == 9);
			If(事件玩家.data[6] == 0);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!\r\n按住互动来开始挑战"));
				等待(1, 无视条件);
				If(事件玩家.Victory == 假);
					大字体信息(事件玩家, 自定义字符串("请先完成原版内容"));
				Else;
					If(按钮被按下(事件玩家, 按钮(互动)));
						事件玩家.data[5] = 1;
						开始强制玩家选择英雄(事件玩家, 英雄(末日铁拳));
						设置不可见(事件玩家, 全部);
						事件玩家.data[0] = 0;
						事件玩家.pengzhuang = 真;
						事件玩家.daxiao = 1;
						开启与环境的移动碰撞(事件玩家);
						事件玩家.CanDie = 真;
						等待(0.500, 无视条件);
						设置启用技能 2(事件玩家, 假);
						设置启用技能 1(事件玩家, 假);
						事件玩家.tiequanlevel = 0;
						等待(0.100, 无视条件);
						击杀(事件玩家, 空);
						大字体信息(事件玩家, 自定义字符串("已开始安娜娜超级跳挑战"));
					End;
				End;
			Else;
				If(按钮被按下(事件玩家, 按钮(装填)));
					事件玩家.tiequanlevel = 0;
					事件玩家.data[5] = 1;
					开始强制玩家选择英雄(事件玩家, 英雄(末日铁拳));
					设置不可见(事件玩家, 全部);
					事件玩家.data[0] = 0;
					事件玩家.pengzhuang = 真;
					事件玩家.daxiao = 1;
					开启与环境的移动碰撞(事件玩家);
					事件玩家.CanDie = 真;
					等待(0.500, 无视条件);
					设置启用技能 2(事件玩家, 假);
					设置启用技能 1(事件玩家, 假);
					事件玩家.tiequanlevel = 0;
					等待(0.100, 无视条件);
					击杀(事件玩家, 空);
					大字体信息(事件玩家, 自定义字符串("已开始安娜娜超级跳挑战"));
				Else;
					消除效果(事件玩家.Effect__);
					事件玩家.data[13] = 1;
					小字体信息(事件玩家, 自定义字符串("已选择 特效九"));
				End;
			End;
		Else If(事件玩家.Effect_Choice == 10);
			If(事件玩家.data[11] == 0);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!\r\n按住互动来开始挑战"));
				等待(1, 无视条件);
				If(事件玩家.maomao != 5);
					大字体信息(事件玩家, 自定义字符串("请先完成权限彩蛋"));
				Else;
					If(按钮被按下(事件玩家, 按钮(互动)));
						开始强制玩家选择英雄(事件玩家, 英雄(卢西奥));
						事件玩家.Destination = 数组(真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真);
						事件玩家.data[0] = 0;
						传送(事件玩家, 矢量(75.700, 97.580, 145.160));
						事件玩家.Respawn = 矢量(75.700, 97.580, 145.160);
						击杀(事件玩家, 空);
						事件玩家.zhongju = 真;
						事件玩家.tiaozhanpanding[0] = 1;
						事件玩家.Respawn = 全局.DJlocation[0];
						事件玩家.daxiao = 1;
						事件玩家.pengzhuang = 真;
						事件玩家.TutorialMode = 真;
						开启与环境的移动碰撞(事件玩家);
						事件玩家.CanDie = 假;
						等待直到 (所用英雄(事件玩家) == 英雄(卢西奥), 99999);
						大字体信息(事件玩家, 自定义字符串("开启DJ挑战，开启无敌"));
					End;
				End;
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), “死神”幽灵形态效果, 队伍1, 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效十"));
			End;
		Else If(事件玩家.Effect_Choice == 11);
			If(事件玩家.weihezhe != 6);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!\r\n按住互动来开始挑战"));
				等待(1, 无视条件);
				If(事件玩家.maomao != 5);
					大字体信息(事件玩家, 自定义字符串("请先完成权限彩蛋"));
				Else;
					If(按钮被按下(事件玩家, 按钮(互动)));
						开始强制玩家选择英雄(事件玩家, 英雄(卡西迪));
						事件玩家.Destination = 数组(真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真);
						事件玩家.data[0] = 0;
						传送(事件玩家, 矢量(-20.730, 101.580, 184.610));
						事件玩家.Respawn = 矢量(-20.730, 101.580, 184.610);
						击杀(事件玩家, 空);
						事件玩家.zhongju = 真;
						事件玩家.daxiao = 1;
						事件玩家.pengzhuang = 真;
						事件玩家.TutorialMode = 真;
						开启与环境的移动碰撞(事件玩家);
						事件玩家.CanDie = 真;
						等待直到 (所用英雄(事件玩家) == 英雄(卡西迪), 99999);
						大字体信息(事件玩家, 自定义字符串("收集维和者碎片！"));
					End;
				End;
			Else;
				消除效果(事件玩家.Effect__);
				事件玩家.data[15] = 1;
				小字体信息(事件玩家, 自定义字符串("已选择 特效十一"));
			End;
		Else If(事件玩家.Effect_Choice == 12);
			If(事件玩家.data[16] == 0);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), 美冰冻效果, 颜色(白色), 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效十二"));
			End;
		Else If(事件玩家.Effect_Choice == 13);
			If(事件玩家.data[23] == 0);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效十三"));
				事件玩家.data[17] = 1;
			End;
		Else If(事件玩家.Effect_Choice == 14);
			If(事件玩家.data[22] == 0);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), 艾什延时雷管燃烧材料效果, 颜色(白色), 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效十四"));
			End;
		Else If(事件玩家.Effect_Choice == 15);
			If(事件玩家.data[24] == 0);
				小字体信息(事件玩家, 自定义字符串("条件未达成 无法设置该特效!"));
			Else;
				消除效果(事件玩家.Effect__);
				创建效果(所有玩家(所有队伍), “黑影”黑客入侵完成循环效果, 颜色(白色), 事件玩家, 1, 可见，位置和半径);
				事件玩家.Effect__ = 最后创建的实体;
				小字体信息(事件玩家, 自定义字符串("已选择 特效十五"));
			End;
		End;
	}
}

规则("源氏天使隐藏特效")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		正在交流(事件玩家, 需要治疗) == 真;
		所用英雄(射线命中玩家(眼睛位置(事件玩家), 眼睛位置(事件玩家) + 面朝方向(事件玩家) * 20, 所有玩家(所有队伍), 事件玩家, 假)) == 英雄(天使);
	}

	动作
	{
		等待(1, 无视条件);
		If(死亡(事件玩家));
			事件玩家.data[11] = 1;
	}
}

规则("观战模式开启")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(技能2)) == 真;
	}

	动作
	{
		等待(2, 当为“假”时中止);
		事件玩家.Watch = (事件玩家.Watch + 1) % 2;
		击杀(事件玩家.Watch ? 事件玩家 : 空数组, 空);
		If(事件玩家.Watch == 真);
			开启游戏预设复生模式(事件玩家);
			关闭游戏预设复生模式(事件玩家);
			If(事件玩家.jingsu_Sel == 2);
				停止限制阈值(事件玩家);
			End;
		Else;
			关闭游戏预设复生模式(事件玩家);
			开启游戏预设复生模式(事件玩家);
			If(事件玩家.jingsu_Sel == 2);
				开始限制阈值(事件玩家, 1, 1, 0, 0, 0, 1);
			End;
		End;
		If(所用英雄(事件玩家) == 英雄(卡西迪));
			If(事件玩家.Watch == 真);
				可用按钮(事件玩家, 按钮(辅助攻击模式));
			Else;
				禁用按钮(事件玩家, 按钮(辅助攻击模式));
			End;
		End;
		复活(事件玩家.Watch ? 空数组 : 事件玩家);
		小字体信息(事件玩家, 事件玩家.Watch ? 自定义字符串("Watching the battle Press {0} to exit the watching mode", 输入绑定字符串(按钮(技能2))) : 自定义字符串(
			"Exited the watching mode"));
		If(所用英雄(事件玩家) == 英雄(D.Va) && 事件玩家.Watch && 存活(事件玩家));
			等待(1, 无视条件);
			击杀(事件玩家, 空);
		End;
		If(所用英雄(事件玩家) == 英雄(巴蒂斯特) && 事件玩家.Watch && 存活(事件玩家));
			等待(0.250, 无视条件);
			传送(事件玩家, 所选位置(事件玩家) + 矢量(0, 50, 0));
			等待(0.250, 无视条件);
			清除状态(事件玩家, 无法杀死);
			击杀(事件玩家, 空);
		End;
		播放效果(事件玩家, “黑影”位移传动材料效果, 队伍1, 事件玩家, 1);
	}
}

规则("Watch")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		正在使用技能 2(事件玩家) == 真;
		数组包含(数组(正在复制的英雄(事件玩家), 所用英雄(事件玩家)), 英雄(天使)) == 真;
	}

	动作
	{
		取消主要动作(事件玩家);
		设置技能冷却(事件玩家, 按钮(技能2), 8);
	}
}

规则("麦克雷shft")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		正在使用技能 1(事件玩家) == 真;
		所用英雄(事件玩家) == 首个(全局.HeroRoster);
	}

	动作
	{
		等待(0.250, 无视条件);
		If(!在地面上(事件玩家));
			设置引力(事件玩家, 0);
			开始限制阈值(事件玩家, 1, 1, 0, 0, 0, 0);
			施加推力(事件玩家, 面朝方向(事件玩家), 3, 至地图, 取消相反运动);
			施加推力(事件玩家, 上, 1, 至玩家, 合并相反运动);
			等待(0.250, 无视条件);
			If(事件玩家.jingsu_Sel == 2);
				开始限制阈值(事件玩家, 1, 1, 0, 0, 0, 1);
			Else;
				停止限制阈值(事件玩家);
			End;
			设置引力(事件玩家, 100);
	}
}

规则("黑名单")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"素质人员"
		全局.blacklist = 数组(自定义字符串("丿血腥丶兔崽子灬"), 自定义字符串("河南幼儿源小马"), 自定义字符串("雾是风吹不散的伤"), 自定义字符串("莱因哈特"), 自定义字符串("guazi66"), 自定义字符串("叶温"),
			自定义字符串("温情"), 自定义字符串("morri"), 自定义字符串("她味不好总吃辣"), 自定义字符串(""), 自定义字符串(""), 自定义字符串(""));
	}
}

规则("规则")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	动作
	{
		If(数组包含(全局.blacklist, 自定义字符串("{0}", 事件玩家)));
			等待(0.250, 无视条件);
			大字体信息(所有玩家(所有队伍), 自定义字符串("检测到黑名单玩家“{0}”进入游戏，开始执行清除程序", 事件玩家));
			等待(10, 无视条件);
			移除玩家(事件玩家);
		End;
	}
}

规则("无限二段跳")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount >= 5;
		事件玩家.EasterEggCount == 5;
		数量(事件玩家.FoundSecretHero) == 5;
		事件玩家.setting[7] == 0;
		事件玩家.data[5] == 0;
		按钮被按下(事件玩家, 按钮(跳跃)) == 真;
		在墙上(事件玩家) == 假;
		存活(事件玩家) == 真;
		事件玩家.maomao >= 5;
		事件玩家.zhongju != 真;
	}

	动作
	{
		If(首个(事件玩家.data) == 0);
			等待(3, 当为“假”时中止);
			事件玩家.data[0] = 1;
			大字体信息(事件玩家, 自定义字符串("开启无限二段跳"));
			事件玩家.only_maker[2] = 首个(事件玩家.data);
		Else;
			施加推力(事件玩家, 上, 8, 至地图, 取消相反运动);
			等待(0.250, 当为“假”时中止);
			While(按钮被按下(事件玩家, 按钮(跳跃)));
				施加推力(事件玩家, 上, 8, 至地图, 取消相反运动);
				根据条件中止(首个(事件玩家.data) == 0);
				等待(0.250, 当为“假”时中止);
			End;
	}
}

规则("关闭无限二段跳")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount >= 5;
		事件玩家.maomao >= 5;
		首个(事件玩家.data) == 1;
		按钮被按下(事件玩家, 按钮(跳跃)) == 真;
		按钮被按下(事件玩家, 按钮(蹲下)) == 真;
	}

	动作
	{
		等待(1, 当为“假”时中止);
		事件玩家.data[0] = 0;
		大字体信息(事件玩家, 自定义字符串("关闭无限二段跳"));
		事件玩家.only_maker[2] = 首个(事件玩家.data);
	}
}

规则("规则")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	动作
	{
		全局.administrator = 数组(自定义字符串("雷姆"), 自定义字符串("城维大队"), 自定义字符串("白银之鹰"));
	}
}

规则("懒得跑")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		按钮被按下(事件玩家, 按钮(主要攻击模式)) == 真;
		事件玩家.Victory == 假;
	}

	动作
	{
		If(数组包含(全局.chat, 自定义字符串("{0}", 事件玩家)));
			根据条件中止(垂直朝向角度(事件玩家) > -0.750);
			等待(0.100, 无视条件);
			根据条件中止(!按钮被按下(事件玩家, 按钮(装填)));
			事件玩家.file = 4;
			传送(事件玩家, 全局.ZoneLocations[1]);
			事件玩家.ZonesReached = 数组(真, 真, 真, 真);
			事件玩家.HeroesUnlocked = 数组(真, 真, 真, 真);
			事件玩家.FoundSecretHero = 数组(真, 真, 真, 真, 真);
			事件玩家.Abi_1 = 数组(真, 真, 真, 真);
			事件玩家.Abi_2 = 数组(真, 真, 真, 真);
			事件玩家.R_Click = 数组(真, 真, 真, 真);
			事件玩家.PortalUnlocked = 数组(真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真);
			事件玩家.SkillsFound = 数组(真, 真, 真, 真, 真, 真);
			事件玩家.Destination = 数组(真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真);
			调用子程序(Skill_SetUp);
			事件玩家.ZoneCount = 4;
			事件玩家.HeroCount = 4;
			事件玩家.EasterEggCount = 5;
			事件玩家.Victory = 真;
			事件玩家.setting[10] = 0;
			事件玩家.SpeedRunMode = 真;
			事件玩家.Timer = 599;
			事件玩家.data[2] = 1;
			事件玩家.data[3] = 1;
			事件玩家.chatstart = 真;
			事件玩家.chatcount = 5;
			事件玩家.chat1count = 5;
			事件玩家.settingCount = 6;
			事件玩家.setting[0] = 520;
			事件玩家.data[16] = 1;
			事件玩家.er_wai_jing_su[0] = 0;
			设置移动速度(事件玩家, 100);
			事件玩家.CanDie = 假;
			事件玩家.maomao = 5;
			If(事件玩家.jingsu_Sel == 2);
				停止限制阈值(事件玩家);
			End;
			事件玩家.jingsu_Sel = 0;
			事件玩家.EasterEggsFound = 数组(真, 真, 真, 真, 真, 真);
			If(!数组包含(全局.playname, 自定义字符串("{0}", 事件玩家)));
				修改全局变量(playname, 添加至数组, 自定义字符串("{0}", 事件玩家));
			End;
			事件玩家.fileIndex = 数组值的索引(全局.playname, 自定义字符串("{0}", 事件玩家));
			全局.playdata[事件玩家.fileIndex] = 5;
			事件玩家.file = 0;
			If(数组包含(全局.administrator, 自定义字符串("{0}", 事件玩家)));
				事件玩家.data[11] = 1;
				事件玩家.data[23] = 1;
				事件玩家.data[22] = 1;
				事件玩家.data[24] = 1;
				事件玩家.weihezhe = 6;
				事件玩家.maomao = 5;
				事件玩家.tiaozhanzhe = 5;
				事件玩家.data[11] = 1;
				事件玩家.setting[6] = 1;
				事件玩家.data[6] = 1;
				事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 数组(自定义字符串("霍金"), 自定义字符串("假如给我三天光明"), 自定义字符串("源氏的神"), 自定义字符串("捣蛋鬼"), 自定义字符串("世界boss"),
					自定义字符串("一拳超人")));
				事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 数组(颜色(白色), 颜色(白色), 颜色(黄色), 颜色(白色), 颜色(红色), 颜色(黄色)));
			End;
			If(事件玩家.jingsu_Sel != 3);
				事件玩家.Switch = 真;
			End;
			事件玩家.data[0] = 1;
			事件玩家.only_maker[2] = 首个(事件玩家.data);
			事件玩家.only_maker[3] = !事件玩家.CanDie;
			事件玩家.only_maker[4] = !事件玩家.pengzhuang;
			等待(2, 无视条件);
			事件玩家.quiet = 真;
			大字体信息(事件玩家, 事件玩家.quiet ? 自定义字符串("{0}", 数组(自定义字符串("You can't be affected by foreign objects"), 自定义字符串("感受宁静"))[事件玩家.lang]) : 自定义字符串(
				"{0}", 数组(自定义字符串("You can accept the ‘help’ of your teammates"), 自定义字符串("你可以接受队友的“帮助”"))[事件玩家.lang]));
			事件玩家.only_maker[6] = !事件玩家.quiet;
	}
}

规则("隐藏英雄回家")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		(数组包含(全局.ExtraHero, 所用英雄(事件玩家)) || 所用英雄(事件玩家) == 英雄(西格玛)) == 真;
		按钮被按下(事件玩家, 按钮(装填)) == 真;
		按钮被按下(事件玩家, 按钮(主要攻击模式)) == 假;
		按钮被按下(事件玩家, 按钮(蹲下)) == 假;
	}

	动作
	{
		If(按钮被按下(事件玩家, 按钮(装填)));
			If(相距距离(所选位置(事件玩家), 事件玩家.Respawn) > 1);
				传送(事件玩家, 事件玩家.Respawn);
				开始强制设置玩家位置(事件玩家, 所选位置(事件玩家), 假);
				调用子程序(ResetCoolDown);
				停止强制设置玩家位置(事件玩家);
				等待(0.050, 无视条件);
				播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
			Else;
				If(事件玩家.AlternativeRespawn != 空);
					If(相距距离(所选位置(事件玩家), 事件玩家.AlternativeRespawn) > 1);
						传送(事件玩家, 事件玩家.AlternativeRespawn);
						调用子程序(ResetCoolDown);
						事件玩家.Respawn = 事件玩家.AlternativeRespawn;
					Else;
						If(首个(事件玩家.ZonesReached) == 真);
							传送(事件玩家, 全局.ZoneLocations[1]);
						End;
					End;
				End;
			End;
		Else;
			传送(事件玩家, 全局.ZoneLocations[1]);
		End;
		等待(0.500, 无视条件);
	}
}

规则("开始区域按近战加F进入重生室")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.maomao >= 5;
		相距距离(全局.ZoneLocations[1], 所选位置(事件玩家)) <= 3;
		事件玩家.EasterEggCount == 5;
		数量(事件玩家.FoundSecretHero) == 5;
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		按钮被按下(事件玩家, 按钮(近身攻击)) == 真;
		事件玩家.zhongju == 假;
	}

	动作
	{
		传送(事件玩家, 矢量(79.345, 6.686, -33.638));
	}
}

规则("开关无敌")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount >= 5;
		事件玩家.setting[7] != 1;
		事件玩家.data[5] == 0;
		事件玩家.maomao >= 5;
		事件玩家.zhongju != 真;
		按钮被按下(事件玩家, 按钮(近身攻击)) == 真;
	}

	动作
	{
		等待(3, 当为“假”时中止);
		事件玩家.CanDie = !事件玩家.CanDie;
		大字体信息(事件玩家, 事件玩家.CanDie ? 自定义字符串("关闭无敌") : 自定义字符串("开启无敌"));
		等待(0.250, 无视条件);
		治疗(事件玩家, 空, 1000);
		事件玩家.only_maker[3] = !事件玩家.CanDie;
	}
}

规则("安娜给大无敌7.5s")
{
	事件
	{
		玩家受到治疗;
		双方;
		全部;
	}

	条件
	{
		所用英雄(治疗者) == 英雄(安娜);
		事件技能 == 按钮(终极技能);
		受治疗者.CanDie == 真;
	}

	动作
	{
		小字体信息(所有玩家(所有队伍), 自定义字符串("{0}{1}", 自定义字符串("{0}{1}{2}", 英雄图标字符串(英雄(安娜)), 治疗者, 技能图标字符串(英雄(安娜), 按钮(终极技能))), 自定义字符串("{0}{1}", 英雄图标字符串(
			所用英雄(受治疗者)), 受治疗者)));
		播放效果(所有玩家(所有队伍), 有益爆炸, 颜色(蓝色), 受治疗者, 8);
		受治疗者.CanDie = 假;
		等待(7.500, 无视条件);
		受治疗者.CanDie = 真;
	}
}

规则("隐藏球体")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount >= 5;
		按钮被按下(事件玩家, 按钮(蹲下)) == 真;
		按钮被按下(事件玩家, 按钮(装填)) == 真;
		按钮被按下(事件玩家, 按钮(主要攻击模式)) == 假;
		按钮被按下(事件玩家, 按钮(辅助攻击模式)) == 假;
		事件玩家.EasterEggCount == 5;
		数量(事件玩家.FoundSecretHero) == 5;
	}

	动作
	{
		等待(1.500, 当为“假”时中止);
		事件玩家.data[1] = (事件玩家.data[1] + 1) % 2;
		大字体信息(事件玩家, 事件玩家.data[1] == 1 ? 自定义字符串("关闭岩浆显示") : 自定义字符串("开启岩浆显示"));
		等待(3, 无视条件);
		事件玩家.only_maker[5] = 事件玩家.data[1];
	}
}

规则("重生室设置")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		在重生室中(事件玩家) == 真;
		事件玩家.maomao >= 5;
	}

	动作
	{
		If(事件玩家.chatcount >= 5 && 事件玩家.setting[7] == 0 && 事件玩家.data[5] == 0);
			停止强制玩家选择英雄(事件玩家);
			设置玩家可选的英雄(事件玩家, 全部英雄);
			等待(0.250, 无视条件);
			预加载英雄(事件玩家, 全部英雄);
		Else;
			传送(事件玩家, 事件玩家.Respawn);
	}
}

规则("Lava Effect")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		等待(2, 无视条件);
		For 全局变量(LavaLoop, 0, 数量(全局.LavaLocations_3), 1);
			创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.data[1] == 0), 球体, 颜色(亮紫色), (Y方向分量(所选位置(本地玩家)) <= 50 ? 全局.LavaLocations_1 : (Y方向分量(所选位置(本地玩家))
				>= 200 ? 全局.LavaLocations_3 : 全局.LavaLocations_2))[单次赋值(全局.LavaLoop)], (Y方向分量(所选位置(本地玩家)) <= 50 ? 全局.LavaRadius_1 : (Y方向分量(
				所选位置(本地玩家)) >= 200 ? 全局.LavaRadius_3 : 全局.LavaRadius_2))[单次赋值(全局.LavaLoop)], 可见，位置和半径);
			等待(0.050, 无视条件);
		End;
	}
}

规则("绑定玩家")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chat1count >= 5;
		按钮被按下(事件玩家, 按钮(主要攻击模式)) == 真;
		按钮被按下(事件玩家, 按钮(装填)) == 假;
		按钮被按下(事件玩家, 按钮(互动)) == 假;
		按钮被按下(事件玩家, 按钮(蹲下)) == 真;
		事件玩家.playset == 0;
	}

	动作
	{
		等待(0.500, 当为“假”时中止);
		If(事件玩家.play == 空数组);
			事件玩家.play = 射线命中玩家(眼睛位置(事件玩家), 眼睛位置(事件玩家) + 面朝方向(事件玩家) * 100, 所有玩家(所有队伍), 事件玩家, 假);
			根据条件中止(事件玩家.play == 空数组 || 死亡(事件玩家.play) || 事件玩家.play.quiet);
			事件玩家.play.play = 事件玩家;
			事件玩家.play.played = 真;
			事件玩家.played = 真;
			绑定玩家(事件玩家.play, 事件玩家, 矢量(0, 事件玩家.daxiao * 1.750, 0));
			If(事件玩家.play.CanDie == 真);
				事件玩家.play.playset = 1;
				事件玩家.play.CanDie = 假;
			Else;
				事件玩家.play.playset = 2;
			End;
		Else;
			解除绑定(事件玩家.play);
			事件玩家.play.played = 假;
			事件玩家.played = 假;
			If(事件玩家.play.playset == 1);
				事件玩家.play.CanDie = 真;
			End;
			事件玩家.play.playset = 0;
			事件玩家.play.play = 空数组;
			事件玩家.play = 空数组;
	}
}

规则("绑定玩家无了")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.play != 空数组;
		事件玩家.playset == 0;
		相距距离(所选位置(事件玩家), 所选位置(事件玩家.play)) > 事件玩家.daxiao * 1.750 + 0.500;
	}

	动作
	{
		解除绑定(事件玩家.play);
		事件玩家.play.played = 假;
		事件玩家.played = 假;
		If(事件玩家.play.playset == 1);
			事件玩家.play.CanDie = 真;
		End;
		事件玩家.play.playset = 0;
		事件玩家.play.play = 空数组;
		事件玩家.play = 空数组;
	}
}

规则("绑定主体没了")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.play != 空数组;
		事件玩家.playset != 0;
		实体存在(事件玩家.play) == 假;
	}

	动作
	{
		解除绑定(事件玩家);
		If(事件玩家.playset == 1);
			事件玩家.CanDie = 真;
		End;
		事件玩家.play.playset = 0;
		事件玩家.play = 空数组;
	}
}

规则("绑定的玩家要下来")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.playset != 0;
		事件玩家.played == 真;
		按钮被按下(事件玩家, 按钮(蹲下)) == 真;
	}

	动作
	{
		等待(1, 当为“假”时中止);
		解除绑定(事件玩家);
		If(事件玩家.playset == 1);
			事件玩家.CanDie = 真;
		End;
		事件玩家.play.play = 空数组;
		事件玩家.play.played = 假;
		事件玩家.playset = 0;
		事件玩家.played = 假;
		事件玩家.play = 空数组;
	}
}

规则("穿墙")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount >= 5;
		事件玩家.EasterEggCount == 5;
		数量(事件玩家.FoundSecretHero) == 5;
		事件玩家.setting[7] != 1;
		事件玩家.data[5] == 0;
		事件玩家.maomao >= 5;
		事件玩家.zhongju != 真;
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		按钮被按下(事件玩家, 按钮(蹲下)) == 假;
	}

	动作
	{
		等待(2, 当为“假”时中止);
		If(事件玩家.pengzhuang == 真);
			取消与环境的移动碰撞(事件玩家, 假);
			事件玩家.pengzhuang = 假;
			大字体信息(事件玩家, 自定义字符串("已开启穿墙"));
		Else;
			开启与环境的移动碰撞(事件玩家);
			事件玩家.pengzhuang = 真;
			大字体信息(事件玩家, 自定义字符串("已关闭穿墙"));
		End;
		事件玩家.only_maker[4] = !事件玩家.pengzhuang;
	}
}

规则("通关给大")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount >= 5;
		事件玩家.setting[7] != 1;
		事件玩家.data[5] == 0;
		按钮被按下(事件玩家, 按钮(终极技能)) == 真;
		按钮被按下(事件玩家, 按钮(蹲下)) == 真;
		终极技能充能百分比(事件玩家) != 100;
	}

	动作
	{
		设置终极技能充能(事件玩家, 100);
	}
}

规则("hud")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建HUD文本(已过滤的数组(本地玩家, 本地玩家.chatstart == 真 && 本地玩家.only_maker[9] == 0 && 当前数组元素.chat1count < 5), 空, 空, 自定义字符串(
			"额外彩蛋:\r\n{0} / 5\r\n额外隐藏彩蛋:\r\n{1} / 5", 本地玩家.chatcount, 本地玩家.chat1count), 左边, 99, 空, 空, 颜色(蓝色), 可见和字符串, 默认可见度);
	}
}

规则("额外隐藏位置")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.chatLocation = 数组(矢量(14.940, 14.663, -15.295), 矢量(13.222, 21.084, -21.370), 矢量(2.096, 324.241, 266.395), 矢量(26.308, 25.500,
			-34.797), 矢量(9, 30, -55.957));
		创建效果(本地玩家.chatstart && 所用英雄(本地玩家) == 全局.HeroRoster[本地玩家.chatcount] ? 本地玩家 : 空数组, 有害光环, 颜色(蓝色), 全局.chatLocation[本地玩家.chatcount], 1,
			可见，位置和半径);
	}
}

规则("开始魔改内容")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatstart != 真;
		事件玩家.EasterEggCount == 5;
		数量(已过滤的数组(事件玩家.FoundSecretHero, 当前数组元素 == 真)) == 5;
	}

	动作
	{
		事件玩家.chatstart = 真;
		大字体信息(事件玩家, 自定义字符串("自动存档：原版全部内容"));
		全局.playdata[事件玩家.fileIndex] = 2;
	}
}

规则("捡到额额额外彩蛋")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		事件玩家.chatstart == 真;
		所用英雄(事件玩家) == 全局.HeroRoster[事件玩家.chatcount];
		事件玩家.chatcount < 5;
		相距距离(眼睛位置(事件玩家), 全局.chatLocation[事件玩家.chatcount]) < 1;
	}

	动作
	{
		事件玩家.chatcount += 1;
		播放效果(所有玩家(所有队伍), 正面状态施加声音, 颜色(白色), 事件玩家, 99);
	}
}

规则("权限彩蛋")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount >= 5;
		事件玩家.chat1count >= 5;
	}

	动作
	{
		全局.maomao = 数组(矢量(-0.900, 9.150, -70.470), 矢量(14.600, 288, 273.600), 矢量(-2.230, 258.480, 256.690), 矢量(-89.260, 96.600, 135.130),
			矢量(-88.910, 97, 132.430));
		创建效果(本地玩家.chatstart && 所用英雄(本地玩家) == 全局.HeroRoster[本地玩家.maomao] ? 本地玩家 : 空数组, 有害光环, 颜色(蓝色), 全局.maomao[本地玩家.maomao], 1, 可见，位置和半径);
	}
}

规则("权限彩蛋拾取")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		事件玩家.chatstart == 真;
		所用英雄(事件玩家) == 全局.HeroRoster[事件玩家.maomao];
		事件玩家.chat1count >= 5;
		事件玩家.maomao < 5;
		相距距离(眼睛位置(事件玩家), 全局.maomao[事件玩家.maomao]) < 1.200;
	}

	动作
	{
		事件玩家.maomao += 1;
		播放效果(所有玩家(所有队伍), 正面状态施加声音, 颜色(白色), 事件玩家, 99);
		调用子程序(Skill_SetUp);
	}
}

规则("权限hud")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建HUD文本(已过滤的数组(本地玩家, 本地玩家.chatstart == 真 && 本地玩家.only_maker[9] == 0 && 当前数组元素.chat1count > 5), 自定义字符串("权限彩蛋:{0} / 5", 本地玩家.maomao),
			空, 空, 左边, 0, 颜色(蓝色), 空, 颜色(蓝色), 可见和字符串, 默认可见度);
	}
}

规则("最终上房穿墙")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		相距距离(眼睛位置(事件玩家), 矢量(-16.700, 276.200, 346.100)) < 2;
	}

	动作
	{
		取消与环境的移动碰撞(事件玩家, 真);
		等待直到 (相距距离(眼睛位置(事件玩家), 矢量(-16.700, 276.200, 346.100)) > 2, 99999);
		开启与环境的移动碰撞(事件玩家);
	}
}

规则("权限源禁用s")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		事件玩家.Victory == 真;
	}

	动作
	{
		等待(0.250, 无视条件);
		If(事件玩家.maomao == 3);
			设置启用技能 1(事件玩家, 假);
			设置启用终极技能(事件玩家, 假);
	}
}

规则("挑战者源禁用")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		事件玩家.Victory == 真;
	}

	动作
	{
		等待(0.250, 无视条件);
		If(事件玩家.tiaozhanzhe == 3);
			设置启用技能 2(事件玩家, 假);
			设置启用技能 1(事件玩家, 假);
			设置启用终极技能(事件玩家, 假);
	}
}

规则("终局彩蛋位置")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatcount >= 5;
		事件玩家.chat1count >= 5;
		事件玩家.maomao >= 5;
		事件玩家.zhongju == 真;
	}

	动作
	{
		全局.tiaozhanzhe = 数组(矢量(-13, 275.300, 275.500), 矢量(1.610, 15.500, -69.600), 矢量(-49.230, 96, 135.260), 矢量(-66, 101.960, 140.710), 矢量(
			-90.260, 96.730, 143.920));
		全局.weihelocation = 数组(矢量(-89.150, 97.110, 136), 矢量(17.160, 267.800, 341.400), 矢量(68.480, 100, 136.340), 矢量(51.010, 104.700,
			124.200), 矢量(22.450, 101.540, 134.450), 矢量(-24.080, 274.300, 282.930));
		创建效果(本地玩家.chatstart && 所用英雄(本地玩家) == 全局.HeroRoster[0] ? 本地玩家 : 空数组, 有害光环, 颜色(蓝色), 全局.weihelocation[本地玩家.weihezhe], 1, 可见，位置和半径);
		创建效果(本地玩家.chatstart && 所用英雄(本地玩家) == 全局.HeroRoster[本地玩家.tiaozhanzhe] ? 本地玩家 : 空数组, 有害光环, 颜色(蓝色), 全局.tiaozhanzhe[本地玩家.tiaozhanzhe],
			1, 可见，位置和半径);
	}
}

规则("挑战者拾取")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		事件玩家.chatstart == 真;
		所用英雄(事件玩家) == 全局.HeroRoster[事件玩家.tiaozhanzhe];
		事件玩家.chat1count >= 5;
		事件玩家.maomao >= 5;
		事件玩家.tiaozhanzhe < 5;
		事件玩家.zhongju == 真;
		相距距离(眼睛位置(事件玩家), 全局.tiaozhanzhe[事件玩家.tiaozhanzhe]) < 1.200;
	}

	动作
	{
		If(事件玩家.tiaozhanzhe == 3);
			等待(5, 当为“假”时中止);
			事件玩家.tiaozhanzhe += 1;
			播放效果(所有玩家(所有队伍), 正面状态施加声音, 颜色(白色), 事件玩家, 99);
			调用子程序(Skill_SetUp);
		Else If(事件玩家.tiaozhanzhe == 4);
			等待(5, 当为“假”时中止);
			事件玩家.tiaozhanzhe += 1;
			播放效果(所有玩家(所有队伍), 正面状态施加声音, 颜色(白色), 事件玩家, 99);
			调用子程序(Skill_SetUp);
		Else If(事件玩家.tiaozhanzhe == 5);
			事件玩家.zhongju = 假;
			事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 自定义字符串("“终局挑战者”"));
			事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 颜色(红色));
			事件玩家.cheng_hao[0] = 数量(事件玩家.cheng_hao[1] - 1);
			大字体信息(所有玩家(所有队伍), 自定义字符串("{0}拿到了终局门票！！", 事件玩家));
		Else;
			事件玩家.tiaozhanzhe += 1;
			播放效果(所有玩家(所有队伍), 正面状态施加声音, 颜色(白色), 事件玩家, 99);
			调用子程序(Skill_SetUp);
		End;
	}
}

规则("维和者拾取")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		事件玩家.chatstart == 真;
		所用英雄(事件玩家) == 全局.HeroRoster[0];
		事件玩家.chat1count >= 5;
		事件玩家.maomao >= 5;
		事件玩家.weihezhe <= 6;
		事件玩家.zhongju == 真;
		相距距离(眼睛位置(事件玩家), 全局.weihelocation[事件玩家.weihezhe]) < 1.200;
	}

	动作
	{
		If(事件玩家.weihezhe != 6);
			事件玩家.weihezhe += 1;
			播放效果(所有玩家(所有队伍), 正面状态施加声音, 颜色(白色), 事件玩家, 99);
			调用子程序(Skill_SetUp);
	}
}

规则("规则")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.weihezhe == 6;
	}

	动作
	{
		事件玩家.zhongju = 假;
		传送(事件玩家, 全局.ZoneLocations[0]);
		事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 自定义字符串("“警长”"));
		事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 颜色(蓝色));
		事件玩家.cheng_hao[0] = 数量(事件玩家.cheng_hao[1] - 1);
		大字体信息(所有玩家(所有队伍), 自定义字符串("{0}收集了全部维和者碎片 成为了新的警长！", 事件玩家));
	}
}

规则("终局进度hud")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建HUD文本(已过滤的数组(本地玩家, 本地玩家.chatstart == 真 && 本地玩家.only_maker[9] == 0 && 当前数组元素.maomao == 5), 自定义字符串(
			"  ==终局进度==\r\n挑战者:{0} / 5\r\n维和者：{1}/6\r\n{2}", 本地玩家.tiaozhanzhe, 本地玩家.weihezhe, 自定义字符串("安娜娜挑战：{0}/1\r\nDJ科目二：{1}/1\r\n{2}",
			本地玩家.data[6], 本地玩家.data[11], 自定义字符串("仓鼠挑战：{0}/1", 本地玩家.setting[6]))), 空, 空, 左边, 99, 颜色(红色), 空, 颜色(红色), 可见和字符串, 默认可见度);
	}
}

规则("终局开启")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		事件玩家.maomao >= 5;
		相距距离(事件玩家, 全局.zhongjuloction) <= 3;
		按钮被按下(事件玩家, 按钮(辅助攻击模式)) == 真;
	}

	动作
	{
		等待(2, 当为“假”时中止);
		事件玩家.zhongju = 真;
		事件玩家.CanDie = 真;
		事件玩家.pengzhuang = 真;
		开启与环境的移动碰撞(事件玩家);
		播放效果(所有玩家(所有队伍), 状态爆炸声音, 颜色(白色), 所选位置(事件玩家), 100);
	}
}

规则("终局栏2")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.maomao >= 5), 自定义字符串("终局挑战"), 全局.zhongjuloction, 4, 根据表面截取, 可见，位置和字符串, 颜色(红色), 默认可见度);
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.mianban[2] == 1), 自定义字符串("    长按{0}开启终局挑战\r\n\r\n 进入挑战 失去权限\r\n （难度一般，进阶挑战）", 输入绑定字符串(按钮(
			辅助攻击模式))), 空, 空, 顶部, 7, 颜色(红色), 颜色(红色), 颜色(红色), 可见和字符串, 默认可见度);
	}
}

规则("花男")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		生命之梭;
	}

	动作
	{
		设置启用技能 2(事件玩家, 假);
	}
}

规则("改变大小")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chat1count >= 5;
		事件玩家.maomao >= 5;
		事件玩家.setting[7] != 1;
		事件玩家.zhongju == 假;
		事件玩家.data[5] == 0;
		按钮被按下(事件玩家, 按钮(蹲下)) == 真;
		按钮被按下(事件玩家, 按钮(互动)) == 真;
		数组包含(全局.chat, 自定义字符串("{0}", 事件玩家)) == 真;
		(按钮被按下(事件玩家, 按钮(主要攻击模式)) || 按钮被按下(事件玩家, 按钮(辅助攻击模式))) == 真;
	}

	动作
	{
		If(事件玩家.daxiao <= 1);
			If(按钮被按下(事件玩家, 按钮(主要攻击模式)));
				根据条件中止(事件玩家.daxiao <= 0.100);
				事件玩家.daxiao -= 0.100;
			Else;
				事件玩家.daxiao += 事件玩家.daxiao == 1 ? 1 : 0.100;
			End;
		Else;
			If(按钮被按下(事件玩家, 按钮(主要攻击模式)));
				事件玩家.daxiao -= 1;
			Else;
				根据条件中止(事件玩家.daxiao >= 2);
				事件玩家.daxiao += 1;
			End;
		End;
		小字体信息(事件玩家, 自定义字符串("当前大小:{0}", 事件玩家.daxiao));
	}
}

规则("额外英雄的额外彩蛋")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.ExtraHeroEggLocation = 数组(矢量(699.557, 731.767, -652.697), 矢量(-40.910, 420, 323.040), 矢量(-42.004, 30.216, -14.005), 矢量(-276.465,
			-8.943, 481.465), 矢量(48.280, 7.677, 1.786));
		全局.ExtraHeroEggLocation[0] = 数组随机取值(数组(矢量(699.557, 731.767, -652.697), 矢量(-936.809, 21.727, -1000)));
		创建效果(本地玩家.chatcount == 5 && 所用英雄(本地玩家) == 全局.ExtraHero[本地玩家.chat1count] ? 本地玩家 : 空数组, 有害光环, 颜色(黄色),
			全局.ExtraHeroEggLocation[本地玩家.chat1count], 0.500, 可见，位置和半径);
	}
}

规则("捡到隐藏额额额外彩蛋")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		事件玩家.chatstart == 真;
		事件玩家.chatcount == 5;
		所用英雄(事件玩家) == 全局.ExtraHero[事件玩家.chat1count];
		事件玩家.chat1count < 5;
		相距距离(眼睛位置(事件玩家), 全局.ExtraHeroEggLocation[事件玩家.chat1count]) < 1;
	}

	动作
	{
		事件玩家.chat1count += 1;
		播放效果(所有玩家(所有队伍), 正面状态施加声音, 颜色(白色), 事件玩家, 99);
	}
}

规则("封球位置与半径")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.no_pass[0] = 数组(英雄(布丽吉塔), 英雄(源氏));
		全局.no_pass[1] = 数组(数组(矢量(-48.408, 7.448, 13.106), 矢量(15.106, 10.722, -14.044)), 数组(矢量(25.884, 7.177, -27.301)));
		全局.no_pass[2] = 数组(数组(6, 5), 数组(3));
	}
}

规则("切换英雄获取封球数据")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.play_date[1] != 所用英雄(事件玩家);
		事件玩家.chatstart == 真;
		事件玩家.chatcount < 5;
		数组包含(首个(全局.no_pass), 所用英雄(事件玩家)) == 真;
	}

	动作
	{
		事件玩家.play_date[1] = 所用英雄(事件玩家);
		事件玩家.play_date[2] = 全局.no_pass[1][数组值的索引(全局.no_pass[0], 所用英雄(事件玩家))];
		事件玩家.play_date[3] = 全局.no_pass[2][数组值的索引(全局.no_pass[0], 所用英雄(事件玩家))];
	}
}

规则("封球效果")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建效果(已过滤的数组(本地玩家, 数量(当前数组元素.play_date[2]) > 0), 球体, 颜色(红色), 首个(已排序的数组(本地玩家.play_date[2], 相距距离(所选位置(本地玩家), 当前数组元素))),
			本地玩家.play_date[3][数组值的索引(本地玩家.play_date[2], 首个(已排序的数组(本地玩家.play_date[2], 相距距离(所选位置(本地玩家), 当前数组元素))))], 可见，位置和半径);
	}
}

规则("球击杀")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.CanDie == 真;
		事件玩家.chatstart == 真;
		事件玩家.chatcount < 5;
		数组包含(首个(全局.no_pass), 所用英雄(事件玩家)) == 真;
		相距距离(眼睛位置(事件玩家), 首个(已排序的数组(事件玩家.play_date[2], 相距距离(眼睛位置(事件玩家), 当前数组元素)))) < 事件玩家.play_date[3][数组值的索引(事件玩家.play_date[2], 首个(已排序的数组(
			事件玩家.play_date[2], 相距距离(眼睛位置(事件玩家), 当前数组元素))))];
	}

	动作
	{
		击杀(事件玩家, 空);
	}
}

规则("额外彩蛋源氏禁用shft")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		事件玩家.chatcount == 3;
	}

	动作
	{
		等待(0.250, 无视条件);
		设置启用技能 1(事件玩家, 假);
		设置启用技能 2(事件玩家, 真);
	}
}

规则("源氏E推力")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		正在使用技能 2(事件玩家) == 真;
	}

	动作
	{
		施加推力(事件玩家, 上, 2, 至地图, 取消相反运动);
	}
}

规则("提示乘客下车")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.playset != 0;
	}

	动作
	{
		等待(2, 当为“假”时中止);
		小字体信息(事件玩家, 自定义字符串("长按蹲下车"));
		循环;
	}
}

规则("存档hud")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.fileText = 数组(自定义字符串("解锁全部区域和英雄"), 自定义字符串("解锁全部区域和英雄 \r\n解锁隐藏英雄和西格玛"), 自定义字符串("解锁原版内容 \r\n5个额外彩蛋"), 自定义字符串("解锁游戏全部内容"), 自定义字符串(
			"解锁游戏全部内容\r\n(包括空气彩蛋)"));
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.file != 0), 自定义字符串(
			"    你有一份自动存档 \r\n存档内容: \r\n {0} \r\n按 {1} 键读取，按 {2} 键不读取 \r\n 不读取存档 \r\n存档将清除", 全局.fileText[本地玩家.file - 1], 输入绑定字符串(按钮(终极技能)),
			输入绑定字符串(按钮(装填))), 空, 空, 顶部, 999, 颜色(蓝色), 空, 空, 可见和字符串, 默认可见度);
	}
}

规则("玩家加入比赛(存档系统)")
{
	事件
	{
		玩家加入比赛;
		双方;
		全部;
	}

	动作
	{
		事件玩家.fileIndex = 数组值的索引(全局.playname, 自定义字符串("{0}", 事件玩家));
		事件玩家.file = 全局.playdata[事件玩家.fileIndex];
		If(事件玩家.file != 0);
			等待直到 (已重生(事件玩家), 99999);
			等待(0.250, 无视条件);
			开始强制设置玩家位置(事件玩家, 所选位置(事件玩家), 假);
			等待直到 (按钮被按下(事件玩家, 按钮(终极技能)) || 按钮被按下(事件玩家, 按钮(装填)), 99999);
			If(按钮被按下(事件玩家, 按钮(终极技能)));
				事件玩家.Victory = 真;
				事件玩家.ZonesReached = 数组(真, 真, 真, 真);
				事件玩家.HeroesUnlocked = 数组(真, 真, 真, 真);
				事件玩家.ZoneCount = 4;
				事件玩家.HeroCount = 4;
				事件玩家.PortalUnlocked = 数组(真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真);
				事件玩家.Destination = 数组(真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真, 真);
				事件玩家.Abi_1 = 数组(真, 真, 真, 真);
				事件玩家.Abi_2 = 数组(真, 假, 假, 假);
				事件玩家.R_Click = 数组(假, 真, 真, 真);
				事件玩家.SkillsFound = 数组(真, 真, 真, 真, 真, 真);
				If(事件玩家.file >= 2);
					事件玩家.chatstart = 真;
					事件玩家.FoundSecretHero = 数组(真, 真, 真, 真, 真);
					事件玩家.EasterEggsFound = 数组(真, 真, 真, 真, 真, 真);
					事件玩家.EasterEggCount = 5;
				End;
				If(事件玩家.file >= 3);
					事件玩家.chatcount = 5;
				End;
				If(事件玩家.file >= 4);
					事件玩家.chat1count = 5;
					事件玩家.Abi_2 = 数组(真, 真, 真, 真);
				End;
				If(事件玩家.file >= 5);
					事件玩家.settingCount = 6;
					事件玩家.setting[0] = 520;
				End;
				停止强制设置玩家位置(事件玩家);
				事件玩家.file = 0;
				调用子程序(Skill_SetUp);
				传送(事件玩家, 全局.ZoneLocations[1]);
			Else;
				事件玩家.file = 0;
				停止强制设置玩家位置(事件玩家);
	}
}

规则("声音切换")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		首个(事件玩家.setting) == 520;
		按钮被按下(事件玩家, 按钮(装填)) == 真;
		按钮被按下(事件玩家, 按钮(蹲下)) == 真;
		数组包含(全局.chat, 自定义字符串("{0}", 事件玩家)) == 真;
		(按钮被按下(事件玩家, 按钮(主要攻击模式)) || 按钮被按下(事件玩家, 按钮(辅助攻击模式))) == 真;
	}

	动作
	{
		If(按钮被按下(事件玩家, 按钮(主要攻击模式)));
			根据条件中止(事件玩家.shenying <= 0.500);
			事件玩家.shenying -= 0.100;
		Else;
			根据条件中止(事件玩家.shenying >= 1.500);
			事件玩家.shenying += 0.100;
		End;
		小字体信息(事件玩家, 自定义字符串("{0}", 数组(自定义字符串("Current volume: {0} (upper limit 1.5, lower limit 0.5)", 事件玩家.shenying), 自定义字符串(
			"当前音量： {0}（上限 1.5，下限 0.5）", 事件玩家.shenying))[事件玩家.lang]));
	}
}

规则("空气彩蛋位置")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.settingLocation = 数组(矢量(-0.637, 7.345, -8.126), 矢量(71.062, 95.165, 145.627), 矢量(54.628, 265.719, 335.821), 矢量(-0.087, 271.104,
			333.345), 矢量(-65.738, 3.051, -6.058), 矢量(0.010, 156.034, 150.041));
	}
}

规则("捡到空气彩蛋")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.settingCount < 6;
		事件玩家.chat1count >= 5;
		数量(已过滤的数组(全局.settingLocation, 相距距离(眼睛位置(事件玩家), 当前数组元素) <= 0.500)) > 0;
	}

	动作
	{
		事件玩家.settingIndex = 数组值的索引(全局.settingLocation, 已过滤的数组(全局.settingLocation, 相距距离(眼睛位置(事件玩家), 当前数组元素) <= 0.500));
		If(事件玩家.settingIndex == 0);
			If(事件玩家.settingCount == 0);
				事件玩家.setting[0] += 500;
			Else;
				事件玩家.setting[0] += 9999;
			End;
		Else If(事件玩家.settingIndex == 1);
			If(事件玩家.settingCount == 1);
				事件玩家.setting[0] *= 2;
			Else;
				事件玩家.setting[0] -= 9999;
			End;
		Else If(事件玩家.settingIndex == 2);
			If(事件玩家.settingCount == 2);
				事件玩家.setting[0] -= 300;
			Else;
				事件玩家.setting[0] = 0;
			End;
		Else If(事件玩家.settingIndex == 3);
			事件玩家.setting[0] -= 200;
		Else If(事件玩家.settingIndex == 4);
			If(事件玩家.settingCount != 4);
				事件玩家.setting[0] += 750;
			Else If(事件玩家.settingCount == 5);
				事件玩家.setting[0] += 100;
			Else;
				事件玩家.setting[0] += 10;
			End;
		Else;
			事件玩家.setting[0] = 首个(事件玩家.setting) * 2 - 500;
		End;
		大字体信息(事件玩家, 自定义字符串("{0}", 首个(事件玩家.setting)));
		事件玩家.settingCount += 1;
		等待(5, 无视条件);
	}
}

规则("路霸")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		路霸;
	}

	条件
	{
		事件玩家.chat1count >= 5;
		首个(事件玩家.setting) == 520;
		正在使用技能 1(事件玩家) == 真;
	}

	动作
	{
		等待(0.100, 无视条件);
		根据条件中止(射线命中玩家(眼睛位置(事件玩家), 眼睛位置(事件玩家) + 面朝方向(事件玩家) * 30, 所有玩家(所有队伍), 事件玩家, 假).quiet == 真);
		传送(射线命中玩家(眼睛位置(事件玩家), 眼睛位置(事件玩家) + 面朝方向(事件玩家) * 30, 所有玩家(所有队伍), 事件玩家, 假), 所选位置(事件玩家) + 归一化(面朝方向(事件玩家)) * 矢量(1, 0, 1));
	}
}

规则("存档检测5")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		全局.playdata[事件玩家.fileIndex] != 4;
		事件玩家.chatcount == 5;
		首个(事件玩家.setting) == 0;
		事件玩家.file == 0;
	}

	动作
	{
		大字体信息(事件玩家, 自定义字符串("{0}", 数组(自定义字符串("自动存档：游戏原版内容\r\n5个额外彩蛋"), 自定义字符串("Automatically archived: game content \r\n5 extra eggs"))
			[事件玩家.lang]));
		全局.playdata[事件玩家.fileIndex] = 3;
	}
}

规则("存档检测3")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		全局.playdata[事件玩家.fileIndex] != 4;
		事件玩家.chat1count == 5;
		首个(事件玩家.setting) == 0;
		事件玩家.file == 0;
	}

	动作
	{
		大字体信息(事件玩家, 自定义字符串("{0}", 数组(自定义字符串("自动存档：游戏全部内容"), 自定义字符串("Autoarchived: All contents of the game"))[事件玩家.lang]));
		全局.playdata[事件玩家.fileIndex] = 4;
		事件玩家.Abi_2 = 数组(真, 真, 真, 真);
	}
}

规则("存档检测4")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		全局.playdata[事件玩家.fileIndex] != 5;
		首个(事件玩家.setting) == 520;
		事件玩家.file == 0;
	}

	动作
	{
		大字体信息(事件玩家, 自定义字符串("{0}", 数组(自定义字符串("自动存档：游戏全部内容\r\n(包括空气彩蛋)"), 自定义字符串(
			"Autoarchived: All contents of the game \r\n (including air eggs)"))[事件玩家.lang]));
		全局.playdata[事件玩家.fileIndex] = 5;
	}
}

规则("防止工坊吞源氏E冷却")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		技能冷却时间(事件玩家, 按钮(技能2)) > 1;
	}

	动作
	{
		设置技能冷却(事件玩家, 按钮(技能2), 1);
	}
}

规则("西格玛")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		西格玛;
	}

	条件
	{
		正在使用终极技能(事件玩家) == 真;
		按钮被按下(事件玩家, 按钮(主要攻击模式)) == 真;
	}

	动作
	{
		等待(0.500, 无视条件);
		已过滤的数组(范围内玩家(射线命中位置(眼睛位置(事件玩家), 眼睛位置(事件玩家) + 面朝方向(事件玩家) * 100, 所有玩家(所有队伍), 事件玩家, 假), 7.500, 所有队伍, 关闭), 当前数组元素.quiet == 假)
			.setting[2] = 1;
		等待直到 (!正在使用终极技能(事件玩家), 99999);
	}
}

规则("西格玛")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.setting[2] == 1;
	}

	动作
	{
		设置引力(事件玩家, 0);
		施加推力(事件玩家, 上, 6, 至地图, 取消相反运动);
		等待(3, 无视条件);
		设置引力(事件玩家, 100);
		事件玩家.setting[2] = 0;
	}
}

规则("大锤带人")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		莱因哈特;
	}

	条件
	{
		首个(事件玩家.setting) == 520;
		正在使用技能 1(事件玩家) == 真;
		事件玩家.setting[3] == 0;
		数量(从数组中移除(范围内玩家(所选位置(事件玩家) + 面朝方向(事件玩家) * 矢量(1, 0, 1), 0.750, 所有队伍, 关闭), 事件玩家)) > 0;
	}

	动作
	{
		事件玩家.setting[3] = 从数组中移除(范围内玩家(所选位置(事件玩家) + 面朝方向(事件玩家) * 矢量(1, 0, 1), 0.750, 所有队伍, 关闭), 事件玩家);
		事件玩家.setting[3] = 已过滤的数组(事件玩家.setting[3], 当前数组元素.quiet == 假);
		If(事件玩家.setting[3] == 空数组);
			事件玩家.setting[3] = 0;
			中止;
		End;
		If(数量(事件玩家.setting[3] > 1));
			事件玩家.setting[3] = 数组随机取值(事件玩家.setting[3]);
		End;
		事件玩家.setting[4] = 事件玩家.setting[3].CanDie;
		If(事件玩家.setting[4] == 真);
			事件玩家.setting[3].CanDie = 假;
		End;
		绑定玩家(事件玩家.setting[3], 事件玩家, 归一化(面朝方向(事件玩家)));
		等待直到 (!正在使用技能 1(事件玩家), 99999);
		解除绑定(事件玩家.setting[3]);
		If(事件玩家.setting[4] == 真);
			事件玩家.setting[3].CanDie = 真;
		End;
		事件玩家.setting[3] = 0;
	}
}

规则("无法被影响")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.jingsu_Sel < 2;
		正在使用表情交流(事件玩家) == 真;
		按钮被按下(事件玩家, 按钮(互动)) == 真;
	}

	动作
	{
		事件玩家.quiet = !事件玩家.quiet;
		大字体信息(事件玩家, 事件玩家.quiet ? 自定义字符串("{0}", 数组(自定义字符串("感受宁静"), 自定义字符串("You can't be affected by foreign objects"))[事件玩家.lang]) : 自定义字符串(
			"{0}", 数组(自定义字符串("你可以接受队友的“帮助”"), 自定义字符串("You can accept the ‘help’ of your teammates"))[事件玩家.lang]));
		事件玩家.only_maker[6] = !事件玩家.quiet;
		等待(6, 无视条件);
	}
}

规则("仓鼠位置")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		"6：是否完成仓鼠挑战，7：是否开始仓鼠挑战，8：位置索引，9：落地死 10：箭头是否显示"
		全局.cangsuLocation = 数组(矢量(1.124, 2.098, -77.474), 矢量(60.458, 9.082, -8.489), 矢量(17.873, 98.326, 183.445), 矢量(6.781, 98.123,
			173.452), 矢量(0.005, 96.098, 106.818), 矢量(19.055, 91.340, 126.863), 矢量(15.931, 95.137, 112.236), 矢量(58.855, 94.115, 138.422),
			矢量(42.960, 84.200, 171.670));
		全局.cangsuRadius = 数组(2.500, 2.500, 2.200, 2.500, 2.500, 2.500, 2.500, 2.500);
		修改全局变量(Point, 添加至数组, 全局.cangsuLocation);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.setting[9] == 1), 环, 颜色(绿色), 全局.cangsuLocation[本地玩家.setting[8] - 1],
			全局.cangsuRadius[本地玩家.setting[8] - 1], 可见，位置和半径);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.setting[7] == 1), 云, 颜色(绿色), 全局.cangsuLocation[本地玩家.setting[8]], 1, 可见，位置和半径);
	}
}

规则("仓鼠箭头")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		事件玩家.setting[7] != 0;
		相距距离(全局.Point[数量(事件玩家.Destination)], 所选位置(事件玩家)) < 1;
	}

	动作
	{
		修改玩家变量(事件玩家, Destination, 添加至数组, 真);
		事件玩家.setting[8] += 1;
		If(事件玩家.setting[8] == 1);
			事件玩家.setting[9] = 1;
			设置辅助攻击模式启用(事件玩家, 真);
			大字体信息(事件玩家, 自定义字符串("{0}", 数组(自定义字符串("落地死已开启"), 自定义字符串("If you land, you will die"))[事件玩家.lang]));
		Else If(事件玩家.setting[8] == 3);
			可用按钮(事件玩家, 按钮(蹲下));
			设置辅助攻击模式启用(事件玩家, 假);
		Else If(事件玩家.setting[8] == 4);
			设置辅助攻击模式启用(事件玩家, 真);
		Else If(事件玩家.setting[8] == 6);
			事件玩家.setting[9] = 0;
			大字体信息(事件玩家, 自定义字符串("{0}", 数组(自定义字符串("落地死已关闭"), 自定义字符串("You won't die if you land"))[事件玩家.lang]));
			事件玩家.setting[8] += 1;
			修改玩家变量(事件玩家, Destination, 添加至数组, 真);
		Else If(事件玩家.setting[8] == 8);
			设置启用技能 2(事件玩家, 真);
		Else If(事件玩家.setting[8] == 9);
			事件玩家.setting[6] = 1;
			事件玩家.setting[7] = 0;
			事件玩家.setting[8] = 0;
			事件玩家.setting[9] = 0;
			事件玩家.setting[10] = 0;
			大字体信息(所有玩家(所有队伍), 自定义字符串("{0}", 数组(自定义字符串("{0}完成仓鼠挑战", 事件玩家), 自定义字符串("{0}Completed hamster challenge", 事件玩家))[事件玩家.lang]));
			传送(事件玩家, 全局.ZoneLocations[1]);
			事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 自定义字符串("“仓鼠跳弹”"));
			事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 自定义颜色(255, 182, 193, 255));
			事件玩家.cheng_hao[0] = 数量(事件玩家.cheng_hao[1] - 1);
			大字体信息(所有玩家(所有队伍), 自定义字符串("{0}通关了 仓鼠挑战！！！", 事件玩家));
	}
}

规则("仓鼠落地死")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.setting[7] == 1;
		事件玩家.setting[9] == 1;
		在地面上(事件玩家) == 真;
		相距距离(全局.cangsuLocation[事件玩家.setting[8] - 1], 所选位置(事件玩家)) > 全局.cangsuRadius[事件玩家.setting[8] - 1];
	}

	动作
	{
		击杀(事件玩家, 空);
	}
}

规则("科目二位置")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.DJlocation[0] = 矢量(75.700, 97.740, 145.160);
		全局.DJlocation[1] = 矢量(-20.280, 97.180, 135.270);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.tiaozhanpanding[0] == 1), 环, 颜色(绿色), 全局.DJlocation[0], 1.500, 可见，位置和半径);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.tiaozhanpanding[0] == 1), 环, 颜色(绿色), 全局.DJlocation[1], 1.500, 可见，位置和半径);
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.tiaozhanpanding[0] == 1), 自定义字符串("DJ科目二有限时哦，按住蹲下+换弹可开关岩浆"), 空, 空, 顶部, 999, 颜色(绿色), 颜色(绿色), 颜色(
			绿色), 可见和字符串, 默认可见度);
		创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.tiaozhanpanding[0] == 1), 自定义字符串("推倒他们！！！"), 全局.DJlocation[1], 3, 根据表面截取, 可见，位置和字符串, 颜色(红色),
			默认可见度);
	}
}

规则("科目二")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.tiaozhanpanding[0] == 1;
		相距距离(眼睛位置(事件玩家), 全局.DJlocation[1]) < 1.500;
	}

	动作
	{
		事件玩家.tiaozhanpanding[0] = 0;
		播放效果(所有玩家(所有队伍), 有益爆炸, 颜色(蓝色), 事件玩家, 10);
		事件玩家.data[11] = 1;
		大字体信息(所有玩家(所有队伍), 自定义字符串(" \r\n{0} {1}!", 事件玩家, 自定义字符串("恭喜！，允许去竞技推推乐！")));
		事件玩家.zhongju = 假;
		击杀(事件玩家, 空);
		事件玩家.Respawn = 全局.ZoneLocations[1];
		传送(事件玩家, 全局.ZoneLocations[1]);
		事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 自定义字符串("“青蛙王子”"));
		事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 颜色(绿色));
		事件玩家.cheng_hao[0] = 数量(事件玩家.cheng_hao[1] - 1);
	}
}

规则("科目二")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.tiaozhanpanding[0] == 1;
		相距距离(眼睛位置(事件玩家), 全局.DJlocation[0]) > 1.500;
	}

	动作
	{
		等待(8, 当为“假”时中止);
		击杀(事件玩家, 空);
		事件玩家.Respawn = 全局.DJlocation[0];
		传送(事件玩家, 全局.DJlocation[0]);
	}
}

规则("铁拳跑酷效果")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.data[5] == 1), 环, 颜色(蓝色), 全局.tiequanLocation[本地玩家.tiequanlevel], 1, 可见，位置和半径);
		创建效果(已过滤的数组(所有玩家(所有队伍), 当前数组元素.data[5] == 1), 环, 颜色(黄色), 全局.tiequanLocation[本地玩家.tiequanlevel + 1], 1, 可见，位置和半径);
		创建地图文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.data[5] == 1), 自定义字符串("anna"), 全局.tiequanLocation[本地玩家.tiequanlevel + 1], 2, 不要截取, 可见，位置和字符串, 颜色(
			白色), 默认可见度);
	}
}

规则("安娜挑战hud")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建进度条HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.data[5] == 1), 本地玩家.tiequanlevel / (数量(全局.tiequanLocation) - 1) * 100, 自定义字符串(
			"安娜娜挑战进度：{0}/{1}", 本地玩家.tiequanlevel, 数量(全局.tiequanLocation) - 1), 顶部, -10, 颜色(蓝色), 颜色(绿色), 可见，值和颜色, 默认可见度);
	}
}

规则("初始化铁拳位置")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.tiequanLocation = 数组(矢量(-14.065, -1, -73.499), 矢量(17.837, -1.482, -74.640), 矢量(-1.963, 2, -78.948), 矢量(19.057, 3.098, -53.985),
			矢量(-12.746, 2.292, -44.751), 矢量(-23.082, 6, -26.646), 矢量(-30.480, 6, -13.120), 矢量(-54.210, 9.900, -29.510), 矢量(-20.107,
			101.664, 184.556), 矢量(-34.230, 95.940, 139.360), 矢量(-11.820, 94.229, 135.219), 矢量(-25.560, 94, 152), 矢量(-9.051, 98, 176.545),
			矢量(16.777, 96.455, 135.595), 矢量(-17.513, 95.255, 111.165), 矢量(34.445, 95.921, 139.391), 矢量(40.328, 94.901, 136.232), 矢量(76.090,
			100.479, 162.130), 矢量(79.700, 97.570, 142.600), 矢量(76.540, 100.350, 117.320), 矢量(12.627, 270.259, 258.365), 矢量(44.869, 267.201,
			298.965), 矢量(41.334, 270.247, 340.837), 矢量(32.110, 267, 318.170), 矢量(23.420, 268.068, 305.010), 矢量(8.489, 270.161, 279.651),
			矢量(-1.900, 278, 300.649), 矢量(0.940, 270, 306.440), 矢量(-55.264, 9.620, -29.242), 矢量(-12.569, 2.292, -45.377), 矢量(6.092, 1.500,
			-70.923), 矢量(10.790, 1.500, -59.705), 矢量(29.170, 6, -24.955), 矢量(27.960, 6.095, -13.250), 矢量(58.681, 8.992, -9.142), 矢量(
			-53.794, 271.668, 325.438), 矢量(21.271, 270.161, 352.092), 矢量(44.200, 271.567, 335.100), 矢量(52.970, 271.450, 355.080), 矢量(
			24.336, 270, 340.664), 矢量(17.076, 270.510, 325.581), 矢量(28.980, 6.017, -12.960), 矢量(45.689, 4.774, -43.860), 矢量(1.045, -1,
			-60.534));
	}
}

规则("铁拳到下一关")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.data[5] == 1;
		存活(事件玩家) == 真;
		在地面上(事件玩家) == 真;
		全局.tiequanLocation[事件玩家.tiequanlevel + 1] != 0;
		相距距离(所选位置(事件玩家), 全局.tiequanLocation[事件玩家.tiequanlevel]) >= 1;
	}

	动作
	{
		If(相距距离(所选位置(事件玩家), 全局.tiequanLocation[事件玩家.tiequanlevel + 1]) > 2);
			击杀(事件玩家, 空);
		Else;
			事件玩家.tiequanlevel += 1;
			If(数组包含(数组(7, 14, 19, 27, 34, 40), 事件玩家.tiequanlevel));
				事件玩家.tiequanlevel += 1;
				击杀(事件玩家, 空);
			End;
			调用子程序(tiequanskill);
			取消主要动作(事件玩家);
			设置技能冷却(事件玩家, 按钮(辅助攻击模式), 0);
			设置技能冷却(事件玩家, 按钮(技能1), 0);
			设置技能冷却(事件玩家, 按钮(技能2), 0);
			If(事件玩家.tiequanlevel == 数量(全局.tiequanLocation) - 1);
				事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 自定义字符串("一拳超人"));
				事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 颜色(黄色));
				事件玩家.cheng_hao[0] = 数量(事件玩家.cheng_hao[1] - 1);
				大字体信息(所有玩家(所有队伍), 自定义字符串("恭喜{0}这个B通关了安娜娜超级跳挑战", 事件玩家));
				事件玩家.data[5] = 0;
				事件玩家.data[6] = 1;
				设置不可见(事件玩家, 无);
	}
}

规则("E升天")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		存活(事件玩家) == 真;
		事件玩家.data[5] == 1;
		数组包含(数组(35, 37, 38), 事件玩家.tiequanlevel) != 真;
		正在使用技能 2(事件玩家) == 真;
	}

	动作
	{
		If(事件玩家.tiequanlevel >= 11);
			If(事件玩家.tiequanlevel <= 16);
				施加推力(事件玩家, 面朝方向(事件玩家) * 矢量(1, 0, 1), 20, 至地图, 取消相反运动);
			Else If(数组包含(数组(17, 41), 事件玩家.tiequanlevel));
				施加推力(事件玩家, 面朝方向(事件玩家) * 矢量(1, 0, 1), 25, 至地图, 取消相反运动);
			Else If(事件玩家.tiequanlevel == 41);
				施加推力(事件玩家, 面朝方向(事件玩家) * 矢量(1, 0, 1), 28, 至地图, 取消相反运动);
			Else If(事件玩家.tiequanlevel == 35);
				中止;
			Else;
				施加推力(事件玩家, 面朝方向(事件玩家) * 矢量(1, 0, 1), 20, 至地图, 取消相反运动);
			End;
			施加推力(事件玩家, 上, 12, 至地图, 取消相反运动);
	}
}

规则("铁拳技能解锁-----子程序")
{
	事件
	{
		子程序;
		tiequanskill;
	}

	动作
	{
		If(数组包含(数组(24, 32, 37, 42), 事件玩家.tiequanlevel));
			设置启用技能 1(事件玩家, 真);
		End;
		If(数组包含(数组(22, 28, 36, 41), 事件玩家.tiequanlevel));
			设置启用技能 1(事件玩家, 假);
		End;
		If(数组包含(数组(18, 22, 32, 36), 事件玩家.tiequanlevel));
			设置启用技能 2(事件玩家, 假);
		End;
		If(数组包含(数组(11, 20, 26, 33, 39), 事件玩家.tiequanlevel));
			设置启用技能 2(事件玩家, 真);
		End;
	}
}

规则("一次性右键")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.data[5] == 1;
		全局.tiequanLocation[事件玩家.tiequanlevel + 1] != 0;
		技能冷却时间(事件玩家, 按钮(辅助攻击模式)) > 0;
	}

	动作
	{
		If(相距距离(所选位置(事件玩家), 全局.tiequanLocation[事件玩家.tiequanlevel]) >= 1);
			设置技能冷却(事件玩家, 按钮(辅助攻击模式), 999);
	}
}

规则("一次性E")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.data[5] == 1;
		事件玩家.tiequanlevel != 35;
		全局.tiequanLocation[事件玩家.tiequanlevel + 1] != 0;
		技能冷却时间(事件玩家, 按钮(技能2)) > 0;
	}

	动作
	{
		If(相距距离(所选位置(事件玩家), 全局.tiequanLocation[事件玩家.tiequanlevel]) >= 1);
			设置技能冷却(事件玩家, 按钮(技能2), 999);
	}
}

规则("一次性shft")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.data[5] == 1;
		事件玩家.tiequanlevel != 35;
		全局.tiequanLocation[事件玩家.tiequanlevel + 1] != 0;
		技能冷却时间(事件玩家, 按钮(技能1)) > 0;
	}

	动作
	{
		If(相距距离(所选位置(事件玩家), 全局.tiequanLocation[事件玩家.tiequanlevel]) >= 1);
			设置技能冷却(事件玩家, 按钮(技能1), 999);
	}
}

规则("黑影随机位置数据")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.heiyingLocation = 数组(矢量(-61.125, 8.791, 8.993), 矢量(-61.095, 95.286, 148.086), 矢量(83.007, 2.617, -29.192));
		全局.ExtraHeroEggLocation[2] = 数组随机取值(全局.heiyingLocation);
	}
}

规则("仓鼠限时退出")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.setting[7] != 0;
	}

	动作
	{
		等待(540, 当为“假”时中止);
		大字体信息(事件玩家, 自定义字符串("仓鼠挑战剩余1分钟"));
		等待(50, 当为“假”时中止);
		大字体信息(事件玩家, 自定义字符串("仓鼠挑战剩余10秒"));
		等待(10, 当为“假”时中止);
		事件玩家.setting[7] = 0;
		传送(事件玩家, 全局.ZoneLocations[1]);
	}
}

规则("称号数据")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.map_text[0] = 数组(自定义字符串("雷姆"), 自定义字符串("城维大队"), 自定义字符串("阿冷"), 自定义字符串("南巷清风"), 自定义字符串("脏牧永远滴神"), 自定义字符串("唯爱轻衣"), 自定义字符串(
			"cyyyyyy"), 自定义字符串("挽挽挽挽挽衾"), 自定义字符串("你也不是我的唯一"), 自定义字符串("Joe7yr"), 自定义字符串("神狐"), 自定义字符串("九万七千零一"), 自定义字符串("谈料"), 自定义字符串(
			"范范不吃饭"), 自定义字符串("Feng"), 自定义字符串("ghost"), 自定义字符串("风待葬"), 自定义字符串("阿一好累"), 自定义字符串("Sicca"), 自定义字符串("雾子圈外女友"), 自定义字符串(
			"双手健在何须女友"), 自定义字符串("绪翎"), 自定义字符串("SEMIS"), 自定义字符串("平凡的上班族"));
		全局.map_text[1] = 数组(自定义字符串("孤独患者\r\n懒癌晚期\r\n\r\n"), 自定义字符串("(●'◡'●)猫猫老师(●'◡'●)\r\n\r\n"), 自定义字符串("冷艳小妈\r\n\r\n"), 自定义字符串(
			"“清风难解故人情” \r\n\r\n"), 自定义字符串("“路过的假面骑士”\r\n\r\n"), 自定义字符串("“只愁风断青衣渡”\r\n\r\n"), 自定义字符串("\\(￣︶￣*\\))\r\n\r\n"), 自定义字符串(
			"挽挽QAQ\r\n\r\n"), 自定义字符串("美少女战士\r\n\r\n"), 自定义字符串("点歌姬\r\n\r\n"), 自定义字符串("南桐\r\n\r\n"), 自定义字符串("萌新跑酷导师\r\n\r\n"), 自定义字符串(
			"肝到肾虚\r\n\r\n"), 自定义字符串("南铜杀手\r\n\r\n"), 自定义字符串("风\r\n\r\n"), 自定义字符串("孤独患者\r\n懒癌晚期\r\n\r\n"), 自定义字符串("肥猪流\r\n\r\n"), 自定义字符串(
			"成都必吃榜\r\n\r\n"), 自定义字符串("脑子离家出走中\r\n\r\n"), 自定义字符串("雾子圈外女友\r\n\r\n"), 自定义字符串("泪水打湿迈巴赫 一生只爱sak酱\r\n\r\n"), 自定义字符串(
			"嘿嘿(●ˇ∀ˇ●)\r\n\r\n"), 自定义字符串("《美术老师也是老师》\r\n\r\n"), 自定义字符串("吉良吉影\r\n\r\n"));
		全局.map_text[2] = 数组(颜色(天蓝色), 自定义颜色(255, 182, 193, 255), 自定义颜色(255, 182, 193, 255), 颜色(天蓝色), 自定义颜色(135, 206, 250, 255), 颜色(白色), 颜色(
			白色), 自定义颜色(255, 182, 193, 255), 自定义颜色(255, 182, 193, 255), 自定义颜色(255, 192, 203, 255), 自定义颜色(255, 192, 203, 255), 颜色(黄色), 颜色(
			白色), 颜色(黄色), 自定义颜色(241, 158, 194, 255), 自定义颜色(255, 192, 203, 255), 自定义颜色(255, 192, 203, 255), 自定义颜色(255, 192, 203, 255), 颜色(
			黄色), 自定义颜色(255, 192, 203, 255), 自定义颜色(255, 192, 203, 255), 颜色(绿色), 颜色(蓝色), 自定义颜色(255, 200, 245, 255));
		While(数量(首个(全局.map_text) > 数量(全局.map_text[2])));
			全局.map_text[2] = 添加至数组(全局.map_text[2], 颜色(白色));
		End;
	}
}

规则("塔主")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.weihezhe == 6;
		事件玩家.maomao == 5;
		事件玩家.tiaozhanzhe == 5;
		事件玩家.data[11] == 1;
		事件玩家.setting[6] == 1;
		事件玩家.data[6] == 1;
	}

	动作
	{
		事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 自定义字符串(""));
		事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 自定义颜色(255, 182, 193, 255));
		事件玩家.cheng_hao[0] = 数量(事件玩家.cheng_hao[1] - 1);
		大字体信息(所有玩家(所有队伍), 自定义字符串("{0}完成了终局挑战 成为了新任  “漓江塔塔主！”", 事件玩家));
		事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 自定义字符串(
			"“      警长      ”\r\n\r\n“  一拳超人  ”\r\n\r\n“  源氏的神  ”\r\n\r\n“  仓鼠跳弹  ”\r\n\r\n“  青蛙王子  ”\r\n\r\n“漓江塔塔主”\r\n"));
		事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 自定义颜色(255, 182, 193, 255));
		事件玩家.cheng_hao[0] = 数量(事件玩家.cheng_hao[1] - 1);
		事件玩家.zhongju = 假;
	}
}

规则("初始化称号")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		实体存在(事件玩家) == 真;
		数组包含(首个(全局.map_text), 自定义字符串("{0}", 事件玩家)) == 真;
	}

	动作
	{
		事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 全局.map_text[1][数组值的索引(首个(全局.map_text), 自定义字符串("{0}", 事件玩家))]);
		事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 全局.map_text[2][数组值的索引(首个(全局.map_text), 自定义字符串("{0}", 事件玩家))]);
		事件玩家.cheng_hao[0] = 1;
		全局.yuanshigod = 数组(自定义字符串("你也不是我的唯一"), 自定义字符串("아기"), 自定义字符串("OuchAah"));
		If(数组包含(全局.yuanshigod, 自定义字符串("{0}", 事件玩家)));
			事件玩家.cheng_hao[1] = 添加至数组(事件玩家.cheng_hao[1], 自定义字符串("源氏的神"));
			事件玩家.cheng_hao[2] = 添加至数组(事件玩家.cheng_hao[2], 颜色(黄色));
	}
}

规则("特效9")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.data[13] == 1;
		在地面上(事件玩家) == 真;
	}

	动作
	{
		播放效果(所有玩家(所有队伍), “末日铁拳”毁天灭地击中效果, 颜色(白色), 事件玩家, 0.200);
		等待(4, 无视条件);
	}
}

规则("特效11")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.data[15] == 1;
		按钮被按下(事件玩家, 按钮(主要攻击模式)) == 真;
	}

	动作
	{
		播放效果(所有玩家(所有队伍), D.Va自毁爆炸效果, 颜色(白色), 射线命中位置(眼睛位置(事件玩家), 眼睛位置(事件玩家) + 面朝方向(事件玩家) * 100, 空, 空, 假), 1);
		播放效果(所有玩家(所有队伍), 莱因哈特烈焰打击目标击中效果, 颜色(白色), 事件玩家, 1);
		等待(2, 无视条件);
	}
}

规则("特效12拾取")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.chatstart == 真;
		正在使用终极技能(事件玩家) == 真;
		所用英雄(事件玩家) == 数组(英雄(末日铁拳), 英雄(莱因哈特), 英雄(死神), 英雄(堡垒), 英雄(黑百合), 英雄(天使), 英雄(卡西迪))[事件玩家.data[21]];
		相距距离(所选位置(事件玩家), 全局.texiao12[事件玩家.data[21]]) <= 2;
	}

	动作
	{
		事件玩家.data[21] += 1;
		If(事件玩家.data[21] >= 7);
			事件玩家.data[16] = 1;
	}
}

规则("特效13")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.data[17] == 1;
	}

	动作
	{
		等待(0.200, 无视条件);
		播放效果(所有玩家(所有队伍), 环状爆炸, 数组随机取值(数组(颜色(白色), 颜色(红色), 颜色(绿色), 颜色(黄色), 颜色(紫色), 颜色(蓝色))), 事件玩家 + 矢量(0, 0.500, 0), 2);
		如条件为“真”则循环;
	}
}

规则("修复炫迈表情停止前进bug")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		正在使用表情交流(事件玩家) == 真;
		事件玩家.jingsu_Sel >= 2;
	}

	动作
	{
		设置状态(事件玩家, 空, 击倒, 0.016);
	}
}

规则("dj")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		卢西奥;
	}

	条件
	{
		事件玩家.chatcount < 5;
	}

	动作
	{
		设置造成治疗(事件玩家, 0);
	}
}

规则("dj")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		所用英雄(事件玩家) != 英雄(卢西奥);
	}

	动作
	{
		设置造成治疗(事件玩家, 100);
	}
}

规则("特效14")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.data[22] == 0;
		头像火力全开(事件玩家) == 真;
	}

	动作
	{
		事件玩家.data[22] = 1;
	}
}

规则("称号")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建HUD文本(已过滤的数组(所有玩家(所有队伍), 当前数组元素.mianban[1] == 1), 自定义字符串("{0}", 数组(自定义字符串(
			"                    Title Selection Panel                    \r\n{0}\r\n\r\n\r\n{1}", 自定义字符串(
			"{0} or {1}Toggle Selection\r\n<{2}>Confirmation title", 输入绑定字符串(按钮(主要攻击模式)), 输入绑定字符串(按钮(辅助攻击模式)), 输入绑定字符串(按钮(互动))),
			本地玩家.cheng_hao[1][本地玩家.cheng_hao[3]]), 自定义字符串("                    称号选择                    \r\n{0}\r\n\r\n\r\n{1}", 自定义字符串(
			"{0}或{1}切换选择\r\n<{2}>选择称号", 输入绑定字符串(按钮(主要攻击模式)), 输入绑定字符串(按钮(辅助攻击模式)), 输入绑定字符串(按钮(互动))), 本地玩家.cheng_hao[1][本地玩家.cheng_hao[3]]))
			[本地玩家.lang]), 空, 空, 顶部, 127, 颜色(橙色), 空, 空, 可见和字符串, 始终不可见);
		创建地图文本(已过滤的数组(所有玩家(所有队伍), 相距距离(当前数组元素, 全局.cheng_hao_Location) <= 10), 自定义字符串("你瞅啥"), 全局.cheng_hao_Location, 2, 不要截取, 可见，位置和字符串, 颜色(
			白色), 默认可见度);
		全局.cheng_hao_Location = 矢量(9.623, -0.575, -83.621);
	}
}

规则("称号选择")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		事件玩家.Watch != 真;
		(按钮被按下(事件玩家, 按钮(主要攻击模式)) || 按钮被按下(事件玩家, 按钮(辅助攻击模式))) == 真;
		相距距离(事件玩家, 全局.cheng_hao_Location) <= 3;
	}

	动作
	{
		If(按钮被按下(事件玩家, 按钮(主要攻击模式)));
			事件玩家.cheng_hao[3] = (事件玩家.cheng_hao[3] + 1) % 数量(事件玩家.cheng_hao[1]);
		Else;
			If(事件玩家.cheng_hao[3] == 0);
				事件玩家.cheng_hao[3] = 数量(事件玩家.cheng_hao[1]) - 1;
			Else;
				事件玩家.cheng_hao[3] -= 1;
			End;
		End;
		等待(0.250, 无视条件);
	}
}

规则("选择称号")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		相距距离(事件玩家, 全局.cheng_hao_Location) <= 3;
		事件玩家.Watch != 真;
		按钮被按下(事件玩家, 按钮(互动)) == 真;
	}

	动作
	{
		事件玩家.cheng_hao[0] = 事件玩家.cheng_hao[3];
		If(事件玩家.cheng_hao[0] == 0);
			显示姓名板(所有玩家(所有队伍), 事件玩家);
		Else;
			隐藏姓名板(所有玩家(所有队伍), 事件玩家);
		End;
		小字体信息(事件玩家, 自定义字符串("{0}", 数组(自定义字符串("The title has been changed to:{0}", 事件玩家.cheng_hao[1][首个(事件玩家.cheng_hao)]), 自定义字符串(
			"已选择称号:{0}", 事件玩家.cheng_hao[1][首个(事件玩家.cheng_hao)]))[事件玩家.lang]));
		事件玩家.cheng_hao[3] = 0;
		等待(1, 无视条件);
	}
}

规则("艾什弹球")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.aishi_tanqiu = 数组(数组(矢量(-0.390, 269.998, 332.980), 矢量(-1.721, 265.028, 394.530), 矢量(-8.905, 287.246, 382.813), 矢量(5.563,
			307.170, 375.574)), 数组(2, 25, 28, 25));
		创建效果(本地玩家.chatcount == 2 ? 本地玩家 : 空, 球, 颜色(绿色), 首个(全局.aishi_tanqiu)[数组值的索引(首个(全局.aishi_tanqiu), 首个(已排序的数组(首个(全局.aishi_tanqiu),
			相距距离(所选位置(本地玩家), 当前数组元素))))], 1, 可见，位置和半径);
	}
}

规则("艾什弹起")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		艾什;
	}

	条件
	{
		事件玩家.chatstart == 真;
		所用英雄(事件玩家) == 全局.HeroRoster[事件玩家.chatcount];
		事件玩家.chatcount == 2;
		数量(已过滤的数组(首个(全局.aishi_tanqiu), 相距距离(当前数组元素, 所选位置(事件玩家)) <= 1)) > 0;
	}

	动作
	{
		If(数组值的索引(首个(全局.aishi_tanqiu), 首个(已排序的数组(首个(全局.aishi_tanqiu), 相距距离(当前数组元素, 所选位置(事件玩家))))) == 0);
			传送(事件玩家, 首个(全局.aishi_tanqiu)[1] + 矢量(0, 2, 0));
		End;
		施加推力(事件玩家, 上, 全局.aishi_tanqiu[1][数组值的索引(首个(全局.aishi_tanqiu), 首个(已排序的数组(首个(全局.aishi_tanqiu), 相距距离(当前数组元素, 所选位置(事件玩家)))))], 至地图,
			取消相反运动);
	}
}

规则("松开跳跃")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		事件玩家.sanduan[1] == 1;
		按钮被按下(事件玩家, 按钮(跳跃)) == 假;
	}

	动作
	{
		事件玩家.sanduan[1] = 0;
	}
}

规则("按下跳跃")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		事件玩家.sanduan[1] == 0;
		按钮被按下(事件玩家, 按钮(跳跃)) == 真;
	}

	动作
	{
		If(首个(事件玩家.sanduan) == 0);
			If(事件玩家.sanduan[2] == 0);
				事件玩家.sanduan[0] += 1;
				事件玩家.sanduan[1] = 1;
			End;
		Else If(首个(事件玩家.sanduan) == 1);
			事件玩家.sanduan[0] += 1;
			事件玩家.sanduan[1] = 1;
			If(在地面上(事件玩家));
				施加推力(事件玩家, 上, 9, 至地图, 取消相反运动);
				事件玩家.sanduan[2] = 1;
			End;
		Else If(首个(事件玩家.sanduan) == 2 && 事件玩家.sanduan[2] == 1);
			事件玩家.sanduan[0] += 1;
			事件玩家.sanduan[1] = 1;
	}
}

规则("三段跳时间判定")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		在地面上(事件玩家) == 真;
		首个(事件玩家.sanduan) != 0;
	}

	动作
	{
		等待(0.070, 当为“假”时中止);
		事件玩家.sanduan[0] = 0;
		事件玩家.sanduan[2] = 0;
		事件玩家.sanduan[3] = 0;
	}
}

规则("爬墙或shft检测")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		(正在使用技能 1(事件玩家) || 在墙上(事件玩家)) == 真;
	}

	动作
	{
		事件玩家.sanduan[3] = 1;
	}
}

规则("结束爬墙或shft，已代替一段")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		事件玩家.sanduan[3] == 1;
		(正在使用技能 1(事件玩家) || 在墙上(事件玩家)) == 假;
		在地面上(事件玩家) == 假;
		首个(事件玩家.sanduan) == 0;
	}

	动作
	{
		事件玩家.sanduan[0] += 1;
		事件玩家.sanduan[1] = 1;
	}
}

规则("锤妹cd修复")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		布丽吉塔;
	}

	条件
	{
		技能冷却时间(事件玩家, 按钮(主要攻击模式)) > 1.250;
	}

	动作
	{
		设置技能冷却(事件玩家, 按钮(主要攻击模式), 1.100);
	}
}

规则("白名单")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		全局.chat = 数组(自定义字符串("雷姆"), 自定义字符串("城维大队"), 自定义字符串("庆花被打搞菜生"), 自定义字符串("脏牧永远滴神"), 自定义字符串("绪翎"), 自定义字符串("挽挽挽挽挽衾"), 自定义字符串("白银之鹰"),
			自定义字符串("你也不是我的唯一"), 自定义字符串("OuchAah"), 自定义字符串("阿一好累"), 自定义字符串("阿冷"), 自定义字符串("草莓冷饮马里布"), 自定义字符串("渝年"), 自定义字符串("城维大队"), 自定义字符串(
			"九万七千零一"), 自定义字符串("Joe7yr"), 自定义字符串("南巷清风"), 自定义字符串("乌鸦像写字台"), 自定义字符串("戰熋無敵"), 自定义字符串("范范不吃饭"), 自定义字符串("风待葬"), 自定义字符串("旧时桥"),
			自定义字符串("好想被中野一花"), 自定义字符串("大大怪将军"), 自定义字符串("Sicca"), 自定义字符串("金牌男艺人"), 自定义字符串("時崎狂三"), 自定义字符串("神舟行我看行"), 自定义字符串("妄念啊"), 自定义字符串(
			"离子"), 自定义字符串("何不等风寻你"), 自定义字符串("雾子圈外女友"), 自定义字符串("SEMIS"), 自定义字符串("静吟灯火阑珊处"), 自定义字符串("cyyyyyy"), 自定义字符串("不要压力您的队友"), 自定义字符串(
			"她怎么又可爱了"), 自定义字符串("华宇心"), 自定义字符串("乌鸦坐飞机"), 自定义字符串("王雷卖鱼真好吃"), 自定义字符串("彭少崇"), 自定义字符串("UIIAIO"), 自定义字符串("mili"), 自定义字符串("九峥儿"),
			自定义字符串("勿梦竹"), 自定义字符串("源批"), 自定义字符串("白鹄"), 自定义字符串("平凡的上班族"), 自定义字符串("偽艺术家"), 自定义字符串("岛田卢西奥"), 自定义字符串("Agoni"), 自定义字符串("雷牢尸"),
			自定义字符串("飞狼舰长"));
	}
}

规则("额外彩蛋锤妹解锁shift效果")
{
	事件
	{
		持续 - 全局;
	}

	动作
	{
		创建图标(已过滤的数组(所有玩家(所有队伍), 当前数组元素.chatcount == 1), 矢量(-44.376, 9.615, -25.921), 箭头：向下, 可见, 颜色(绿色), 真);
	}
}

规则("万圣节彩蛋源氏技能修正")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		源氏;
	}

	条件
	{
		事件玩家.Victory == 真;
		事件玩家.EasterEggsFound[3] == 假;
		事件玩家.FoundSecretHero[3] == 假;
	}

	动作
	{
		等待(0.250, 无视条件);
		设置启用技能 1(事件玩家, 假);
		设置启用技能 2(事件玩家, 真);
	}
}

规则("夺取传送")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		相距距离(事件玩家, 矢量(0, 127.790, 190.200)) <= 3;
	}

	动作
	{
		传送(事件玩家, 矢量(0, 133, 189));
	}
}

规则("源氏最终加速")
{
	事件
	{
		持续 - 每名玩家;
		双方;
		全部;
	}

	条件
	{
		相距距离(事件玩家, 矢量(-50.049, 267.620, 338.882)) <= 5;
		按钮被按下(事件玩家, 按钮(跳跃)) == 真;
	}

	动作
	{
		设置移动速度(事件玩家, 112);
		等待(10, 无视条件);
		设置移动速度(事件玩家, 100);
	}
}
