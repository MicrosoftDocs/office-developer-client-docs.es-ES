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
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348051"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="d1cf4-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="d1cf4-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="d1cf4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1cf4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1cf4-105">Crea una cadena ASCII que representa un identificador de entrada compuesto para un objeto, normalmente un mensaje en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1cf4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d1cf4-106">Header file:</span></span>  <br/> |<span data-ttu-id="d1cf4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d1cf4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d1cf4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d1cf4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d1cf4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d1cf4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d1cf4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d1cf4-110">Called by:</span></span>  <br/> |<span data-ttu-id="d1cf4-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="d1cf4-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d1cf4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d1cf4-112">Parameters</span></span>

 <span data-ttu-id="d1cf4-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="d1cf4-113">_psession_</span></span>
  
> <span data-ttu-id="d1cf4-114">a Puntero a la sesión que usa la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="d1cf4-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="d1cf4-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="d1cf4-116">a Tamaño, en bytes, de la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="d1cf4-117">Si se pasa cero en el parámetro _cbStoreRecordKey_ , el parámetro _pszMsgID_ apunta a una copia del identificador de entrada convertida en texto.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="d1cf4-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="d1cf4-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="d1cf4-119">a Puntero a la clave de registro del almacén de mensajes que contiene el mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="d1cf4-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="d1cf4-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="d1cf4-121">a Tamaño, en bytes, del identificador de entrada del mensaje u otro objeto.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="d1cf4-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="d1cf4-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="d1cf4-123">a Puntero al identificador de entrada del objeto.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="d1cf4-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="d1cf4-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="d1cf4-125">contempla Puntero a la cadena ASCII devuelta.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="d1cf4-126">Si el parámetro _cbStoreRecordKey_ es mayor que cero, el parámetro _pszMsgID_ apunta a un identificador de entrada compuesto convertido en texto.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="d1cf4-127">Si _cbStoreRecordKey_ es cero, _pszMsgID_ apunta a un identificador de entrada no compuesto convertido en texto.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d1cf4-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1cf4-128">Return value</span></span>

<span data-ttu-id="d1cf4-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1cf4-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1cf4-130">Remarks</span></span>

<span data-ttu-id="d1cf4-131">Si el mensaje u otro objeto para el que se crea el identificador de entrada compuesto reside en un almacén de mensajes, la cadena de identificador se crea a partir del identificador de entrada del objeto y la clave de registro del almacén.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="d1cf4-132">Si el objeto no está en un almacén, es decir, si el número de bytes para la clave de registro de almacén que se pasa en el parámetro _cbStoreRecordKey_ es cero, el identificador de entrada del objeto simplemente se copia y se convierte en una cadena.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="d1cf4-133">Llamar a la función **HrComposeMsgID** equivale a llamar a la función [HrComposeEID](hrcomposeeid.md) y, a continuación, a la función [HrSzFromEntryID](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="d1cf4-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="d1cf4-134">**HrComposeMsgID** permite a las aplicaciones cliente trabajar con objetos en varios almacenes a través del uso de identificadores de entrada compuesta.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="d1cf4-135">Una aplicación puede llamar a la función [HrDecomposeMsgID](hrdecomposemsgid.md) para dividir el identificador de entrada compuesta en sus componentes originales.</span><span class="sxs-lookup"><span data-stu-id="d1cf4-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

