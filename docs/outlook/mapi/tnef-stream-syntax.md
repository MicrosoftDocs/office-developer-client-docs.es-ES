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
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339637"
---
# <a name="tnef-stream-syntax"></a>Sintaxis de la secuencia TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se presenta un Bakus-Nauer como la descripción de la sintaxis de la secuencia TNEF. En esta descripción, los elementos nonterminal que tienen una definición adicional se muestran en cursiva. Las constantes y los elementos literales están en negrita. Las secuencias de elementos se enumeran en orden en una sola línea. Por ejemplo, el elemento _Stream_ se compone de la constante **TNEF_SIGNATURE**, seguida de una _clave_seguida de un _objeto_. Cuando un elemento tiene más de una implementación posible, las alternativas se enumeran en líneas consecutivas. Por ejemplo, un _objeto_ puede constar de un _Message_Seq_, un _Message_Seq_ seguido de un _Attach_Seq_o solo un _Attach_Seq_.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _Clave_ _Objeto_
    
 _Fundamental_
  
> entero de 16 bits sin signo que no es cero
    
Los transportes habilitados para TNEF generan este valor antes de usar la implementación TNEF para generar una secuencia TNEF.
  
 _DataObject_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> **LVL_MESSAGE attTnefVersion sizeof (ulong)** suma de comprobación **0x00010000** 
    
 _attMessageClass:_
  
> **LVL_MESSAGE attMessageClass** suma de comprobación de _msg_class_length msg_class_ 
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE** atributo de longitud de atributo de longitud de atributo-ID 
    
Attribute-ID es uno de los identificadores de atributo TNEF, como **attSubject**. La longitud de atributo es la longitud en bytes de los datos del atributo. Attribute-Data es el dato asociado al atributo.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT attRenddata** suma de comprobación **sizeof (RENDDATA)** RENDDATA 
    
Renddata son los datos asociados a la estructura **Renddata** que contiene la información de representación de los datos adjuntos correspondientes. La estructura **RENDDATA** se define en la TNEF. H archivo de encabezado. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** atributo de longitud de atributo de longitud de atributo-ID 
    
El identificador de atributo, la longitud de atributo y los datos de atributo tienen los mismos significados que para el elemento Msg_Attribute.
  

