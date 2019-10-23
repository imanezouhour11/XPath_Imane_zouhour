# XPath_Imane_zouhour
XPATH_tp

#### Quelle est la population de l'Afrique ? 
 - sum(//country/encompassed[@continent="africa"]/../population[last()])
#### Combien de pays en Afrique ?
 - count(//country/encompassed[@continent="africa"])
#### Quels sont les pays traversés par l' Amazone ? 
 - //country[@car_code=//river[@id="river-Amazonas"]/located/@country]/name
#### Quels sont les pays qui bordent l'océan Atlantique ?
- //country[@car_code=//sea[name="Atlantic Ocean"]/located/@country]/name
#### Combien de musulmans en Europe ?
- sum(//country/encompassed[@continent="europe"]/parent::country/religion[text()="Muslim"]/(@percentage parent::country/population[last()] div 100))
#### quels sont  les pays qui ont  la plus dun continent ?
- //country[count(encompassed)>=2]/name
#### combien de pays qui ont plus d'un continent ?
- count(//country[count(encompassed)>=2])
#### quelle sont  les pays limitrophes de l'allemagne ?
- //country[@car_code=//country[name="Germany"]/border/@country]/name
#### quelle  est le pays ou la population est la plus dense ? 
- //country/population[.=max(//country/population)]/../name
