---
title: Función LANGUAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite operaciones de comparación entre diferentes representaciones de idioma. Se usa mejor para convertir los valores de etiquetas de idioma de internet Engineering Task Force (BCP 47) en valores de identificador de configuración regional (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424759"
---
# <a name="language-function"></a><span data-ttu-id="d4743-104">Función LANGUAGE</span><span class="sxs-lookup"><span data-stu-id="d4743-104">LANGUAGE Function</span></span>

<span data-ttu-id="d4743-105">Permite operaciones de comparación entre diferentes representaciones de idioma.</span><span class="sxs-lookup"><span data-stu-id="d4743-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="d4743-106">Se usa mejor para convertir los valores de etiquetas de idioma de internet Engineering Task Force (BCP 47) en valores de identificador de configuración regional (LCID).</span><span class="sxs-lookup"><span data-stu-id="d4743-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d4743-107">Información de versiones</span><span class="sxs-lookup"><span data-stu-id="d4743-107">Version Information</span></span>

<span data-ttu-id="d4743-108">Versión añadida: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="d4743-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d4743-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4743-109">Syntax</span></span>

 <span data-ttu-id="d4743-110">**LANGUAGE**( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="d4743-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="d4743-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4743-111">Parameters</span></span>

|<span data-ttu-id="d4743-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="d4743-112">**Name**</span></span>|<span data-ttu-id="d4743-113">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d4743-113">**Required/Optional**</span></span>|<span data-ttu-id="d4743-114">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="d4743-114">**Data Type**</span></span>|<span data-ttu-id="d4743-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4743-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d4743-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="d4743-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="d4743-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d4743-117">Required</span></span>  <br/> |<span data-ttu-id="d4743-118">**String**</span><span class="sxs-lookup"><span data-stu-id="d4743-118">**String**</span></span> <br/> |<span data-ttu-id="d4743-119">El valor LCID o BCP 47 para el idioma.</span><span class="sxs-lookup"><span data-stu-id="d4743-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="d4743-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4743-120">Return value</span></span>

<span data-ttu-id="d4743-121">Entero</span><span class="sxs-lookup"><span data-stu-id="d4743-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="d4743-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4743-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="d4743-123">Devuelve un valor de '1033'.</span><span class="sxs-lookup"><span data-stu-id="d4743-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="d4743-124">Devuelve un valor de '3082'.</span><span class="sxs-lookup"><span data-stu-id="d4743-124">Returns a value of '3082'.</span></span>
  

