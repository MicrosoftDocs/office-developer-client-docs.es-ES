---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585685"
---
# <a name="mtsid"></a>MTSID

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un identificador de entrada del sistema (MTS) de transporte de mensaje X.400. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Members

 **cb**
  
> Número de bytes de la matriz descritos por el miembro **abEntry** . 
    
 **abEntry**
  
> Matriz de bytes que contiene los datos del identificador de entrada MTS.
    
## <a name="remarks"></a>Comentarios

La estructura **MTSID** se usa solo para X.400 asignaciones de identificadores de entrada MAPI. Se corresponde con la estructura MAPI [FLATENTRY](flatentry.md) . 
  
Un identificador MTS tiene el mismo formato que un identificador de entrada MAPI o un valor de la propiedad binaria. Los identificadores MTS pueden ser especialmente útiles para cancelar mensajes diferidos. 
  
## <a name="see-also"></a>Recursos adicionales



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Estructuras MAPI](mapi-structures.md)

