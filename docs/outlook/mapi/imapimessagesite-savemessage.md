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
ms.openlocfilehash: 938eaa6c1a39d24157d5d690c42b435af6192cb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417108"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="f0cf6-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="f0cf6-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="f0cf6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0cf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0cf6-105">Solicita que se guarde el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="f0cf6-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="f0cf6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0cf6-106">Parameters</span></span>

<span data-ttu-id="f0cf6-107">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0cf6-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="f0cf6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0cf6-108">Return value</span></span>

<span data-ttu-id="f0cf6-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0cf6-109">S_OK</span></span> 
  
> <span data-ttu-id="f0cf6-110">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f0cf6-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f0cf6-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f0cf6-111">Remarks</span></span>

<span data-ttu-id="f0cf6-112">Los formularios llaman al método **IMAPIMessageSite:: SaveMessage** para solicitar que se guarde un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f0cf6-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="f0cf6-113">Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f0cf6-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f0cf6-114">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f0cf6-114">MFCMAPI reference</span></span>

<span data-ttu-id="f0cf6-115">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f0cf6-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f0cf6-116">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f0cf6-116">**File**</span></span>|<span data-ttu-id="f0cf6-117">**Función**</span><span class="sxs-lookup"><span data-stu-id="f0cf6-117">**Function**</span></span>|<span data-ttu-id="f0cf6-118">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f0cf6-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0cf6-119">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="f0cf6-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f0cf6-120">CMyMAPIFormViewer:: SaveMessage</span><span class="sxs-lookup"><span data-stu-id="f0cf6-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="f0cf6-121">MFCMAPI usa el método **IMAPIMessageSite:: SaveMessage** para guardar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f0cf6-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0cf6-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="f0cf6-122">See also</span></span>



[<span data-ttu-id="f0cf6-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0cf6-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="f0cf6-124">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="f0cf6-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f0cf6-125">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="f0cf6-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

