---
title: Sintaxis de secuencia TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423030"
---
# <a name="tnef-stream-syntax"></a>Sintaxis de secuencia TNEF

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se presenta una Bakus-Nauer como la descripción de la sintaxis de secuencia TNEF. En esta descripción, los elementos noterminales que tienen una definición adicional están en cursiva. Las constantes y los elementos literales están en negrita. Las secuencias de elementos se enumeran en orden en una sola línea. Por ejemplo, el  _elemento Stream_ consta de la constante **TNEF_SIGNATURE**, seguida de  _una tecla_, seguida de un objeto  _Object_. Cuando un elemento tiene más de una implementación posible, las alternativas se enumeran en líneas consecutivas. Por ejemplo, un _objeto puede_ constar de  un Message_Seq _,_ un Message_Seq seguido de un _Attach_Seq_ o simplemente un _Attach_Seq_.
  
 _TNEF_Stream:_
  
> **TNEF_SIGNATURE** _key (objeto)_ 
    
 _Clave:_
  
> un entero sin signo de 16 bits distinto de cero
    
Los transportes habilitados para TNEF generan este valor antes de usar la implementación de TNEF para generar una secuencia TNEF.
  
 _Objeto:_
  
>  _Message_Seq Message_Seq Attach_Seq Attach_Seq_
    
 _Message_Seq:_
  
>  _attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_
    
 _attTnefVersion:_
  
> LVL_MESSAGE suma de comprobación de 0x00010000 **attTnefVersion sizeof(ULONG)**  
    
 _attMessageClass:_
  
> **LVL_MESSAGE suma de comprobación msg_class_length msg_class attMessageClass**  
    
 _Msg_Attribute_Seq:_
  
>  _Msg_Attribute Msg_Attribute Msg_Attribute_Seq_
    
 _Msg_Attribute:_
  
> **LVL_MESSAGE** suma de comprobación de atributo-ID de atributo-longitud de atributo-datos 
    
Attribute-ID es uno de los identificadores de atributo TNEF, como **attSubject**. La longitud del atributo es la longitud en bytes de los datos del atributo. Los datos de atributo son los datos asociados con el atributo.
  
 _Attach_Seq:_
  
>  _attRenddata attRenddata Att_Attribute_Seq_
    
 _attRenddata:_
  
> **LVL_ATTACHMENT suma de comprobación de renddata attRenddata** **sizeof(RENDDATA)** 
    
Renddata es los datos asociados a la **estructura RENDDATA** que contiene la información de representación de los datos adjuntos correspondientes. La **estructura RENDDATA** se define en el TNEF. Archivo de encabezado H. 
  
 _Att_Attribute_Seq:_
  
>  _Att_Attribute Att_Attribute Att_Attribute_Seq_
    
 _Att_Attribute:_
  
> **LVL_ATTACHMENT** suma de comprobación de atributo-ID de atributo-longitud de atributo-datos 
    
Los datos de atributo-id, longitud de atributo y atributo tienen los mismos significados que para el Msg_Attribute atributo.
  

