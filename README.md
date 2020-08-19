---- Minecraft Crash Report ----
// You should try our sister game, Minceraft!

Time: 8/19/20 11:43 AM
Description: Exception in server tick loop

com.google.gson.JsonSyntaxException: java.lang.IllegalStateException: This is not a JSON Array.
	at com.google.gson.Gson.fromJson(Gson.java:815)
	at com.google.gson.Gson.fromJson(Gson.java:741)
	at com.stateshifterlabs.achievementbooks.data.GameSave.load(GameSave.java:63)
	at com.stateshifterlabs.achievementbooks.data.GameSave.onWorldLoad(GameSave.java:96)
	at cpw.mods.fml.common.eventhandler.ASMEventHandler_726_GameSave_onWorldLoad_Load.invoke(.dynamic)
	at cpw.mods.fml.common.eventhandler.ASMEventHandler.invoke(ASMEventHandler.java:54)
	at cpw.mods.fml.common.eventhandler.EventBus.post(EventBus.java:140)
	at net.minecraft.server.integrated.IntegratedServer.func_71247_a(IntegratedServer.java:73)
	at net.minecraft.server.integrated.IntegratedServer.func_71197_b(IntegratedServer.java:92)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:387)
	at net.minecraft.server.MinecraftServer$2.run(MinecraftServer.java:685)
Caused by: java.lang.IllegalStateException: This is not a JSON Array.
	at com.google.gson.JsonElement.getAsJsonArray(JsonElement.java:106)
	at com.stateshifterlabs.achievementbooks.serializers.AchievementStorageSerializer.deserialize(AchievementStorageSerializer.java:54)
	at com.stateshifterlabs.achievementbooks.serializers.AchievementStorageSerializer.deserialize(AchievementStorageSerializer.java:15)
	at com.google.gson.TreeTypeAdapter.read(TreeTypeAdapter.java:58)
	at com.google.gson.Gson.fromJson(Gson.java:803)
	... 10 more


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- System Details --
Details:
	Minecraft Version: 1.7.10
	Operating System: Windows 10 (amd64) version 10.0
	Java Version: 1.8.0_51, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 2172471112 bytes (2071 MB) / 3662675968 bytes (3493 MB) up to 5760352256 bytes (5493 MB)
	JVM Flags: 4 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xmx6180m -Xms256m -XX:PermSize=256m
	AABB Pool Size: 0 (0 bytes; 0 MB) allocated, 0 (0 bytes; 0 MB) used
	IntCache: cache: 0, tcache: 0, allocated: 13, tallocated: 103
	FML: MCP v9.05 FML v7.10.99.99 Minecraft Forge 10.13.4.1614 151 mods loaded, 142 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored
	UCHIJAAAAAAA	mcp{9.05} [Minecraft Coder Pack] (minecraft.jar) 
	UCHIJAAAAAAA	FML{7.10.99.99} [Forge Mod Loader] (forge-1.7.10-10.13.4.1614-1.7.10.jar) 
	UCHIJAAAAAAA	Forge{10.13.4.1614} [Minecraft Forge] (forge-1.7.10-10.13.4.1614-1.7.10.jar) 
	UCHIJAAAAAAA	additionalresources{0.0.2} [Additional Resources] (additionalresources-1.7.10_0.1.0.unknown.jar) 
	UCHIJAAAAAAA	appliedenergistics2-core{rv3-beta-5} [Applied Energistics 2 Core] (minecraft.jar) 
	UCHIJAAAAAAA	CodeChickenCore{1.0.7.47} [CodeChicken Core] (minecraft.jar) 
	UCHIJAAAAAAA	MobiusCore{1.2.5} [MobiusCore] (minecraft.jar) 
	UCHIJAAAAAAA	NotEnoughItems{1.0.5.118} [Not Enough Items] (NotEnoughItems-1.7.10-1.0.5.118-universal.jar) 
	UCHIJAAAAAAA	OpenComputers|Core{1.5.22.46} [OpenComputers (Core)] (minecraft.jar) 
	UCHIJAAAAAAA	PotionExtensionCore{1.7.10-1.1.0} [PotionExtensionCore] (minecraft.jar) 
	UCHIJAAAAAAA	OpenModsCore{0.9.1} [OpenModsCore] (minecraft.jar) 
	UCHIJAAAAAAA	<CoFH ASM>{000} [CoFH ASM] (minecraft.jar) 
	UCHIJAAAAAAA	FastCraft{1.23} [FastCraft] (fastcraft-1.23-entitydbg.jar) 
	UCHIJAAAAAAA	bspkrsCore{6.15} [bspkrsCore] ([1.7.10]bspkrsCore-universal-6.15.jar) 
	UCHIJAAAAAAA	StartingInventory{1.7.10.r03} [StartingInventory] ([1.7.10]StartingInventory-universal-1.7.10.r03.jar) 
	UCHIJAAAAAAA	achievementbooks{v1.0-MC1.7.10} [Achievement Books] (achievementbooks-v1.0-MC1.7.10.jar) 
	UCHIJAAAAAAA	AgriCraft{1.7.10-1.5.0} [AgriCraft] (AgriCraft-1.7.10-1.5.0.jar) 
	UCHIJAAAAAAA	nevermine{2.3} [AdventOfAscension] (AoA-2.4.B.jar) 
	UCHIJAAAAAAA	AppleCore{1.3.0} [AppleCore] (AppleCore-mc1.7.10-1.3.0.jar) 
	UCHIJAAAAAAA	appliedenergistics2{rv3-beta-5} [Applied Energistics 2] (appliedenergistics2-rv3-beta-5.jar) 
	UCHIJAAAAAAA	MovingWorld{1.7.10-1.8} [Moving World] (movingworld-1.7.10-1.8.jar) 
	UCHIJAAAAAAA	ArchimedesShipsPlus{1.7.10-1.8} [Archimedes' Ships Plus] (archimedesshipsplus-1.7.10-1.8.jar) 
	UCHIJAAAAAAA	audiodeath{0.6.0_1.7.10-e8c5987} [Audio Death] (audiodeath-0.6.0-1.7.10r25+e8c5987.jar) 
	UCHIJAAAAAAA	bdlib{1.9.4.109} [BD Lib] (bdlib-1.9.4.109-mc1.7.10.jar) 
	UCHIJAAAAAAA	BetterAchievements{0.1.0} [Better Achievements] (BetterAchievements-1.7.10-0.1.0.jar) 
	UCHIJAAAAAAA	BetterTitleScreen{1.7.10-1.1} [Better Title Screen] (BetterTitleScreen-1.7.10-1.1.jar) 
	UCHIJAAAAAAA	BiblioCraft{1.11.5} [BiblioCraft] (BiblioCraft[v1.11.5][MC1.7.10].jar) 
	UCHIJAAAAAAA	CoFHCore{1.7.10R3.1.4} [CoFH Core] (CoFHCore-[1.7.10]3.1.4-329.jar) 
	UCHIJAAAAAAA	Baubles{1.0.1.10} [Baubles] (Baubles-1.7.10-1.0.1.10.jar) 
	UCHIJAAAAAAA	ThermalFoundation{1.7.10R1.2.6} [Thermal Foundation] (ThermalFoundation-[1.7.10]1.2.6-118.jar) 
	UCHIJAAAAAAA	ThermalExpansion{1.7.10R4.1.5} [Thermal Expansion] (ThermalExpansion-[1.7.10]4.1.5-248.jar) 
	UCHIJAAAAAAA	BigReactors{0.4.3A} [Big Reactors] (BigReactors-0.4.3A.jar) 
	UCHIJAAAAAAA	qmunitylib{1.0} [QmunityLib] (QmunityLib-1.7.10-0.1.114-universal.jar) 
	UCHIJAAAAAAA	bluepower{0.2.962} [Blue Power] (BluePower-1.7.10-0.2.962-universal.jar) 
	UCHIJAAAAAAA	Thaumcraft{4.2.3.5} [Thaumcraft] (Thaumcraft-1.7.10-4.2.3.5.jar) 
	UCHIJAAAAAAA	Botania{r1.8-249} [Botania] (Botania r1.8-249.jar) 
	UCHIJAAAAAAA	BrandonsCore{1.0.0.12} [Brandon's Core] (BrandonsCore-1.0.0.12.jar) 
	UCHIJAAAAAAA	chancecubes{1.7.10-2.3.2.126} [Chance Cubes] (ChanceCubes-1.7.10-2.3.2.126.jar) 
	UCHIJAAAAAAA	ChickenChunks{1.3.4.19} [ChickenChunks] (ChickenChunks-1.7.10-1.3.4.19-universal.jar) 
	UCHIJAAAAAAA	TwilightForest{2.3.7} [The Twilight Forest] (twilightforest-1.7.10-2.3.7.jar) 
	UCHIJAAAAAAA	ForgeMultipart{1.2.0.345} [Forge Multipart] (ForgeMultipart-1.7.10-1.2.0.345-universal.jar) 
	UCHIJAAAAAAA	chisel{2.9.5.11} [Chisel] (Chisel-2.9.5.11.jar) 
	UCHIJAAAAAAA	cookingbook{1.0.134} [Cooking for Blockheads] (cookingbook-mc1.7.10-1.0.134.jar) 
	UCHIJAAAAAAA	CustomMainMenu{1.9.2} [Custom Main Menu] (CustomMainMenu-MC1.7.10-1.9.2.jar) 
	UCHIJAAAAAAA	customnpcs{1.7.10d} [CustomNpcs] (CustomNPCs_1.7.10d(21feb16).jar) 
	UCHIJAAAAAAA	CustomPets{1.0.5} [Custom Pets] (custompets-1.7.10-1.0.5-universal.jar) 
	UCHIJAAAAAAA	lootablebodies{1.3.7} [DrCyano's Lootable Bodies] (CyanosLootableBodies-1.7.10-backport_1.3.7.jar) 
	UCHIJAAAAAAA	PTRModelLib{1.0.0} [PTRModelLib] (Decocraft-2.3.6.1_1.7.10.jar) 
	UCHIJAAAAAAA	props{2.3.6.1} [Decocraft] (Decocraft-2.3.6.1_1.7.10.jar) 
	UCHIJAAAAAAA	Mekanism{9.1.0} [Mekanism] (Mekanism-1.7.10-9.1.0.281.jar) 
	UCHIJAAAAAAA	DefenseTech{1.0.1} [DefenseTech] (DefenseTech-1.7.10-1.0.1.46.jar) 
	UCHIJAAAAAAA	DraconicEvolution{1.0.2h} [Draconic Evolution] (Draconic-Evolution-1.7.10-1.0.2h.jar) 
	UCHIJAAAAAAA	DragonMounts{r41-1.7.10} [Dragon Mounts] (DragonMounts-r41-1.7.10.jar) 
	UCHIJAAAAAAA	endercore{1.7.10-0.2.0.32_beta} [EnderCore] (EnderCore-1.7.10-0.2.0.32_beta.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded{1.7.10R2.8.1} [MineFactory Reloaded] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	Waila{1.5.10} [Waila] (Waila-1.5.10_1.7.10.jar) 
	UCHIJAAAAAAA	EnderIO{1.7.10-2.3.0.424_beta} [Ender IO] (EnderIO-1.7.10-2.3.0.424_beta.jar) 
	UCHIJAAAAAAA	EnderStorage{1.4.7.37} [EnderStorage] (EnderStorage-1.7.10-1.4.7.37-universal.jar) 
	UCHIJAAAAAAA	etfuturum{1.5.5} [Et Futurum] (Et Futurum-1.5.5.jar) 
	UCHIJAAAAAAA	evilcraft{0.9.6} [EvilCraft] (EvilCraft-1.7.10-0.9.6.jar) 
	UCHIJAAAAAAA	extracells{2.3.9} [Extra Cells 2] (ExtraCells-1.7.10-2.3.9b188.jar) 
	UCHIJAAAAAAA	ExtraUtilities{1.2.12} [Extra Utilities] (extrautilities-1.2.12.jar) 
	UCHIJAAAAAAA	Mantle{1.7.10-0.3.2.jenkins191} [Mantle] (Mantle-1.7.10-0.3.2b.jar) 
	UCHIJAAAAAAA	Natura{2.2.0} [Natura] (natura-1.7.10-2.2.1a2.jar) 
	UCHIJAAAAAAA	harvestcraft{1.7.10j} [Pam's HarvestCraft] (Pam's HarvestCraft 1.7.10Lb.jar) 
	UCHIJAAAAAAA	ImmersiveEngineering{0.7.5} [Immersive Engineering] (ImmersiveEngineering-0.7.5.jar) 
	UCHIJAAAAAAA	TConstruct{1.7.10-1.8.8.build988} [Tinkers' Construct] (TConstruct-1.7.10-1.8.8.jar) 
	UCHIJAAAAAAA	ExtraTiC{1.4.5} [ExtraTiC] (ExtraTiC-1.7.10-1.4.5.jar) 
	UCHIJAAAAAAA	fastleafdecay{1.4} [Fast Leaf Decay] (FastLeafDecay-1.7.10-1.4.jar) 
	UCHIJAAAAAAA	Forestry{4.2.11.59} [Forestry for Minecraft] (forestry_1.7.10-4.2.11.59.jar) 
	UCHIJAAAAAAA	iChunUtil{4.2.2} [iChunUtil] (iChunUtil-4.2.2.jar) 
	UCHIJAAAAAAA	GraviGun{4.0.0-beta} [GraviGun] (GravityGun-4.0.0-beta.jar) 
	UCHIJAAAAAAA	hardcorewither{1.1.3} [Hardcore Wither] (Hardcore Wither-1.7.10-1.1.3-21-universal.jar) 
	UCHIJAAAAAAA	Hats{4.0.1} [Hats] (Hats-4.0.1.jar) 
	UCHIJAAAAAAA	headcrumbs{1.7.4} [Headcrumbs] (Headcrumbs-1.7.4.jar) 
	UCHIJAAAAAAA	InventoryPets{1.4.9} [Inventory Pets] (inventorypets-1.7.10-1.4.9-universal.jar) 
	UCHIJAAAAAAA	inventorytweaks{1.59-dev-152-cf6e263} [Inventory Tweaks] (InventoryTweaks-1.59-dev-152.jar) 
	UCHIJAAAAAAA	IronChest{6.0.62.742} [Iron Chest] (ironchest-1.7.10-6.0.62.742-universal.jar) 
	UCHIJAAAAAAA	JABBA{1.2.1} [JABBA] (Jabba-1.2.1a_1.7.10.jar) 
	UCHIJAAAAAAA	LostBooks{1.2.2} [Lost Books] (LostBooks-1.7.10-1.2.2.jar) 
	UCHIJAAAAAAA	magicalcrops{4.0.0_PUBLIC_BETA_4b} [Magical Crops: Core] (magicalcrops-4.0.0_PUBLIC_BETA_5.jar) 
	UCHIJAAAAAAA	magicalcropsarmour{4.0.0_PUBLIC_BETA_4} [Magical Crops: Armoury] (magicalcropsarmoury-4.0.0_PUBLIC_BETA_4.jar) 
	UCHIJAAAAAAA	magicalcropsdeco{4.0.0_PUBLIC_BETA_4a} [Magical Crops: Decorative] (magicalcropsdeco-4.0.0_PUBLIC_BETA_4a.jar) 
	UCHIJAAAAAAA	magicclover{1.7.10-0.7.4} [Magic Clover] (magicclover-1.7.10-0.7.4.jar) 
	UCHIJAAAAAAA	malisiscore{1.7.10-0.14.3} [MalisisCore] (malisiscore-1.7.10-0.14.3.jar) 
	UCHIJAAAAAAA	malisisdoors{1.7.10-1.13.2} [Malisis' Doors] (malisisdoors-1.7.10-1.13.2.jar) 
	UCHIJAAAAAAA	mo{0.4.1} [Matter Overdrive] (MatterOverdrive-1.7.10-0.4.1.jar) 
	UCHIJAAAAAAA	RadixCore{2.1.3} [RadixCore] (RadixCore-1.7.10-2.1.3-universal.jar) 
	UCHIJAAAAAAA	MCA{1.7.10-5.2.2} [Minecraft Comes Alive] (MCA-1.7.10-5.2.2-universal.jar) 
	UCHIJAAAAAAA	MCEF{0.6} [Minecraft Chromium Embedded Framework] (MCEF-1.7.10-0.6.jar) 
	UCHIJAAAAAAA	MekanismGenerators{9.1.0} [MekanismGenerators] (MekanismGenerators-1.7.10-9.1.0.281.jar) 
	UCHIJAAAAAAA	MekanismTools{9.1.0} [MekanismTools] (MekanismTools-1.7.10-9.1.0.281.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded|CompatAppliedEnergistics{1.7.10R2.8.1} [MFR Compat: Applied Energistics] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded|CompatForestry{1.7.10R2.8.1} [MFR Compat: Forestry] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded|CompatForgeMicroblock{1.7.10R2.8.1} [MFR Compat: ForgeMicroblock] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded|CompatThaumcraft{1.7.10R2.8.1} [MFR Compat: Thaumcraft] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded|CompatThermalExpansion{1.7.10R2.8.1} [MFR Compat: Thermal Expansion] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded|CompatTConstruct{1.7.10R2.8.1} [MFR Compat: Tinkers' Construct] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded|CompatTwilightForest{1.7.10R2.8.1} [MFR Compat: TwilightForest] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	MineFactoryReloaded|CompatVanilla{1.7.10R2.8.1} [MFR Compat: Vanilla] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UCHIJAAAAAAA	MineTweaker3{3.0.10} [MineTweaker 3] (MineTweaker3-1.7.10-3.0.10B.jar) 
	UCHIJAAAAAAA	MobProperties{1.0.2} [Mob Properties] (MobProperties-1.7.10-1.0.2.jar) 
	UCHIJAAAAAAA	numina{0.4.0.131} [Numina] (Numina-0.4.0.131.jar) 
	UCHIJAAAAAAA	powersuits{0.11.0.300} [MachineMuse's Modular Powersuits] (ModularPowersuits-0.11.0.300.jar) 
	UCHIJAAAAAAA	Morph{0.9.2} [Morph] (Morph-Beta-0.9.2.jar) 
	UCHIJAAAAAAA	MouseTweaks{2.4.4} [Mouse Tweaks] (MouseTweaks-2.4.4-mc1.7.10.jar) 
	UCHIJAAAAAAA	NEIAddons{1.12.14.40} [NEI Addons] (neiaddons-1.12.14.40-mc1.7.10.jar) 
	UCHIJAAAAAAA	NEIAddons|Developer{1.12.14.40} [NEI Addons: Developer Tools] (neiaddons-1.12.14.40-mc1.7.10.jar) 
	UCHIJAAAAAAA	NEIAddons|AppEng{1.12.14.40} [NEI Addons: Applied Energistics 2] (neiaddons-1.12.14.40-mc1.7.10.jar) 
	UCHIJAAAAAAA	NEIAddons|Botany{1.12.14.40} [NEI Addons: Botany] (neiaddons-1.12.14.40-mc1.7.10.jar) 
	UCHIJAAAAAAA	NEIAddons|Forestry{1.12.14.40} [NEI Addons: Forestry] (neiaddons-1.12.14.40-mc1.7.10.jar) 
	UCHIJAAAAAAA	NEIAddons|CraftingTables{1.12.14.40} [NEI Addons: Crafting Tables] (neiaddons-1.12.14.40-mc1.7.10.jar) 
	UCHIJAAAAAAA	NEIAddons|ExNihilo{1.12.14.40} [NEI Addons: Ex Nihilo] (neiaddons-1.12.14.40-mc1.7.10.jar) 
	UCHIJAAAAAAA	neiintegration{1.1.2} [NEI Integration] (NEIIntegration-MC1.7.10-1.1.2.jar) 
	UCHIJAAAAAAA	NetherOres{1.7.10R2.3.1} [Nether Ores] (NetherOres-[1.7.10]2.3.1-22.jar) 
	UCHIJAAAAAAA	OpenMods{0.9.1} [OpenMods] (OpenModsLib-1.7.10-0.9.1.jar) 
	UCHIJAAAAAAA	OpenBlocks{1.5.1} [OpenBlocks] (OpenBlocks-1.7.10-1.5.1.jar) 
	UCHIJAAAAAAA	OpenComputers{1.5.22.46} [OpenComputers] (OpenComputers-MC1.7.10-1.5.22.46-universal.jar) 
	UCHIJAAAAAAA	MapWriter{2.1.2} [MapWriter] (Opis-1.2.5_1.7.10.jar) 
	UCHIJAAAAAAA	Opis{1.2.5} [Opis] (Opis-1.2.5_1.7.10.jar) 
	UCHIJAAAAAAA	PortalGun{4.0.0-beta-6} [PortalGun] (PortalGun-4.0.0-beta-6.jar) 
	UCHIJAAAAAAA	ProjectE{1.7.10-PE1.10.1} [ProjectE] (ProjectE-1.7.10-PE1.10.1.jar) 
	UCHIJAAAAAAA	RedstoneArsenal{1.7.10R1.1.2} [Redstone Arsenal] (RedstoneArsenal-[1.7.10]1.1.2-92.jar) 
	UCHIJAAAAAAA	libsandstone{1.0.0} [libsandstone] (LibSandstone-1.0.0.jar) 
	UCHIJAAAAAAA	xreliquary{1.2} [Reliquary] (Reliquary-1.2.jar) 
	UCHIJAAAAAAA	ResourceLoader{1.3} [Resource Loader] (ResourceLoader-MC1.7.10-1.3.jar) 
	UCHIJAAAAAAA	rftools{4.23} [RFTools] (rftools-4.23.jar) 
	UCHIJAAAAAAA	RouterReborn{1.2.0.41} [Router Reborn] (RouterReborn-1.7.10-1.2.0.41-universal.jar) 
	UCHIJAAAAAAA	secretroomsmod{4.7.1} [The SecretRoomsMod] (secretroomsmod-1.7.10-4.7.1.406.jar) 
	UCHIJAAAAAAA	simplyjetpacks{1.5.3} [Simply Jetpacks] (SimplyJetpacks-MC1.7.10-1.5.3.jar) 
	UCHIJAAAAAAA	StorageDrawers{1.7.10-1.9.7} [Storage Drawers] (StorageDrawers-1.7.10-1.9.7.jar) 
	UCHIJAAAAAAA	ThermalDynamics{1.7.10R1.2.1} [Thermal Dynamics] (ThermalDynamics-[1.7.10]1.2.1-172.jar) 
	UCHIJAAAAAAA	TiCTooltips{1.2.5} [TiC Tooltips] (TiCTooltips-mc1.7.10-1.2.5.jar) 
	UCHIJAAAAAAA	UtilityMobs{3.1.1} [Utility Mobs] (UtilityMobs-1.7.10-3.1.1.jar) 
	UCHIJAAAAAAA	VeinMiner{0.31.4_build.unknown} [Vein Miner] (VeinMiner-1.7.10_0.31.4.unknown.jar) 
	UCHIJAAAAAAA	VeinMinerModSupport{0.31.4_build.unknown} [Mod Support] (VeinMiner-1.7.10_0.31.4.unknown.jar) 
	UCHIJAAAAAAA	WebDisplay{0.12} [Web Displays] (WebDisplays-1.7.10-0.12TC.jar) 
	UCHIJAAAAAAA	witchery{0.24.1} [Witchery] (witchery-1.7.10-0.24.1.jar) 
	UCHIJAAAAAAA	worldedit{6.0-beta-01} [WorldEdit] (worldedit-forge-mc1.7.10-6.0-beta-01.jar) 
	UCHIJAAAAAAA	McMultipart{1.2.0.345} [Minecraft Multipart Plugin] (ForgeMultipart-1.7.10-1.2.0.345-universal.jar) 
	UCHIJAAAAAAA	IguanaTweaksTConstruct{1.7.10-2.1.6.163} [Iguana Tinker Tweaks] (IguanaTinkerTweaks-1.7.10-2.1.6.jar) 
	UCHIJAAAAAAA	ForgeMicroblock{1.2.0.345} [Forge Microblocks] (ForgeMultipart-1.7.10-1.2.0.345-universal.jar) 
	UD	MineFactoryReloaded|CompatAtum{1.7.10R2.8.1} [MFR Compat: Atum] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UD	MineFactoryReloaded|CompatBackTools{1.7.10R2.8.1} [MFR Compat: BackTools] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UD	MineFactoryReloaded|CompatBuildCraft{1.7.10R2.8.1} [MFR Compat: BuildCraft] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UD	MineFactoryReloaded|CompatChococraft{1.7.10R2.8.1} [MFR Compat: Chococraft] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UD	MineFactoryReloaded|CompatExtraBiomes{1.7.10R2.8.1} [MFR Compat: ExtraBiomes] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UD	MineFactoryReloaded|CompatIC2{1.7.10R2.8.1} [MFR Compat: IC2] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UD	MineFactoryReloaded|CompatProjRed{1.7.10R2.8.1} [MFR Compat ProjectRed] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UD	MineFactoryReloaded|CompatRailcraft{1.7.10R2.8.1} [MFR Compat: Railcraft] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	UD	MineFactoryReloaded|CompatSufficientBiomes{1.7.10R2.8.1} [MFR Compat: Sufficient Biomes] (MineFactoryReloaded-[1.7.10]2.8.1-174.jar) 
	GL info: ~~ERROR~~ RuntimeException: No OpenGL context found in the current thread.
	OpenModsLib class transformers: [stencil_patches:FINISHED],[movement_callback:FINISHED],[map_gen_fix:FINISHED],[gl_capabilities_hook:FINISHED],[player_render_hook:FINISHED]
	Class transformer null safety: found misbehaving transformers: squeek.applecore.asm.TransformerModuleHandler(squeek.applecore.asm.TransformerModuleHandler@2cd9b7f6) crashed with java.lang.NullPointerException(null)
	AE2 Version: beta rv3-beta-5 for Forge 10.13.4.1448
	CoFHCore: -[1.7.10]3.1.4-329
	ThermalFoundation: -[1.7.10]1.2.6-118
	ThermalExpansion: -[1.7.10]4.1.5-248
	MineFactoryReloaded: -[1.7.10]2.8.1-174
	Mantle Environment: Environment healthy.
	TConstruct Environment: Environment healthy.
	NetherOres: -[1.7.10]2.3.1-22
	RedstoneArsenal: -[1.7.10]1.1.2-92
	ThermalDynamics: -[1.7.10]1.2.1-172
	List of loaded APIs: 
		* AgriCraftAPI (1.0) from AgriCraft-1.7.10-1.5.0.jar
		* AppleCoreAPI (1.2.0) from AppleCore-mc1.7.10-1.3.0.jar
		* appliedenergistics2|API (rv3) from appliedenergistics2-rv3-beta-5.jar
		* Baubles|API (1.0.1.4) from Reliquary-1.2.jar
		* BetterAchievements|API (0.1.0) from BetterAchievements-1.7.10-0.1.0.jar
		* bluepowerAPI (1.0) from BluePower-1.7.10-0.2.962-universal.jar
		* BotaniaAPI (76) from Botania r1.8-249.jar
		* BuildCraftAPI|core (1.0) from extrautilities-1.2.12.jar
		* BuildCraftAPI|tools (1.0) from extrautilities-1.2.12.jar
		* ChiselAPI (0.1.1) from Chisel-2.9.5.11.jar
		* ChiselAPI|Carving (0.1.1) from Chisel-2.9.5.11.jar
		* ChiselAPI|Rendering (0.1.1) from Chisel-2.9.5.11.jar
		* CoFHAPI (1.7.10R1.0.2) from BrandonsCore-1.0.0.12.jar
		* CoFHAPI|block (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|core (1.7.10R1.0.12) from RouterReborn-1.7.10-1.2.0.41-universal.jar
		* CoFHAPI|energy (1.7.10R1.0.13) from ImmersiveEngineering-0.7.5.jar
		* CoFHAPI|fluid (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|inventory (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|item (1.7.10R1.0.10) from Mekanism-1.7.10-9.1.0.281.jar
		* CoFHAPI|modhelpers (1.7.10R1.1.0) from MatterOverdrive-1.7.10-0.4.1.jar
		* CoFHAPI|tileentity (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|transport (1.7.10R1.0.13) from EnderIO-1.7.10-2.3.0.424_beta.jar
		* CoFHAPI|world (1.7.10R1.0.12) from RouterReborn-1.7.10-1.2.0.41-universal.jar
		* CoFHLib (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|audio (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui|container (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui|element (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui|element|listbox (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui|slot (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|inventory (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|render (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|render|particle (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|util (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|util|helpers (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|util|position (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|world (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|world|feature (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* ComputerCraft|API (1.65) from WebDisplays-1.7.10-0.12TC.jar
		* ComputerCraft|API|FileSystem (1.65) from WebDisplays-1.7.10-0.12TC.jar
		* ComputerCraft|API|Lua (1.65) from WebDisplays-1.7.10-0.12TC.jar
		* ComputerCraft|API|Media (1.65) from WebDisplays-1.7.10-0.12TC.jar
		* ComputerCraft|API|Peripheral (1.65) from WebDisplays-1.7.10-0.12TC.jar
		* ComputerCraft|API|Redstone (1.65) from WebDisplays-1.7.10-0.12TC.jar
		* ComputerCraft|API|Turtle (1.65) from WebDisplays-1.7.10-0.12TC.jar
		* CSLib|API (0.3.0) from Decocraft-2.3.6.1_1.7.10.jar
		* DraconicEvolution|API (1.2) from Draconic-Evolution-1.7.10-1.0.2h.jar
		* EnderIOAPI (0.0.2) from EnderIO-1.7.10-2.3.0.424_beta.jar
		* EnderIOAPI|Redstone (0.0.2) from EnderIO-1.7.10-2.3.0.424_beta.jar
		* EnderIOAPI|Teleport (0.0.2) from EnderIO-1.7.10-2.3.0.424_beta.jar
		* EnderIOAPI|Tools (0.0.2) from EnderIO-1.7.10-2.3.0.424_beta.jar
		* ForestryAPI|apiculture (4.8.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|arboriculture (4.2.1) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|circuits (3.1.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|core (5.0.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|farming (2.1.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|food (1.1.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|fuels (2.0.1) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|genetics (4.7.1) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|hives (4.1.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|lepidopterology (1.3.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|mail (3.0.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|multiblock (3.0.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|recipes (5.4.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|storage (3.0.0) from forestry_1.7.10-4.2.11.59.jar
		* ForestryAPI|world (2.1.0) from forestry_1.7.10-4.2.11.59.jar
		* ImmersiveEngineering|API (1.0) from ImmersiveEngineering-0.7.5.jar
		* MatterOverdrive|API (0.4.1) from MatterOverdrive-1.7.10-0.4.1.jar
		* McJtyLib (1.8.1) from mcjtylib-1.8.1.jar
		* MekanismAPI|core (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* MekanismAPI|energy (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* MekanismAPI|gas (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* MekanismAPI|infuse (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* MekanismAPI|laser (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* MekanismAPI|reactor (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* MekanismAPI|recipe (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* MekanismAPI|transmitter (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* MekanismAPI|util (9.0.0) from Mekanism-1.7.10-9.1.0.281.jar
		* OpenBlocks|API (1.1) from OpenBlocks-1.7.10-1.5.1.jar
		* OpenComputersAPI|Component (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Core (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Driver (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Driver|Item (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Event (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|FileSystem (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Internal (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Machine (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Manual (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Network (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* OpenComputersAPI|Prefab (5.6.4) from OpenComputers-MC1.7.10-1.5.22.46-universal.jar
		* ProjectEAPI (7) from ProjectE-1.7.10-PE1.10.1.jar
		* RailcraftAPI|crafting (1.0.0) from ImmersiveEngineering-0.7.5.jar
		* StorageDrawersAPI (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* StorageDrawersAPI|config (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* StorageDrawersAPI|event (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* StorageDrawersAPI|inventory (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* StorageDrawersAPI|pack (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* StorageDrawersAPI|registry (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* StorageDrawersAPI|render (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* StorageDrawersAPI|storage (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* StorageDrawersAPI|storage-attribute (1.7.10-1.2.0) from StorageDrawers-1.7.10-1.9.7.jar
		* Thaumcraft|API (4.2.2.0) from Thaumcraft-1.7.10-4.2.3.5.jar
		* VeinMinerApi (0.1) from VeinMiner-1.7.10_0.31.4.unknown.jar
		* WailaAPI (1.2) from Waila-1.5.10_1.7.10.jar
	Chisel: Errors like "[FML]: Unable to lookup ..." are NOT the cause of this crash. You can safely ignore these errors. And update forge while you're at it.
	EnderIO: Found the following problem(s) with your installation:
                  * An unknown AE2 API is installed (rv3 from appliedenergistics2-rv3-beta-5.jar).
                    Ender IO was build against API version rv2 and may or may not work with a newer version.
                  * The RF API that is being used (1.7.10R1.0.2 from <unknown>) differes from that that is reported as being loaded (1.7.10R1.0.13 from ImmersiveEngineering-0.7.5.jar).
                    It is a supported version, but that difference may lead to problems.
                 This may have caused the error. Try reproducing the crash WITHOUT this/these mod(s) before reporting it.
	Stencil buffer state: Function set: GL30, pool: forge, bits: 8
	Forestry : Info: The following plugins have been disabled in the config: erebus
	AE2 Integration: IC2:OFF, RotaryCraft:OFF, RC:OFF, BuildCraftCore:OFF, BuildCraftTransport:OFF, BuildCraftBuilder:OFF, RF:ON, RFItem:ON, MFR:ON, DSU:ON, FZ:OFF, FMP:ON, RB:OFF, CLApi:OFF, Waila:ON, InvTweaks:ON, NEI:ON, CraftGuide:OFF, Mekanism:ON, ImmibisMicroblocks:OFF, BetterStorage:OFF, OpenComputers:ON, PneumaticCraft:OFF
	Profiler Position: N/A (disabled)
	Vec3 Pool Size: 0 (0 bytes; 0 MB) allocated, 0 (0 bytes; 0 MB) used
	Player Count: 0 / 8; []
	Type: Integrated Server (map_client.txt)
	Is Modded: Definitely; Client brand changed to 'fml,forge'
