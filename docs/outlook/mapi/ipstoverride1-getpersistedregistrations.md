---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315473"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="cc3cb-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="cc3cb-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="cc3cb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc3cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc3cb-105">Recupera la lista de registros del archivo de carpetas personales (. pst).</span><span class="sxs-lookup"><span data-stu-id="cc3cb-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="cc3cb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cc3cb-106">Parameters</span></span>

 <span data-ttu-id="cc3cb-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="cc3cb-107">_ppmval_</span></span>
  
> <span data-ttu-id="cc3cb-108">a Un puntero a un puntero a una estructura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="cc3cb-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="cc3cb-109">El miembro ulPropTag de esta estructura es del tipo PT_MV_UNICODE y el miembro del valor MVszW será una matriz de cadenas Unicode terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="cc3cb-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="cc3cb-110">Estas cadenas son rutas de archivos DLL para las que se ha conservado el registro.</span><span class="sxs-lookup"><span data-stu-id="cc3cb-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="cc3cb-111">no se ha implementado la compatibilidad con. pst para ANSI.</span><span class="sxs-lookup"><span data-stu-id="cc3cb-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="cc3cb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc3cb-112">Return value</span></span>

<span data-ttu-id="cc3cb-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc3cb-113">S_OK</span></span> 
  
> <span data-ttu-id="cc3cb-114">La llamada a la función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc3cb-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc3cb-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc3cb-115">See also</span></span>



[<span data-ttu-id="cc3cb-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc3cb-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="cc3cb-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc3cb-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

