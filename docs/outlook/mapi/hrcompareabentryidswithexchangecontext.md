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
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="c4d22-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="c4d22-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="c4d22-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4d22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4d22-105">Compara dos **EntryID** de la libreta de direcciones de forma segura en un perfil de Exchange múltiple.</span><span class="sxs-lookup"><span data-stu-id="c4d22-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="c4d22-106">Esta función es una función de reemplazo para [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="c4d22-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4d22-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c4d22-107">Header file:</span></span>  <br/> |<span data-ttu-id="c4d22-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="c4d22-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="c4d22-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c4d22-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4d22-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d22-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="c4d22-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c4d22-111">Called by:</span></span>  <br/> |<span data-ttu-id="c4d22-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c4d22-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="c4d22-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="c4d22-113">Parameters</span></span>

 <span data-ttu-id="c4d22-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="c4d22-114">_pmsess_</span></span>
  
> <span data-ttu-id="c4d22-115">a La sesión iniciada en **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="c4d22-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="c4d22-116">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="c4d22-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c4d22-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="c4d22-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="c4d22-118">a Un puntero a una **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de la libreta de direcciones de Exchange que esta función debe usar para mostrar detalles sobre el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4d22-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="c4d22-119">Si el identificador de entrada entrante no es un identificador de entrada de proveedor de libreta de direcciones de Exchange, se omite este parámetro y la llamada a la función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c4d22-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="c4d22-120">Si este parámetro es NULL o un MAPIUID cero, esta función se comporta como [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="c4d22-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="c4d22-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="c4d22-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="c4d22-122">a La libreta de direcciones que se usa para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4d22-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="c4d22-123">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="c4d22-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="c4d22-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c4d22-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="c4d22-125">a El número de bytes del primer identificador de entrada especificado por el parámetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="c4d22-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="c4d22-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="c4d22-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="c4d22-127">a Un puntero al primer identificador de entrada que representa la entrada de la libreta de direcciones que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="c4d22-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="c4d22-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c4d22-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="c4d22-129">a El número de bytes del segundo identificador de entrada especificado por el parámetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="c4d22-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="c4d22-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="c4d22-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="c4d22-131">a Un puntero al segundo identificador de entrada utilizado en la comparación que representa la entrada de la libreta de direcciones que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="c4d22-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="c4d22-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c4d22-132">_ulFlags_</span></span>
  
> <span data-ttu-id="c4d22-133">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c4d22-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c4d22-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="c4d22-134">_lpulResult_</span></span>
  
> <span data-ttu-id="c4d22-135">contempla Un puntero a la ubicación que contiene los resultados de la comparación.</span><span class="sxs-lookup"><span data-stu-id="c4d22-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

