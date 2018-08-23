---
title: Compruebe que se bloquea un dato adjunto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: bb83b57de3bb484e4fb5f94f76a7d9bfa0fce876
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589801"
---
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="2a286-103">Compruebe que se bloquea un dato adjunto</span><span class="sxs-lookup"><span data-stu-id="2a286-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="2a286-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a286-105">En este ejemplo de código en C++, se muestra cómo usar el [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interfaz para averiguar si un archivo adjunto está bloqueado por Microsoft Outlook 2010 o Microsoft Outlook 2013 para su visualización e indización.</span><span class="sxs-lookup"><span data-stu-id="2a286-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="2a286-106">[IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) se deriva de la interfaz [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2a286-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="2a286-107">Puede obtener el [IAttachmentSecurity: IUnknown](iattachmentsecurityiunknown.md) interfaz mediante una llamada a [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) en el objeto de sesión MAPI, que solicita **IID_IAttachmentSecurity**.</span><span class="sxs-lookup"><span data-stu-id="2a286-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="2a286-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) devuelve **true** en _pfBlocked_ si los datos adjuntos se consideran seguros por Outlook 2010 o Outlook 2013 y está bloqueado para su visualización e indización en Outlook 2010 o Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="2a286-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
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


