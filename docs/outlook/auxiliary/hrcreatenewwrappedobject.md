---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crea un objeto al que un cliente puede tener acceso en un formato de carácter preferido.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317608"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="78201-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="78201-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="78201-104">Crea un objeto al que un cliente puede tener acceso en un formato de carácter preferido.</span><span class="sxs-lookup"><span data-stu-id="78201-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="78201-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="78201-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78201-106">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="78201-106">Exported by:</span></span>  <br/> |<span data-ttu-id="78201-107">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="78201-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="78201-108">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="78201-108">Called by:</span></span>  <br/> |<span data-ttu-id="78201-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="78201-109">Client</span></span>  <br/> |
|<span data-ttu-id="78201-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="78201-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="78201-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="78201-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a><span data-ttu-id="78201-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78201-112">Parameters</span></span>

<span data-ttu-id="78201-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="78201-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="78201-114">[entrada] Objeto inicial de Outlook sin envolver.</span><span class="sxs-lookup"><span data-stu-id="78201-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="78201-115">Debe implementar una de las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="78201-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="78201-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), o [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="78201-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="78201-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="78201-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="78201-118">[entrada] Marcas que caracterizan el objeto inicial sin envolver.</span><span class="sxs-lookup"><span data-stu-id="78201-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="78201-119">Debe ser uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="78201-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="78201-120">DDLWRAP_FLAG_ANSI: el objeto sin envolver es ANSI.</span><span class="sxs-lookup"><span data-stu-id="78201-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="78201-121">DDLWRAP_FLAG_UNICODE: el objeto sin envolver es UNICODE.</span><span class="sxs-lookup"><span data-stu-id="78201-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="78201-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="78201-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="78201-123">[entrada] Marcas para el formato de carácter preferido.</span><span class="sxs-lookup"><span data-stu-id="78201-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="78201-124">Debe ser uno o varios de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="78201-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="78201-125">DDLWRAP_FLAG_ANSI: el objeto ajustado se mostrará como ANSI.</span><span class="sxs-lookup"><span data-stu-id="78201-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="78201-126">DDLWRAP_FLAG_UNICODE: el objeto ajustado se mostrará como UNICODE.</span><span class="sxs-lookup"><span data-stu-id="78201-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="78201-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="78201-127">_pIID_</span></span>
  
>  <span data-ttu-id="78201-128">[entrada] Identificador de la interfaz admitida por el objeto sin envolver; esta opción se establece en NULL si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="78201-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="78201-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="78201-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="78201-130">[entrada] Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="78201-130">[in] This parameter is not used.</span></span> <span data-ttu-id="78201-131">Debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="78201-131">It must be NULL.</span></span> 
    
<span data-ttu-id="78201-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="78201-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="78201-133">[entrada] Establezca este parámetro en **true si** se debe comprobar el formato de  _pvUnwrapped_ antes del ajuste; se establece en **false** si el objeto debe ajustarse sin comprobarlo.</span><span class="sxs-lookup"><span data-stu-id="78201-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="78201-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="78201-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="78201-135">[salida] Puntero al objeto solicitado, ajustado en el formato de carácter solicitado.</span><span class="sxs-lookup"><span data-stu-id="78201-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="78201-136">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="78201-136">Return values</span></span>

<span data-ttu-id="78201-137">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="78201-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78201-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78201-138">Remarks</span></span>

<span data-ttu-id="78201-139">Pasar un objeto ajustado con  _fCheckWrap_ establecido en **true** dará como resultado un objeto sin envolver.</span><span class="sxs-lookup"><span data-stu-id="78201-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="78201-140">Independientemente de si el objeto devuelto está ajustado o no, el cliente es responsable de liberar la referencia en el objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="78201-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="78201-141">Al usar **GetProcAddress para** buscar la dirección de esta función en msmapi32.dll, especifique **HrCreateNewWrappedObject@28** como nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="78201-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78201-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="78201-142">See also</span></span>

- [<span data-ttu-id="78201-143">Acerca de la capa de degradación de datos API</span><span class="sxs-lookup"><span data-stu-id="78201-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="78201-144">Constantes (API de capa de degradación de datos)</span><span class="sxs-lookup"><span data-stu-id="78201-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

