-- Calculate the average concentration of nitrogen dioxide (NO2) by geographical area

SELECT `East New York`,
       AVG(`Data Value`) AS avg_NO2_concentration
FROM air_quality_data
WHERE `Name` = 'Nitrogen dioxide (NO2)'
      AND `Measure Info` = 'ppb'
GROUP BY `East New York`
ORDER BY avg_NO2_concentration DESC;