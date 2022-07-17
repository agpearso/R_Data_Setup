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

    New_File_name$##Colum_Header_Name##

    length(New_File_name$##Colum_Header_Name##

## Stratify by a variable. Example: Age ##


    #Young adults##
    
    New_File_name_Young_adults<-New_File_name[!(New_File_name$Age=="1"),] # remove older adults from data frame #

    view(New_File_name_Young_adults)

    length(New_File_name_Young_adults$Age)

    #Older Adults##
    
    New_File_name_Older_adults<-New_File_name[!(New_File_name$Age=="0"),] # remove younger adults from data frame #

    view(New_File_name_Older_adults)

    length(New_File_name_Older_adults$Age)

