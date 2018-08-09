---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4f9d2f4d271e467d8fac32b8f17faa8f66cd3f99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817149"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="cea93-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="cea93-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="cea93-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cea93-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cea93-105">Establece una nueva ruta de acceso de búsqueda en el perfil que se usa para el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="cea93-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="cea93-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="cea93-106">Parameters</span></span>

 <span data-ttu-id="cea93-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cea93-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cea93-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cea93-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cea93-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="cea93-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="cea93-110">[entrada] Un puntero a la estructura [SRowSet](srowset.md) que se utiliza para contener la ruta de acceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cea93-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="cea93-111">La primera propiedad para cada miembro de **aRow** de **SRowSet** debe ser una **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cea93-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cea93-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cea93-112">Return value</span></span>

<span data-ttu-id="cea93-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="cea93-113">S_OK</span></span> 
  
> <span data-ttu-id="cea93-114">La ruta de acceso de búsqueda se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="cea93-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="cea93-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="cea93-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="cea93-116">Uno de los contenedores que se describen en la estructura **SRowSet** no incluía su propiedad de **entrada del objeto** .</span><span class="sxs-lookup"><span data-stu-id="cea93-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cea93-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cea93-117">Remarks</span></span>

<span data-ttu-id="cea93-118">Los clientes y proveedores de servicios de llamar al método **SetSearchPath** para guardar los cambios realizados en el orden de búsqueda de contenedor que se utiliza para resolver nombres con el método [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="cea93-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="cea93-119">Se guarda la ruta de acceso de búsqueda entre instancias de una sesión.</span><span class="sxs-lookup"><span data-stu-id="cea93-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="cea93-120">Los clientes y proveedores no es necesario que llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para que los cambios de la ruta de acceso de búsqueda sea permanente.</span><span class="sxs-lookup"><span data-stu-id="cea93-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cea93-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="cea93-121">See also</span></span>



[<span data-ttu-id="cea93-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="cea93-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="cea93-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="cea93-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="cea93-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="cea93-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="cea93-125">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="cea93-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="cea93-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cea93-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

