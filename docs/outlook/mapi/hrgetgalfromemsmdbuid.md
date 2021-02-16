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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439110"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="248a2-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="248a2-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="248a2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="248a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="248a2-105">Devuelve el identificador de entrada de la libreta de direcciones global para el servicio de Exchange identificado por  _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="248a2-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="248a2-106">El identificador de entrada devuelto debe liberarse [con MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="248a2-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="248a2-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="248a2-107">Header file:</span></span>  <br/> |<span data-ttu-id="248a2-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="248a2-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="248a2-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="248a2-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="248a2-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="248a2-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="248a2-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="248a2-111">Called by:</span></span>  <br/> |<span data-ttu-id="248a2-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="248a2-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="248a2-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="248a2-113">Parameters</span></span>

 <span data-ttu-id="248a2-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="248a2-114">_pSess_</span></span>
  
> <span data-ttu-id="248a2-115">[entrada] Ha iniciado sesión en IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="248a2-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="248a2-116">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="248a2-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="248a2-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="248a2-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="248a2-118">[entrada] La libreta de direcciones usada para abrir el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="248a2-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="248a2-119">No puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="248a2-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="248a2-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="248a2-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="248a2-121">[entrada] Puntero a un **emsmdbUID** que identifica la GAL del servicio de Exchange que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="248a2-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="248a2-122">Si  _pEmsmdbUID_ es NULL o el UID cero, esta función obtiene la GAL heredada del servicio de Exchange.</span><span class="sxs-lookup"><span data-stu-id="248a2-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="248a2-123">_lpccvd_</span><span class="sxs-lookup"><span data-stu-id="248a2-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="248a2-124">[salida] Puntero al recuento de bytes del identificador de entrada de la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="248a2-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="248a2-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="248a2-125">_lppeid_</span></span>
  
> <span data-ttu-id="248a2-126">[salida] Puntero al identificador de entrada de la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="248a2-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="248a2-127">Esto debe liberarse con [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="248a2-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

