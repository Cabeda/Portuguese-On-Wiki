# Portuguese-On-Wiki
Data source of portugueses extracted from Portugal. Done in [Date With Date #37](https://www.transparenciahackday.org/2019/06/date-with-data-37-datas/)

# Data Source

Query extracted from [Wikidata](https://query.wikidata.org)

```
SELECT ?entity ?entityLabel ?countryLabel ?entityDescription ?dateBirth ?dateDeath ?picture
WHERE {
    ?entity wdt:P569 ?dateBirth .
    ?entity wdt:P570 ?dateDeath.
    ?entity wdt:P19 ?country.
    ?entity wdt:P18 ?picture.
    FILTER (?country = wd:Q45) #filter by country

SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }   
}
```
