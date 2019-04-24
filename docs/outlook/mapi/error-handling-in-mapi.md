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
# <a name="error-handling-in-mapi"></a><span data-ttu-id="09274-103">Control de errores en MAPI</span><span class="sxs-lookup"><span data-stu-id="09274-103">Error handling in MAPI</span></span>

<span data-ttu-id="09274-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09274-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09274-105">Los valores de éxito, ADVERTENCIA y error se devuelven usando un número de 32 bits conocido como controlador de resultado o HRESULT.</span><span class="sxs-lookup"><span data-stu-id="09274-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="09274-106">Un HRESULT realmente no es un identificador para nada; solo es un valor de 32 bits con varios campos codificados en el valor.</span><span class="sxs-lookup"><span data-stu-id="09274-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="09274-107">Un resultado cero indica que se ha realizado correctamente y un resultado distinto de cero indica un error.</span><span class="sxs-lookup"><span data-stu-id="09274-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="09274-108">Las plataformas MAPI en 32 bits funcionan únicamente con valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="09274-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="09274-109">En la siguiente ilustración se muestra el formato HRESULT para las plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="09274-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="09274-110">**Formato de HRESULT**</span><span class="sxs-lookup"><span data-stu-id="09274-110">**HRESULT format**</span></span>
  
<span data-ttu-id="09274-111">![Formato HRESULT] (media/amapi_49.gif "Formato HRESULT")</span><span class="sxs-lookup"><span data-stu-id="09274-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="09274-112">El bit de orden superior del HRESULT indica si el valor devuelto representa el éxito o el error.</span><span class="sxs-lookup"><span data-stu-id="09274-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="09274-113">Si se establece en cero, el valor indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="09274-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="09274-114">Si se establece en 1, indica un error.</span><span class="sxs-lookup"><span data-stu-id="09274-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="09274-115">Los bits R, C, N y r están reservados en el HRESULT.</span><span class="sxs-lookup"><span data-stu-id="09274-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="09274-116">El campo Facility de ambas versiones indica el área de responsabilidad del error.</span><span class="sxs-lookup"><span data-stu-id="09274-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="09274-117">Hay varias instalaciones, pero la gran mayoría de los errores de MAPI usan FACILITY_ITF para representar errores de interfaz.</span><span class="sxs-lookup"><span data-stu-id="09274-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="09274-118">Las funciones más comunes que se usan actualmente son: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC y FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="09274-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="09274-119">Si se necesitan nuevas instalaciones, Microsoft les asignará los usuarios, ya que deben ser únicas.</span><span class="sxs-lookup"><span data-stu-id="09274-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="09274-120">En la tabla siguiente se describen los distintos campos de instalaciones.</span><span class="sxs-lookup"><span data-stu-id="09274-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="09274-121">Facility</span><span class="sxs-lookup"><span data-stu-id="09274-121">Facility</span></span>|<span data-ttu-id="09274-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="09274-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="09274-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="09274-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="09274-124">Para los códigos de estado comunes de gran aplicación, como S_OK o E_OUTOF_MEMORY; el valor es cero.</span><span class="sxs-lookup"><span data-stu-id="09274-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="09274-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="09274-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="09274-126">Para la mayoría de los códigos de estado devueltos desde los métodos de interfaz; la interfaz define el valor.</span><span class="sxs-lookup"><span data-stu-id="09274-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="09274-127">Es decir, dos valores HRESULT con exactamente el mismo valor de 32 bits devueltos por dos interfaces diferentes pueden tener diferentes significados.</span><span class="sxs-lookup"><span data-stu-id="09274-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="09274-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="09274-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="09274-129">Para los errores de la interfaz [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) de enlace en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="09274-129">For late binding [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="09274-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="09274-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="09274-131">Para los códigos de estado devueltos de las llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="09274-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="09274-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="09274-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="09274-133">Para los códigos de estado devueltos desde las llamadas al método [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) o [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relacionadas con el almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="09274-133">For status codes returned from [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) or [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="09274-134">Los valores de códigos de estado con código (16 bits inferiores) en el intervalo de códigos de error de Windows (es decir, menos de 256) tienen el mismo significado que los errores de Windows correspondientes.</span><span class="sxs-lookup"><span data-stu-id="09274-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="09274-135">El campo Código es un número único que se asigna para representar el error o la advertencia.</span><span class="sxs-lookup"><span data-stu-id="09274-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

