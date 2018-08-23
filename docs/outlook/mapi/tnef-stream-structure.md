---
title: Estructura de la secuencia TNEF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8eda1251-3858-4832-ac43-d817b4a7ea59
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ebe10ae741975b33ee58e1e99032aaca64ef38d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569732"
---
# <a name="tnef-stream-structure"></a>Estructura de la secuencia TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una secuencia TNEF comienza con una firma de 32 bits que identifica la secuencia como una secuencia TNEF. Después de la firma son un entero sin signo de 16 bits que se usa como una clave para hacer referencias cruzadas a los datos adjuntos a su ubicación en el texto del mensaje con etiqueta. En el resto de la secuencia es una secuencia de atributos TNEF. Los atributos de mensaje aparezcan en primer lugar en la secuencia TNEF y siga los atributos de los datos adjuntos. Los atributos que pertenecen a un dato adjunto determinado se agrupan juntos, comenzando con el atributo **attAttachRenddata** . 
  
La mayoría de los valores de constantes utilizados en las secuencias TNEF se define en el TNEF. Archivo de encabezado H. En particular, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**y todos los identificadores de atributo TNEF se definen en este archivo. Otras constantes tienen los valores indicados por su interpretación a un compilador de lenguaje C. Normalmente, esas constantes se utilizan para dar a los tamaños de los siguientes elementos. Por ejemplo, **sizeof (ulong)** en la definición de un elemento indica que debe haber un entero que representa el tamaño de la siguiente entero largo sin signo en ese lugar de la secuencia TNEF. 
  
Todos los números enteros en una secuencia TNEF se almacenan en formato binario "little-endian", pero se muestran en formato hexadecimal a lo largo de esta sección. Los valores de suma de comprobación son enteros sin signo de 16 bits simplemente que son la suma de módulo 65536, de los bytes de datos que se aplica la suma de comprobación. Todas las longitudes de atributo son enteros largos sin signo, incluidos los caracteres de terminación null.
  
La clave es un entero sin signo de distinto de cero, 16 bits que indica el valor inicial de las claves de referencia de los datos adjuntos. Las claves de referencia de los datos adjuntos se asignan a cada dato adjunto secuencialmente que comiencen por el valor inicial que se pasa a la función [OpenTnefStream](opentnefstream.md) por el proveedor de servicio que usa la codificación TNEF. El proveedor de servicios debe generar un valor aleatorio inicial para la clave reducir las posibilidades de que los dos mensajes utilizan la misma clave. 
  
La implementación de TNEF usa los identificadores de atributo para asignar los atributos a las propiedades correspondientes de MAPI. Un identificador de atributo es un entero de 32 bits sin signo formado por dos valores de word. La palabra de orden superior indica el tipo de datos, como cadena o binario, y la palabra de orden inferior identifica el atributo concreto. Los tipos de datos en la palabra de orden superior son:
  
|**Tipo**|**Valor**|
|:-----|:-----|
|atpTriples  <br/> |0x0000  <br/> |
|atpString  <br/> |0 x 0001  <br/> |
|atpText  <br/> |0x0002  <br/> |
|atpDate  <br/> |0x0003  <br/> |
|atpShort  <br/> |0x0004  <br/> |
|atpLong  <br/> |0x0005  <br/> |
|atpByte  <br/> |0x0006  <br/> |
|atpWord  <br/> |0 x 0007  <br/> |
|atpDword  <br/> |0x0008  <br/> |
|atpMax  <br/> |0 x 0009  <br/> |
   
Los valores de la palabra de orden inferior para cada atributo se definen en el TNEF. Archivo de encabezado H.
  

