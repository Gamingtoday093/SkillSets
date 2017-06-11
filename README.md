﻿# AutoSkill

## Default Configuration

#### Accepted values

##### AutoSkillConfiguration

`StorageType` : "memory" or "file" (if none, all players will be skilled to the max value by default)

`FilePath` : The file path (only used if StorageType == file)

`PeriodicSave` : Interval between saves in ms (only used if StorageType == file). Will be used later for mysql to batch insertions

##### SkillSet

`Name` : The name of the skillset (used in the command /skills <Name> [on|off])

`PermissionGroup` : The <Id> of the PermissionGroup located in your Permissions.config.xml (if empty, the skillset is not restricted)

`Default` : Define which SkillSet will be automatically assigned to player (you can set all your SkillSet/Default to false)

`Skills` : The Skills list (all skills missing will be set to 0 by default)


```xml
<?xml version="1.0" encoding="utf-8"?>
<AutoSkillConfiguration xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <StorageType>file</StorageType>
  <FilePath>EnabledAutoSkill.xml</FilePath>
  <PeriodicSave>10000</PeriodicSave>
  <SkillSets>
    <SkillSet>
      <Name>default</Name>
      <PermissionGroup />
      <Default>true</Default>
      <Skills>
		<Skill Name="Agriculture" Level="7" />
		<Skill Name="Cardio" Level="5" />
		<Skill Name="Cooking" Level="3" />
		<Skill Name="Crafting" Level="3" />
		<Skill Name="Dexerity" Level="5" />
		<Skill Name="Diving" Level="5" />
		<Skill Name="Engineer" Level="3" />
		<Skill Name="Exercise" Level="5" />
		<Skill Name="Fishing" Level="5" />
		<Skill Name="Healing" Level="7" />
		<Skill Name="Immunity" Level="5" />
		<Skill Name="Mechanic" Level="5" />
		<Skill Name="Outdoors" Level="5" />
		<Skill Name="Overkill" Level="7" />
		<Skill Name="Parkour" Level="5" />
		<Skill Name="Sharpshooter" Level="7" />
		<Skill Name="Sneakybeaky" Level="7" />
		<Skill Name="Strength" Level="5" />
		<Skill Name="Survival" Level="5" />
		<Skill Name="Toughness" Level="5" />
		<Skill Name="Vitality" Level="5" />
		<Skill Name="Warmblooded" Level="5" />
    </SkillSet>
  </SkillSets>
</AutoSkillConfiguration>
```

## Default Translation

```xml
<?xml version="1.0" encoding="utf-8"?>
<Translations xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <Translation Id="PERMISSION_MISSING" Value="Missing permission" />
  <Translation Id="UNKNOWN_COMMAND" Value="Unknown command &quot;{0}&quot;" />
  <Translation Id="SETMAXSKILL_DONE" Value="Skillset applied" />
  <Translation Id="SETAUTOSKILL_ON" Value="Your skills will be set even if you die (I hope not)" />
  <Translation Id="SETAUTOSKILL_OFF" Value="Your skills will no longer be set after death automatically" />
  <Translation Id="UNVALID_USAGE" Value="Invalid Usage" />
</Translations>
```
