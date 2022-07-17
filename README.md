## Set working directory ##

    setwd("##path on computer##")

## Load previous workspace if necessary ##

    load("##path on computer_File_name##")

    view(##File_name##)

## Install external R package to assist with data ##
    install.packages("ggplot2")
    install.packages("x")

## Load external R package for each new session ##
    library(ggplot2)
    library(x)
    
## Rename File ##

    New_File_name <- File_name

## Remove lines of data ##

    New_File_name <- New_File_name[-c(##line numbers to be removed separated with a comma##),]
    view(New_File_name)

## Double check correct lines have been removed  ##

Orthostatic_Tilt_Raw$Subject.ID
Orthostatic_Tilt_Change$Subject.ID
###

length(Orthostatic_Tilt_Raw$Subject.ID)
length(Orthostatic_Tilt_Change$Subject.ID)
###

#######################
### Stratify by sex ###
#######################

##Males##
Male_Orthostatic_Tilt_Raw<-Orthostatic_Tilt_Raw[!(Orthostatic_Tilt_Raw$Sex=="1"),] # remove Females from data frame #
Male_Orthostatic_Tilt_Change<-Orthostatic_Tilt_Change[!(Orthostatic_Tilt_Change$Sex=="1"),] # remove Females from data frame #
###
view(Male_Orthostatic_Tilt_Raw)
view(Male_Orthostatic_Tilt_Change)
###
sum(Male_Orthostatic_Tilt_Raw$Sex)
sum(Male_Orthostatic_Tilt_Change$Sex)
###
Male_Orthostatic_Tilt_Raw$Subject.ID
Male_Orthostatic_Tilt_Change$Subject.ID
###
length(Male_Orthostatic_Tilt_Raw$Subject.ID)
length(Male_Orthostatic_Tilt_Change$Subject.ID)

##Females##
Female_Orthostatic_Tilt_Raw<-Orthostatic_Tilt_Raw[!(Orthostatic_Tilt_Raw$Sex=="0"),] # remove FeFeFemale's from data frame #
Female_Orthostatic_Tilt_Change<-Orthostatic_Tilt_Change[!(Orthostatic_Tilt_Change$Sex=="0"),] # remove FeFeFemale's from data frame #
###
view(Female_Orthostatic_Tilt_Raw)
view(Female_Orthostatic_Tilt_Change)
###
sum(Female_Orthostatic_Tilt_Raw$Sex)
sum(Female_Orthostatic_Tilt_Change$Sex)
###
Female_Orthostatic_Tilt_Raw$Subject.ID
Female_Orthostatic_Tilt_Change$Subject.ID
###
length(Female_Orthostatic_Tilt_Raw$Subject.ID)
length(Female_Orthostatic_Tilt_Change$Subject.ID)

