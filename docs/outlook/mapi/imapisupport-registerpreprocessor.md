---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 219c15fc00490983e970e4533f927cf4d91916b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817543"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="edb2d-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="edb2d-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="edb2d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="edb2d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="edb2d-105">Registra la función de preprocesador del proveedor de transporte (una función que se ajusta al prototipo [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="edb2d-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="edb2d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edb2d-106">Parameters</span></span>

 <span data-ttu-id="edb2d-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="edb2d-107">_lpMuid_</span></span>
  
> <span data-ttu-id="edb2d-108">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador que controla la función del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="edb2d-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="edb2d-109">El parámetro _lpMuid_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="edb2d-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="edb2d-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="edb2d-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="edb2d-111">[entrada] Un puntero para el tipo de dirección para los mensajes de la función opera en, como FAX, SMTP o X500.</span><span class="sxs-lookup"><span data-stu-id="edb2d-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="edb2d-112">El parámetro _lpszAdrType_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="edb2d-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="edb2d-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="edb2d-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="edb2d-114">[entrada] Un puntero en el nombre de la biblioteca de vínculos dinámicos (DLL) que contiene el punto de entrada para la función de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="edb2d-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="edb2d-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="edb2d-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="edb2d-116">[entrada] Un puntero en el nombre de la función del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="edb2d-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="edb2d-117">El parámetro _lpszPreprocess_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="edb2d-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="edb2d-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="edb2d-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="edb2d-119">[entrada] Un puntero en el nombre de la función que quita la información del preprocesador (una función que se ajusta al prototipo [RemovePreprocessInfo](removepreprocessinfo.md) ).</span><span class="sxs-lookup"><span data-stu-id="edb2d-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="edb2d-120">El parámetro _lpszRemovePreprocessInfo_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="edb2d-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="edb2d-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="edb2d-121">_ulFlags_</span></span>
  
> <span data-ttu-id="edb2d-122">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="edb2d-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="edb2d-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edb2d-123">Return value</span></span>

<span data-ttu-id="edb2d-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="edb2d-124">S_OK</span></span> 
  
> <span data-ttu-id="edb2d-125">La función del preprocesador se ha registrado correctamente.</span><span class="sxs-lookup"><span data-stu-id="edb2d-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="edb2d-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edb2d-126">Remarks</span></span>

<span data-ttu-id="edb2d-127">El método **IMAPISupport::RegisterPreprocessor** se implementa para los objetos de soporte técnico de proveedor de transporte sólo.</span><span class="sxs-lookup"><span data-stu-id="edb2d-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="edb2d-128">Los proveedores de transporte llame a **RegisterPreprocessor** para registrar una función del preprocesador (es decir, una función que se ajusta al prototipo [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="edb2d-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="edb2d-129">Una función del preprocesador debe estar registrada antes de la cola MAPI puede llamarlo.</span><span class="sxs-lookup"><span data-stu-id="edb2d-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="edb2d-130">Los parámetros _lpszPreprocess_, _lpszRemovePreprocessInfo_y _lpszDLLName_ deben apuntar a las cadenas que se pueden usar en combinación con llamadas a la función de Win32 **GetProcAddress** , lo que permite DLL del preprocesador punto de entrada que se llama correctamente.</span><span class="sxs-lookup"><span data-stu-id="edb2d-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="edb2d-131">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="edb2d-131">Notes to callers</span></span>

<span data-ttu-id="edb2d-132">Las llamadas a preprocessors son específicas de orden del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="edb2d-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="edb2d-133">Esto significa que, si otro proveedor de transporte por delante de su proveedor es capaz de controlar un mensaje, no se llamará su función preprocesador para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="edb2d-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="edb2d-134">Se llamará a la función del preprocesador únicamente para los mensajes que va a controlar.</span><span class="sxs-lookup"><span data-stu-id="edb2d-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="edb2d-135">Puede escribir funciones del preprocesador para controlar un identificador de específico almacenado en una estructura [MAPIUID](mapiuid.md) o un tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="edb2d-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="edb2d-136">Si especifica ambos una estructura **MAPIUID** en el parámetro _lpMuid_ y un tipo de dirección en el parámetro _lpszAdrType_ , la función se llamará para los destinatarios del mensaje que coinciden con el **MAPIUID** o el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="edb2d-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="edb2d-137">Si _lpMuid_ es NULL y _lpszAdrType_ no es NULL, la función se llamará sólo para los destinatarios que tienen una dirección que coincide con el tipo que señala _lpszAdrType_.</span><span class="sxs-lookup"><span data-stu-id="edb2d-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="edb2d-138">Si _lpMuid_ es no nulo y _lpszAdrType_ es NULL, la función se llamará para los destinatarios que coinciden con **MAPIUID**, independientemente de su tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="edb2d-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="edb2d-139">Si ambos son NULL, la función se llama para todos los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="edb2d-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edb2d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="edb2d-140">See also</span></span>



[<span data-ttu-id="edb2d-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="edb2d-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="edb2d-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="edb2d-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="edb2d-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="edb2d-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="edb2d-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="edb2d-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

