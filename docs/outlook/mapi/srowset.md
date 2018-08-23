---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 82fa1b0af504cc4774b1dc077a6ef48378740d26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580680"
---
# <a name="srowset"></a>SRowSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de estructuras [SRow](srow.md) . Cada estructura **SRow** describe una fila de una tabla. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **cRows**
  
> Recuento de las estructuras de **SRow** en el miembro **aRow** . 
    
 **aRow**
  
> Matriz de estructuras **SRow** . Hay una estructura para cada fila de la tabla. 
    
## <a name="remarks"></a>Comentarios

Una estructura de **SRowSet** se usa para describir varias filas de datos de una tabla. Estructuras de **SRowSet** se usan en los métodos de interfaz [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)y [IMAPITable](imapitableiunknown.md) , además de las funciones siguientes: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 Se definen las estructuras de **SRowSet** igual que las estructuras [ADRLIST](adrlist.md) para permitir que las filas de una tabla de destinatarios y las entradas de una lista de direcciones tratan de la misma. Estructuras de **SRowSet** y estructuras **ADRLIST** se pueden pasar a métodos como [IMessage::ModifyRecipients](imessage-modifyrecipients.md) y [IAddrBook::Address](iaddrbook-address.md). 
  
Además, las reglas de asignación de memoria para las estructuras de **SRowSet** son los mismos que para las estructuras **ADRLIST** . En resumen, se debe asignar cada estructura [SPropValue](spropvalue.md) en la matriz apuntada por el miembro **lpProps** de cada fila de la fila establecer por separado mediante [MAPIAllocateBuffer](mapiallocatebuffer.md). También se debe desasignar cada estructura de valor de propiedad mediante [MAPIFreeBuffer](mapifreebuffer.md) antes de la cancelación de asignación de su estructura de **SRowSet** para que no se pierden punteros a las estructuras **SPropValue** asignados. Una fila del asigna memoria puede, a continuación, se conserva y volver a usar fuera del contexto de la estructura **SRowSet** . 
  
Para obtener más información acerca de cómo se debe asignar la memoria para las estructuras de **SRowSet** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Recursos adicionales



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Estructuras MAPI](mapi-structures.md)

