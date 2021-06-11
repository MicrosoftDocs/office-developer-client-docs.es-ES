---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410472"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="1d05c-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="1d05c-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="1d05c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d05c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d05c-105">Devuelve el almacén de mensajes que contiene el mensaje actual, si existe dicho almacén.</span><span class="sxs-lookup"><span data-stu-id="1d05c-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="1d05c-106">Este método devolverá NULL en el  _parámetro ppStore_ para los mensajes incrustados, que se almacenan en otro mensaje en lugar de directamente en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1d05c-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="1d05c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="1d05c-107">Parameters</span></span>

 <span data-ttu-id="1d05c-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="1d05c-108">_ppStore_</span></span>
  
> <span data-ttu-id="1d05c-109">[salida] Puntero a un puntero al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1d05c-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d05c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d05c-110">Return value</span></span>

<span data-ttu-id="1d05c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d05c-111">S_OK</span></span> 
  
> <span data-ttu-id="1d05c-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1d05c-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1d05c-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="1d05c-113">S_FALSE</span></span> 
  
> <span data-ttu-id="1d05c-114">No hay ningún almacén que contenga el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1d05c-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d05c-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d05c-115">Remarks</span></span>

<span data-ttu-id="1d05c-116">Para obtener una lista de interfaces relacionadas con servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="1d05c-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d05c-117">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1d05c-117">MFCMAPI reference</span></span>

<span data-ttu-id="1d05c-118">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1d05c-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d05c-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1d05c-119">**File**</span></span>|<span data-ttu-id="1d05c-120">**Función**</span><span class="sxs-lookup"><span data-stu-id="1d05c-120">**Function**</span></span>|<span data-ttu-id="1d05c-121">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1d05c-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d05c-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="1d05c-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="1d05c-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="1d05c-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="1d05c-124">MFCMAPI usa el método **IMAPIMessageSite::GetStore** para obtener el puntero almacenado actualmente en caché al almacén especificado, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="1d05c-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d05c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d05c-125">See also</span></span>



[<span data-ttu-id="1d05c-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d05c-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="1d05c-127">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="1d05c-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1d05c-128">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="1d05c-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

