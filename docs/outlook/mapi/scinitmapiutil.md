---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420594"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Reemplaza [MAPIInitialize](mapiinitialize.md) cuando solo se usan funciones de utilidad selectas. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las **funciones ScInitMapiUtil** y [DeinitMapiUtil](deinitmapiutil.md) colaboran para llamar y liberar funciones de utilidad select, en lugar de [MAPIInitialize](mapiinitialize.md), que llama a las funciones principales y de utilidad. Cuando **ScInitMapiUtil llama** a funciones de utilidad, también inicializa la memoria necesaria. 
  
Cuando se complete el uso de las funciones a las que **scInitMapiUtil** ha llamado, se debe llamar explícitamente **a DeinitMapiUtil** para liberarlas. En cambio, **MAPIInitialize** llama implícitamente **a DeinitMapiUtil**. 
  
## <a name="see-also"></a>Vea también



[MAPIUninitialize](mapiuninitialize.md)

