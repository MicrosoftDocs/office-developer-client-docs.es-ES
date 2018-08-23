---
title: Sintaxis de la secuencia TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ce2b2497bd89f00ce7f063d3e482752fabfeb731
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594337"
---
# <a name="tnef-stream-syntax"></a>Sintaxis de la secuencia TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se presenta un Nauer Bakus parecido a la descripción de la sintaxis de la secuencia TNEF. En esta descripción, no terminal elementos que tienen una definición más están en cursiva. Constantes y elementos literales están en negrita. Las secuencias de elementos se enumeran en el orden de una sola línea. Por ejemplo, el elemento de _secuencia_ consta de la constante **TNEF_SIGNATURE**, seguido de una _clave_, seguido de un _objeto_. Cuando un elemento tiene más de una implementación posible, las alternativas se muestran en líneas consecutivas. Por ejemplo, un _objeto_ puede constar de un _Message_Seq_, un _Message_Seq_ seguido de un _Attach_Seq_, o simplemente un _Attach_Seq_.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Clave_ _Objeto_
    
 _Clave:_
  
> un entero sin signo de 16 bits distinto de cero
    
Los transportes TNEF habilitado para generan este valor antes de usar la implementación de TNEF para generar una secuencia TNEF.
  
 _Objeto:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **Sizeof (ulong) attTnefVersion LVL_MESSAGE** **0 x 00010000** suma de comprobación 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** suma de comprobación de _msg_class_length msg_class_ 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> Suma de comprobación de datos de atributos de longitud de atributo **LVL_MESSAGE** identificador de atributo 
    
Identificador de atributo es uno de los identificadores de atributo TNEF, como **attSubject**. Atributo-length es la longitud en bytes de los datos del atributo. Datos de atributos son los datos asociados con el atributo.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** suma de comprobación de **sizeof(RENDDATA)** renddata 
    
Renddata es los datos asociados con la estructura **RENDDATA** que contiene la información de representación de los datos adjuntos correspondiente. La estructura **RENDDATA** se define en el TNEF. Archivo de encabezado H. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> Suma de comprobación de datos de atributos de longitud de atributo **LVL_ATTACHMENT** identificador de atributo 
    
Identificador de atributo, la longitud de atributo y datos de atributos tienen el mismo significado que para el elemento Msg_Attribute.
  

