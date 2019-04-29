---
title: Función LANGUAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite realizar operaciones de comparación entre distintas representaciones del idioma. Se recomienda usar para convertir los valores de las etiquetas de idioma de Internet Engineering Task Force (BCP 47) a valores de identificador de configuración regional (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424759"
---
# <a name="language-function"></a><span data-ttu-id="ce79d-104">Función LANGUAGE</span><span class="sxs-lookup"><span data-stu-id="ce79d-104">LANGUAGE Function</span></span>

<span data-ttu-id="ce79d-105">Permite realizar operaciones de comparación entre distintas representaciones del idioma.</span><span class="sxs-lookup"><span data-stu-id="ce79d-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="ce79d-106">Se recomienda usar para convertir los valores de las etiquetas de idioma de Internet Engineering Task Force (BCP 47) a valores de identificador de configuración regional (LCID).</span><span class="sxs-lookup"><span data-stu-id="ce79d-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="ce79d-107">Información de versiones</span><span class="sxs-lookup"><span data-stu-id="ce79d-107">Version Information</span></span>

<span data-ttu-id="ce79d-108">Versión añadida: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="ce79d-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ce79d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce79d-109">Syntax</span></span>

 <span data-ttu-id="ce79d-110">**Idioma** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="ce79d-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="ce79d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce79d-111">Parameters</span></span>

|<span data-ttu-id="ce79d-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="ce79d-112">**Name**</span></span>|<span data-ttu-id="ce79d-113">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="ce79d-113">**Required/Optional**</span></span>|<span data-ttu-id="ce79d-114">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="ce79d-114">**Data Type**</span></span>|<span data-ttu-id="ce79d-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce79d-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ce79d-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="ce79d-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="ce79d-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ce79d-117">Required</span></span>  <br/> |<span data-ttu-id="ce79d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ce79d-118">**String**</span></span> <br/> |<span data-ttu-id="ce79d-119">El valor LCID o BCP 47 para el idioma.</span><span class="sxs-lookup"><span data-stu-id="ce79d-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="ce79d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce79d-120">Return value</span></span>

<span data-ttu-id="ce79d-121">Entero</span><span class="sxs-lookup"><span data-stu-id="ce79d-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="ce79d-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce79d-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="ce79d-123">Devuelve un valor de ' 1033 '.</span><span class="sxs-lookup"><span data-stu-id="ce79d-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="ce79d-124">Devuelve un valor de ' 3082 '.</span><span class="sxs-lookup"><span data-stu-id="ce79d-124">Returns a value of '3082'.</span></span>
  

