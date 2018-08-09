---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 418ffdd19412dcf948d36a5e7df33f7978d0df3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817030"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="44cd8-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="44cd8-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="44cd8-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44cd8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44cd8-105">Crea una cadena de ASCII que representa un identificador de entrada compuestos para un objeto, normalmente un mensaje en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="44cd8-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44cd8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="44cd8-106">Header file:</span></span>  <br/> |<span data-ttu-id="44cd8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="44cd8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="44cd8-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="44cd8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="44cd8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="44cd8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="44cd8-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="44cd8-110">Called by:</span></span>  <br/> |<span data-ttu-id="44cd8-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="44cd8-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a><span data-ttu-id="44cd8-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44cd8-112">Parameters</span></span>

 <span data-ttu-id="44cd8-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="44cd8-113">_psession_</span></span>
  
> <span data-ttu-id="44cd8-114">[entrada] Puntero a la sesión en uso por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="44cd8-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="44cd8-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="44cd8-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="44cd8-116">[entrada] Tamaño, en bytes, de la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="44cd8-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="44cd8-117">Si se pasa cero en el parámetro _cbStoreRecordKey_ , los puntos de parámetro _pszMsgID_ a una copia del identificador de entrada se convierten en texto.</span><span class="sxs-lookup"><span data-stu-id="44cd8-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="44cd8-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="44cd8-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="44cd8-119">[entrada] Puntero a la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="44cd8-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="44cd8-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="44cd8-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="44cd8-121">[entrada] Tamaño, en bytes, del identificador de entrada del mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="44cd8-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="44cd8-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="44cd8-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="44cd8-123">[entrada] Puntero al identificador de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="44cd8-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="44cd8-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="44cd8-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="44cd8-125">[out] Puntero a la cadena devuelta de ASCII.</span><span class="sxs-lookup"><span data-stu-id="44cd8-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="44cd8-126">Si el parámetro _cbStoreRecordKey_ es mayor que cero, los puntos de parámetro _pszMsgID_ a un identificador de entrada compuestos se convierten en texto.</span><span class="sxs-lookup"><span data-stu-id="44cd8-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="44cd8-127">Si _cbStoreRecordKey_ es cero, _pszMsgID_ puntos a un identificador de entrada los convierten en texto.</span><span class="sxs-lookup"><span data-stu-id="44cd8-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="44cd8-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44cd8-128">Return value</span></span>

<span data-ttu-id="44cd8-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44cd8-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44cd8-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44cd8-130">Remarks</span></span>

<span data-ttu-id="44cd8-131">Si el mensaje u otro objeto para el que se está creando el identificador de entrada compuestos reside en un almacén de mensajes, se crea la cadena de identificador de identificador de entrada del objeto y la clave de registro de la tienda.</span><span class="sxs-lookup"><span data-stu-id="44cd8-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="44cd8-132">Si el objeto no está en un almacén, es decir, si el número de bytes de la clave de registro del almacén de pasa en el parámetro _cbStoreRecordKey_ es cero, el identificador del objeto entrada es simplemente copiado y convertir en una cadena.</span><span class="sxs-lookup"><span data-stu-id="44cd8-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="44cd8-133">Llamar a la función **HrComposeMsgID** es equivalente a llamar a la función [HrComposeEID](hrcomposeeid.md) y, a continuación, la función [HrSzFromEntryID](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="44cd8-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="44cd8-134">**HrComposeMsgID** permite que las aplicaciones de cliente trabajar con objetos en varios almacenes mediante el uso de los identificadores de entrada compuestos.</span><span class="sxs-lookup"><span data-stu-id="44cd8-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="44cd8-135">Una aplicación puede llamar a la función [HrDecomposeMsgID](hrdecomposemsgid.md) para dividir el identificador de entrada compuesto en sus componentes originales.</span><span class="sxs-lookup"><span data-stu-id="44cd8-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

