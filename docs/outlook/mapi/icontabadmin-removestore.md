---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435421"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Quita la libreta de direcciones de contactos (CAB) especificada por el identificador de entrada especificado de la jerarquía de la libreta de direcciones.
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [in] Puntero al identificador de entrada del objeto que se debe abrir.
    

