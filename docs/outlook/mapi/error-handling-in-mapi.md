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
ms.openlocfilehash: 6f0ebd2112b65140a106a1376896f6de9c00da1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816767"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="65479-103">Control de errores en MAPI</span><span class="sxs-lookup"><span data-stu-id="65479-103">Error handling in MAPI</span></span>

<span data-ttu-id="65479-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65479-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65479-105">Devuelve valores de éxito, error y advertencia usando un número de 32 bits conocido como resultado controlador o HRESULT.</span><span class="sxs-lookup"><span data-stu-id="65479-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="65479-106">Un HRESULT realmente no es un identificador de nada; es simplemente un valor de 32 bits con varios campos codificado en el valor.</span><span class="sxs-lookup"><span data-stu-id="65479-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="65479-107">Un resultado de cero indica éxito y un resultado distinto de cero indica un error.</span><span class="sxs-lookup"><span data-stu-id="65479-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="65479-108">MAPI en plataformas de 32 bits funciona únicamente con valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="65479-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="65479-109">En la siguiente ilustración muestra el formato HRESULT para plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="65479-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="65479-110">**Formato de HRESULT**</span><span class="sxs-lookup"><span data-stu-id="65479-110">**HRESULT format**</span></span>
  
<span data-ttu-id="65479-111">![Formato HRESULT] (media/amapi_49.gif "Formato HRESULT")</span><span class="sxs-lookup"><span data-stu-id="65479-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="65479-112">El bit de orden superior en el HRESULT indica si el valor devuelto representa el éxito o el fracaso.</span><span class="sxs-lookup"><span data-stu-id="65479-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="65479-113">Si se establece en cero, el valor indica éxito.</span><span class="sxs-lookup"><span data-stu-id="65479-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="65479-114">Si se establece en 1, indica un error.</span><span class="sxs-lookup"><span data-stu-id="65479-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="65479-115">La R, C, N y r bits están reservados en el valor de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="65479-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="65479-116">El campo de instalaciones en ambas versiones indica el área de responsabilidad para el error.</span><span class="sxs-lookup"><span data-stu-id="65479-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="65479-117">Existen varias funciones, pero la mayoría de los errores de MAPI utilizar FACILITY_ITF para representar errores de interfaz.</span><span class="sxs-lookup"><span data-stu-id="65479-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="65479-118">Las instalaciones más comunes que se usan actualmente son: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC y FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="65479-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="65479-119">Si son necesarias nuevas instalaciones, Microsoft les asigna porque deben ser únicos.</span><span class="sxs-lookup"><span data-stu-id="65479-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="65479-120">En la siguiente tabla se describe los diferentes campos de instalaciones.</span><span class="sxs-lookup"><span data-stu-id="65479-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="65479-121">Instalaciones</span><span class="sxs-lookup"><span data-stu-id="65479-121">Facility</span></span>|<span data-ttu-id="65479-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="65479-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="65479-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="65479-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="65479-124">Para los códigos de estado comunes aplicables a grandes rasgos como S_OK o E_OUTOF_MEMORY; el valor es cero.</span><span class="sxs-lookup"><span data-stu-id="65479-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="65479-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="65479-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="65479-126">Para la mayoría de los códigos estado devuelta desde los métodos de interfaz; el valor está definido por la interfaz.</span><span class="sxs-lookup"><span data-stu-id="65479-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="65479-127">Es decir, dos valores HRESULT con exactamente el mismo valor de 32 bits devuelto desde dos interfaces diferentes pueden tener diferentes significados.</span><span class="sxs-lookup"><span data-stu-id="65479-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="65479-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="65479-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="65479-129">Errores de interfaz del enlace en [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) .</span><span class="sxs-lookup"><span data-stu-id="65479-129">For late binding [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="65479-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="65479-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="65479-131">Para los códigos de estado devueltos por llamadas a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="65479-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="65479-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="65479-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="65479-133">Para los códigos de estado devueltos desde [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) o [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) llamadas al método relacionada con el almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="65479-133">For status codes returned from [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) or [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="65479-134">Códigos de estado con los valores de código (16 bits inferiores) de los códigos de error de Windows (es decir, menos de 256) tienen el mismo significado que los errores de Windows correspondientes.</span><span class="sxs-lookup"><span data-stu-id="65479-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="65479-135">El campo de código es un número único que se asigna para representar el error o la advertencia.</span><span class="sxs-lookup"><span data-stu-id="65479-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

