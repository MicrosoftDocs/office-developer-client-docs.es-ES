---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a9aa6deeca930da82db61ba517796bfbc0676467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817031"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="19739-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="19739-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="19739-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19739-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19739-105">Crea un identificador de entrada compuestos para un objeto, normalmente un mensaje en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="19739-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19739-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="19739-106">Header file:</span></span>  <br/> |<span data-ttu-id="19739-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="19739-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="19739-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="19739-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="19739-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="19739-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="19739-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="19739-110">Called by:</span></span>  <br/> |<span data-ttu-id="19739-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="19739-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a><span data-ttu-id="19739-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19739-112">Parameters</span></span>

 <span data-ttu-id="19739-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="19739-113">_psession_</span></span>
  
> <span data-ttu-id="19739-114">[entrada] Puntero a la sesión en uso por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="19739-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="19739-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="19739-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="19739-116">[entrada] Tamaño, en bytes, de la clave de registro del almacén de mensajes mantiene el mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="19739-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="19739-117">Si se pasa cero en el parámetro _cbStoreRecordKey_ , el parámetro _ppEID_ apunta a una copia del identificador de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="19739-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="19739-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="19739-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="19739-119">[entrada] Puntero a la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="19739-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="19739-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="19739-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="19739-121">[entrada] Tamaño, en bytes, del identificador de entrada del mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="19739-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="19739-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="19739-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="19739-123">[entrada] Puntero al identificador de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="19739-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="19739-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="19739-124">_pcbEID_</span></span>
  
> <span data-ttu-id="19739-125">[out] Puntero al tamaño, en bytes, del identificador devuelto.</span><span class="sxs-lookup"><span data-stu-id="19739-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="19739-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="19739-126">_ppEID_</span></span>
  
> <span data-ttu-id="19739-127">[out] Puntero a un puntero al identificador de la entrada devuelta.</span><span class="sxs-lookup"><span data-stu-id="19739-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="19739-128">Si el valor del parámetro _cbStoreRecordKey_ es mayor que cero, el parámetro _ppEID_ apunta a un puntero al identificador de entrada compuestos que se crea.</span><span class="sxs-lookup"><span data-stu-id="19739-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="19739-129">Si _cbStoreRecordKey_ es cero, _ppEID_ apunta a un puntero a una copia del identificador de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="19739-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="19739-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19739-130">Return value</span></span>

<span data-ttu-id="19739-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="19739-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19739-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19739-132">Remarks</span></span>

<span data-ttu-id="19739-133">Si el mensaje u otro objeto para el que se está creando el identificador de entrada compuestos reside en un almacén de mensajes, se crea el identificador de identificador de entrada del objeto y la clave de registro de la tienda.</span><span class="sxs-lookup"><span data-stu-id="19739-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="19739-134">Si el objeto no está en un almacén, es decir, si el número de bytes para la clave de registro de almacenamiento que se pasan en _cbStoreRecordKey_ es cero, el identificador del objeto entrada es simplemente se copian.</span><span class="sxs-lookup"><span data-stu-id="19739-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="19739-135">La función **HrComposeEID** permite a las aplicaciones trabajar con objetos en varios almacenes mediante el uso de los identificadores de entrada compuestos.</span><span class="sxs-lookup"><span data-stu-id="19739-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="19739-136">Una aplicación puede llamar a la función [HrDecomposeEID](hrdecomposeeid.md) para dividir el identificador de entrada compuesto en sus componentes originales.</span><span class="sxs-lookup"><span data-stu-id="19739-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19739-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="19739-137">See also</span></span>



[<span data-ttu-id="19739-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="19739-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="19739-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="19739-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

