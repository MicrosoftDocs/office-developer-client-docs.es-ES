---
title: Control de errores en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287286"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="437ee-103">Control de errores en MAPI</span><span class="sxs-lookup"><span data-stu-id="437ee-103">Error handling in MAPI</span></span>

<span data-ttu-id="437ee-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="437ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="437ee-105">Los valores correctos, de advertencia y de error se devuelven con un número de 32 bits conocido como identificador de resultados o HRESULT.</span><span class="sxs-lookup"><span data-stu-id="437ee-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="437ee-106">Un HRESULT no es realmente un controlador para nada; es simplemente un valor de 32 bits con varios campos codificados en el valor.</span><span class="sxs-lookup"><span data-stu-id="437ee-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="437ee-107">Un resultado cero indica el éxito y un resultado distinto de cero indica un error.</span><span class="sxs-lookup"><span data-stu-id="437ee-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="437ee-108">MAPI en plataformas de 32 bits funciona únicamente con valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="437ee-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="437ee-109">En la siguiente ilustración se muestra el formato HRESULT para plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="437ee-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="437ee-110">**Formato de HRESULT**</span><span class="sxs-lookup"><span data-stu-id="437ee-110">**HRESULT format**</span></span>
  
<span data-ttu-id="437ee-111">![Formato HRESULT formato](media/amapi_49.gif "HRESULT")</span><span class="sxs-lookup"><span data-stu-id="437ee-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="437ee-112">El bit de orden alto en el HRESULT indica si el valor devuelto representa el éxito o el error.</span><span class="sxs-lookup"><span data-stu-id="437ee-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="437ee-113">Si se establece en cero, el valor indica que se ha hecho correctamente.</span><span class="sxs-lookup"><span data-stu-id="437ee-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="437ee-114">Si se establece en 1, indica un error.</span><span class="sxs-lookup"><span data-stu-id="437ee-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="437ee-115">Los bits R, C, N y r están reservados en el HRESULT.</span><span class="sxs-lookup"><span data-stu-id="437ee-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="437ee-116">El campo de instalación en ambas versiones indica el área de responsabilidad del error.</span><span class="sxs-lookup"><span data-stu-id="437ee-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="437ee-117">Hay varias instalaciones, pero la gran mayoría de los errores MAPI usan FACILITY_ITF para representar errores de interfaz.</span><span class="sxs-lookup"><span data-stu-id="437ee-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="437ee-118">Las instalaciones más comunes que se usan actualmente son: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC y FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="437ee-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="437ee-119">Si son necesarias nuevas instalaciones, Microsoft las asigna porque deben ser únicas.</span><span class="sxs-lookup"><span data-stu-id="437ee-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="437ee-120">En la tabla siguiente se describen los distintos campos de instalación.</span><span class="sxs-lookup"><span data-stu-id="437ee-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="437ee-121">Facility</span><span class="sxs-lookup"><span data-stu-id="437ee-121">Facility</span></span>|<span data-ttu-id="437ee-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="437ee-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="437ee-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="437ee-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="437ee-124">Para códigos de estado comunes aplicables ampliamente, como S_OK o E_OUTOF_MEMORY; el valor es cero.</span><span class="sxs-lookup"><span data-stu-id="437ee-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="437ee-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="437ee-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="437ee-126">Para la mayoría de los códigos de estado devueltos desde métodos de interfaz; el valor se define mediante la interfaz.</span><span class="sxs-lookup"><span data-stu-id="437ee-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="437ee-127">Es decir, dos valores HRESULT con exactamente el mismo valor de 32 bits devuelto de dos interfaces diferentes pueden tener significados diferentes.</span><span class="sxs-lookup"><span data-stu-id="437ee-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="437ee-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="437ee-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="437ee-129">Para errores de interfaz [IDispatch de enlace](https://msdn.microsoft.com/library/ms221608.aspx) tardío.</span><span class="sxs-lookup"><span data-stu-id="437ee-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="437ee-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="437ee-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="437ee-131">Para los códigos de estado devueltos de llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="437ee-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="437ee-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="437ee-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="437ee-133">Para los códigos de estado devueltos de llamadas de [método IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) [o IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relacionadas con el almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="437ee-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="437ee-134">Los códigos de estado con valores de código (16 bits inferiores) en el intervalo de códigos de error de Windows (es decir, menos de 256) tienen el mismo significado que los errores de Windows correspondientes.</span><span class="sxs-lookup"><span data-stu-id="437ee-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="437ee-135">El campo de código es un número único que se asigna para representar el error o advertencia.</span><span class="sxs-lookup"><span data-stu-id="437ee-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

