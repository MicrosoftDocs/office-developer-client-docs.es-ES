---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2d4100d9bcd1b086747d742d9636c4bf7a39f50b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419460"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="7b320-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="7b320-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="7b320-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b320-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b320-105">Devuelve una interfaz de administrador de formularios, que un servidor de formularios puede usar para abrir otro servidor de formularios.</span><span class="sxs-lookup"><span data-stu-id="7b320-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="7b320-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="7b320-106">Parameters</span></span>

 <span data-ttu-id="7b320-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="7b320-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="7b320-108">[salida] Puntero a un puntero a la interfaz del administrador de formularios devuelta.</span><span class="sxs-lookup"><span data-stu-id="7b320-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b320-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b320-109">Return value</span></span>

<span data-ttu-id="7b320-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7b320-110">S_OK</span></span> 
  
> <span data-ttu-id="7b320-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="7b320-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7b320-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b320-112">Remarks</span></span>

<span data-ttu-id="7b320-113">Para obtener una lista de interfaces relacionadas con servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7b320-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7b320-114">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7b320-114">MFCMAPI reference</span></span>

<span data-ttu-id="7b320-115">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7b320-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7b320-116">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="7b320-116">**File**</span></span>|<span data-ttu-id="7b320-117">**Función**</span><span class="sxs-lookup"><span data-stu-id="7b320-117">**Function**</span></span>|<span data-ttu-id="7b320-118">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7b320-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7b320-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="7b320-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="7b320-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="7b320-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="7b320-121">MFCMAPI usa el **método IMAPIMessageSite::GetFormManager** para llamar a [MAPIOpenFormMgr](mapiopenformmgr.md) y devolver los resultados de esa llamada.</span><span class="sxs-lookup"><span data-stu-id="7b320-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b320-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b320-122">See also</span></span>



[<span data-ttu-id="7b320-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="7b320-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="7b320-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b320-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="7b320-125">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="7b320-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7b320-126">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="7b320-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

