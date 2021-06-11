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
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410458"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El **atributo attMAPIProps** es especial, ya que se puede usar para codificar cualquier propiedad MAPI que no tenga un equivalente en el conjunto de atributos definidos por TNEF existentes. Los datos de atributo son un conjunto de propiedades MAPI contadas de un extremo a otro. El formato de esta codificación, que permite cualquier conjunto de propiedades MAPI, es el siguiente:  
  
 _Property_Seq:_
  
> número de  _propiedades Property_Value,..._
    
Debe haber tantos  _elementos Property_Value_ como indica el valor de recuento de propiedades. 
  
 _Property_Value:_
  
> property-tag _Property_property-tag Proptag_Name  _Property_
    
La etiqueta de propiedad es simplemente el valor asociado con el identificador de propiedad, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Propiedad:_
  
>  _Value-count_  _Value,..._
    
 _Valor:_
  
> value-data value-size value-data padding value-size value-IID value-data padding
    
 _Proptag_Name:_
  
> name-guid name-kind name-id name-guid name-kind name-string-length name-string name-string padding
    
La encapsulación de cada propiedad varía según el identificador de propiedad y el tipo de propiedad. Las etiquetas de propiedad, los identificadores y los tipos se definen en los archivos de encabezado Mapitags.h y Mapidefs.h.
  
Si la propiedad es una propiedad con nombre, la etiqueta de propiedad se sigue inmediatamente con el nombre de la propiedad MAPI, que consiste en un identificador único global (GUID), un tipo y un identificador o una cadena Unicode.
  
Las propiedades y propiedades multivalor con valores de longitud variable, como los tipos de propiedad PT_BINARY, PT_STRING8, PT_UNICODE o PT_OBJECT, se tratan de la siguiente manera. En primer lugar, el número de valores, codificados como un long sin signo de 32 bits, se coloca en la secuencia TNEF, seguido de los valores individuales. Los datos de valor de cada propiedad se codifican como su tamaño en bytes seguidos de los propios datos de valor. Los datos de valor se agregan a un límite de 4 bytes, aunque la cantidad de relleno no se incluye en el tamaño del valor.
  
Si la propiedad es de tipo PT_OBJECT, el tamaño del valor va seguido del identificador de interfaz del objeto. La implementación actual de TNEF solo admite los identificadores IID_IMessage, IID_IStorage y IID_Istream de interfaz. El tamaño del identificador de interfaz se incluye en el valor-size.
  
Si el objeto es un mensaje incrustado (es decir, tiene un tipo de propiedad de PT_OBJECT y un identificador de interfaz de IID_Imessage), los datos de valor se codifican como una secuencia TNEF incrustada. La codificación real de un mensaje incrustado en la implementación de TNEF se realiza abriendo un segundo objeto TNEF para la secuencia original y procesando la secuencia en línea.
  

