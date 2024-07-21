Note that our data/CO2.csv is for years 1750 ~ 2022,
and net_zero/CO2_{i}.csv is for years   1750 ~ 2100

Didn't find any article about the precise definition of net zeros, 
Using the lowest degree of polynomials that fit the description for now.


CO2_1.csv:
Annual anthropogenic greenhouse gas emissions continue to increase at the same trajectory they have for the last 20 years, 
begin to grow less quickly and then, at the year 2050, 
plateau and remain at the same level ('net zero rate of change') for the rest of the century.

For t = 2023 ~ 2050, we have:
E(t) = a(t - 2022)^2 + b(t - 2022) + c, where
    a := some value, such that E'(2050) = 2a(28) + b = 0
    b := average growth rate for the last 20 years (t = 2003 ~ 2022)
    c := some value, such that E(2022) = c = the true value in CO2.csv
For t = 2051 ~ 2100, we have:
    E(t) = E(2050)


CO2_2.csv:
Annual emission splateau now and begin to reduce until zero annual emissions are achieved at the year 2080 
then they remain zero there-after ('net-zero annual emissions' - this is the conventional meaning of 'net zero').

For t = 2023 ~ 2080, we have:
E(t) = b(t - 2022) + c, where
    c := some value, such that E(2022) = c = the true value in CO2.csv
    b := some value, such that E(2080) = b(2080 - 2022) + c = 0 
For t = 2081 ~ 2100, we have:
    E(t) = E(2080) = 0


CO2_3.csv:
Annual emissions begin to fall now and continue to do so such that zero annual emissions are achieved at the year 2050 and then they become negative. 
This continues until 2100 when as much anthropogenic carbon has been removed from the atmosphere as was originally emitted throughout history ('integrated net zero').

For t = 2023 ~ 2100, we have:
E(t) = a(t - 2022)^2 + b(t - 2022) + c, such that:
    E(2022) = c = the true value in CO2.csv
    E(2050) = a(2050 - 2022)^2 + b(2050 - 2022) + c = 0
    sum E[t = 1750~2100] = 0