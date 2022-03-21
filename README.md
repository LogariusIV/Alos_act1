### **ALOS project.**
## Hi this my Football api project.
# The project is la liga live scores api.

**Pair : Benzidane Mohamed G2 & Belghali Abdallah G1**

the first act 1 of the project :
we generated 100 records using the code in listing 1 after of course modifying it to match our theme.
Here's our code that we use in [JSON Generator](https://next.json-generator.com/)
```
JG.repeat(1, 100, {
  id: JG.objectId(),
  name: "la liga",
   matches: {
     matchday: `${JG.integer(1, 38)}`,
     home_team: _.uniq(JG.repeat(1, JG.random('Real Madrid','SD Eibar','Athletic Club Bilbao', 'Real Betis','RC Celta Vigo','Cádiz CF','Deportivo Alavés'))),
     away_team: _.uniq(JG.repeat(1, JG.random('Valencia CF','FC Barcelona', 'Sevilla FC', 'Atlético Madrid','Granada CF','Elche CF','Getafe CF'))),
  },
  score:{
   time:_.uniq(JG.repeat(1, JG.random('Fin time','1','2','3','4','5','6','7','8','9','10','11','12','13','14','15','16','17','18','19','20','21','22','23','24','25','26','27','28','29','30','31','32','33','34','35','36','37','38','39','40','41','42','43','44','45','45+1','45+2','45+3','46','47','48','49','50','51','52','53','54','55','56','57','58','59','60','61','62','63','64','65','66','67','68','69','70','71','72','73','74','75','76','77','78','79','80','81','82','83','84','85','86','87','88','89','90','90+1','90+2','90+3','90+4','90+5'))),
   home:`${JG.integer(0, 7)}`,
   away:`${JG.integer(0, 7)}`,
  },
  statistics:{
    home_team:{
      shots:`${JG.integer(1, 25)}`,
      "Shots on target":`${JG.integer(1, 12)}`,
      passes:`${JG.integer(80, 702)}`,
      fouls:`${JG.integer(1, 15)}`,
      "yellow cards":`${JG.integer(1, 8)}`,
      "red cards":`${JG.integer(0, 1)}`,
      corners:`${JG.integer(0, 8)}`,
    },
    away_team:{
      shots:`${JG.integer(1, 25)}`,
      "Shots on target":`${JG.integer(1, 12)}`,
      passes:`${JG.integer(80, 702)}`,
      fouls:`${JG.integer(1, 15)}`,
      "yellow cards":`${JG.integer(1, 8)}`,
      "red cards":`${JG.integer(0, 1)}`,
      corners:`${JG.integer(0, 8)}`,
    }
  },

});
```
After that, we saved the data generated in a [db.json](https://github.com/LogariusIV/Alos_act1/blob/main/db.json).
Next, we start our first service by running the command
```
json-server -watch db.json
```
