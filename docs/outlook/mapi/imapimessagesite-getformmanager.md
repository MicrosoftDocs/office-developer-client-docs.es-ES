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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: abaf8f665ea7add92a34c2e4d6fcbf9d5fc08d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817356"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="208d5-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="208d5-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="208d5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="208d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="208d5-105">Devuelve una interfaz de administrador de formulario, que puede usar un servidor de formulario para abrir otro servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="208d5-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="208d5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="208d5-106">Parameters</span></span>

 <span data-ttu-id="208d5-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="208d5-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="208d5-108">[out] Un puntero a un puntero a la interfaz de administrador de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="208d5-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="208d5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="208d5-109">Return value</span></span>

<span data-ttu-id="208d5-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="208d5-110">S_OK</span></span> 
  
> <span data-ttu-id="208d5-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="208d5-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="208d5-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="208d5-112">Remarks</span></span>

<span data-ttu-id="208d5-113">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="208d5-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="208d5-114">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="208d5-114">MFCMAPI reference</span></span>

<span data-ttu-id="208d5-115">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="208d5-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="208d5-116">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="208d5-116">**File**</span></span>|<span data-ttu-id="208d5-117">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="208d5-117">**Function**</span></span>|<span data-ttu-id="208d5-118">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="208d5-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="208d5-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="208d5-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="208d5-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="208d5-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="208d5-121">MFCMAPI, utiliza el método **IMAPIMessageSite::GetFormManager** para llamar a [MAPIOpenFormMgr](mapiopenformmgr.md) y devolver los resultados de la llamada.</span><span class="sxs-lookup"><span data-stu-id="208d5-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="208d5-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="208d5-122">See also</span></span>



[<span data-ttu-id="208d5-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="208d5-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="208d5-124">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="208d5-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="208d5-125">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="208d5-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="208d5-126">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="208d5-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

