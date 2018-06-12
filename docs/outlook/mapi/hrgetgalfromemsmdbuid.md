---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817050"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="8028f-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="8028f-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="8028f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8028f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8028f-105">Devuelve el identificador de entrada de la libreta de direcciones global para el servicio de Exchange identificado por _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="8028f-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="8028f-106">Debe liberar el identificador de la entrada devuelta mediante [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="8028f-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8028f-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8028f-107">Header file:</span></span>  <br/> |<span data-ttu-id="8028f-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="8028f-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="8028f-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="8028f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="8028f-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="8028f-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="8028f-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8028f-111">Called by:</span></span>  <br/> |<span data-ttu-id="8028f-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8028f-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="8028f-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8028f-113">Parameters</span></span>

 <span data-ttu-id="8028f-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="8028f-114">_pSess_</span></span>
  
> <span data-ttu-id="8028f-115">[entrada] La ha iniciado la sesión IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="8028f-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="8028f-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="8028f-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="8028f-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="8028f-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="8028f-118">[entrada] La libreta de direcciones que se usó para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="8028f-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="8028f-119">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="8028f-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="8028f-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="8028f-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="8028f-121">[entrada] Un puntero a un **emsmdbUID** que identifica la lista global de direcciones del servicio de Exchange que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="8028f-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="8028f-122">Si _pEmsmdbUID_ es NULL o el UID cero, esta función obtiene la LGD heredada del servicio de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8028f-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="8028f-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="8028f-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="8028f-124">[out] Un puntero para el número de bytes del identificador de entrada de la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8028f-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="8028f-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="8028f-125">_lppeid_</span></span>
  
> <span data-ttu-id="8028f-126">[out] Un puntero al identificador de entrada de la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8028f-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="8028f-127">Esto debe liberarse mediante [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="8028f-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

