---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 56bf1366cdd44fac185277280d2e8ab80c644c45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579126"
---
# <a name="srow"></a>SRow

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe una fila de una tabla que contiene las propiedades seleccionadas de un objeto específico. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a>Members

**ulAdrEntryPad**
  
> Espaciado interno bytes para alinear correctamente los valores de propiedad que señala el miembro **lpProps** . 
    
**cValues**
  
> Recuento de valores de propiedad que señala **lpProps**. 
    
**lpProps**
  
> Puntero a una matriz de estructuras [SPropValue](spropvalue.md) que describen los valores de propiedad para las columnas de la fila. 
    
## <a name="remarks"></a>Comentarios

Una estructura **SRow** describe una fila en una tabla. Se incluye en la estructura [TABLE_NOTIFICATION](table_notification.md) que acompaña a una notificación de la tabla. 
  
Estructuras de **SRow** se usan en los siguientes métodos: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData: IUnknown](itabledataiunknown.md) (muchos métodos de) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Cuando más de una fila necesita ser descrito, se usa una estructura de [SRowSet](srowset.md) . Una estructura **SRowSet** contiene una matriz de estructuras **SRow** y un recuento de las estructuras de la matriz. 
  
En la siguiente ilustración se muestra la relación entre un **SRow** y una estructura de datos **SRowSet** . 
  
**Relación entre SRow y SRowSet**
  
![Relación entre SRow y SRowSet] (media/amapi_17.gif "Relación entre SRow y SRowSet")
  
Se definen las estructuras **SRow** el mismo como estructuras [ADRENTRY](adrentry.md) . Por lo tanto, puede ser una fila de una tabla de destinatarios y una entrada en una lista de direcciones tratan de la misma. 
  
Para obtener información acerca de cómo se debe asignar la memoria para las estructuras de **SRow** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Recursos adicionales

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [Estructuras MAPI](mapi-structures.md)
- [Administrar memoria para ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

