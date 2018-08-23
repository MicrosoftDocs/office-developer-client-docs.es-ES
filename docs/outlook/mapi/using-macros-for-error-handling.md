---
title: Uso de macros para el control de errores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567128"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="91509-103">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="91509-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="91509-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91509-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91509-105">Hay varias macros para hacer que sea más fácil trabajar con los valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="91509-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="91509-106">Hay dos conjuntos de las macros que pruebas en busca de éxito o fracaso: HR_SUCCEEDED y HR_FAILED y SUCCEEDED y error.</span><span class="sxs-lookup"><span data-stu-id="91509-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="91509-107">Se ha realizado correctamente es que el mismo que HR_SUCCEEDED y error es el mismo que HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="91509-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="91509-108">En este caso, use la macro **ResultFromScode** para establecer la variable HRESULT el valor HRESULT correspondiente para S_OK.</span><span class="sxs-lookup"><span data-stu-id="91509-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="91509-109">Las macros usadas con más frecuencia se describen brevemente en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="91509-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="91509-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="91509-110">**Macro**</span></span>|<span data-ttu-id="91509-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="91509-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="91509-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="91509-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="91509-113">Construye un HRESULT de sus componentes.</span><span class="sxs-lookup"><span data-stu-id="91509-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="91509-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="91509-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="91509-115">Comprueba un HRESULT para un éxito o condición de advertencia.</span><span class="sxs-lookup"><span data-stu-id="91509-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="91509-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="91509-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="91509-117">Pruebas de un HRESULT para una condición de error.</span><span class="sxs-lookup"><span data-stu-id="91509-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="91509-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="91509-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="91509-119">Extrae la parte de código de error de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="91509-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="91509-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="91509-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="91509-121">Extrae las instalaciones de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="91509-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="91509-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="91509-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="91509-123">Extrae el bit de gravedad de la gravedad.</span><span class="sxs-lookup"><span data-stu-id="91509-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="91509-124">**SE HA REALIZADO CORRECTAMENTE**</span><span class="sxs-lookup"><span data-stu-id="91509-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="91509-125">Comprueba un HRESULT para un éxito o condición de advertencia.</span><span class="sxs-lookup"><span data-stu-id="91509-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="91509-126">**NO SE PUDO**</span><span class="sxs-lookup"><span data-stu-id="91509-126">**FAILED**</span></span> <br/> |<span data-ttu-id="91509-127">Pruebas de un HRESULT para una condición de error.</span><span class="sxs-lookup"><span data-stu-id="91509-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

