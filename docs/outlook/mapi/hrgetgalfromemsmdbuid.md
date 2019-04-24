---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347834"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="56b87-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="56b87-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="56b87-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56b87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56b87-105">Devuelve el identificador de entrada de la libreta de direcciones global para el servicio de Exchange identificado por _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="56b87-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="56b87-106">El identificador de entrada devuelto debe liberarse mediante [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="56b87-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56b87-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="56b87-107">Header file:</span></span>  <br/> |<span data-ttu-id="56b87-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="56b87-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="56b87-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="56b87-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="56b87-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="56b87-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="56b87-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="56b87-111">Called by:</span></span>  <br/> |<span data-ttu-id="56b87-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="56b87-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="56b87-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="56b87-113">Parameters</span></span>

 <span data-ttu-id="56b87-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="56b87-114">_pSess_</span></span>
  
> <span data-ttu-id="56b87-115">a La sesión iniciada en IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="56b87-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="56b87-116">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="56b87-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="56b87-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="56b87-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="56b87-118">a La libreta de direcciones que se usa para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="56b87-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="56b87-119">No puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="56b87-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="56b87-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="56b87-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="56b87-121">a Un puntero a una **emsmdbUID** que identifica la GAL del servicio de Exchange que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="56b87-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="56b87-122">Si _pEmsmdbUID_ es null o el UID cero, esta función obtiene la GAL heredada del servicio de Exchange.</span><span class="sxs-lookup"><span data-stu-id="56b87-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="56b87-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="56b87-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="56b87-124">contempla Un puntero al número de bytes del identificador de entrada de la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="56b87-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="56b87-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="56b87-125">_lppeid_</span></span>
  
> <span data-ttu-id="56b87-126">contempla Un puntero al identificador de entrada de la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="56b87-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="56b87-127">Debe liberarse con [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="56b87-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

