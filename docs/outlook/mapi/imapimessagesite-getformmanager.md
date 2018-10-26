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
ms.openlocfilehash: 5e3a2224daace9be7f4504a693806ccb3cf4abbe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570495"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="f614e-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="f614e-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="f614e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f614e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f614e-105">Devuelve una interfaz de administrador de formulario, que puede usar un servidor de formulario para abrir otro servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="f614e-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="f614e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f614e-106">Parameters</span></span>

 <span data-ttu-id="f614e-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="f614e-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="f614e-108">[out] Un puntero a un puntero a la interfaz de administrador de formulario devuelto.</span><span class="sxs-lookup"><span data-stu-id="f614e-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f614e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f614e-109">Return value</span></span>

<span data-ttu-id="f614e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f614e-110">S_OK</span></span> 
  
> <span data-ttu-id="f614e-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f614e-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f614e-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f614e-112">Remarks</span></span>

<span data-ttu-id="f614e-113">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f614e-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f614e-114">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f614e-114">MFCMAPI reference</span></span>

<span data-ttu-id="f614e-115">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f614e-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f614e-116">**File**</span><span class="sxs-lookup"><span data-stu-id="f614e-116">**File**</span></span>|<span data-ttu-id="f614e-117">**Función**</span><span class="sxs-lookup"><span data-stu-id="f614e-117">**Function**</span></span>|<span data-ttu-id="f614e-118">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f614e-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f614e-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="f614e-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f614e-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="f614e-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="f614e-121">MFCMAPI, utiliza el método **IMAPIMessageSite::GetFormManager** para llamar a [MAPIOpenFormMgr](mapiopenformmgr.md) y devolver los resultados de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f614e-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f614e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f614e-122">See also</span></span>



[<span data-ttu-id="f614e-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="f614e-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="f614e-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f614e-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="f614e-125">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="f614e-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f614e-126">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="f614e-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

