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
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426208"
---
# <a name="iaddrbooksetsearchpath"></a><span data-ttu-id="40684-103">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="40684-103">IAddrBook::SetSearchPath</span></span>

  
  
<span data-ttu-id="40684-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40684-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40684-105">Establece una nueva ruta de búsqueda en el perfil que se usa para el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="40684-105">Sets a new search path in the profile that is used for the name resolution process.</span></span> 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="40684-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="40684-106">Parameters</span></span>

 <span data-ttu-id="40684-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40684-107">_ulFlags_</span></span>
  
> <span data-ttu-id="40684-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="40684-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="40684-109">_lpSearchPath_</span><span class="sxs-lookup"><span data-stu-id="40684-109">_lpSearchPath_</span></span>
  
> <span data-ttu-id="40684-110">a Puntero a la estructura [SRowSet](srowset.md) que se usa para contener la ruta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="40684-110">[in] A pointer to the [SRowSet](srowset.md) structure used to hold the search path.</span></span> <span data-ttu-id="40684-111">La primera propiedad de cada miembro **aRow** en **SRowSet** debe ser \*\*\*\* el nombre del usuario ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="40684-111">The first property for each **aRow** member in **SRowSet** must be **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40684-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40684-112">Return value</span></span>

<span data-ttu-id="40684-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="40684-113">S_OK</span></span> 
  
> <span data-ttu-id="40684-114">La ruta de búsqueda se estableció correctamente.</span><span class="sxs-lookup"><span data-stu-id="40684-114">The search path was successfully set.</span></span>
    
<span data-ttu-id="40684-115">MAPI_E_MISSING_REQUIRED_COLUMN</span><span class="sxs-lookup"><span data-stu-id="40684-115">MAPI_E_MISSING_REQUIRED_COLUMN</span></span> 
  
> <span data-ttu-id="40684-116">Uno de los contenedores descritos en la estructura **SRowSet** no incluía \*\*\*\* su propiedad 1.</span><span class="sxs-lookup"><span data-stu-id="40684-116">One of the containers described in the **SRowSet** structure did not include its **PR_ENTRYID** property.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="40684-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40684-117">Remarks</span></span>

<span data-ttu-id="40684-118">Los clientes y los proveedores de servicios llaman al método **SetSearchPath** para guardar los cambios realizados en el orden de búsqueda del contenedor que se usa para resolver nombres con el método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="40684-118">Clients and service providers call the **SetSearchPath** method to save changes that were made to the container search order that is used to resolve names with the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="40684-119">La ruta de búsqueda se guarda entre instancias de una sesión.</span><span class="sxs-lookup"><span data-stu-id="40684-119">The search path is saved between instances of a session.</span></span> 
  
<span data-ttu-id="40684-120">Los clientes y proveedores no tienen que llamar al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para hacer permanentes los cambios en la ruta de acceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="40684-120">Clients and providers do not have to call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to make the search path changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="40684-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="40684-121">See also</span></span>



[<span data-ttu-id="40684-122">IAddrBook::GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="40684-122">IAddrBook::GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md)
  
[<span data-ttu-id="40684-123">IAddrBook::GetPAB</span><span class="sxs-lookup"><span data-stu-id="40684-123">IAddrBook::GetPAB</span></span>](iaddrbook-getpab.md)
  
[<span data-ttu-id="40684-124">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="40684-124">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
  
[<span data-ttu-id="40684-125">Propiedad canónica PidTagContainerFlags</span><span class="sxs-lookup"><span data-stu-id="40684-125">PidTagContainerFlags Canonical Property</span></span>](pidtagcontainerflags-canonical-property.md)
  
[<span data-ttu-id="40684-126">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="40684-126">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

