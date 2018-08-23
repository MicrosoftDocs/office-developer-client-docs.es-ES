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
ms.openlocfilehash: eb91f4998f94ffafbc33b6024228945f7c91cf43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564993"
---
# <a name="hrcompareabentryidswithexchangecontext"></a><span data-ttu-id="d435b-103">HrCompareABEntryIDsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d435b-103">HrCompareABEntryIDsWithExchangeContext</span></span>

  
  
<span data-ttu-id="d435b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d435b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d435b-105">Compara dos de la libreta de dirección **identificadores** con seguridad en un perfil de Exchange varios.</span><span class="sxs-lookup"><span data-stu-id="d435b-105">Compares two address book **entryIDs** safely in a Multiple Exchange profile.</span></span> <span data-ttu-id="d435b-106">Esta función es una función de reemplazo para [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span><span class="sxs-lookup"><span data-stu-id="d435b-106">This function is a replacement function for [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d435b-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d435b-107">Header file:</span></span>  <br/> |<span data-ttu-id="d435b-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="d435b-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d435b-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d435b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d435b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d435b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d435b-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d435b-111">Called by:</span></span>  <br/> |<span data-ttu-id="d435b-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d435b-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d435b-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d435b-113">Parameters</span></span>

 <span data-ttu-id="d435b-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="d435b-114">_pmsess_</span></span>
  
> <span data-ttu-id="d435b-115">[entrada] La ha iniciado la sesión **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="d435b-115">[in] The logged on **IMAPISession**.</span></span> <span data-ttu-id="d435b-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d435b-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d435b-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="d435b-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d435b-118">[entrada] Un puntero a un **emsmdbUID** que identifica el servicio de Exchange que contiene el proveedor de libreta de direcciones de Exchange que se debe usar esta función para mostrar los detalles en el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d435b-118">[in] A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange Address Book Provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="d435b-119">Si el identificador de entrada entrante no es un identificador de entrada del proveedor de libreta de direcciones de Exchange, este parámetro se omite y la llamada a la función se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="d435b-119">If the incoming entry identifier is not an Exchange Address Book Provider entry identifier, this parameter is ignored and the function call behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="d435b-120">Si este parámetro es NULL o un cero MAPIUID, esta función se comporta como [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="d435b-120">If this parameter is NULL or a zero MAPIUID, this function behaves like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="d435b-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d435b-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="d435b-122">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="d435b-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d435b-123">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="d435b-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d435b-124">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d435b-124">_cbEntryID1_</span></span>
  
> <span data-ttu-id="d435b-125">[entrada] El número de bytes del primer identificador de entrada especificado por el parámetro _lpEntryID1_ .</span><span class="sxs-lookup"><span data-stu-id="d435b-125">[in] The byte count of the first entry identifier specified by the  _lpEntryID1_ parameter.</span></span> 
    
 <span data-ttu-id="d435b-126">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="d435b-126">_lpEntryID1_</span></span>
  
> <span data-ttu-id="d435b-127">[entrada] Un puntero para el primer identificador de entrada que representa la entrada de la libreta de direcciones se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="d435b-127">[in] A pointer to the first entry identifier that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="d435b-128">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d435b-128">_cbEntryID2_</span></span>
  
> <span data-ttu-id="d435b-129">[entrada] El número de bytes del segundo identificador de entrada especificado por el parámetro _lpEntryID2_ .</span><span class="sxs-lookup"><span data-stu-id="d435b-129">[in] The byte count of the second entry identifier specified by the  _lpEntryID2_ parameter.</span></span> 
    
 <span data-ttu-id="d435b-130">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="d435b-130">_lpEntryID2_</span></span>
  
> <span data-ttu-id="d435b-131">[entrada] Un puntero al segundo identificador de entrada utilizado en la comparación que representa la entrada de la libreta de direcciones se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="d435b-131">[in] A pointer to the second entry identifier used in the comparison that represents the address book entry to compare.</span></span>
    
 <span data-ttu-id="d435b-132">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d435b-132">_ulFlags_</span></span>
  
> <span data-ttu-id="d435b-133">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d435b-133">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d435b-134">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="d435b-134">_lpulResult_</span></span>
  
> <span data-ttu-id="d435b-135">[out] Un puntero a la ubicación que contiene los resultados de la comparación.</span><span class="sxs-lookup"><span data-stu-id="d435b-135">[out] A pointer to the location that contains the results of the comparison.</span></span> 
    

