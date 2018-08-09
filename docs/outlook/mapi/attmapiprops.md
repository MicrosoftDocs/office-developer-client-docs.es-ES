---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: eef480e8b024565ab282fb242a36336cd17384a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816460"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Hace referencia a**: Outlook 
  
El atributo **attMAPIProps** es especial en que se puede usar para codificar cualquier propiedad MAPI que no tiene un equivalente en el conjunto de atributos definidas por el TNEF existentes. Los datos del atributo están un conjunto contado de las propiedades MAPI que distribuyen un extremo a otro. El formato de codificación, lo cual permite cualquier conjunto de propiedades MAPI, que es como sigue:  
  
 _Property_Seq:_
  
> propiedad count _Property_Value..._
    
Debe haber tantos elementos _Property_Value_ tal y como indica el valor de la propiedad count. 
  
 _Property_Value:_
  
> etiqueta de la propiedad _Property_property etiqueta _Proptag_Name (propiedad)_
    
La etiqueta de propiedad es simplemente el valor asociado con el identificador de la propiedad, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Propiedad:_
  
>  Valor-recuento de _valor_ _valor..._
    
 _Valor:_
  
> datos de valor valor tamaño-datos de valor espaciado espaciado interno de datos del valor de tamaño de valor valor-IID
    
 _Proptag_Name:_
  
> relleno de nombre guid nombre del identificador de nombre de tipo de nombre-guid nombre tipo longitud de la cadena de nombre de la cadena de nombre
    
La encapsulación de cada propiedad varía según el tipo de propiedad y el identificador de la propiedad. Tipos, identificadores y etiquetas de propiedad se definen en los archivos de encabezado Mapitags.h y Mapidefs.h.
  
Si la propiedad es una propiedad con nombre, a continuación, la etiqueta de propiedad es seguida por el nombre de la propiedad MAPI, formado por un identificador único global (GUID), un tipo y un identificador o una cadena Unicode.
  
Propiedades multivalor y las propiedades con valores de longitud variable, como los tipos de propiedad PT_BINARY, PT_STRING8, PT_UNICODE o pt Object, se tratan de la siguiente manera. En primer lugar el número de valores, que se codifica como un 32-bit sin firmar durante cuánto tiempo, se coloca en la secuencia TNEF, seguida de los valores individuales. Datos del valor de la propiedad se codifican como su tamaño en bytes seguido de los datos de valor propio. Los datos del valor se rellenen hasta un límite de 4 bytes, aunque no se incluye la cantidad de relleno en el tamaño del valor.
  
Si la propiedad es de tipo pt Object, el tamaño del valor es seguido por el identificador de interfaz del objeto. La implementación actual de TNEF sólo es compatible con los identificadores de interfaz IID_IMessage, IID_IStorage y IID_Istream. El tamaño del identificador de interfaz se incluye en el tamaño del valor.
  
Si el objeto es un mensaje incrustado (es decir, tiene un tipo de propiedad de PT Object y un identificador de interfaz de IID_Imessage), los datos de valor se codifican como una secuencia de TNEF incrustada. La codificación real de un mensaje incrustado en la implementación de TNEF se realiza abriendo un segundo objeto TNEF de la secuencia original y el en línea de la secuencia de procesamiento.
  

