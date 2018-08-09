---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c2e6600af66f3dab8ff0fbb5442a1354687a3cbb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817792"
---
# <a name="imslogoncompareentryids"></a><span data-ttu-id="27219-103">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="27219-103">IMSLogon::CompareEntryIDs</span></span>

  
  
<span data-ttu-id="27219-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27219-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27219-105">Compara dos identificadores de entrada para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="27219-105">Compares two entry identifiers to determine whether they refer to the same object.</span></span> <span data-ttu-id="27219-106">MAPI hace referencia esta llamada a un proveedor de servicio únicamente si los identificadores únicos (UID) en ambos identificadores de entrada que se va a comparar son resueltos por dicho proveedor.</span><span class="sxs-lookup"><span data-stu-id="27219-106">MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.</span></span>
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="27219-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27219-107">Parameters</span></span>

 <span data-ttu-id="27219-108">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="27219-108">_cbEntryID1_</span></span>
  
> <span data-ttu-id="27219-109">[entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="27219-109">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="27219-110">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="27219-110">_lpEntryID1_</span></span>
  
> <span data-ttu-id="27219-111">[entrada] Un puntero para el primer identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="27219-111">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="27219-112">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="27219-112">_cbEntryID2_</span></span>
  
> <span data-ttu-id="27219-113">[entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="27219-113">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="27219-114">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="27219-114">_lpEntryID2_</span></span>
  
> <span data-ttu-id="27219-115">[entrada] Un puntero para el segundo identificador de entrada que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="27219-115">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="27219-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27219-116">_ulFlags_</span></span>
  
> <span data-ttu-id="27219-117">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="27219-117">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="27219-118">_lpulResult_</span><span class="sxs-lookup"><span data-stu-id="27219-118">_lpulResult_</span></span>
  
> <span data-ttu-id="27219-119">[out] Un puntero al resultado devuelto de la comparación.</span><span class="sxs-lookup"><span data-stu-id="27219-119">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="27219-120">TRUE si los identificadores de dos entrada hacen referencia al mismo objeto; en caso contrario, es FALSE.</span><span class="sxs-lookup"><span data-stu-id="27219-120">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="27219-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27219-121">Return value</span></span>

<span data-ttu-id="27219-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="27219-122">S_OK</span></span> 
  
> <span data-ttu-id="27219-123">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="27219-123">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27219-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27219-124">Remarks</span></span>

<span data-ttu-id="27219-125">Los proveedores de almacén de mensajes implementan el método **IMSLogon::CompareEntryIDs** para comparar dos identificadores de entrada para una entrada determinada en un almacén de mensajes para determinar si hacen referencia al mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="27219-125">Message store providers implement the **IMSLogon::CompareEntryIDs** method to compare two entry identifiers for a given entry in a message store to determine whether they refer to the same object.</span></span> <span data-ttu-id="27219-126">Si los identificadores de dos entrada hacer referencia al mismo objeto, **CompareEntryIDs** establece el parámetro _lpulResult_ en TRUE; Si hacen referencia a objetos diferentes, **CompareEntryIDs** establece _lpulResult_ en FALSE.</span><span class="sxs-lookup"><span data-stu-id="27219-126">If the two entry identifiers refer to the same object, **CompareEntryIDs** sets the  _lpulResult_ parameter to TRUE; if they refer to different objects, **CompareEntryIDs** sets  _lpulResult_ to FALSE.</span></span> 
  
 <span data-ttu-id="27219-127">**CompareEntryIDs** es útil porque un objeto puede tener más de un identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="27219-127">**CompareEntryIDs** is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="27219-128">Esto puede suceder, por ejemplo, después de instalar una nueva versión de un proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="27219-128">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27219-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="27219-129">See also</span></span>



[<span data-ttu-id="27219-130">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27219-130">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

