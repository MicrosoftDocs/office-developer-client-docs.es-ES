---
title: Comprobar si los datos adjuntos están bloqueados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: c1c6f960f2e24108bebdc8f6cbf08bf1d94d85ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393841"
---
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="3ec79-103">Comprobar si los datos adjuntos están bloqueados</span><span class="sxs-lookup"><span data-stu-id="3ec79-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="3ec79-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ec79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ec79-105">En este ejemplo de código en C++, se muestra cómo usar el [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interfaz para averiguar si un archivo adjunto está bloqueado por Microsoft Outlook 2010 o Microsoft Outlook 2013 para su visualización e indización.</span><span class="sxs-lookup"><span data-stu-id="3ec79-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="3ec79-106">[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) se deriva de la interfaz [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3ec79-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="3ec79-107">Puede obtener el [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interfaz mediante una llamada a [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) en el objeto de sesión MAPI, que solicita **IID_IAttachmentSecurity**.</span><span class="sxs-lookup"><span data-stu-id="3ec79-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="3ec79-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) devuelve **true** en _pfBlocked_ si los datos adjuntos se consideran seguros por Outlook 2010 o Outlook 2013 y está bloqueado para su visualización e indización en Outlook 2010 o Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec79-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
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


