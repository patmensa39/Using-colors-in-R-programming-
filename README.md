# Using-colors-in-R-programming-
### Using colors in R programming ###

philant<- seq(from = 50, to = 0, by = -7) #creating a sequence from 50 to 0  
                                        
philant

barplot(philant)
barplot(philant, main = "Barplot", xlab = "Values", ylab = "frequency") # creating a barplot for the data

?colors
colors() # showing all the 657 colors

# Downloadable table of colors
browseURL(https:/datalab.cc/rcolors)

# Color names 

barplot(philant, col = "red") # red
barplot(philant, col = "blue") # blue

# RGB triplets (0.00-1.00)
barplot(philant, col = rgb(1.00, .00, .00)) # red 
barplot(philant, col = rgb(.00, .00, 1.00)) # blue

# RGB triplets (0.00-255)
barplot(philant, col = rgb(255, 0, 0, max = 255)) # red
barplot(philant, col = rgb(0, 0, 255, max = 255)) # blue

# RGB Haxacodes ##  this means base 16 
barplot(philant, col = "#FF0000") # red
barplot(philant, col = "#0000FF") # blue


# index numbers 
barplot(philant, col = colors() [552]) # red
barplot(philant, col = colors()[26]) # blue

# Using multiple colors
barplot(philant, col = c("red", "blue"))

# using palettes 
?palette
palette()

barplot(philant, col = 1:8) #Using current palettes 
barplot(philant, col = 1:6)  #Using current palettes 
barplot(philant, col = rainbow(7)) # Colors of the rainbow
barplot(philant, col = heat.colors(5)) # Yellow through red 
barplot(philant, col = terrain.colors(6)) #Gray through tan 
barplot(philant, col = topo.colors(7)) # purples through tan 
barplot(philant, col = cm.colors(6)) # Pinks and blues

dev.off() # clear plots 
