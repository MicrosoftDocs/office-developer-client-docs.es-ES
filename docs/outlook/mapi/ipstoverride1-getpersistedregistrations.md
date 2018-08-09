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
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817917"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="03e97-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="03e97-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="03e97-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03e97-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03e97-105">Recupera la lista de registros para el archivo de carpetas personales (.pst).</span><span class="sxs-lookup"><span data-stu-id="03e97-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="03e97-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03e97-106">Parameters</span></span>

 <span data-ttu-id="03e97-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="03e97-107">_ppmval_</span></span>
  
> <span data-ttu-id="03e97-108">[entrada] Un puntero a un puntero a una estructura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="03e97-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="03e97-109">El miembro ulPropTag de esta estructura es del tipo PT_MV_UNICODE, y el miembro de valor MVszW será una matriz de cadenas de Unicode terminada en null.</span><span class="sxs-lookup"><span data-stu-id="03e97-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="03e97-110">Estas cadenas son las rutas de acceso a los archivos DLL para el que se ha conservado el registro.</span><span class="sxs-lookup"><span data-stu-id="03e97-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="03e97-111">no se implementa la compatibilidad con .pst ANSI.</span><span class="sxs-lookup"><span data-stu-id="03e97-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="03e97-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03e97-112">Return value</span></span>

<span data-ttu-id="03e97-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="03e97-113">S_OK</span></span> 
  
> <span data-ttu-id="03e97-114">La llamada a la función fue correcta.</span><span class="sxs-lookup"><span data-stu-id="03e97-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03e97-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="03e97-115">See also</span></span>



[<span data-ttu-id="03e97-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03e97-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="03e97-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03e97-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

