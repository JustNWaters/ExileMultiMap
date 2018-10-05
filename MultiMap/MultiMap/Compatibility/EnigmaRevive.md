Got Enigma Revive to work you need to edit the following line.

-Unpack @Engima\Addons\enigma_exile_revive.pbo (Possibly in your @exileserver\addons folder)
-Open 'enigma_exile_revive\compile\Enigma\Exile_RevivePlayer.sqf'
-Change the following line, located at line 270 (if not modified)
FROM
```SQF
			_playerID = format["createPlayer:%1:%2", _player getVariable ["ExileOwnerUID", "SomethingWentWrong"], _player getVariable ["ExileName", "SomethingWentWrong"]] call ExileServer_system_database_query_insertSingle;
```
TO
```SQF
			_playerID = format["createPlayer:%1:%2:%3", _player getVariable ["ExileOwnerUID", "SomethingWentWrong"], _player getVariable ["ExileName", "SomethingWentWrong"],worldName] call ExileServer_system_database_query_insertSingle;
```
