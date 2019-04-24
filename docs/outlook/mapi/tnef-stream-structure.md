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
ms.openlocfilehash: 7e77c043e4f152740af9bdb2b8fb5b7bedece1c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327387"
---
# <a name="tnef-stream-structure"></a>Estructura de la secuencia TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un flujo TNEF comienza con una firma de 32 bits que identifica la secuencia como una secuencia TNEF. El seguimiento de la firma es un entero de 16 bits sin signo que se usa como clave para hacer una referencia cruzada de los datos adjuntos a su ubicación en el texto del mensaje etiquetado. El resto de la secuencia es una secuencia de atributos TNEF. Los atributos de mensaje aparecen primero en la secuencia TNEF y los atributos de datos adjuntos siguen. Los atributos que pertenecen a un archivo adjunto en particular se agrupan juntos, comenzando con el atributo **attAttachRenddata** . 
  
La mayoría de los valores de constantes usados en las secuencias TNEF se definen en la TNEF. H archivo de encabezado. En particular, **TNEF_SIGNATURE**, **LVL_MESSAGE**, **LVL_ATTACHMENT**, y todos los identificadores de atributo TNEF se definen en este archivo. Otras constantes tienen los valores indicados por su interpretación a un compilador de lenguaje C. Normalmente, estas constantes se usan para proporcionar los tamaños del siguiente elemento. Por ejemplo, **sizeof (ulong)** en la definición de un elemento indica que debe producirse un entero que represente el tamaño del siguiente entero largo sin signo en ese lugar del flujo TNEF. 
  
Todos los enteros de una secuencia TNEF se almacenan en formato binario Little-endian, pero se muestran en formato hexadecimal en esta sección. Los valores de suma de comprobación son sencillamente enteros sin signo de 16 bits que son la suma, módulo 65536, de los bytes de datos a los que se aplica la suma de comprobación. Todas las longitudes de atributo son enteros largos sin signo, incluidos los caracteres null de terminación.
  
La clave es un entero de 16 bits sin signo que representa el valor inicial de las claves de referencia de datos adjuntos. Las claves de referencia de datos adjuntos se asignan a todos los datos adjuntos que comienzan secuencialmente por el valor inicial que pasa a la función [OpenTnefStream](opentnefstream.md) por el proveedor de servicios que usa TNEF. El proveedor de servicios debe generar un valor inicial aleatorio para la clave a fin de minimizar la posibilidad de que dos mensajes usen la misma clave. 
  
La implementación de TNEF usa identificadores de atributo para asignar atributos a sus propiedades MAPI correspondientes. Un identificador de atributo es un entero sin signo de 32 bits formado por dos valores de palabras. La palabra de orden superior indica el tipo de datos, como String o Binary, y la palabra de orden inferior identifica el atributo en particular. Los tipos de datos en la palabra de orden superior son:
  
|**Type**|**Value**|
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
   
Los valores de palabra de orden inferior de cada atributo se definen en la TNEF. H archivo de encabezado.
  

