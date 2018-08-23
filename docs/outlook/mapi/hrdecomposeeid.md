---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7cae156e29503c8b50755c99023805aa6d14e704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573372"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="0d5e1-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="0d5e1-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="0d5e1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d5e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d5e1-105">Separa el identificador de entrada compuesta de un objeto, normalmente un mensaje en un almacén de mensajes, en el identificador de entrada de ese objeto en el almacén y el identificador de entrada de la tienda.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d5e1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0d5e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d5e1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0d5e1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0d5e1-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="0d5e1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d5e1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d5e1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d5e1-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0d5e1-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d5e1-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="0d5e1-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="0d5e1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d5e1-112">Parameters</span></span>

 <span data-ttu-id="0d5e1-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="0d5e1-113">_psession_</span></span>
  
> <span data-ttu-id="0d5e1-114">[entrada] Puntero a la sesión en uso por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="0d5e1-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="0d5e1-115">_cbEID_</span></span>
  
> <span data-ttu-id="0d5e1-116">[entrada] Tamaño, en bytes, del identificador de entrada compuestos para estar separados.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="0d5e1-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="0d5e1-117">_pEID_</span></span>
  
> <span data-ttu-id="0d5e1-118">[entrada] Puntero al identificador de entrada compuestos a estar separados.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="0d5e1-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="0d5e1-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="0d5e1-120">[out] Puntero al tamaño devuelto, en bytes, del identificador de entrada del almacén de mensajes que contiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="0d5e1-121">Si el parámetro _pEID_ señala a un identificador de entrada los, a continuación, el parámetro _pcbStoreEID_ apunta a un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="0d5e1-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="0d5e1-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="0d5e1-123">[out] Puntero a un puntero al identificador de entrada devuelto del almacén de mensajes que contiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="0d5e1-124">Si el parámetro _pEID_ señala a un identificador de entrada los, se devuelve NULL en el parámetro _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="0d5e1-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="0d5e1-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="0d5e1-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="0d5e1-126">[out] Puntero al tamaño devuelto, en bytes, del identificador de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="0d5e1-127">Si el parámetro _pEID_ señala a un identificador de entrada los, el parámetro _pcbMsgEID_ es igual que el valor del parámetro _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="0d5e1-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="0d5e1-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="0d5e1-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="0d5e1-129">[out] Puntero a un puntero al identificador de entrada devuelta del objeto.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="0d5e1-130">Si el parámetro _pEID_ señala a un identificador de entrada los, _ppMsgEID_ apunta a un puntero a una copia del identificador de entrada de los.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d5e1-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d5e1-131">Return value</span></span>

<span data-ttu-id="0d5e1-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d5e1-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d5e1-133">Remarks</span></span>

<span data-ttu-id="0d5e1-134">Si el identificador especificado por el parámetro _pEID_ es compuesto, se divide en el identificador de entrada del objeto dentro de su almacén de mensajes y el identificador de entrada de la tienda.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="0d5e1-135">Las cadenas de identificador de entrada los simplemente se copian.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="0d5e1-136">El identificador de compuestos para estar separados suele ser uno creado por la función [HrComposeEID](hrcomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="0d5e1-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0d5e1-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="0d5e1-137">Notes to callers</span></span>

<span data-ttu-id="0d5e1-138">Tras completar correctamente esta función, se libera la memoria que contiene el parámetro _pEID_ .</span><span class="sxs-lookup"><span data-stu-id="0d5e1-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="0d5e1-139">La implementación de la llamada es responsable de liberar memoria para los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="0d5e1-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

