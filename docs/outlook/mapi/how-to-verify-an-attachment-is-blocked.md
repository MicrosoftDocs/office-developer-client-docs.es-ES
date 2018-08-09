---
title: Compruebe que se bloquea un dato adjunto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: a21383e0ea6920075a57d872e82851462bf0e8d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817014"
---
# <a name="verify-an-attachment-is-blocked"></a>Compruebe que se bloquea un dato adjunto

**Hace referencia a**: Outlook 
  
En este ejemplo de código en C++, se muestra cómo usar el [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interfaz para averiguar si un archivo adjunto está bloqueado por Microsoft Outlook 2010 o Microsoft Outlook 2013 para su visualización e indización. 
  
[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) se deriva de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) . Puede obtener el [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interfaz mediante una llamada a [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) en el objeto de sesión MAPI, que solicita **IID_IAttachmentSecurity**. [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) devuelve **true** en _pfBlocked_ si los datos adjuntos se consideran seguros por Outlook 2010 o Outlook 2013 y está bloqueado para su visualización e indización en Outlook 2010 o Outlook 2013. 
  
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


