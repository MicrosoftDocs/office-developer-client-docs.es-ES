---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: 'Libera el objeto de sesión MAPI devuelto por IOlkAccountHelper:: GetMapiSession.'
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322095"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Libera el objeto de sesión MAPI devuelto por- [IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md).
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Si la implementación de **IOlkAccountHelper** crea su propia sesión MAPI que se devuelve en **IOlkAccountHelper:: GetMapiSession**, debe liberar la sesión aquí y devolver S_OK.  <br/> |
|E_NOTIMPL  <br/> |Si la implementación de **IOlkAccountHelper** no crea su propia sesión MAPI, debe devolver sólo E_NOTIMPL. En este caso, es el único valor devuelto admitido.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

