---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d5d86af111bc778839a78f9b56ba7126e6c973d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567380"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="7807f-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="7807f-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="7807f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7807f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7807f-105">Devuelve la sesión MAPI en el que se ha creado o abierto el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="7807f-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="7807f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7807f-106">Parameters</span></span>

 <span data-ttu-id="7807f-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="7807f-107">_ppSession_</span></span>
  
> <span data-ttu-id="7807f-108">[out] Un puntero a un puntero al objeto de sesión devuelto.</span><span class="sxs-lookup"><span data-stu-id="7807f-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7807f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7807f-109">Return value</span></span>

<span data-ttu-id="7807f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7807f-110">S_OK</span></span> 
  
> <span data-ttu-id="7807f-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="7807f-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7807f-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="7807f-112">S_FALSE</span></span> 
  
> <span data-ttu-id="7807f-113">No existe ninguna sesión para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="7807f-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7807f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7807f-114">Remarks</span></span>

<span data-ttu-id="7807f-115">Para obtener una lista de las interfaces que están relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7807f-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7807f-116">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7807f-116">MFCMAPI reference</span></span>

<span data-ttu-id="7807f-117">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7807f-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7807f-118">**File**</span><span class="sxs-lookup"><span data-stu-id="7807f-118">**File**</span></span>|<span data-ttu-id="7807f-119">**Función**</span><span class="sxs-lookup"><span data-stu-id="7807f-119">**Function**</span></span>|<span data-ttu-id="7807f-120">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7807f-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7807f-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="7807f-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7807f-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="7807f-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="7807f-123">MFCMAPI usa el método **IMAPIMessageSite::GetSession** para devolver el puntero de sesión actualmente en caché, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="7807f-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7807f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7807f-124">See also</span></span>



[<span data-ttu-id="7807f-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7807f-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="7807f-126">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="7807f-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

