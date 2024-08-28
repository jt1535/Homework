1.1 
- Select Accel from evCars

1.2 
- Select RTRIM(Accel,' sec') as Secs from evCars

1.3 
- SELECT Accel,RTRIM(Accel,' sec')
From evCars

1.4 
- UPDATE evCars 
SET Accel = RTRIM(Accel, ' sec')

1.5 
- SELECT Accel FROM evCars

1.6 
- ALTER TABLE evCars
RENAME Accel TO accelSec

 1.7  
 - SELECT TopSpeed, Range, efficiency, FastCharge
    FROM evCars
    LIMIT 10

2.1  
- SELECT TopSpeed from evCars

2.2 
- SELECT RTRIM(TopSpeed,' km/h')
From evCars

2.3 
- SELECT TopSpeed,RTRIM(TopSpeed,' km/h')
From evCars

2.4 
- UPDATE evCars
    SET
	TopSpeed=RTRIM(TopSpeed,' km/h')

2.5 
- SELECT TopSpeed from evCars

2.6 
- SELECT TopSpeed,round((TopSpeed*.621371),1) as TopspeedMPH from evCars

- UPDATE evCars
SET
TopSpeed=round((TopSpeed*.621371),1)

- SELECT TopSpeed from evCars

2.7 
- ALTER TABLE evCars
RENAME TopSpeed TO topSpeedMPH

2.8 
- SELECT * 
FROM evCars

3.1 
- SELECT Range from evCars

3.2 
- SELECT RTRIM(Range,' km')
From evCars

3.3 
- SELECT Range,RTRIM(Range,' km')
From evCars

3.4 
- UPDATE evCars
    SET
	Range=RTRIM(Range,' km')

3.5  
- SELECT Range from evCars

3.6  
- SELECT Range,round((Range*.621371),1) as RangeMiles from evCars

- UPDATE evCars
SET
Range=round((Range*.621371),1)

- SELECT Range from evCars

3.7 
- ALTER TABLE evCars
RENAME Range TO rangeMiles

3.8 
- SELECT * FROM evCars

4.1 
- SELECT Efficiency,FastCharge from evCars

4.2 
- SELECT RTRIM(Efficiency,' Wh/km'),RTRIM(FastCharge,' km/h') From evCars


4.3 
- SELECT Efficiency,RTRIM(Efficiency,' Wh/km'),FastCharge,RTRIM(FastCharge,' km/h') From evCars

4.4 
- UPDATE evCars 
SET 
Efficiency = RTRIM(Efficiency,' Wh/km'), 
FastCharge = RTRIM(FastCharge,' km/h')

4.5 
- SELECT Efficiency,RTRIM(Efficiency,' Wh/km'),FastCharge,RTRIM(FastCharge,' km/h') From evCars

4.6 
- SELECT FastCharge,round((FastCharge*.621371),1) as OneHourFastChargeMiles from evCars

- UPDATE evCars 
SET 
FastCharge = round((FastCharge*.621371),1)

- SELECT FastCharge From evCars

4.7 
- ALTER TABLE evCars
RENAME 
FastCharge TO OneHourFastChargeMiles

- ALTER TABLE evCars
RENAME 
Efficiency to efficiencyWHperKM

4.8 
- SELECT * FROM evCars

5.1 
- SELECT RapidCharge, Count(RapidCharge)
FROM evCars
GROUP BY RapidCharge

5.2 
- UPDATE evCars
SET RapidCharge = 'yes'
WHERE RapidCharge = "Rapid charging possible"

- UPDATE evCars
SET RapidCharge = 'no'
WHERE RapidCharge = "Rapid charging not possible"

5.3 
- For the purpose of this exercise, if the car's `RapidCharge` value equals "Rapid charging possible" then I want you to change the value to 'Yes' 
- If the `RapidCharge` value equals "Rapid charging not possible" then I want you to change the value to 'No'. 

6.1 
- SELECT PowerTrain, Count(PowerTrain)
FROM evCars
GROUP BY PowerTrain

6.2
look at the three DISTINCT values from the query you wrote in 6.1 and fill in the blanks.
- If the PowerTrain equals "All Wheel Drive" then I want you to change the value to 'AWD'
- If the PowerTrain equals "Rear Wheel Drive" then I want you to change the value to 'RWD'
- If the PowerTrain equals "Front Wheel Drive" then I want you to change the value to 'FWD'

6.3 
- UPDATE evCars
SET PowerTrain = 'AWD'
WHERE PowerTrain = "All Wheel Drive"

- UPDATE evCars
SET PowerTrain = 'FWD'
WHERE PowerTrain = "Front Wheel Drive"

- UPDATE evCars
SET PowerTrain = 'RWD'
WHERE PowerTrain = "Rear Wheel Drive"

6.4 
- SELECT * FROM evCars

7.1 
- SELECT PriceEuro, Round((PriceEuro*1.09),2) as PriceUSD from evCars

7.2 
- UPDATE evCars
SET PriceEuro = Round((PriceEuro*1.09),2)

7.3 
- ALTER TABLE evCars
RENAME 
PriceEuro to PriceUSD





