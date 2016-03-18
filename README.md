# 18.Marzo.16
### Simular la tasa de desocpacion del ejercicio anterior
### Crear serie de tiempo con nombre tdesoc
### Para descomponer serie de tiempo se utiliza la funcion decompose()

tdesocup<-sample(3:8, 60, replace=T)
tdesoc<-ts(tdesocup,start=c(2010,1),freq=12)
tdesoc.de<-decompose(tdesoc)
names(tdesoc.de)
plot(tdesoc.de)
plot(decompose(tdesoc))
Trend<-tdesoc.de$trend
Season<-tdesoc.de$seasonal
tdesoc.dom<-decompose(tdesoc,type="mult")
