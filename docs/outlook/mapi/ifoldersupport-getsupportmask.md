---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567856"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene información sobre la compatibilidad de una carpeta para compartir.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Parámetros

 _pdwSupportMask_
  
> [out] Una máscara de bits que indica si la carpeta es compatible con el uso compartido.
    
 **FS_NONE**
  
> Indica que la carpeta no es compatible con el uso compartido.
    
 **FS_SUPPORTS_SHARING**
  
> Indica que la carpeta es compatible con el uso compartido.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada tuvo éxito.
    

