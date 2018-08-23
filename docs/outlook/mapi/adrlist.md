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
ms.openlocfilehash: 87b91b66807ce79533029a8d5b5c4956bc4d5ce9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565770"
---
# <a name="adrlist"></a>ADRLIST

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se describen cero o más propiedades que pertenecen a uno o más destinatarios. 
  
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
  
> Número de entradas en la matriz especificada por el miembro **aEntries** . 
    
**aEntries**
  
> Matriz de estructuras [ADRENTRY](adrentry.md) , una estructura para cada destinatario. 
    
## <a name="remarks"></a>Comentarios

Una estructura de **ADRLIST** contiene una o más estructuras **ADRENTRY** , que describen las propiedades de un destinatario. Un destinatario puede ser sin resolver. Esto significa que le falta un identificador de entrada en su matriz de valores de propiedad. Un destinatario resuelto significa que el **PR\_ENTRYID** se incluye la propiedad ([PidTagEntryId](pidtagentryid-canonical-property.md)). Normalmente, los destinatarios resueltos también tienen un correo electrónico la propiedad **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) de direcciones. Sin embargo, no es necesaria la dirección de correo electrónico. Por ejemplo, las estructuras **ADRLIST** se utilizan para describir la lista de destinatarios de un mensaje saliente y por MAPI para mostrar las entradas en la libreta de direcciones. 
  
Estructuras **ADRLIST** son similares a las estructuras de [SRowSet](srowset.md) las estructuras utilizadas para representar las filas de tablas. De hecho, estas dos estructuras están diseñadas para que se pueden utilizar indistintamente. Ambos contienen una matriz de estructuras que describe un grupo de propiedades y un recuento de los valores de la matriz. Mientras que en la estructura **ADRLIST** , que contiene la matriz de estructuras [ADRENTRY](adrentry.md) , en la estructura de **SRowSet** la matriz contiene estructuras [SRow](srow.md) . Estructuras **ADRENTRY** y estructuras **SRow** son idénticas en diseño. Debido a que las estructuras **ADRLIST** y **SRowSet** seguir las mismas reglas de asignación, una estructura **SRowSet** que se recupera de la tabla de contenido de un contenedor de la libreta de direcciones se puede convertir en una estructura de **ADRLIST** y usa tal y como está. 
  
En la siguiente ilustración muestra el diseño de una estructura de **ADRLIST** . 
  
**Componentes de ADRLIST**
  
![Componentes de ADRLIST] (media/amapi_18.gif "Componentes de ADRLIST")
  
Las partes **ADRENTRY** y [SPropValue](spropvalue.md) en una estructura de **ADRLIST** deben ser asignadas y liberadas independientemente de las demás partes. Es decir, cada estructura **SPropValue** debe asignarse individualmente después de que se ha asignado y liberado antes de la estructura **ADRENTRY** se libera memoria para la estructura **ADRENTRY** . Esta independencia de gestión de memoria permite a los destinatarios y las propiedades de destinatarios individuales libremente se agregan o eliminan de la lista de direcciones. 
  
Las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIFreeBuffer](mapifreebuffer.md) deben usarse para asignar y liberar la estructura **ADRLIST** y todas sus partes. 
  
Si una lista de destinatarios es demasiado grande para que quepa en la memoria, los clientes pueden llamar al método de [IMessage::ModifyRecipients](imessage-modifyrecipients.md) para trabajar con un subconjunto de la lista. Los clientes no deben usar los cuadros de diálogo comunes de dirección libreta en esta situación. 
  
Para obtener más información acerca de cómo asignar memoria para las estructuras **ADRENTRY** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Recursos adicionales

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Estructuras MAPI](mapi-structures.md)

