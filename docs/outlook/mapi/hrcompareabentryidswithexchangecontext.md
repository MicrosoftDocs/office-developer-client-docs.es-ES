---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436436"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="c0ff0-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="c0ff0-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="c0ff0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0ff0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0ff0-105">Compara dos entradas de libreta de direcciones **de** forma segura en un perfil de Exchange de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="c0ff0-106">Esta función es una función de reemplazo para [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="c0ff0-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0ff0-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c0ff0-107">Header file:</span></span>  <br/> |<span data-ttu-id="c0ff0-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="c0ff0-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="c0ff0-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c0ff0-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0ff0-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c0ff0-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c0ff0-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c0ff0-111">Called by:</span></span>  <br/> |<span data-ttu-id="c0ff0-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c0ff0-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="c0ff0-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="c0ff0-113">Parameters</span></span>

 <span data-ttu-id="c0ff0-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-114">_pmsess_</span></span>
  
> <span data-ttu-id="c0ff0-115">[in] La sesión iniciada **en IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="c0ff0-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c0ff0-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="c0ff0-118">[in] Puntero a **un emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que esta función debe usar para mostrar detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="c0ff0-119">Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada de función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c0ff0-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="c0ff0-120">Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c0ff0-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="c0ff0-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="c0ff0-122">[in] La libreta de direcciones usada para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="c0ff0-123">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c0ff0-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="c0ff0-125">[in] Recuento de bytes del primer identificador de entrada especificado por el _parámetro lpEntryID1._</span><span class="sxs-lookup"><span data-stu-id="c0ff0-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="c0ff0-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="c0ff0-127">[in] Puntero al primer identificador de entrada que representa la entrada de libreta de direcciones que se debe comparar.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="c0ff0-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="c0ff0-129">[in] Recuento de bytes del segundo identificador de entrada especificado por el _parámetro lpEntryID2._</span><span class="sxs-lookup"><span data-stu-id="c0ff0-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="c0ff0-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="c0ff0-131">[in] Puntero al segundo identificador de entrada usado en la comparación que representa la entrada de libreta de direcciones que se debe comparar.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="c0ff0-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-132">_ulFlags_</span></span>
  
> <span data-ttu-id="c0ff0-133">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c0ff0-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="c0ff0-134">_lpulResult_</span></span>
  
> <span data-ttu-id="c0ff0-135">[salida] Puntero a la ubicación que contiene los resultados de la comparación.</span><span class="sxs-lookup"><span data-stu-id="c0ff0-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

