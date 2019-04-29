---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412355"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="1178c-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="1178c-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="1178c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1178c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1178c-105">Crea un objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="1178c-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1178c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1178c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1178c-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="1178c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="1178c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1178c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1178c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1178c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1178c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1178c-110">Called by:</span></span>  <br/> |<span data-ttu-id="1178c-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="1178c-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="1178c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="1178c-112">Parameters</span></span>

 <span data-ttu-id="1178c-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1178c-113">_ulFlags_</span></span>
  
> <span data-ttu-id="1178c-114">a Máscara de máscara de los indicadores que indican las opciones de la función de entrada de servicio.</span><span class="sxs-lookup"><span data-stu-id="1178c-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="1178c-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="1178c-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="1178c-116">contempla Puntero a un puntero al nuevo objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="1178c-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1178c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1178c-117">Return value</span></span>

<span data-ttu-id="1178c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1178c-118">S_OK</span></span> 
  
> <span data-ttu-id="1178c-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1178c-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1178c-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1178c-120">MFCMAPI reference</span></span>

<span data-ttu-id="1178c-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1178c-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1178c-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1178c-122">**File**</span></span>|<span data-ttu-id="1178c-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="1178c-123">**Function**</span></span>|<span data-ttu-id="1178c-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1178c-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1178c-125">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="1178c-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="1178c-126">CMapiObjects:: GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="1178c-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="1178c-127">MFCMAPI usa el método **MAPIAdminProfiles** para obtener el objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="1178c-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1178c-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="1178c-128">See also</span></span>



[<span data-ttu-id="1178c-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="1178c-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="1178c-130">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="1178c-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

