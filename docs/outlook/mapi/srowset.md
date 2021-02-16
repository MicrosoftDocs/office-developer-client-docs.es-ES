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
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407259"
---
# <a name="srowset"></a>SRowSet

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de [estructuras SRow.](srow.md) Cada **estructura de SRow** describe una fila de una tabla. 
  
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

## <a name="members"></a>Miembros

 **cRows**
  
> Recuento de **estructuras de SRow** en el **miembro aRow.** 
    
 **aRow**
  
> Matriz de **estructuras SRow.** Hay una estructura para cada fila de la tabla. 
    
## <a name="remarks"></a>Comentarios

Una **estructura SRowSet** se usa para describir varias filas de datos de una tabla. **Las estructuras SRowSet** se usan en los métodos de interfaz [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)e [IMAPITable,](imapitableiunknown.md) además de las siguientes funciones: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 **Las estructuras SRowSet** se definen igual que las estructuras [ADRLIST](adrlist.md) para permitir que las filas de una tabla de destinatarios y las entradas de una lista de direcciones se traten igual. Tanto **las estructuras SRowSet** como las estructuras **ADRLIST** se pueden pasar a métodos como [IMessage::ModifyRecipients](imessage-modifyrecipients.md) e [IAddrBook::Address](iaddrbook-address.md). 
  
Además, las reglas para la asignación de memoria para **las estructuras SRowSet** son las mismas que para las **estructuras ADRLIST.** En resumen, cada estructura [SPropValue](spropvalue.md) de la matriz a la que apunta el miembro **lpProps** de cada fila del conjunto de filas debe asignarse por separado mediante [MAPIAllocateBuffer](mapiallocatebuffer.md). También se debe desasignar cada estructura de valores de propiedad mediante [MAPIFreeBuffer](mapifreebuffer.md) antes de la desasignación de su estructura **SRowSet** para que no se pierdan los punteros a las estructuras **SPropValue** asignadas. A continuación, se puede conservar y reutilizar la memoria asignada de una fila fuera del contexto de la **estructura SRowSet.** 
  
Para obtener más información acerca de cómo se debe asignar la memoria para las estructuras **SRowSet,** vea Managing [Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Consulte también



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Estructuras MAPI](mapi-structures.md)

