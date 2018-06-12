---
title: Formatos de fecha y hora personalizados para la función Format (aplicación web personalizada de Access)
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f7d15fe6-bdad-4f1f-aa18-12a21fc111c4
description: Aprenda a controlar cómo se muestra una fecha o una hora creando un formato personalizado.
ms.openlocfilehash: 17724cfe1c26a2b3e52eea18dfef53aff027085c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815349"
---
# <a name="custom-date-and-time-formats-for-the-format-function-access-custom-web-app"></a>Formatos de fecha y hora personalizados para la función Format (aplicación web personalizada de Access)

Aprenda a controlar cómo se muestra una fecha o una hora creando un formato personalizado.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="format-specifications"></a>Especificaciones de formato

La siguiente tabla muestra los caracteres que puede usar con la función [Función Format (aplicación web personalizada de Access)](format-function-access-custom-web-app.md) para crear formatos de fecha y de hora personalizados. 
  
|**Especificación de formato**|**Descripción**|
|:-----|:-----|
|(:)  <br/> |Separador de hora. En algunas configuraciones regionales, se pueden usar otros caracteres para representar el separador de hora. El separador de hora separa las horas, los minutos y los segundos cuando los valores de hora tienen formato. El carácter real que se usa como separador de hora en la salida con formato se determina por el valor cultural actual de la aplicación.  <br/> |
|(/)  <br/> |Separador de fecha. En algunas configuraciones regionales, se pueden usar otros caracteres para representar el separador de fecha. El separador de fecha separa el día, el mes y el año cuando los valores de fecha tienen formato. El carácter real que se usa como separador de fecha en la salida con formato se determina por la cultura actual de la aplicación.  <br/> |
|(%)  <br/> |Se usa para indicar que el siguiente carácter se debe leer como formato de letra única sin tener en cuenta las letras finales. También se usa para indicar que un formato de letra única se lee como formato definido por el usuario. Consulte a continuación para obtener más detalles.  <br/> |
|d  <br/> |Muestra el día como un número sin un cero a la izquierda (por ejemplo, 1). Use %d si es el único carácter del formato numérico definido por el usuario.  <br/> |
|dd  <br/> |Muestra el día como un número con un cero a la izquierda (por ejemplo, 01).  <br/> |
|ddd  <br/> |Muestra el día como una abreviatura (por ejemplo, Dom).  <br/> |
|dddd  <br/> |Muestra el día como un nombre completo (por ejemplo, domingo).  <br/> |
|M  <br/> |Muestra el mes como un número sin un cero a la izquierda (por ejemplo, enero se representa como 1). Use %M si es el único carácter del formato numérico definido por el usuario.  <br/> |
|MM  <br/> |Muestra el mes como un número con un cero a la izquierda (por ejemplo, 12/01/01).  <br/> |
|MMM  <br/> |Muestra el mes como una abreviatura (por ejemplo, ene).  <br/> |
|MMMM  <br/> |Muestra el mes como un nombre completo del mes (por ejemplo, enero).  <br/> |
|gg  <br/> |Muestra la cadena de periodo o era (por ejemplo, D.C.).  <br/> |
|h  <br/> |Muestra la hora como un número sin ceros a la izquierda con el reloj de 12 horas (por ejemplo, 1:15:15 PM). Use %h si es el único carácter del formato numérico definido por el usuario.  <br/> |
|hh  <br/> |Muestra la hora como un número con ceros a la izquierda con el reloj de 12 horas (por ejemplo, 01:15:15 PM).  <br/> |
|H  <br/> |Muestra la hora como un número sin ceros a la izquierda con el reloj de 24 horas (por ejemplo, 1:15:15). Use %H si es el único carácter del formato numérico definido por el usuario.  <br/> |
|HH  <br/> |Muestra la hora como un número con ceros a la izquierda con el reloj de 24 horas (por ejemplo, 01:15:15).  <br/> |
|m  <br/> |Muestra el minuto como un número sin ceros a la izquierda (por ejemplo, 12:1:15). Use %m si es el único carácter del formato numérico definido por el usuario.  <br/> |
|mm  <br/> |Muestra el minuto como un número con ceros a la izquierda (por ejemplo, 12:01:15).  <br/> |
|s  <br/> |Muestra el segundo como un número sin ceros a la izquierda (por ejemplo, 12:15:5). Use %s si es el único carácter del formato numérico definido por el usuario.  <br/> |
|ss  <br/> |Muestra el segundo como un número con ceros a la izquierda (por ejemplo, 12:15:05).  <br/> |
|f  <br/> |Muestra fracciones de segundos. Por ejemplo ff muestra centésimas de segundo, mientras que ffff muestra diez milésimas de segundo. Puede usar hasta siete símbolos f en el formato definido por el usuario. Use %f si es el único carácter del formato numérico definido por el usuario.  <br/> |
|t  <br/> |Usa el reloj de 12 horas y muestra una A mayúscula para cualquier hora antes del mediodía; muestra una P mayúscula para cualquier hora entre el mediodía y las 11:59 P.M. Use %t si es el único carácter del formato numérico definido por el usuario.  <br/> |
|tt  <br/> |Para las configuraciones regionales que usan el reloj de 12 horas, muestra AM en mayúsculas con cualquier hora antes del mediodía; muestra PM en mayúsculas con cualquier hora entre el mediodía y las 11:59 P.M.  <br/> Para las configuraciones regionales que usan el reloj de 24 horas, no muestra nada.  <br/> |
|y  <br/> |Muestra el número del año (0-9) sin ceros a la izquierda. Use %y si es el único carácter del formato numérico definido por el usuario.  <br/> |
|yy  <br/> |Muestra el año en formato numérico de dos dígitos con un cero a la izquierda, si procede.  <br/> |
|yyy  <br/> |Muestra el año en formato numérico de cuatro dígitos.  <br/> |
|yyyy  <br/> |Muestra el año en formato numérico de cuatro dígitos.  <br/> |
||Muestra el desplazamiento de zona horaria sin un cero a la izquierda (por ejemplo, -8). Use %z si es el único carácter del formato numérico definido por el usuario.  <br/> |
|z  <br/> |Muestra el desplazamiento de zona horaria con un cero a la izquierda (por ejemplo, -08).  <br/> |
|zz  <br/> |Muestra el desplazamiento de zona horaria con un cero a la izquierda (por ejemplo, -08)  <br/> |
|zzz  <br/> |Muestra el desplazamiento de zona horaria completo (por ejemplo, -08:00)  <br/> |
   
## <a name="remarks"></a>Comentarios

Las cadenas de formato distinguen mayúsculas de minúsculas. Se puede obtener un formato diferente con mayúsculas y minúsculas distintas. Por ejemplo, al dar formato a un valor de fecha con la cadena "D" obtiene la fecha en el formato largo (según la configuración regional actual). Sin embargo, si cambia la mayúscula a "d" obtiene la fecha en el formato corto. Además, pueden ocurrir resultados inesperados o errores si no coinciden las mayúsculas y minúsculas del formato deseado con las de cualquier cadena de formato definido.
  
## <a name="see-also"></a>Ver también

- [Función Format (aplicación web personalizado de Access)](format-function-access-custom-web-app.md) 
- [Formatos numéricos personalizados para la función Format (aplicación web personalizada de Access)](custom-numeric-formats-for-the-format-function-access-custom-web-app.md)
  

