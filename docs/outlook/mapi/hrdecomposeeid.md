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
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436114"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="afaca-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="afaca-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="afaca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afaca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afaca-105">Separa el identificador de entrada compuesto de un objeto, normalmente un mensaje en un almacén de mensajes, en el identificador de entrada de ese objeto en el almacén y en el identificador de entrada de la tienda.</span><span class="sxs-lookup"><span data-stu-id="afaca-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="afaca-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="afaca-106">Header file:</span></span>  <br/> |<span data-ttu-id="afaca-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="afaca-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="afaca-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="afaca-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="afaca-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="afaca-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="afaca-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="afaca-110">Called by:</span></span>  <br/> |<span data-ttu-id="afaca-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="afaca-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="afaca-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="afaca-112">Parameters</span></span>

 <span data-ttu-id="afaca-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="afaca-113">_psession_</span></span>
  
> <span data-ttu-id="afaca-114">a Puntero a la sesión que usa la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="afaca-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="afaca-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="afaca-115">_cbEID_</span></span>
  
> <span data-ttu-id="afaca-116">a Tamaño, en bytes, del identificador de entrada compuesto que se va a separar.</span><span class="sxs-lookup"><span data-stu-id="afaca-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="afaca-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="afaca-117">_pEID_</span></span>
  
> <span data-ttu-id="afaca-118">a Puntero al identificador de entrada compuesto que se va a separar.</span><span class="sxs-lookup"><span data-stu-id="afaca-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="afaca-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="afaca-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="afaca-120">contempla Puntero al tamaño devuelto, en bytes, del identificador de entrada del almacén de mensajes que contiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="afaca-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="afaca-121">Si el parámetro _pEID_ apunta a un identificador de entrada no compuesto, el parámetro _pcbStoreEID_ apunta a un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="afaca-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="afaca-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="afaca-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="afaca-123">contempla Puntero a un puntero al identificador de entrada devuelto del almacén de mensajes que contiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="afaca-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="afaca-124">Si el parámetro _pEID_ apunta a un identificador de entrada no compuesto, se devuelve null en el parámetro _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="afaca-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="afaca-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="afaca-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="afaca-126">contempla Puntero al tamaño devuelto, en bytes, del identificador de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="afaca-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="afaca-127">Si el parámetro _pEID_ apunta a un identificador de entrada no compuesto, el parámetro _pcbMsgEID_ es igual al valor del parámetro _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="afaca-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="afaca-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="afaca-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="afaca-129">contempla Puntero a un puntero al identificador de entrada devuelto del objeto.</span><span class="sxs-lookup"><span data-stu-id="afaca-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="afaca-130">Si el parámetro _pEID_ apunta a un identificador de entrada no compuesto, _ppMsgEID_ apunta a un puntero a una copia del identificador de entrada no compuesto.</span><span class="sxs-lookup"><span data-stu-id="afaca-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="afaca-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afaca-131">Return value</span></span>

<span data-ttu-id="afaca-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="afaca-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afaca-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="afaca-133">Remarks</span></span>

<span data-ttu-id="afaca-134">Si el identificador especificado por el parámetro _pEID_ es compuesto, se divide en el identificador de entrada del objeto dentro de su almacén de mensajes y el identificador de entrada del almacén.</span><span class="sxs-lookup"><span data-stu-id="afaca-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="afaca-135">Simplemente se copian las cadenas del identificador de entrada no compuesto.</span><span class="sxs-lookup"><span data-stu-id="afaca-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="afaca-136">El identificador compuesto que se va a separar suele ser uno de los creados por la función [HrComposeEID](hrcomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="afaca-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="afaca-137">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="afaca-137">Notes to callers</span></span>

<span data-ttu-id="afaca-138">La memoria que contiene el parámetro _pEID_ se publica tras la finalización correcta de esta función.</span><span class="sxs-lookup"><span data-stu-id="afaca-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="afaca-139">La implementación de la llamada es responsable de liberar memoria para los parámetros de salida.</span><span class="sxs-lookup"><span data-stu-id="afaca-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

