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
ms.openlocfilehash: 3176280de33bda01bfd09ebaafc31d326d455a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575038"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Reemplaza [MAPIInitialize](mapiinitialize.md) cuando se usan sólo las funciones de utilidad select. 
  
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

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las funciones **ScInitMapiUtil** y [DeinitMapiUtil](deinitmapiutil.md) cooperan para llamar a y seleccione utilidad funciones, en lugar de [MAPIInitialize](mapiinitialize.md), que llama a principal, así como la utilidad de funciones de la versión. Cuando **ScInitMapiUtil** llama a las funciones de utilidad, también inicializa la memoria necesaria. 
  
Una vez finalizada la utilización de las funciones que se ha llamado a **ScInitMapiUtil** , **DeinitMapiUtil** debe llamarse explícitamente para liberarlos. Por el contrario, **MAPIInitialize** implícitamente llama a **DeinitMapiUtil**. 
  
## <a name="see-also"></a>Vea también



[MAPIUninitialize](mapiuninitialize.md)

