---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415918"
---
# <a name="adrlist"></a>ADRLIST

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe cero o más propiedades que pertenecen a uno o más destinatarios. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Recuento de entradas en la matriz especificada por el **miembro aEntries.** 
    
**aEntries**
  
> Matriz de [estructuras ADRENTRY,](adrentry.md) una estructura para cada destinatario. 
    
## <a name="remarks"></a>Comentarios

Una **estructura ADRLIST** contiene una o más estructuras **ADRENTRY,** cada una de las que describe las propiedades de un destinatario. Un destinatario puede no resolverse. Esto significa que carece de un identificador de entrada en su matriz de valores de propiedad. Un destinatario resuelto significa que se incluye la propiedad **\_ PR ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Normalmente, los destinatarios resueltos también tienen una dirección de correo **electrónico PR_EMAIL_ADDRESS** propiedad ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). Sin embargo, la dirección de correo electrónico no es necesaria. **Las estructuras ADRLIST** se usan, por ejemplo, para describir la lista de destinatarios de un mensaje saliente y mapi para mostrar las entradas de la libreta de direcciones. 
  
**Las estructuras ADRLIST** se asemejan a [las estructuras SRowSet](srowset.md) que se usan para representar filas en tablas. De hecho, estas dos estructuras están diseñadas para que se puedan usar indistintamente. Ambos contienen una matriz de estructuras que describen un grupo de propiedades y un recuento de los valores de la matriz. Mientras que en la **estructura ADRLIST,** la matriz contiene estructuras [ADRENTRY,](adrentry.md) en la **estructura SRowSet** la matriz contiene [estructuras SRow.](srow.md) **Las estructuras ADRENTRY** y **SRow** son idénticas en diseño. Dado que las estructuras **ADRLIST** y **SRowSet** siguen las mismas reglas de asignación, una estructura **SRowSet** que se recupera de la tabla de contenido de un contenedor de libreta de direcciones se puede convertir en una estructura **ADRLIST** y usarse tal como está. 
  
En la siguiente ilustración se muestra el diseño de una **estructura ADRLIST.** 
  
**Componentes de ADRLIST**
  
![Componentes ADRLIST componentes](media/amapi_18.gif "ADRLIST")
  
Las **partes ADRENTRY** y [SPropValue](spropvalue.md) de una estructura **ADRLIST** deben asignarse y liberarse independientemente de las demás partes. Es decir, cada estructura **SPropValue** debe asignarse individualmente después de asignar y liberar la memoria de la estructura **ADRENTRY** antes de liberar la estructura **ADRENTRY.** Esta independencia en el control de la memoria permite a los destinatarios y a las propiedades de destinatarios individuales agregarse o eliminarse libremente de la lista de direcciones. 
  
Las [funciones MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIFreeBuffer](mapifreebuffer.md) deben usarse para asignar y liberar la estructura **ADRLIST** y todas sus partes. 
  
Si una lista de destinatarios es demasiado grande para caber en la memoria, los clientes pueden llamar al método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) para trabajar con un subconjunto de la lista. Los clientes no deben usar los cuadros de diálogo comunes de la libreta de direcciones en esta situación. 
  
Para obtener más información acerca de cómo asignar memoria para estructuras **ADRENTRY,** vea [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Vea también

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Estructuras MAPI](mapi-structures.md)

