#Another try
#read in data 
#pbp_2015 <- season_play_by_play(2015)
T<-c(17,18,33,38,60) # columns I want 
Datanew <- pbp_2016[,T]
View(Datanew) # Just because 
Datanew$oteamcode <- NA # for computations later 
Datanew$dteamcode <- NA 
TEAMCODESarray <- c("DEN", "SF", "SEA", "NE", "GB", "ATL", "BAL", "HOU", "NO", "PIT", "NYG", "CIN", "WAS", "CHI", "DAL", "MIN", "DET", "MIA", "CAR", "IND", "SD", "TB", "PHI", "LA", "KC", "NYJ", "BUF", "CLE", "ARI", "TEN", "OAK", "JAX")
TEAMNUM <-c(1:32)
Datanew$oteamcode[Datanew$posteam == "DEN"] <- 1
Datanew$oteamcode[Datanew$posteam == "SF"] <- 2
Datanew$oteamcode[Datanew$posteam == "SEA"] <- 3
Datanew$oteamcode[Datanew$posteam == "NE"] <- 4
Datanew$oteamcode[Datanew$posteam == "GB"] <- 5
Datanew$oteamcode[Datanew$posteam == "ATL"] <- 6
Datanew$oteamcode[Datanew$posteam == "BAL"] <- 7
Datanew$oteamcode[Datanew$posteam == "HOU"] <- 8
Datanew$oteamcode[Datanew$posteam == "NO"] <- 9
Datanew$oteamcode[Datanew$posteam == "PIT"] <- 10
Datanew$oteamcode[Datanew$posteam == "NYG"] <- 11
Datanew$oteamcode[Datanew$posteam == "CIN"] <- 12
Datanew$oteamcode[Datanew$posteam == "WAS"] <- 13
Datanew$oteamcode[Datanew$posteam == "CHI"] <- 14
Datanew$oteamcode[Datanew$posteam == "DAL"] <- 15
Datanew$oteamcode[Datanew$posteam == "MIN"] <- 16
Datanew$oteamcode[Datanew$posteam == "DET"] <- 17
Datanew$oteamcode[Datanew$posteam == "MIA"] <- 18
Datanew$oteamcode[Datanew$posteam == "CAR"] <- 19
Datanew$oteamcode[Datanew$posteam == "IND"] <- 20
Datanew$oteamcode[Datanew$posteam == "SD"] <- 21
Datanew$oteamcode[Datanew$posteam == "TB"] <- 22
Datanew$oteamcode[Datanew$posteam == "PHI"] <- 23
Datanew$oteamcode[Datanew$posteam == "LA"] <- 24
Datanew$oteamcode[Datanew$posteam == "KC"] <- 25
Datanew$oteamcode[Datanew$posteam == "NYJ"] <- 26
Datanew$oteamcode[Datanew$posteam == "BUF"] <- 27
Datanew$oteamcode[Datanew$posteam == "CLE"] <- 28
Datanew$oteamcode[Datanew$posteam == "ARI"] <- 29
Datanew$oteamcode[Datanew$posteam == "TEN"] <- 30
Datanew$oteamcode[Datanew$posteam == "OAK"] <- 31
Datanew$oteamcode[Datanew$posteam == "JAC"] <- 32

Datanew$dteamcode[Datanew$DefensiveTeam == "DEN"] <- 1
Datanew$dteamcode[Datanew$DefensiveTeam == "SF"] <- 2
Datanew$dteamcode[Datanew$DefensiveTeam == "SEA"] <- 3
Datanew$dteamcode[Datanew$DefensiveTeam == "NE"] <- 4
Datanew$dteamcode[Datanew$DefensiveTeam == "GB"] <- 5
Datanew$dteamcode[Datanew$DefensiveTeam == "ATL"] <- 6
Datanew$dteamcode[Datanew$DefensiveTeam == "BAL"] <- 7
Datanew$dteamcode[Datanew$DefensiveTeam == "HOU"] <- 8
Datanew$dteamcode[Datanew$DefensiveTeam == "NO"] <- 9
Datanew$dteamcode[Datanew$DefensiveTeam == "PIT"] <- 10
Datanew$dteamcode[Datanew$DefensiveTeam == "NYG"] <- 11
Datanew$dteamcode[Datanew$DefensiveTeam == "CIN"] <- 12
Datanew$dteamcode[Datanew$DefensiveTeam == "WAS"] <- 13
Datanew$dteamcode[Datanew$DefensiveTeam == "CHI"] <- 14
Datanew$dteamcode[Datanew$DefensiveTeam == "DAL"] <- 15
Datanew$dteamcode[Datanew$DefensiveTeam == "MIN"] <- 16
Datanew$dteamcode[Datanew$DefensiveTeam == "DET"] <- 17
Datanew$dteamcode[Datanew$DefensiveTeam == "MIA"] <- 18
Datanew$dteamcode[Datanew$DefensiveTeam== "CAR"] <- 19
Datanew$dteamcode[Datanew$DefensiveTeam == "IND"] <- 20
Datanew$dteamcode[Datanew$DefensiveTeam == "SD"] <- 21
Datanew$dteamcode[Datanew$DefensiveTeam == "TB"] <- 22
Datanew$dteamcode[Datanew$DefensiveTeam == "PHI"] <- 23
Datanew$dteamcode[Datanew$DefensiveTeam == "LA"] <- 24
Datanew$dteamcode[Datanew$DefensiveTeam == "KC"] <- 25
Datanew$dteamcode[Datanew$DefensiveTeam == "NYJ"] <- 26
Datanew$dteamcode[Datanew$DefensiveTeam == "BUF"] <- 27
Datanew$dteamcode[Datanew$DefensiveTeam == "CLE"] <- 28
Datanew$dteamcode[Datanew$DefensiveTeam == "ARI"] <- 29
Datanew$dteamcode[Datanew$DefensiveTeam == "TEN"] <- 30
Datanew$dteamcode[Datanew$DefensiveTeam == "OAK"] <- 31
Datanew$dteamcode[Datanew$DefensiveTeam == "JAC"] <- 32

NDatanew <- na.omit(Datanew)#create new data.frame omitting rows with NA's 
OLine <- rep(0,32)
DLine <- rep(0,32)
OLineHit<-rep(0,32)
for (i in c(1:32)){
  OLine[i]<- sum(NDatanew$Sack[NDatanew$oteamcode== i])/sum(NDatanew$PassAttempt[NDatanew$oteamcode==i])
  OLineHit[i]<- sum(NDatanew$QBHit[NDatanew$oteamcode== i])/sum(NDatanew$PassAttempt[NDatanew$oteamcode==i])
  DLine[i]<- sum(NDatanew$Sack[NDatanew$dteamcode== i])/sum(NDatanew$PassAttempt[NDatanew$dteamcode==i])
}

WORK<- rep(0, 1024)#empty array to assign values 
X<-rep(0,1024)#empty array to assign values 
COUNTER<- 1 #counter 
for (i in c(1:32)){ #to work through all offenses 
  for (j in c(1:32)){ #to work through all defenses 
    X[COUNTER]<-sum(NDatanew$Sack[NDatanew$oteamcode == i & NDatanew$dteamcode == j])/sum(NDatanew$PassAttempt[NDatanew$oteamcode == i & NDatanew$dteamcode == j])
    WORK[COUNTER]<- i
    COUNTER <- COUNTER+1 #update counter
  }
}
F<- cbind(X, WORK)
f<- as.data.frame(F)
#IND<- f$X[f$WORK == 20]
#INDIANAPOLIS <- cbind(DLine, IND)
#plot(INDIANAPOLIS)
#INDIANAPOLIS <- as.data.frame(INDIANAPOLIS)
#fit<- lm(DEN~ DLine, data = INDIANAPOLIS)
#summary(fit)

z = 1
for (w in c(0:31)){
  for(r in c(1:32)){
    f[z,3]<- r
    z=z+1
  }
}
f<- na.omit(f)
for(M in c(1:32)){
  f$V3[f$D==M]<-DLine[M]
}
f$RATIO<- f$X/f$V3
OL_RANK<- rep(0,32)
for (e in c(1:32)){
  OL_RANK[e]<-mean(f$RATIO[f$WORK==e])
}
OL_RANK<- as.data.frame(OL_RANK)
OL_RANK$TEAMNAME<- NA
OL_RANK$TEAMNAME<-TEAMCODESarray
OL_RANK$rank<- NA
OL_RANK$rank[order(OL_RANK$OL_RANK)] <- 1:nrow(OL_RANK)

