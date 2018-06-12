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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817190"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Se aplica a**: Outlook 
  
Obtiene información sobre la compatibilidad de una carpeta para compartir.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Sintaxis

 _pdwSupportMask_
  
> [out] Una máscara de bits que indica si la carpeta es compatible con el uso compartido.
    
 **FS_NONE**
  
> Indica que la carpeta no es compatible con el uso compartido.
    
 **FS_SUPPORTS_SHARING**
  
> Indica que la carpeta es compatible con el uso compartido.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada tuvo éxito.
    

