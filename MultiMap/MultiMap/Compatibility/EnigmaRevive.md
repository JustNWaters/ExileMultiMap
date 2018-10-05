Got Enigma Revive to work you need to edit the following line.

1. Unpack @Engima\Addons\enigma_exile_revive.pbo (Possibly in your @exileserver\addons folder)
2. Open 'enigma_exile_revive\compile\Enigma\Exile_RevivePlayer.sqf'
3. Change the following line, located at line 270 (if not modified)

From:
```SQF
			_playerID = format["createPlayer:%1:%2", _player getVariable ["ExileOwnerUID", "SomethingWentWrong"], _player getVariable ["ExileName", "SomethingWentWrong"]] call ExileServer_system_database_query_insertSingle;
```

To:
```SQF
			_playerID = format["createPlayer:%1:%2:%3", _player getVariable ["ExileOwnerUID", "SomethingWentWrong"], _player getVariable ["ExileName", "SomethingWentWrong"],worldName] call ExileServer_system_database_query_insertSingle;
```
