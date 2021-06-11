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
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412985"
---
# <a name="iaddrbookgetsearchpath"></a><span data-ttu-id="9bbe7-103">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="9bbe7-103">IAddrBook::GetSearchPath</span></span>

  
  
<span data-ttu-id="9bbe7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bbe7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bbe7-105">Devuelve una lista ordenada de identificadores de entrada de los contenedores que se incluirán en el proceso de resolución de nombres iniciado por el [método IAddrBook::ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="9bbe7-105">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a><span data-ttu-id="9bbe7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9bbe7-106">Parameters</span></span>

 <span data-ttu-id="9bbe7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9bbe7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9bbe7-108">[in] Máscara de bits de marcas que controla el tipo de cadenas devueltas en la ruta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-108">[in] A bitmask of flags that controls the type of the strings returned in the search path.</span></span> <span data-ttu-id="9bbe7-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="9bbe7-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9bbe7-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9bbe7-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9bbe7-111">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="9bbe7-112">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9bbe7-113">_lppSearchPath_</span><span class="sxs-lookup"><span data-stu-id="9bbe7-113">_lppSearchPath_</span></span>
  
> <span data-ttu-id="9bbe7-114">[salida] Puntero a un puntero a una lista ordenada de identificadores de entrada de contenedor.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-114">[out] A pointer to a pointer to an ordered list of container entry identifiers.</span></span> <span data-ttu-id="9bbe7-115">**GetSearchPath** almacena la lista ordenada en una [estructura SRowSet.](srowset.md)</span><span class="sxs-lookup"><span data-stu-id="9bbe7-115">**GetSearchPath** stores the ordered list in an [SRowSet](srowset.md) structure.</span></span> <span data-ttu-id="9bbe7-116">Si no hay contenedores en la jerarquía de libreta de direcciones, se devuelve cero en la **estructura SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="9bbe7-116">If there are no containers in the address book hierarchy, zero is returned in the **SRowSet** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9bbe7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bbe7-117">Return value</span></span>

<span data-ttu-id="9bbe7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9bbe7-118">S_OK</span></span> 
  
> <span data-ttu-id="9bbe7-119">La ruta de acceso de búsqueda se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-119">The search path was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9bbe7-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bbe7-120">Remarks</span></span>

<span data-ttu-id="9bbe7-121">Los clientes y proveedores de servicios llaman al **método GetSearchPath** para obtener la ruta de búsqueda que se usa para resolver nombres con el **método ResolveName.**</span><span class="sxs-lookup"><span data-stu-id="9bbe7-121">Clients and service providers call the **GetSearchPath** method to get the search path that is used to resolve names with the **ResolveName** method.</span></span> <span data-ttu-id="9bbe7-122">Normalmente, los clientes llaman al método [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) para establecer una ruta de búsqueda de contenedor en el perfil antes de llamar a **GetSearchPath** para recuperarla.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-122">Typically, clients call the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method to establish a container search path in the profile before they call **GetSearchPath** to retrieve it.</span></span> <span data-ttu-id="9bbe7-123">Sin embargo, llamar **a SetSearchPath** es opcional.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-123">However, calling **SetSearchPath** is optional.</span></span> 
  
<span data-ttu-id="9bbe7-124">Si nunca se ha llamado a **SetSearchPath,** **GetSearchPath** crea una ruta de acceso trabajando en las tablas jerárquicas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-124">If **SetSearchPath** has never been called, **GetSearchPath** builds a path by working through the address book's hierarchy tables.</span></span> <span data-ttu-id="9bbe7-125">La ruta de búsqueda predeterminada establecida **por GetSearchPath** consta de los siguientes contenedores en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="9bbe7-125">The default search path established by **GetSearchPath** consists of the following containers in the following order:</span></span> 
  
1. <span data-ttu-id="9bbe7-126">El primer contenedor con permiso de lectura y escritura, normalmente la libreta de direcciones personal (PAB).</span><span class="sxs-lookup"><span data-stu-id="9bbe7-126">The first container with read/write permission, usually the personal address book (PAB).</span></span>
    
2. <span data-ttu-id="9bbe7-127">Cada contenedor que tiene su **propiedad PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) establecida en DT_GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-127">Every container that has its **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) property set to DT_GLOBAL.</span></span> <span data-ttu-id="9bbe7-128">Esta configuración indica que el contenedor contiene destinatarios.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-128">This setting indicates that the container holds recipients.</span></span> 
    
3. <span data-ttu-id="9bbe7-129">El contenedor designado como predeterminado, si no hay contenedores que tengan la marca de DT_GLOBAL establecida en su propiedad **PR_DISPLAY_TYPE** y el contenedor predeterminado difiere del primer contenedor con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-129">The container designated as the default, if there are no containers that have the DT_GLOBAL flag set in their **PR_DISPLAY_TYPE** property and the default container differs from the first container with read/write permission.</span></span> 
    
<span data-ttu-id="9bbe7-130">Si se ha llamado a **SetSearchPath,** **GetSearchPath** crea una ruta de acceso mediante los contenedores de libreta de direcciones almacenados en el perfil.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-130">If **SetSearchPath** has been called, **GetSearchPath** builds a path by using the address book containers that have been stored in the profile.</span></span> <span data-ttu-id="9bbe7-131">**GetSearchPath valida** esta ruta antes de devolverla al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-131">**GetSearchPath** validates this path before it returns it to the caller.</span></span> 
  
<span data-ttu-id="9bbe7-132">Después de la primera llamada a **SetSearchPath**, las llamadas posteriores a **SetSearchPath** deben usarse para modificar la ruta de búsqueda devuelta por **GetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-132">After the first call to **SetSearchPath**, subsequent calls to **SetSearchPath** must be used to modify the search path returned by **GetSearchPath**.</span></span> <span data-ttu-id="9bbe7-133">En otras palabras, el cliente o proveedor de llamadas no recibe la ruta de búsqueda predeterminada después de la primera llamada a **SetSearchPath**.</span><span class="sxs-lookup"><span data-stu-id="9bbe7-133">In other words, the calling client or provider does not receive the default search path after the first call to **SetSearchPath**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9bbe7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9bbe7-134">See also</span></span>



[<span data-ttu-id="9bbe7-135">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="9bbe7-135">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
  
[<span data-ttu-id="9bbe7-136">SRowSet</span><span class="sxs-lookup"><span data-stu-id="9bbe7-136">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="9bbe7-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9bbe7-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

