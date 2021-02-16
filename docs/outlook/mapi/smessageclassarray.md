---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412698"
---
# <a name="smessageclassarray"></a>SMessageClassArray

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una matriz de punteros a cadenas de clase de mensaje.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiform.h  <br/> |
|Macro relacionada:  <br/> |[CbMessageClassArray](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a>Miembros

 **cValues**
  
> Número de punteros de cadena de clase de mensaje en la matriz.
    
 **aMessageClass**
  
> Matriz de punteros a cadenas de clase de mensaje.
    
## <a name="remarks"></a>Comentarios

La **estructura SMessageClassArray** se pasa como parámetro en los métodos siguientes: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Consulte también



[Estructuras MAPI](mapi-structures.md)

