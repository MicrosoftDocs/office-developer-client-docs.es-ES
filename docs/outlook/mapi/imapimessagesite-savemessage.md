---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ec85f7bdfc9d2d275bdb5ffe7ba0113ad4a35c3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817359"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="52da8-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="52da8-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="52da8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52da8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52da8-105">Solicitudes que se guarde el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="52da8-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="52da8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52da8-106">Parameters</span></span>

<span data-ttu-id="52da8-107">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="52da8-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="52da8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52da8-108">Return value</span></span>

<span data-ttu-id="52da8-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="52da8-109">S_OK</span></span> 
  
> <span data-ttu-id="52da8-110">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="52da8-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="52da8-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52da8-111">Remarks</span></span>

<span data-ttu-id="52da8-112">Formularios de llamar al método **IMAPIMessageSite::SaveMessage** para solicitar que se guarde un mensaje.</span><span class="sxs-lookup"><span data-stu-id="52da8-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="52da8-113">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="52da8-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="52da8-114">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="52da8-114">MFCMAPI reference</span></span>

<span data-ttu-id="52da8-115">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="52da8-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="52da8-116">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="52da8-116">**File**</span></span>|<span data-ttu-id="52da8-117">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="52da8-117">**Function**</span></span>|<span data-ttu-id="52da8-118">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="52da8-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="52da8-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="52da8-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="52da8-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="52da8-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="52da8-121">MFCMAPI utiliza el método **IMAPIMessageSite::SaveMessage** para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="52da8-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52da8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="52da8-122">See also</span></span>



[<span data-ttu-id="52da8-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52da8-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="52da8-124">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="52da8-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="52da8-125">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="52da8-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

