---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426712"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="417a8-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="417a8-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="417a8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="417a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="417a8-105">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="417a8-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="417a8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="417a8-106">Parameters</span></span>

 <span data-ttu-id="417a8-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="417a8-107">_hResult_</span></span>
  
> <span data-ttu-id="417a8-108">[entrada] Un tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="417a8-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="417a8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="417a8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="417a8-110">[entrada] Máscara de bits de marcas que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="417a8-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="417a8-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="417a8-111">The following flag can be set:</span></span>
    
<span data-ttu-id="417a8-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="417a8-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="417a8-113">Las cadenas de la [estructura MAPIERROR](mapierror.md) devueltas en el parámetro  _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="417a8-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="417a8-114">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="417a8-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="417a8-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="417a8-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="417a8-116">[salida] Puntero a un puntero a una **estructura MAPIERROR** que contiene información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="417a8-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="417a8-117">El _parámetro lppMAPIError_ se puede establecer en NULL si el formulario no puede proporcionar la información adecuada para una **estructura MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="417a8-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="417a8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="417a8-118">Return value</span></span>

<span data-ttu-id="417a8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="417a8-119">S_OK</span></span> 
  
> <span data-ttu-id="417a8-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="417a8-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="417a8-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="417a8-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="417a8-122">Se estableció MAPI_UNICODE marca y el proveedor de libreta de direcciones no admite Unicode o MAPI_UNICODE no se estableció y el proveedor de libreta de direcciones solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="417a8-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="417a8-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="417a8-123">Remarks</span></span>

<span data-ttu-id="417a8-124">Los objetos de formulario implementan **el método IPersistMessage::GetLastError** para proporcionar información sobre una llamada de método anterior que ha fallado.</span><span class="sxs-lookup"><span data-stu-id="417a8-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="417a8-125">Los visores de formularios pueden proporcionar a sus usuarios información detallada sobre el error incluyendo los datos de la estructura [MAPIERROR](mapierror.md) en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="417a8-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="417a8-126">Una llamada a **GetLastError** no afecta al estado del formulario.</span><span class="sxs-lookup"><span data-stu-id="417a8-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="417a8-127">Cuando **se devuelve GetLastError,** el formulario permanece en el estado en el que estaba antes de que se realizara la llamada.</span><span class="sxs-lookup"><span data-stu-id="417a8-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="417a8-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="417a8-128">Notes to callers</span></span>

<span data-ttu-id="417a8-129">Puede usar la estructura **MAPIERROR,** si el formulario proporciona una, a la que apunta el parámetro  _lppMAPIError_ sólo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="417a8-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="417a8-130">A veces, el formulario no puede determinar cuál fue el último error o no tiene nada más que informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="417a8-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="417a8-131">En esta situación, el formulario devuelve un puntero a NULL  _en lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="417a8-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="417a8-132">Para obtener más información acerca **del método GetLastError,** vea [errores extendidos de MAPI.](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="417a8-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="417a8-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="417a8-133">See also</span></span>



[<span data-ttu-id="417a8-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="417a8-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="417a8-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="417a8-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="417a8-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="417a8-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

