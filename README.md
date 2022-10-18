
# idTip

Adds IDs to the ingame tooltips.

![Screenshot](http://i.imgur.com/ngS3fc9.jpg)

Please report any requests/bugs through an [issue](https://github.com/ItsJustMeChris/idTip-Community-Fork/issues/new).

## Downloads

TBD

[GitHub](https://github.com/ItsJustMeChris/idTip-Community-Fork/releases)

## Usage
```
Hover over stuff

You can enable/disable displaying IDs with the command

/idtip
```

## API

##### IDTip now exposes a LibStub('idTip') library

```lua

-- The kinds of IDs you can apply to Tooltips
IDTip.kinds = {
	spell = "SpellID",
	item = "ItemID",
	unit = "NPC ID",
	quest = "QuestID",
	talent = "TalentID",
	achievement = "AchievementID",
	criteria = "CriteriaID",
	ability = "AbilityID",
	currency = "CurrencyID",
	artifactpower = "ArtifactPowerID",
	enchant = "EnchantID",
	bonus = "BonusID",
	gem = "GemID",
	mount = "MountID",
	companion = "CompanionID",
	macro = "MacroID",
	equipmentset = "EquipmentSetID",
	visual = "VisualID",
	source = "SourceID",
	species = "SpeciesID",
	icon = "IconID",
	areapoi = "AreaPoiID",
	vignette = "VignetteID",
	ctrait = "TraitNodeID",
	cgarrisontalent = "GarrisonTalentID",
	ccovenantsanctumtree = "SanctumTalentTreeID",
	cgarrisontalenttree = "GarrisonTalentTreeID",
	mission = "MissionID",
	guid = "GUID",
}

-- Inverse of the kinds table, useful for going back and forth programmatically for whatever reason
IDTip.kinds_inverse = table_invert(IDTip.kinds)

-- Add raw text to a tooltip
-- @tooltip | Tooltip frame IE: GameTooltip
-- @line | string | number the text to apply to the tooltip
function IDTipLib:addGenericLine(tooltip, line)

-- Add a 'kinds' line to a tooltip
-- @tooltip | Tooltip frame IE: GameTooltip
-- @id | a single id (string | number) or an array of id's
-- @kind | an IDTip.kinds kind
function IDTipLib:addLine(tooltip, id, kind)

-- Programmatically get all IDTip IDs applied to a tooltip
function IDTipLib:GetAllIds()

-- Add an IDTip kinds line based on the text value of a kinds key
-- @tooltip | Tooltip frame IE: GameTooltip
-- @id | a single id (string | number) or an array of id's
-- @kind | an IDTip.kinds kind
function IDTipLib:addLineByKind(frame, id, kind)

-- Register the addon loaded event listener for a specific addon
-- @addon | string Addon name
-- @cb | function callback method to invoke when addon loaded
function IDTipLib:RegisterAddonLoad(addon, cb)

-- Log a message to the chat with IDTip 'branding'
-- @... | vararg parameters to add to the print statement
function IDTipLib:Log(...)


```
