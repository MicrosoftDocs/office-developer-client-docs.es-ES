---
title: IMAPIViewContextGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351403"
---
# <a name="imapiviewcontextgetlasterror"></a><span data-ttu-id="0784c-103">IMAPIViewContext::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0784c-103">IMAPIViewContext::GetLastError</span></span>

  
  
<span data-ttu-id="0784c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0784c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0784c-105">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de contexto de vista.</span><span class="sxs-lookup"><span data-stu-id="0784c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the view context object.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="0784c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0784c-106">Parameters</span></span>

 <span data-ttu-id="0784c-107">_Valores_</span><span class="sxs-lookup"><span data-stu-id="0784c-107">_hResult_</span></span>
  
> <span data-ttu-id="0784c-108">a Tipo de datos HRESULT que contiene el valor de error generado en la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="0784c-108">[in] HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="0784c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0784c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0784c-110">a Máscara de máscara de los marcadores que controla el tipo de cadenas devueltas.</span><span class="sxs-lookup"><span data-stu-id="0784c-110">[in] Bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="0784c-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="0784c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0784c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0784c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0784c-113">Las cadenas de la estructura **MAPIERROR** devueltas en el parámetro _lppMAPIError_ están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0784c-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="0784c-114">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0784c-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="0784c-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="0784c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="0784c-116">contempla Puntero a un puntero a la estructura **MAPIERROR** devuelta que contiene la información de versión, componente y contexto del error.</span><span class="sxs-lookup"><span data-stu-id="0784c-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="0784c-117">Este parámetro se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver.</span><span class="sxs-lookup"><span data-stu-id="0784c-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0784c-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0784c-118">Return value</span></span>

<span data-ttu-id="0784c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0784c-119">S_OK</span></span> 
  
> <span data-ttu-id="0784c-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0784c-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0784c-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0784c-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0784c-122">Se estableció la marca MAPI_UNICODE y **GetLastError** no admite Unicode, o bien no se estableció MAPI_UNICODE y **GetLastError** solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="0784c-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** only supports Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0784c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0784c-123">Remarks</span></span>

<span data-ttu-id="0784c-124">El método **IMAPIViewContext:: GetLastError** proporciona información sobre una llamada a un método anterior que produjo un error.</span><span class="sxs-lookup"><span data-stu-id="0784c-124">The **IMAPIViewContext::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="0784c-125">Los autores de llamadas pueden proporcionar a sus usuarios información detallada acerca del error al incluir los datos de la estructura **MAPIERROR** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0784c-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0784c-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="0784c-126">Notes to callers</span></span>

<span data-ttu-id="0784c-127">Puede hacer uso de la estructura **MAPIERROR** apuntado por el parámetro _lppMAPIError_ si MAPI proporciona solo una si **GetLastError** Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="0784c-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="0784c-128">A veces MAPI no puede determinar el último error o no tiene nada más para informar sobre el error.</span><span class="sxs-lookup"><span data-stu-id="0784c-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="0784c-129">En esta situación, un puntero a NULL se devuelve en _lppMAPIError_ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0784c-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="0784c-130">Para obtener más información sobre el método **GetLastError** , vea [errores extendidos de MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="0784c-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0784c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0784c-131">See also</span></span>



[<span data-ttu-id="0784c-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="0784c-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="0784c-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0784c-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0784c-134">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0784c-134">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

