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
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="98c0c-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="98c0c-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="98c0c-104">Crea un objeto al que un cliente puede tener acceso en un formato de carácter preferido.</span><span class="sxs-lookup"><span data-stu-id="98c0c-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="98c0c-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="98c0c-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98c0c-106">ExPortado por:</span><span class="sxs-lookup"><span data-stu-id="98c0c-106">Exported by:</span></span>  <br/> |<span data-ttu-id="98c0c-107">MSMAPI32. dll</span><span class="sxs-lookup"><span data-stu-id="98c0c-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="98c0c-108">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="98c0c-108">Called by:</span></span>  <br/> |<span data-ttu-id="98c0c-109">Client</span><span class="sxs-lookup"><span data-stu-id="98c0c-109">Client</span></span>  <br/> |
|<span data-ttu-id="98c0c-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="98c0c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="98c0c-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="98c0c-111">Outlook</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="98c0c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="98c0c-112">Parameters</span></span>

<span data-ttu-id="98c0c-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="98c0c-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="98c0c-114">a El objeto de Outlook desajustado inicial.</span><span class="sxs-lookup"><span data-stu-id="98c0c-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="98c0c-115">Debe implementar una de las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="98c0c-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="98c0c-116">[IMailUser: IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)o [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="98c0c-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="98c0c-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="98c0c-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="98c0c-118">a Marcadores que caracterizan el objeto inicial desajustado.</span><span class="sxs-lookup"><span data-stu-id="98c0c-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="98c0c-119">Debe ser uno o más de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="98c0c-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="98c0c-120">DDLWRAP_FLAG_ANSI: el objeto desempaquetado es ANSI.</span><span class="sxs-lookup"><span data-stu-id="98c0c-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="98c0c-121">DDLWRAP_FLAG_UNICODE: el objeto desempaquetado es uniCODE.</span><span class="sxs-lookup"><span data-stu-id="98c0c-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="98c0c-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="98c0c-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="98c0c-123">a Marcas para el formato de carácter preferido.</span><span class="sxs-lookup"><span data-stu-id="98c0c-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="98c0c-124">Debe ser uno o más de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="98c0c-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="98c0c-125">DDLWRAP_FLAG_ANSI: el objeto ajustado se expondrá como ANSI.</span><span class="sxs-lookup"><span data-stu-id="98c0c-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="98c0c-126">DDLWRAP_FLAG_UNICODE: el objeto ajustado se expondrá como uniCODE.</span><span class="sxs-lookup"><span data-stu-id="98c0c-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="98c0c-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="98c0c-127">_pIID_</span></span>
  
>  <span data-ttu-id="98c0c-128">a Identificador de la interfaz compatible con el objeto desencapsulado; establézcalo en NULL si se desconoce.</span><span class="sxs-lookup"><span data-stu-id="98c0c-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="98c0c-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="98c0c-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="98c0c-130">a Este parámetro no se usa.</span><span class="sxs-lookup"><span data-stu-id="98c0c-130">[in] This parameter is not used.</span></span> <span data-ttu-id="98c0c-131">Debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="98c0c-131">It must be NULL.</span></span> 
    
<span data-ttu-id="98c0c-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="98c0c-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="98c0c-133">a Establezca este parámetro en **true** si se debe comprobar el formato de _pvUnwrapped_ antes de ajustar; establézcalo en **false** si el objeto se debe ajustar sin comprobación.</span><span class="sxs-lookup"><span data-stu-id="98c0c-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="98c0c-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="98c0c-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="98c0c-135">contempla Un puntero al objeto solicitado, ajustado en el formato de carácter solicitado.</span><span class="sxs-lookup"><span data-stu-id="98c0c-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="98c0c-136">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="98c0c-136">Return values</span></span>

<span data-ttu-id="98c0c-137">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="98c0c-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98c0c-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98c0c-138">Remarks</span></span>

<span data-ttu-id="98c0c-139">Pasar un objeto ajustado con _fCheckWrap_ establecido en **true** dará como resultado un objeto desencapsulado.</span><span class="sxs-lookup"><span data-stu-id="98c0c-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="98c0c-140">Independientemente de si el objeto devuelto está ajustado o no, el cliente es responsable de liberar la referencia en el objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="98c0c-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="98c0c-141">Al utilizar **GetProcAddress** para buscar la dirección de esta función en MSMAPI32. dll, especifique **HrCreateNewWrappedObject @ 28** como nombre del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="98c0c-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98c0c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="98c0c-142">See also</span></span>

- [<span data-ttu-id="98c0c-143">Acerca de la capa de degradación de datos API</span><span class="sxs-lookup"><span data-stu-id="98c0c-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="98c0c-144">Constantes (API de capa de degradación de datos)</span><span class="sxs-lookup"><span data-stu-id="98c0c-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

