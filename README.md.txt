//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

                                                                VALIDACIONES POR ATRIBUTO:

1.	Código de producto: 
  Validación tipo de dato numérico INTEGER: evita el ingreso de datos inválidos como decimales, negativos u otro tipo de datos no numéricos.
  Validación unicidad: para asegurar que el producto no fue guardado antes para evitar así redundancia de datos.
  Longitud 12 – 14: longitud estándar para el código universal
2.	Nombre del producto:
  a.	Validación de dato cadena de caracteres VARCHAR: Porque el nombre puede estar compuesto por cualquier tipo de caracteres.
  b.	Se verifica que el tipo de dato no sea nulo: Por que es un campo obligatorio.
  c.	Se verifica que la longitud máxima de caracteres sea 25: Para garantizar legibilidad y practicidad. (el sistema no impedirá ingresar nombres más largos, pero necesita una validación para guardar el dato y avisará que no es recomendable nombres de más de 25 caracteres)
3.	Descripción del producto:
  a.	Validación de tipo de dato cadena de caracteres VARCHAR: Porque el nombre puede estar compuesto por cualquier tipo de caracteres para garantizar coherencia.
  b.	Validación de longitud 500 caracteres: para garantizar la legibilidad y practicidad. (el sistema no impedirá ingresar descripciones más largas, pero necesita una validación para guardar el dato y avisará que no es recomendable nombres de más de 500 caracteres)
4.	Stock inicial:
  a.	Validación tipo de dato enteros positivos INTEGER: porque el stock inicial es representado por números enteros. 
  b.	Tipos de dato no numéricos y caracteres especiales: para evitar errores a la hora de trabajar cantidades ya que las cantidades no se trabajan con letras u otros caracteres.
5.	Punto pedido:
  a.	Validación Tipo de dato enteros positivos INTEGER: para evitar el ingreso de negativos, decimales u otro tipo de dato no numérico y caracteres especiales.
6.	Fecha de compra:
  a.	Validación tipo dato fecha DATE formato dd-mm-aaaa: para que luego se pueda trabajar con fechar de manera correcta sin errores.
7.	Código de proveedor:
  a.	Validación tipo entero positivos INTEGER: para evitar el riesgo de datos decimales, negativos u otro tipo de dato no numérico.
  b.	Validación existencia: el sistema proporcionaría lista con los códigos previamente cargados para acceder a la información de los proveedores. Evita el riesgo de invocar un proveedor no existente.
8.	Precio de compra:
  a.	Validación Tipo de dato decimales positivos FLOAT: para permitir trabajar con precios decimales y evitar el riesgo del ingreso de caracteres no numéricos.
SE VERIFICA que ningún atributo esté nulo, NONE o NULL

//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

                                                                      CODIFICACIÓN:

En este caso usariamos la codificacion de codigos secuenciales simples, por varias razones:
  1. Identificación única y automática: Asignar un código secuencial a cada dato (como productos o proveedores) permite una identificación única y automática. Esto facilita la búsqueda, el seguimiento y la gestión de los elementos en el inventario.
  2. Eficiencia en búsquedas y consultas: Al no requerir conocimiento previo del objeto por su código, los usuarios pueden buscar y acceder rápidamente a la información sin necesidad de recordar nombres específicos o detalles.
  3. Cumplimiento legal: En algunos casos, la ley exige que los productos o proveedores tengan códigos únicos para rastrear su origen, garantizar la seguridad o cumplir con regulaciones específicas.
  4. Facilita la automatización: Los códigos secuenciales son fáciles de generar automáticamente mediante sistemas informáticos. Esto simplifica la entrada de datos y reduce errores humanos.
  5. Escalabilidad: A medida que se agregan más elementos al inventario, los códigos secuenciales siguen siendo efectivos sin requerir cambios significativos en la estructura del sistema.
