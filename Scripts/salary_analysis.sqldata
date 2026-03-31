SELECT 
    Job_Title, 
    MAX_Salary, 
    (SELECT AVG(CAST(AVG_Salary AS FLOAT)) FROM AI_Data_Science_Job_Market) as Global_Avg_Salary
FROM 
    AI_Data_Science_Job_Market
WHERE 
    CAST(MAX_Salary AS FLOAT) > 100000
ORDER BY 
    CAST(MAX_Salary AS FLOAT) DESC
LIMIT 10;

SELECT 
    Industry, 
    COUNT(*) as High_Paying_Job_Count, 
    AVG(CAST(AVG_Salary AS FLOAT)) as Sector_Avg_Salary
FROM 
    AI_Data_Science_Job_Market
WHERE 
    CAST(MAX_Salary AS FLOAT) > 100000
GROUP BY 
    Industry
ORDER BY 
    Sector_Avg_Salary DESC;
