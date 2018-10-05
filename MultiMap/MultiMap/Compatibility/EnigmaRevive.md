To get Enigma Revive to work you need to edit the following file.

Easy Option
1. Copy the included 'enigma_exile_revive.pbo' and overwrite '@Engima\Addons\enigma_exile_revive.pbo' (Possibly in your @exileserver\addons folder)

Manual Option
1. Unpack @Engima\Addons\enigma_exile_revive.pbo (Possibly in your @exileserver\addons folder)
2. Open 'enigma_exile_revive\compile\Enigma\Exile_RevivePlayer.sqf'
3. Change the following lines:
From:
```SQF
Line 270: 
	_playerID = format["createPlayer:%1:%2", _player getVariable ["ExileOwnerUID", "SomethingWentWrong"], _player getVariable ["ExileName", "SomethingWentWrong"]] call ExileServer_system_database_query_insertSingle;

Line 314-317:
	_player getVariable ["ExileWetness", 0],
	_playerID,
	worldName
];
```

To:
```SQF
Line 270:
	_playerID = format["createPlayer:%1:%2:%3", _player getVariable ["ExileOwnerUID", "SomethingWentWrong"], _player getVariable ["ExileName", "SomethingWentWrong"],worldName] call ExileServer_system_database_query_insertSingle;

Line 314-318:
	_player getVariable ["ExileWetness", 0],
	_playerID,
	worldName
];
```
