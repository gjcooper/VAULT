# MDS Research Details

# Contents

  - [MDS Research Details](#MDS%20Research%20Details)
      - [Additional contexts for MDS choice
        task](#MDS%20Research%20Details#Additional%20contexts%20for%20MDS%20choice%20task)
      - [Attribute search](#MDS%20Research%20Details#Attribute%20search)
          - [Rental property
            dimensions](#MDS%20Research%20Details#Attribute%20search#Rental%20property%20dimensions)
          - [Jobs](#MDS%20Research%20Details#Attribute%20search#Jobs)

## Modelling approaches

-  Running individual [[MDS]] on MDS data ala [[Single Subject MDS]]
- Focus on correlated
### Analysis ideas
- Sensitivity analysis on MDS (how volatile solution based on ends of the response scale)
- Drop participant if \> 20% dropped MDS trials
- Drop MDS trial if \< X time (X maybe 1.5 seconds)

- Look at [[MDS]] choices and the coverage of the full range, bar chart for response by participant.
- Look at MDS package used in Jess's analysis for how it deals with missing data
- R package mixl (vs mlogit), clm package may be useful to look into as well

## Multistage Plan

### Plan 1 - probit

Probit on two models, the reduced dimension (MDS) vs all attributes.  This uses the group MDS. For this there would be the likelihood function that takes in the subjects 60 choices, and the pair of phones side 1 and side 2

#### MDS model

Calculate side 2 - side 1 on dim 1 and 2 3 pars for the model, 2 slopes and intercept, and mean of utility diff distribution (udd) in par 1 \* 1st difference col + udd par 2 \* 2nd diff col + intercept pnorm(number from above)

Basic idea is to copy Reilly's SDT stuff

#### Full Attribute Model

The second version is same as first, but input is not difference in dimensions, but difference in MP, $ etc (maybe scaling on dollars etc)

### Plan 2 - ddiffusion

Use ddiffusion with the same types of input from above.

Start point is default (0.5 \* boundary separation) Needs contaminate process Non-decision time is default Still using the group MDS, Do what I did before but with, mean normal distribution is drift rate, both attributes and MDS versions here too. This extends to RT.

Better version, D1 & 2 for both phones, racing walds

For the attribute version use wither mean centered attributes, or perhaps z scored.

## Single Subject

Will need sensitivity analysis on the single subject, fix three points following Quentin's solution for 2D case.

What happens if different options(phones) were selected.

After Quentin's transformation, will probably need to rescale everyone so that no crazy large numbers are possible so each person fits within the prior.


###### Tags

#dailyNote #meeting

## Additional contexts for [[Multidimensional Scaling Phones|MDS choice task]]

Looking at acquiring a new dataset for the MDS analysis/modelling that I
am developing, and I would like to extend the scenario to a new context.
Phones are OK (re common), and most UoN students probably have some
experience of purchasing/attributes. We will be looking for another
scenario to apply the modelling to, and in particular it would be great
if each of the attributes could be continuous in nature.

Some possibilities investigated are:

  - Rental Properties - perhaps limited to single bedroom occupancy
    style rental opportunities (as the most "appropriate" for
    undergraduate University students)
  - Jobs - most likely limited to part time jobs, nice thing here is the
    flip of money attribute from a negative (higher cost is bad) to a
    positive (higher wage is good).
  - Coffee - a possible option for looking at low stress/low cost
    transactions. A few problems are the lack of continuous attribute
    dimensions and what to do for users who are not coffee drinkers.

## Attribute search

### Rental property dimensions

Lit search + website search, general format will be attribute name,
values (range/levels) and source

| Attribute                         | Values                                                                                                            | reference                                     |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| Distance to Work                  | 10min, 30min, 60min                                                                                               | carroll2016low                                |
| \\/                               | \< 3 miles, 5 miles, 10 mile, 20 miles                                                                            | liao2015compact                               |
| \\/                               | Commute time calculator                                                                                           | domain.com.au                                 |
| Condition                         | 10yrs old, 5yrs old, Brand New                                                                                    | carroll2016low                                |
| Building Energy Rating            | A -\> G                                                                                                           | carroll2016low                                |
| Area Safety, crimes per square km | 40, 70, 110                                                                                                       | carroll2016low                                |
| Rent per month                    | €800, €1000, €1200, €1400                                                                                         | carroll2016low                                |
| \\/                               | 20% less, 10% less, Same, 10% more, 20% more                                                                      | liao2015compact                               |
| \\/                               | Nlg. 800, Nlg. 1100, Nlg. 1400                                                                                    | molin1996predicting                           |
| \\/                               | Various in AUD, 200 -\> $600+                                                                                     | realestate.com.au, rent.com.au, domain.com.au |
| Bond                              | 2 weeks, 4 weeks                                                                                                  | realestate.com.au, domain.com.au              |
| Size - total                      | \(30m^2\), \(40m^2\), \(50m^2\)                                                                                   | carroll2016low, domain.com.au                 |
| Size - Living Room                | \(20m^2\), \(30m^2\), \(40m^2\)                                                                                   | molin1996predicting                           |
| Size - backyard                   | 5m, 10m, 15m                                                                                                      | molin1996predicting                           |
| Size - No. of Bedrooms            | 2, 3, 4                                                                                                           | molin1996predicting                           |
| Size - No. of bathrooms           | 1, 2                                                                                                              | realestate.com.au, rent.com.au, domain.com.au |
| Size - Car spaces                 | 0, 1                                                                                                              | rent.com.au, domain.com.au                    |
| Distance to public transport      | Rail & Bus walking distance, Bus walking distance + rail 5 mile, Bus + Rail 5 mile, Bus + Rail 10 mile drive      | liao2015compact                               |
| Street Design                     | Primarily for cars, For cars pedestrians and bikes                                                                | liao2015compact                               |
| Distance to destinations          | Walking distance, \< 3 miles, 3-10 miles, \> 10 miles                                                             | liao2015compact                               |
| Neighbourhood Buildings           | Mainly High Rise, Mix low-rise and high-rise, Mainly low-rise                                                     | molin1996predicting                           |
| \\/                               | Mix of buildings on 0.25 acre lots, Mix on 0.5 acre lots, Only homes on 0.5 acre lots, Only homes on 1+ acre lots | liao2015compact                               |
| Parking                           | In driveway/garage, On street or nearby lot (free), Off-street near house (monthly rental)                        | liao2015compact                               |
| \\/                               | Central in neighbourhood, In street, On private property                                                          | molin1996predicting                           |
| Tenure                            | Rent, Own                                                                                                         | molin1996predicting                           |
| Green space                       | Large central park, A few fairly large public gardens, More small public gardens                                  | molin1996predicting                           |
| Shopping Centre                   | Outside district, Central (one big), In neighbourhood (a few small)                                               | molin1996predicting                           |

### Jobs

| Attribute               | Values                                                                                           | Reference                |
| ----------------------- | ------------------------------------------------------------------------------------------------ | ------------------------ |
| Salary                  | 650k TSH p/month, 500k TSH p/month, 350k TSH p/month, 200k TSH p/month                           | hawkins2011reimbursement |
| \\/                     | Avg earnings, 5% above avg, 10% above avg, 20% above avg                                         | cleland2016uk            |
| \\/                     | \-50% current - +50% current                                                                     | lanfranchi2010shedding   |
| \\/                     | No change, +10%, +20%                                                                            | song2015improving        |
| Education Opportunities | After 2 years, After 4 years, After 6 years, None                                                | hawkins2011reimbursement |
| \\/                     | 3 months p/yr, 1 month p/yr, 10 day p/yr, 5 day p/yr, 1 day p/yr, None                           | lanfranchi2010shedding   |
| \\/                     | Insufficient, some, sufficient                                                                   | song2015improving        |
| Location                | Dar es Salaam, Regional Headquarters, District Headquarters, 3hr bus ride from district HQ       | hawkins2011reimbursement |
| \\/                     | Desirable, Not desirable                                                                         | cleland2016uk            |
| Equipment availability  | Sufficient, Insufficient                                                                         | hawkins2011reimbursement |
| \\/                     | Sufficient, Insufficient                                                                         | song2015improving        |
| Workload                | Normal, Heavy                                                                                    | hawkins2011reimbursement |
| \\/                     | (How demanding) Very, Fairly, Not very \* 2 for speed or deadlines                               | lanfranchi2010shedding   |
| Housing                 | Decent house, No house                                                                           | hawkins2011reimbursement |
| Infrastructure          | Mobile coverage/Electricity/Water, Unreliable mobile coverage/No electricity and water           | hawkins2011reimbursement |
| Familiarity with unit   | Unfamiliar, Quite familiar, Very familiar                                                        | cleland2016uk            |
| Partner opportunities   | Limited, Good                                                                                    | cleland2016uk            |
| Institute reputation    | Indifferent, Good, Excellent                                                                     | cleland2016uk            |
| Working conditions      | Poor, Good, Excellent                                                                            | cleland2016uk            |
| Contract Type           | Permanent NRF, Permanent RFE, Permanent RF, 1yr contract HPP, 1yr contract HPC, 1yr contract NPC | lanfranchi2010shedding   |
| Working Hours           | 20-50 hrs                                                                                        | lanfranchi2010shedding   |
| Working Schedules       | Flexible, Office hours, Rotating shifts, Set by employer and variable                            | lanfranchi2010shedding   |
| Work Oranisation        | No teamwork, varying teamwork, Work in fixed team                                                | lanfranchi2010shedding   |
| Control                 | Fixed routine, Tasks fixed but flexible with when and how, Noone controls work                   | lanfranchi2010shedding   |
| Retirement              | Before retirement age (so demanding), At 55, At 60, No early retirement, Temp - no retirement    | lanfranchi2010shedding   |
| Loyalty                 | Loyalty from both sides (no shirking), No loyalty (shirking possible)                            | lanfranchi2010shedding   |
| Welfare Benefits        | Insufficient, sufficient                                                                         | song2015improving        |
| Career development      | Insufficient, some, sufficient                                                                   | song2015improving        |
| Community respect       | Low, average, high                                                                               | song2015improving        |
