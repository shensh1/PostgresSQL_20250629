
SELECT "name" AS 站名, COUNT("name") AS 筆數, avg("進站人數") AS 平均進站人數
FROM "每日各站進出站人數" LEFT JOIN "台鐵車站資訊" ON "車站代碼" = "stationCode"
WHERE "日期" BETWEEN '2022-01-31' AND '2022-12-31'
GROUP BY "name" --需要用select的欄位名稱

SELECT "name" AS 站名, date_part('year', "日期") AS "年份", COUNT("name") AS 筆數, avg("進站人數") AS 平均進站人數
FROM "每日各站進出站人數" LEFT JOIN "台鐵車站資訊" ON "車站代碼" = "stationCode"
--WHERE "日期" BETWEEN '2022-01-31' AND '2022-12-31'
WHERE "name" = '基隆'
GROUP BY "name", "年份" --需要用select的欄位名稱一致
ORDER BY "平均進站人數" DESC;   --需要用select的欄位名稱一致，例如；不能用"進站人數"，而是必須用"平均進站人數"