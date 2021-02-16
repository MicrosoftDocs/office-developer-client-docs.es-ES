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
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435568"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="20369-103">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="20369-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="20369-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20369-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20369-105">Hay varias macros para facilitar el trabajo con valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="20369-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="20369-106">Hay dos conjuntos de macros que prueban si hay errores o éxitos: HR_SUCCEEDED y HR_FAILED y SUCCEEDED y FAILED.</span><span class="sxs-lookup"><span data-stu-id="20369-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="20369-107">SUCCEEDED es el mismo que HR_SUCCEEDED y FAILED es el mismo que HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="20369-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="20369-108">En este caso, use la macro **ResultFromScode** para establecer la variable HRESULT en el valor HRESULT correspondiente para S_OK.</span><span class="sxs-lookup"><span data-stu-id="20369-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="20369-109">Las macros de uso frecuente se describen brevemente en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="20369-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="20369-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="20369-110">**Macro**</span></span>|<span data-ttu-id="20369-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20369-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20369-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="20369-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="20369-113">Construye un HRESULT a partir de sus componentes.</span><span class="sxs-lookup"><span data-stu-id="20369-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="20369-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="20369-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="20369-115">Prueba un HRESULT en busca de una condición de advertencia o éxito.</span><span class="sxs-lookup"><span data-stu-id="20369-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="20369-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="20369-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="20369-117">Comprueba un HRESULT en busca de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="20369-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="20369-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="20369-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="20369-119">Extrae la parte del código de error del HRESULT.</span><span class="sxs-lookup"><span data-stu-id="20369-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="20369-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="20369-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="20369-121">Extrae la instalación del HRESULT.</span><span class="sxs-lookup"><span data-stu-id="20369-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="20369-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="20369-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="20369-123">Extrae el bit de gravedad de LA GRAVEDAD.</span><span class="sxs-lookup"><span data-stu-id="20369-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="20369-124">**SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="20369-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="20369-125">Prueba un HRESULT en busca de una condición de advertencia o éxito.</span><span class="sxs-lookup"><span data-stu-id="20369-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="20369-126">**ERROR**</span><span class="sxs-lookup"><span data-stu-id="20369-126">**FAILED**</span></span> <br/> |<span data-ttu-id="20369-127">Comprueba un HRESULT en busca de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="20369-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

