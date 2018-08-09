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
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817050"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="2ebe8-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="2ebe8-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="2ebe8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ebe8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ebe8-105">Devuelve el identificador de entrada de la libreta de direcciones global para el servicio de Exchange identificado por _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="2ebe8-106">Debe liberar el identificador de la entrada devuelta mediante [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="2ebe8-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ebe8-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2ebe8-107">Header file:</span></span>  <br/> |<span data-ttu-id="2ebe8-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="2ebe8-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="2ebe8-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="2ebe8-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ebe8-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="2ebe8-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="2ebe8-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2ebe8-111">Called by:</span></span>  <br/> |<span data-ttu-id="2ebe8-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2ebe8-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="2ebe8-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ebe8-113">Parameters</span></span>

 <span data-ttu-id="2ebe8-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="2ebe8-114">_pSess_</span></span>
  
> <span data-ttu-id="2ebe8-115">[entrada] La ha iniciado la sesión IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="2ebe8-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="2ebe8-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="2ebe8-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="2ebe8-118">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="2ebe8-119">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="2ebe8-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="2ebe8-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="2ebe8-121">[entrada] Un puntero a un **emsmdbUID** que identifica la lista global de direcciones del servicio de Exchange que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="2ebe8-122">Si _pEmsmdbUID_ es NULL o el UID cero, esta función obtiene la LGD heredada del servicio de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="2ebe8-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="2ebe8-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="2ebe8-124">[out] Un puntero para el número de bytes del identificador de entrada de la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="2ebe8-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="2ebe8-125">_lppeid_</span></span>
  
> <span data-ttu-id="2ebe8-126">[out] Un puntero al identificador de entrada de la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2ebe8-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="2ebe8-127">Esto debe liberarse mediante [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="2ebe8-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

