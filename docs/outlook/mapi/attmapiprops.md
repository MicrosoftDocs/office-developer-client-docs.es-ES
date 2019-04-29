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
  
El atributo **attMAPIProps** es especial en que se puede usar para codificar cualquier propiedad MAPI que no tenga un homólogo en el conjunto de atributos definidos de TNEF existentes. Los datos de atributo son un conjunto contado de propiedades MAPI que se establecen de extremo a extremo. El formato de esta codificación, que permite cualquier conjunto de propiedades MAPI, es el siguiente:  
  
 _Property_Seq:_
  
> propiedad-Count _Property_Value,..._
    
Debe haber tantos elementos _Property_Value_ como indique Property-Count Value. 
  
 _Property_Value:_
  
> propiedad-Tag _Property_property-tag _Proptag_Name_
    
La etiqueta de propiedad es simplemente el valor asociado al identificador de la propiedad, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Inspector_
  
>  __ Valor de valor _,..._ de valor de recuento
    
 _Valor:_
  
> valor de datos de valor-valor de tamaño-valor de relleno de datos-valor de tamaño-valor de IID-relleno de datos
    
 _Proptag_Name:_
  
> Name-GUID nombre-tipo nombre-ID nombre-identificador GUID nombre de la clase-cadena-longitud nombre-cadena-relleno
    
La encapsulación de cada propiedad varía en función del identificador de propiedad y del tipo de propiedad. Las etiquetas de propiedad, los identificadores y los tipos se definen en los archivos de encabezado Mapitags. h y Mapidefs. h.
  
Si la propiedad es una propiedad con nombre, la etiqueta de propiedad va seguida inmediatamente por el nombre de la propiedad MAPI, formado por un identificador único global (GUID), un tipo y un identificador o una cadena Unicode.
  
Las propiedades y propiedades multivalor con valores de longitud variable, como los tipos de propiedad PT_BINARY, PT_STRING8, PT_UNICODE o PT Object, se tratan de la siguiente manera. En primer lugar, se coloca en la secuencia TNEF el número de valores, codificado como 32-bit unsigned Long, seguido de los valores individuales. Los datos de valor de cada propiedad se codifican como su tamaño en bytes seguidos de los propios datos de valor. Los datos de valor se rellenan a un límite de 4 bytes, aunque la cantidad de relleno no se incluye en el tamaño del valor.
  
Si la propiedad es del tipo PT Object, el tamaño del valor va seguido del identificador de interfaz del objeto. La implementación actual de TNEF solo admite los identificadores de interfaz IID_IMessage, IID_IStorage y IID_Istream. El tamaño del identificador de interfaz se incluye en el valor-size.
  
Si el objeto es un mensaje incrustado (es decir, tiene un tipo de propiedad de PT Object y un identificador de interfaz de IID_Imessage), los datos del valor se codifican como una secuencia TNEF incrustada. La codificación real de un mensaje incrustado en la implementación de TNEF se realiza abriendo un segundo objeto TNEF para la secuencia original y procesando la secuencia en línea.
  

