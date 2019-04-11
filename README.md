# urban-forest-challenge

### Environment
1. scala 2.11.12
2. sbt 1.2.8
3. spark 2.3.2
4. spark standalone cluster with one slave

### Command and configuration
1. The command to submit the spark job. 
```
/bin/spark-submit --properties-file ./spark-defaults.conf --class UrbanForest --jars ~/challenge-urban-forest-jar-assembly-0.0.1.jar ~/eliiza_2.11-0.1.jar /var/lib/spark/data/melb_inner_2016.json /var/lib/spark/data/melb_urban_forest_2016.txt
```
2. Configuration property file
```
spark.master spark://10.224.151.255:7077
spark.executor.cores 2
spark.executor.memory 2g
```

### The result
1. With the above configuraton and environment, the spark job takes around 90 mininutes to finish


2. The result sorted in descending order on ratio
```
(Collingwood,469.0000361899823)
(Brunswick,469.0000280460123)
(Fitzroy,469.0000237161336)
(Richmond (Vic.),469.0000159593949)
(South Melbourne,469.00001322621506)
(Brunswick West,469.00000940746753)
(Flemington,469.00000084918963)
(Fitzroy North,469.0000000481417)
(Prahran - Windsor,469.0)
(Armadale,469.0)
(Ascot Vale,469.0)
(Coburg,469.0)
(Toorak,469.0)
(Elwood,469.0)
(Essendon - Aberfeldie,469.0)
(St Kilda,469.0)
(St Kilda East,469.0)
(Yarra - North,469.0)
(Pascoe Vale South,469.0)
(Port Melbourne,469.0)
(Abbotsford,469.0)
(Northcote,469.0)
(South Yarra - East,469.0)
(Moonee Ponds,469.0)
(Albert Park,469.0)
(Alphington - Fairfield,469.0)
(Thornbury,468.9999999062709)
(Brunswick East,468.9999997905837)
(Flemington Racecourse,467.0686394028727)
(Docklands,461.02587389453544)
(West Melbourne,461.01847603654375)
(Carlton North - Princes Hill,449.0545919045069)
(Carlton,444.1882178198951)
(Port Melbourne Industrial,441.0265151017143)
(South Yarra - West,439.1906877555864)
(Kensington (Vic.),429.1224325897427)
(Melbourne,429.0817454854592)
(North Melbourne,403.10982145266365)
(Southbank,391.21011667463563)
(East Melbourne,368.09465868409586)
(Parkville,289.19843514300675)
```
