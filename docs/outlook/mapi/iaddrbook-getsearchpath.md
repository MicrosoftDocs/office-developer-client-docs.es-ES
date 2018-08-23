---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7bf69e560142ab282d6545389e02766389e4d018
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580701"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="cba4d-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="cba4d-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="cba4d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cba4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cba4d-105">Devuelve una lista ordenada de los identificadores de entrada de los contenedores que se deben incluir en el proceso de resolución de nombres iniciado por el método [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="cba4d-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="cba4d-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="cba4d-106">Parameters</span></span>

 <span data-ttu-id="cba4d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cba4d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cba4d-108">[entrada] Una máscara de bits de indicadores que controla el tipo de las cadenas devueltas en la ruta de acceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cba4d-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="cba4d-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="cba4d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="cba4d-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="cba4d-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="cba4d-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="cba4d-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="cba4d-112">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="cba4d-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="cba4d-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="cba4d-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="cba4d-114">[out] Un puntero a un puntero a una lista ordenada de identificadores de entrada del contenedor.</span><span class="sxs-lookup"><span data-stu-id="cba4d-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="cba4d-115">**GetSearchPath** almacena la lista ordenada en una estructura [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="cba4d-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="cba4d-116">Si no hay ningún contenedores en la jerarquía de la libreta de direcciones, se devuelve cero en la estructura **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="cba4d-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cba4d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cba4d-117">Return value</span></span>

<span data-ttu-id="cba4d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="cba4d-118">S_OK</span></span> 
  
> <span data-ttu-id="cba4d-119">La ruta de acceso de búsqueda se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cba4d-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cba4d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cba4d-120">Remarks</span></span>

<span data-ttu-id="cba4d-121">Los clientes y proveedores de servicios de llamar al método **GetSearchPath** para obtener la ruta de acceso de búsqueda que se utiliza para resolver nombres con el método **ResolveName** .</span><span class="sxs-lookup"><span data-stu-id="cba4d-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="cba4d-122">Normalmente, los clientes de llaman al método [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) para establecer una ruta de acceso de búsqueda de contenedor en el perfil antes de llamar a **GetSearchPath** para recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="cba4d-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="cba4d-123">Sin embargo, al llamar a **SetSearchPath** es opcional.</span><span class="sxs-lookup"><span data-stu-id="cba4d-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="cba4d-124">Si nunca se ha llamado **SetSearchPath** , **GetSearchPath** genera una ruta de acceso por trabajar a través de la dirección de las tablas de jerarquía del libro.</span><span class="sxs-lookup"><span data-stu-id="cba4d-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="cba4d-125">La ruta de acceso de búsqueda predeterminada establecida por **GetSearchPath** consta de los siguientes contenedores en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="cba4d-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="cba4d-126">El primer contenedor con permiso de lectura y escritura, generalmente la libreta de direcciones personales (PAB).</span><span class="sxs-lookup"><span data-stu-id="cba4d-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="cba4d-127">Cada contenedor que tenga su propiedad **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) que se establece en DT_GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="cba4d-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="cba4d-128">Esta configuración indica que el contenedor contiene a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="cba4d-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="cba4d-129">El contenedor designado como el valor predeterminado, si no hay ningún contenedores que tienen la marca DT_GLOBAL establecer en su propiedad **PR_DISPLAY_TYPE** y el contenedor predeterminado difiere del primer contenedor con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cba4d-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="cba4d-130">Si se ha llamado **SetSearchPath** , **GetSearchPath** crea una ruta de acceso mediante el uso de los contenedores de la libreta de direcciones que se han almacenado en el perfil.</span><span class="sxs-lookup"><span data-stu-id="cba4d-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="cba4d-131">**GetSearchPath** valida esta ruta de acceso antes de lo devuelve al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="cba4d-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="cba4d-132">Después de la primera llamada a **SetSearchPath**, las llamadas subsiguientes a **SetSearchPath** se deben usar para modificar la ruta de acceso de búsqueda devuelto por **GetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="cba4d-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="cba4d-133">En otras palabras, el cliente o el proveedor realiza la llamada no recibe la ruta de acceso de búsqueda predeterminada después de la primera llamada a **SetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="cba4d-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cba4d-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cba4d-134">See also</span></span>



[<span data-ttu-id="cba4d-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="cba4d-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="cba4d-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="cba4d-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="cba4d-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cba4d-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

