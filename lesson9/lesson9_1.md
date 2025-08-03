SELECT count(*) AS "筆數"
FROM "台鐵車站資訊"

SELECT count(name) AS "台北市車站數"
FROM "台鐵車站資訊"
WHERE "stationAddrTw" LIKE '%臺北%'

SELECT "name" AS 站名, COUNT("name") AS 筆數, avg("進站人數") AS 平均進站人數
FROM "每日各站進出站人數" LEFT JOIN "台鐵車站資訊" ON "車站代碼" = "stationCode"
WHERE "日期" BETWEEN '2022-01-31' AND '2022-12-31'
GROUP BY "name" --需要用select的欄位名稱
