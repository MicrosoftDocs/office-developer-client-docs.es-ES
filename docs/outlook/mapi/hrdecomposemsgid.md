---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404438"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="c4db5-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="c4db5-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="c4db5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4db5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4db5-105">Separa la representación ASCII del identificador de entrada compuesto de un objeto, normalmente un mensaje en un almacén de mensajes, en el identificador de entrada de ese objeto en el almacén y el identificador de entrada del almacén.</span><span class="sxs-lookup"><span data-stu-id="c4db5-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4db5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c4db5-106">Header file:</span></span>  <br/> |<span data-ttu-id="c4db5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c4db5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c4db5-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c4db5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c4db5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c4db5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c4db5-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c4db5-110">Called by:</span></span>  <br/> |<span data-ttu-id="c4db5-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="c4db5-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="c4db5-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4db5-112">Parameters</span></span>

 <span data-ttu-id="c4db5-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="c4db5-113">_psession_</span></span>
  
> <span data-ttu-id="c4db5-114">[entrada] Puntero a la sesión en uso por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c4db5-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="c4db5-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="c4db5-115">_szMsgID_</span></span>
  
> <span data-ttu-id="c4db5-116">[entrada] Cadena que representa el identificador de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="c4db5-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="c4db5-117">_pbcStoreEID_</span><span class="sxs-lookup"><span data-stu-id="c4db5-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="c4db5-118">[salida] Puntero al tamaño devuelto, en bytes, del identificador de entrada del almacén de mensajes que contiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="c4db5-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="c4db5-119">Si el  _parámetro szMsgID_ apunta a una cadena de identificador de entrada no completa, el parámetro  _szStoreEID_ apunta a cero.</span><span class="sxs-lookup"><span data-stu-id="c4db5-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="c4db5-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="c4db5-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="c4db5-121">[salida] Puntero a un puntero al identificador de entrada devuelto del almacén de mensajes que contiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="c4db5-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="c4db5-122">Si el _parámetro szMsgID_ apunta a un identificador de entrada no completo, se devuelve NULL en el _parámetro ppStoreEID._</span><span class="sxs-lookup"><span data-stu-id="c4db5-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="c4db5-123">_dimmMsgEID_</span><span class="sxs-lookup"><span data-stu-id="c4db5-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="c4db5-124">[salida] Puntero al tamaño devuelto, en bytes, del identificador de entrada del objeto dentro de su almacén.</span><span class="sxs-lookup"><span data-stu-id="c4db5-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="c4db5-125">Si el _parámetro szMsgID_ apunta a una cadena de identificador de entrada no completa, el parámetro _dimmMsgEID_ es igual al valor del _parámetro cbEID._</span><span class="sxs-lookup"><span data-stu-id="c4db5-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="c4db5-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="c4db5-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="c4db5-127">[salida] Puntero a un puntero a la cadena de identificador de entrada devuelta del objeto dentro de su almacén.</span><span class="sxs-lookup"><span data-stu-id="c4db5-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="c4db5-128">Si el  _parámetro szMsgID_ apunta a un identificador de entrada no completo,  _ppMsgEID_ apunta a un puntero a una copia convertida del identificador de entrada no completa.</span><span class="sxs-lookup"><span data-stu-id="c4db5-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c4db5-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4db5-129">Return value</span></span>

<span data-ttu-id="c4db5-130">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c4db5-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4db5-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4db5-131">Remarks</span></span>

<span data-ttu-id="c4db5-132">Si el identificador especificado por el parámetro  _szMsgID_ es compuesto, se convierte de ASCII y se divide en el identificador de entrada del objeto dentro de su almacén de mensajes y el identificador de entrada del almacén.</span><span class="sxs-lookup"><span data-stu-id="c4db5-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="c4db5-133">Las cadenas de identificador de entrada no completa simplemente se convierten y copian.</span><span class="sxs-lookup"><span data-stu-id="c4db5-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="c4db5-134">La cadena de identificador compuesto que se va a separar suele ser una creada por la función [HrComposeMsgID.](hrcomposemsgid.md)</span><span class="sxs-lookup"><span data-stu-id="c4db5-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="c4db5-135">Llamar a **la función HrDecomposeMsgID** equivale a llamar a la función [HrEntryIDFromSz](hrentryidfromsz.md) y, a continuación, a la función [HrDecomposeEID.](hrdecomposeeid.md)</span><span class="sxs-lookup"><span data-stu-id="c4db5-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

