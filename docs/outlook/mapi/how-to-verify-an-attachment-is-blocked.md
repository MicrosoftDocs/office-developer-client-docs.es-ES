---
title: Comprobar si los datos adjuntos están bloqueados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345888"
---
# <a name="verify-an-attachment-is-blocked"></a>Comprobar si los datos adjuntos están bloqueados

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este ejemplo de código en C++ muestra cómo usar la interfaz [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) para averiguar si Microsoft Outlook 2010 o Microsoft Outlook 2013 bloquean los datos adjuntos para su visualización e indización. 
  
[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) se deriva de la [interfaz IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) Puede obtener la [interfaz IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) llamando a [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) en el objeto de sesión MAPI, solicitando IID_IAttachmentSecurity **.** [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) devuelve **true** en  _pfBlocked_ si Outlook 2010 u Outlook 2013 considera que los datos adjuntos no son seguros y está bloqueado para su visualización e indización en Outlook 2010 o Outlook 2013. 
  
```cpp
HRESULT IsAttachmentBlocked(LPMAPISESSION lpMAPISession, LPCWSTR pwszFileName, BOOL* pfBlocked) 
{ 
    if (!lpMAPISession || !pwszFileName || !pfBlocked) return MAPI_E_INVALID_PARAMETER; 
 
    HRESULT hRes = S_OK; 
    IAttachmentSecurity* lpAttachSec = NULL; 
    BOOL bBlocked = false; 
 
    hRes = lpMAPISession-&gt;QueryInterface(IID_IAttachmentSecurity,(void**)&amp;lpAttachSec); 
    if (SUCCEEDED(hRes) &amp;&amp; lpAttachSec) 
    { 
        hRes = lpAttachSec-&gt;IsAttachmentBlocked(pwszFileName,&amp;bBlocked); 
    } 
    if (lpAttachSec) lpAttachSec-&gt;Release(); 
 
    *pfBlocked = bBlocked; 
    return hRes; 
}

```


