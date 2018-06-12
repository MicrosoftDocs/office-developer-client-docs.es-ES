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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 2787150a9fa0fc41e04c58b4a4310ffa844f3743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817350"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="0ba10-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="0ba10-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="0ba10-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0ba10-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0ba10-105">Devuelve el almacén de mensajes que contiene el mensaje actual, si existe un almacén de este tipo.</span><span class="sxs-lookup"><span data-stu-id="0ba10-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="0ba10-106">Este método devolverá NULL en el parámetro _ppStore_ para mensajes incrustados, que se almacenan en otro mensaje en lugar de hacerlo directamente en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0ba10-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="0ba10-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ba10-107">Parameters</span></span>

 <span data-ttu-id="0ba10-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="0ba10-108">_ppStore_</span></span>
  
> <span data-ttu-id="0ba10-109">[out] Un puntero a un puntero al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0ba10-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ba10-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ba10-110">Return value</span></span>

<span data-ttu-id="0ba10-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ba10-111">S_OK</span></span> 
  
> <span data-ttu-id="0ba10-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0ba10-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0ba10-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="0ba10-113">S_FALSE</span></span> 
  
> <span data-ttu-id="0ba10-114">No hay ningún almacén que contiene el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0ba10-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ba10-115">Notas</span><span class="sxs-lookup"><span data-stu-id="0ba10-115">Remarks</span></span>

<span data-ttu-id="0ba10-116">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0ba10-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0ba10-117">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0ba10-117">MFCMAPI reference</span></span>

<span data-ttu-id="0ba10-118">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0ba10-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0ba10-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="0ba10-119">**File**</span></span>|<span data-ttu-id="0ba10-120">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="0ba10-120">**Function**</span></span>|<span data-ttu-id="0ba10-121">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="0ba10-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0ba10-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="0ba10-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="0ba10-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="0ba10-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="0ba10-124">MFCMAPI usa el método **IMAPIMessageSite::GetStore** para obtener el puntero actualmente en caché para el almacén especificado, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="0ba10-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ba10-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="0ba10-125">See also</span></span>



[<span data-ttu-id="0ba10-126">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0ba10-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="0ba10-127">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="0ba10-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0ba10-128">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="0ba10-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

