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
ms.openlocfilehash: a39deb57a24b3a89ee10020a6442bcb1bca612a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575311"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="63ff1-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="63ff1-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="63ff1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63ff1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63ff1-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior en el objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="63ff1-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="63ff1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63ff1-106">Parameters</span></span>

 <span data-ttu-id="63ff1-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="63ff1-107">_hResult_</span></span>
  
> <span data-ttu-id="63ff1-108">[entrada] Un tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="63ff1-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="63ff1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63ff1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="63ff1-110">[entrada] Una máscara de bits de indicadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="63ff1-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="63ff1-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="63ff1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="63ff1-112">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="63ff1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="63ff1-113">Las cadenas en la estructura [MAPIERROR](mapierror.md) devuelta en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="63ff1-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="63ff1-114">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="63ff1-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="63ff1-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="63ff1-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="63ff1-116">[out] Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error.</span><span class="sxs-lookup"><span data-stu-id="63ff1-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="63ff1-117">El parámetro _lppMAPIError_ se puede establecer en NULL si el formulario no puede proporcionar la información adecuada para una estructura **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="63ff1-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="63ff1-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63ff1-118">Return value</span></span>

<span data-ttu-id="63ff1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="63ff1-119">S_OK</span></span> 
  
> <span data-ttu-id="63ff1-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="63ff1-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="63ff1-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="63ff1-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="63ff1-122">Se ha establecido el indicador MAPI_UNICODE y el proveedor de la libreta de direcciones no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y el proveedor de la libreta de direcciones admite sólo Unicode.</span><span class="sxs-lookup"><span data-stu-id="63ff1-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63ff1-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63ff1-123">Remarks</span></span>

<span data-ttu-id="63ff1-124">Objetos de formulario implementan el método **IPersistMessage::GetLastError** para proporcionar información acerca de una llamada de método anteriores que no se pudo.</span><span class="sxs-lookup"><span data-stu-id="63ff1-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="63ff1-125">Visores de formulario pueden proporcionar a sus usuarios con información detallada sobre el error mediante la inclusión de los datos de la estructura [MAPIERROR](mapierror.md) en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="63ff1-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="63ff1-126">Una llamada a **GetLastError** no afecta el estado del formulario.</span><span class="sxs-lookup"><span data-stu-id="63ff1-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="63ff1-127">Cuando se devuelve **GetLastError** , el formulario permanece en el estado en que estaba antes de que se realizó la llamada.</span><span class="sxs-lookup"><span data-stu-id="63ff1-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="63ff1-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="63ff1-128">Notes to callers</span></span>

<span data-ttu-id="63ff1-129">Puede usar la estructura **MAPIERROR** , si el formulario proporciona uno, que señala el parámetro _lppMAPIError_ sólo si **GetLastError** devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="63ff1-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="63ff1-130">En ocasiones, el formulario no puede determinar qué era el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="63ff1-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="63ff1-131">En esta situación, el formulario devuelve un puntero a NULL en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="63ff1-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="63ff1-132">Para obtener más información acerca del método **GetLastError** , vea [Errores de MAPI extendida](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="63ff1-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63ff1-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="63ff1-133">See also</span></span>



[<span data-ttu-id="63ff1-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="63ff1-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="63ff1-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="63ff1-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="63ff1-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63ff1-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

