---
title: Estructura de secuencias TNEF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430206"
---
# <a name="tnef-stream-structure"></a>Estructura de secuencias TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una secuencia TNEF comienza con una firma de 32 bits que identifica la secuencia como una secuencia TNEF. Después de la firma se muestra un entero sin firmar de 16 bits que se usa como clave para hacer referencia cruzada a los datos adjuntos a su ubicación en el texto del mensaje etiquetado. El resto de la secuencia es una secuencia de atributos TNEF. Los atributos de mensaje aparecen primero en la secuencia TNEF y los atributos de datos adjuntos siguen. Los atributos que pertenecen a un dato adjunto determinado se agrupan, empezando por el **atributo attAttachRenddata.** 
  
La mayoría de los valores de constantes usados en secuencias TNEF se definen en el TNEF. Archivo de encabezado H. En particular, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT** y todos los identificadores de atributo TNEF se definen en este archivo. Otras constantes tienen los valores indicados por su interpretación en un compilador de lenguaje C. Normalmente, estas constantes se usan para dar los tamaños del siguiente elemento. Por ejemplo, **sizeof(ULONG)** en la definición de un elemento indica que un entero que representa el tamaño del siguiente entero largo sin signo debe ocurrir en ese lugar en la secuencia TNEF. 
  
Todos los enteros de una secuencia TNEF se almacenan en forma binaria de little-endian, pero se muestran en hexadecimal a lo largo de esta sección. Los valores de suma de comprobación son simplemente enteros sin signo de 16 bits que son la suma, modulo 65536, de los bytes de datos a los que se aplica la suma de comprobación. Todas las longitudes de atributo son enteros largos sin signo, incluidos los caracteres nulos de terminación.
  
La clave es un entero sin signo distinto de cero de 16 bits que significa el valor inicial de las claves de referencia de datos adjuntos. Las claves de referencia de datos adjuntos se asignan a cada dato adjunto secuencialmente a partir del valor inicial que el proveedor de servicios que usa TNEF pasa a la función [OpenTnefStream.](opentnefstream.md) El proveedor de servicios debe generar un valor inicial aleatorio para la clave para minimizar la posibilidad de que dos mensajes usen la misma clave. 
  
La implementación de TNEF usa identificadores de atributo para asignar atributos a sus propiedades MAPI correspondientes. Un identificador de atributo es un entero sin signo de 32 bits que se forma con dos valores de palabra. La palabra de orden alto indica el tipo de datos, como cadena o binario, y la palabra de orden bajo identifica el atributo en particular. Los tipos de datos en la palabra de orden alto son:
  
|**Tipo**|**Valor**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpString  <br/> |0x0001  <br/> |
|atpText  <br/> |0x0002  <br/> |
|atpDate  <br/> |0x0003  <br/> |
|atpShort  <br/> |0x0004  <br/> |
|atpLong  <br/> |0x0005  <br/> |
|atpByte  <br/> |0x0006  <br/> |
|atpWord  <br/> |0x0007  <br/> |
|atpDword  <br/> |0x0008  <br/> |
|atpMax  <br/> |0x0009  <br/> |
   
Los valores de palabra de orden bajo para cada atributo se definen en el TNEF. Archivo de encabezado H.
  

