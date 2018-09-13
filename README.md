# ExileMultiMap
Switch maps and retain data for each map separately
1. Unpack your exile.mapname.pbo file
2. Copy and Paste MultiMap\mpmissions\exile.mapname\custom folder into the root of your unpacked mission folder
3. Open MultiMap\mpmissions\exile.mapname\config.cpp copy #include "custom\multimap.hpp" into config.cpp located at the root of your unpacked mission folder, the line goes inside class CfgExileCustomCode {}; as demonstrated in the config.cpp file.
4. Aslong as you haven't edited your exile.ini you may do step A. otherwise do step B.
	A. Copy MultiMap\@exileserver\extDB\sql_custom_v2\exile.ini to .\@exileserver\extDB\sql_custom_v2\exile.ini and overwrite it.
	B. (ONLY if you didn't do option A.) Open MultiMap\changes.txt and search for the text in each bracket (e.g. [getClanMarkers]) in .\@exileserver\extDB\sql_custom_v2\exile.ini and compare the queries and make appropriate changes. Repeat this for each [QUERYCOMMAND]
5. Enjoy!
