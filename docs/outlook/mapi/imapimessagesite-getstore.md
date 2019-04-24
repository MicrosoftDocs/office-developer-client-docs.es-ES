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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321437"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="23bed-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="23bed-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="23bed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23bed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23bed-105">Devuelve el almacén de mensajes que contiene el mensaje actual, si existe dicho almacén.</span><span class="sxs-lookup"><span data-stu-id="23bed-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="23bed-106">Este método devolverá NULL en el parámetro _ppStore_ para los mensajes incrustados, que se almacenan en otro mensaje en lugar de directamente en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="23bed-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="23bed-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="23bed-107">Parameters</span></span>

 <span data-ttu-id="23bed-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="23bed-108">_ppStore_</span></span>
  
> <span data-ttu-id="23bed-109">contempla Un puntero a un puntero al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="23bed-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="23bed-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23bed-110">Return value</span></span>

<span data-ttu-id="23bed-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="23bed-111">S_OK</span></span> 
  
> <span data-ttu-id="23bed-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="23bed-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="23bed-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="23bed-113">S_FALSE</span></span> 
  
> <span data-ttu-id="23bed-114">No hay ningún almacén que contenga el mensaje.</span><span class="sxs-lookup"><span data-stu-id="23bed-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23bed-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23bed-115">Remarks</span></span>

<span data-ttu-id="23bed-116">Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="23bed-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="23bed-117">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="23bed-117">MFCMAPI reference</span></span>

<span data-ttu-id="23bed-118">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="23bed-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="23bed-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="23bed-119">**File**</span></span>|<span data-ttu-id="23bed-120">**Función**</span><span class="sxs-lookup"><span data-stu-id="23bed-120">**Function**</span></span>|<span data-ttu-id="23bed-121">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="23bed-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="23bed-122">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="23bed-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="23bed-123">CMyMAPIFormViewer:: GetStore</span><span class="sxs-lookup"><span data-stu-id="23bed-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="23bed-124">MFCMAPI usa el método **IMAPIMessageSite:: GetStore** para obtener el puntero actualmente almacenado en caché al almacén especificado, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="23bed-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23bed-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="23bed-125">See also</span></span>



[<span data-ttu-id="23bed-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23bed-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="23bed-127">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="23bed-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="23bed-128">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="23bed-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

