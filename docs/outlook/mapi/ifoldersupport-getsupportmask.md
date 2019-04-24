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
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350837"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Obtiene información sobre la compatibilidad de una carpeta con el uso compartido.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Parameters

 _pdwSupportMask_
  
> contempla Máscara de máscara que indica si la carpeta admite el uso compartido.
    
 **FS_NONE**
  
> Indica que la carpeta no admite el uso compartido.
    
 **FS_SUPPORTS_SHARING**
  
> Indica que la carpeta admite el uso compartido.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realizó correctamente.
    

