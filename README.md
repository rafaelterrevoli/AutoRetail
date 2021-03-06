# Desafio de automatizaci贸n

## Contexto General 馃搵

- El framework de automatizaci贸n est谩 construido con Selenium + Java  + Junit + Cucumber
- Se empleo el patr贸n de dise帽o Page Object Model con Page Factory, este patr贸n ofrece ventajas y 
buenas pr谩cticas para la automatizaci贸n como: separaci贸n del los objetos de p谩gina de las 
  pruebas, actualizar y mantener f谩cilmente las clases objetos de p谩gina.
- Se uso Cocumber (Gherkin) para los escenarios de pruebas, esto permite un formato entendible 
  (Gherkin) por personas sin conocimientos t茅cnicos (Product Owners, negocio). 
- Junit para las validaciones (aserciones)
- Se uso maven para gestionar las librer铆as necsarias para la automatizaci贸n, el archivo pom.xml 
  contiene el listado de dependencias.
  
  
## Pre-requisitos 馃搵

- La automatizaci贸n fue hecha usando el IDE IntelliJ.
- Los datos como url y tipo de navegador para la automatizaci贸n est谩n en el archivo config.properties en src/test/resources.
- Los datos de estrada est谩n en el archivo productos.csv 
- El chromedrive esta en la ruta: "src/test/resources/driver/chromedriver.exe";
- Contenido del archivo config.properties: 


```
url=https://www.hites.com/
navegador=chrome
```

- Contenido del archivo productos.csv: 


```
productos
Mesa
Silla
Refrigerador
```


## Ejecutando las pruebas 鈿欙笍

- Abrir como proyecto maven.
- Ejecutar desde el fuente TestRunner.java en \src\test\java\runner

```
package runner;

import cucumber.api.CucumberOptions;
import cucumber.api.junit.Cucumber;
import org.junit.runner.RunWith;

@RunWith(Cucumber.class)
@CucumberOptions(
        features = "src/test/java/features/Prueba.feature",
        glue = {"steps"},
        tags = {"@prueba"}

)
public class TestRunner {

}

```


## Resultados en detalles_productos.csv 馃搫

- La ubicaci贸n del archivos es: /src/test/resources/detalles_productos.csv
- Ejemplo de los resultados:
```
Nombre Producto,SKU,Despacho a Domicilio,Retiro en Tienda
Mesa De Arrimo Universal Market Lisboa,SKU: 860053001,True,False
Juego de Comedor Casaideal Tokio / 8 Sillas,SKU: B839801,True,False
Refrigerador Side By Side Midea MRSBS-5300G689WE / No Frost / 527 Litros,SKU: 753897001,True,False
```
---
Cualquier duda me pueden contactar por: rafaelterrevoli@gmail.com 馃槉
