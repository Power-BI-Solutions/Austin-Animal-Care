# Austin Animal Care <br><br/>

### Dashboard
<p align="center">
<img width="650em" src="" align = "center"/>
</p>
<br><br/>


### Data Source
- [Austin Animal Center Intakes](https://data.austintexas.gov/Health-and-Community-Services/Austin-Animal-Center-Intakes/wter-evkm)
- [Austin Animal Center Outcomes](https://data.austintexas.gov/Health-and-Community-Services/Austin-Animal-Center-Outcomes/9t4d-g238)

<br><br/>

### Custom Measures

```dax
Animal Counter = CALCULATE(count(Animal[Animal ID]), FILTER('Animal', OR([Intakes] > 0 , [Outcomes] > 0)))
``` 

```dax
As of Date = 
VAR LastDt = CALCULATE(MAX('Intakes'[Intake Date]), ALL('Date'))
RETURN "Data as of " & Format(LastDt, "DD MMM YYYY")
``` 


```dax
Intakes = COUNTROWS(Intakes)
``` 


```dax
Outcomes = COUNTROWS('Outcomes')
``` 

<br><br/>

### Model

<p align="center">
<img width="650em" src="" align = "center"/>
</p>
<br><br/>)

### Acknowledgement
Source: [WoW Power BI](https://www.workout-wednesday.com/pbi-2021-w06/) (Workout Wednesday)
- [Long labels tutorial](https://www.youtube.com/watch?v=UR0r0f79XRA)


