# CoordBioC

Relaciona 1 dataset de latitudes y longitudes  con sus respectivos valores dentro del WorldClim BioClim v.2.1

Los datasets de latitudes y longitudes deben estar separados en ```lat.csv``` y ```lon.csv``` y estos deberán ser colocados en la carpeta de datasets para que el script funcione.
Como resultados, entrega 2 archivos ```dataframe.xslx``` y ```dataframe.csv``` en la carpeta exportdatos.

Los datos de Bioclim son en intervalo 10m y obtiene las 19 variables. Esta DB será descargada al momento de correr el script en un directorio que se creará llamado wc10.

## Referencias

Fick, S.E. and R.J. Hijmans, (2017). WorldClim 2: new 1km spatial resolution 
  climate surfaces for global land areas. 
  International Journal of Climatology 37 (12): 4302-4315.

R Core Team (2020). R: A language and environment for statistical
  computing. R Foundation for Statistical Computing, Vienna, Austria.
  URL https://www.R-project.org/.
  
Pebesma, E.J., R.S. Bivand, 2005. Classes and methods for spatial
  data in R. R News 5 (2), https://cran.r-project.org/doc/Rnews/.
  
Roger S. Bivand, Edzer Pebesma, Virgilio Gomez-Rubio, 2013. Applied
  spatial data analysis with R, Second edition. Springer, NY.
  https://asdar-book.org/
  
Robert J. Hijmans (2021). raster: Geographic Data Analysis and
  Modeling. R package version 3.4-10.
  https://CRAN.R-project.org/package=raster

Jeroen Ooms (2021). writexl: Export Data Frames to Excel 'xlsx'
  Format. R package version 1.4.0.
  https://CRAN.R-project.org/package=writexl
