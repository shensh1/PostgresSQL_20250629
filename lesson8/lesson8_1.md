SELECT "stationCode", name, "stationAddrTw", 日期, 進站人數, 出站人數
FROM "台鐵車站資訊" LEFT JOIN "每日各站進出站人數" ON "stationCode" = "車站代碼"