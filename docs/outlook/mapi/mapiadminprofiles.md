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
ms.openlocfilehash: 3cd1a19b23a3c4d3ff8a297881eb2b959585eb17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818250"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="d3f95-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="d3f95-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="d3f95-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3f95-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3f95-105">Crea un objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="d3f95-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3f95-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d3f95-106">Header file:</span></span>  <br/> |<span data-ttu-id="d3f95-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="d3f95-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="d3f95-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d3f95-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3f95-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d3f95-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d3f95-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d3f95-110">Called by:</span></span>  <br/> |<span data-ttu-id="d3f95-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="d3f95-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="d3f95-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d3f95-112">Parameters</span></span>

 <span data-ttu-id="d3f95-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3f95-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d3f95-114">[entrada] Máscara de bits de marcadores que indica las opciones para la función de entrada de servicio.</span><span class="sxs-lookup"><span data-stu-id="d3f95-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="d3f95-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="d3f95-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="d3f95-116">[out] Puntero a un puntero al nuevo objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="d3f95-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d3f95-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3f95-117">Return value</span></span>

<span data-ttu-id="d3f95-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3f95-118">S_OK</span></span> 
  
> <span data-ttu-id="d3f95-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="d3f95-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d3f95-120">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d3f95-120">MFCMAPI reference</span></span>

<span data-ttu-id="d3f95-121">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d3f95-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d3f95-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d3f95-122">**File**</span></span>|<span data-ttu-id="d3f95-123">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="d3f95-123">**Function**</span></span>|<span data-ttu-id="d3f95-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d3f95-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d3f95-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="d3f95-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="d3f95-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="d3f95-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="d3f95-127">MFCMAPI usa el método **MAPIAdminProfiles** para obtener el objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="d3f95-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3f95-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3f95-128">See also</span></span>



[<span data-ttu-id="d3f95-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="d3f95-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="d3f95-130">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d3f95-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

