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
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326568"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="a4aac-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="a4aac-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="a4aac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4aac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4aac-105">Registra la función de preprocesador del proveedor de transporte (una función que se ajusta al prototipo [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="a4aac-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="a4aac-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a4aac-106">Parameters</span></span>

 <span data-ttu-id="a4aac-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="a4aac-107">_lpMuid_</span></span>
  
> <span data-ttu-id="a4aac-108">a Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador que administra la función preprocesador.</span><span class="sxs-lookup"><span data-stu-id="a4aac-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="a4aac-109">El parámetro _lpMuid_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="a4aac-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a4aac-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="a4aac-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="a4aac-111">a Un puntero al tipo de dirección para los mensajes en los que funciona la función, como FAX, SMTP o X500.</span><span class="sxs-lookup"><span data-stu-id="a4aac-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="a4aac-112">El parámetro _lpszAdrType_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="a4aac-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a4aac-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="a4aac-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="a4aac-114">a Un puntero al nombre de la biblioteca de vínculos dinámicos (DLL) que contiene el punto de entrada de la función de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="a4aac-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="a4aac-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="a4aac-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="a4aac-116">a Un puntero al nombre de la función de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="a4aac-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="a4aac-117">El parámetro _lpszPreprocess_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="a4aac-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a4aac-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="a4aac-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="a4aac-119">a Un puntero al nombre de la función que quita la información del preprocesador (una función que se ajusta al prototipo [RemovePreprocessInfo](removepreprocessinfo.md) ).</span><span class="sxs-lookup"><span data-stu-id="a4aac-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="a4aac-120">El parámetro _lpszRemovePreprocessInfo_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="a4aac-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a4aac-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4aac-121">_ulFlags_</span></span>
  
> <span data-ttu-id="a4aac-122">Reserve debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a4aac-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4aac-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4aac-123">Return value</span></span>

<span data-ttu-id="a4aac-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4aac-124">S_OK</span></span> 
  
> <span data-ttu-id="a4aac-125">La función de preprocesador se registró correctamente.</span><span class="sxs-lookup"><span data-stu-id="a4aac-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4aac-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4aac-126">Remarks</span></span>

<span data-ttu-id="a4aac-127">El método **IMAPISupport:: RegisterPreprocessor** se implementa solo para objetos de soporte de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="a4aac-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="a4aac-128">Los proveedores de transporte llaman a **RegisterPreprocessor** para registrar una función de preprocesador (una función que se ajusta al prototipo [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="a4aac-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="a4aac-129">Una función de preprocesador debe registrarse antes de que la cola MAPI pueda llamarla.</span><span class="sxs-lookup"><span data-stu-id="a4aac-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="a4aac-130">Los parámetros _lpszPreprocess_, _lpszRemovePreprocessInfo_y _lpszDLLName_ deben apuntar a cadenas que se pueden usar junto con llamadas a la función **GetProcAddress** de Win32, lo que permite la dll del preprocesador. punto de entrada al que se va a llamar correctamente.</span><span class="sxs-lookup"><span data-stu-id="a4aac-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a4aac-131">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a4aac-131">Notes to callers</span></span>

<span data-ttu-id="a4aac-132">Las llamadas a los preprocesadores son específicas del orden de los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="a4aac-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="a4aac-133">Esto significa que si otro proveedor de transporte que preantes de su proveedor puede controlar un mensaje, no se llamará a la función de preprocesador para ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="a4aac-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="a4aac-134">Se llamará a la función de preprocesador solo para los mensajes que va a controlar.</span><span class="sxs-lookup"><span data-stu-id="a4aac-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="a4aac-135">Puede escribir funciones de preprocesador para controlar un identificador específico almacenado en una estructura [MAPIUID](mapiuid.md) o un tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="a4aac-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="a4aac-136">Si especifica una estructura **MAPIUID** en el parámetro _lpMuid_ y un tipo de dirección en el parámetro _lpszAdrType_ , se llamará a la función para los destinatarios del mensaje que coinciden con el tipo de dirección o **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="a4aac-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="a4aac-137">Si _lpMuid_ es NULL y _LPSZADRTYPE_ no es null, se llamará a la función solo para los destinatarios que tengan una dirección que coincida con el tipo al que señala _lpszAdrType_.</span><span class="sxs-lookup"><span data-stu-id="a4aac-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="a4aac-138">Si _lpMuid_ no es NULL y _lpszAdrType_ es null, se llamará a la función para los destinatarios que coinciden con **MAPIUID**, independientemente de su tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="a4aac-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="a4aac-139">Si ambos son NULL, se llama a la función para todos los destinatarios del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a4aac-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a4aac-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4aac-140">See also</span></span>



[<span data-ttu-id="a4aac-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a4aac-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a4aac-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="a4aac-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="a4aac-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="a4aac-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="a4aac-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a4aac-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

