#importamos librerías
library(sp)
library(raster)
library(writexl)

#Creamos nuestros almacenadores de bioclim
bioclim <- getData("worldclim",var="bio",res=10)

bioclim <- bioclim[[c(1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19)]]

#Asignamos la columna de las variables de bioclim
names(bioclim) <- c("bio1","bio2","bio3","bio4","bio5","bio6","bio7","bio8","bio9","bio10","bio11","bio12","bio13","bio14","bio15","bio16","bio17","bio18","bio19")

#Leemos nuestros csvs de latitudes y longitudes y los vectorizamos
lats <- read.csv("./datasets/lat.csv", header = FALSE)
lats <- lats[,1]

lons <- read.csv("./datasets/lon.csv", header = FALSE)
lons <- lons[,1]

#Creamos un dataframe de nuestras coordenadas
coords <- data.frame(x=lons,y=lats)

#Creamos nuestro arreglo de puntos con el CRS[https://www.nceas.ucsb.edu/sites/default/files/2020-04/OverviewCoordinateReferenceSystems.pdf]
puntos <- SpatialPoints(coords, proj4string = bioclim@crs)

#Extraemos nuestro valor en la r posi
val_bioclim <- extract(bioclim,puntos)

df <- cbind.data.frame(coordinates(puntos),val_bioclim)

# print(df)

#Exportando nuestro DataFrame a 
write_xlsx(df, "./exportdatos/dataframe.xlsx")
write.csv2(df, "./exportdatos/dataframe.csv", row.names = FALSE)
