---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permite las operaciones de comparación entre las representaciones de idioma diferente. Mejor se utiliza para convertir los valores de etiquetas (BCP 47) de idioma de Internet Engineering Task Force en valores del identificador de (configuración regional LCID) de configuración regional.
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822429"
---
# <a name="language-function"></a><span data-ttu-id="f6d07-104">LANGUAGE Function</span><span class="sxs-lookup"><span data-stu-id="f6d07-104">LANGUAGE Function</span></span>

<span data-ttu-id="f6d07-105">Permite las operaciones de comparación entre las representaciones de idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="f6d07-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="f6d07-106">Mejor se utiliza para convertir los valores de etiquetas (BCP 47) de idioma de Internet Engineering Task Force en valores del identificador de (configuración regional LCID) de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="f6d07-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="f6d07-107">Información de versión</span><span class="sxs-lookup"><span data-stu-id="f6d07-107">Version Information</span></span>

<span data-ttu-id="f6d07-108">Versión añadida: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="f6d07-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f6d07-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6d07-109">Syntax</span></span>

 <span data-ttu-id="f6d07-110">**Idioma** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="f6d07-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="f6d07-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6d07-111">Parameters</span></span>

|<span data-ttu-id="f6d07-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6d07-112">**Name**</span></span>|<span data-ttu-id="f6d07-113">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="f6d07-113">**Required/Optional**</span></span>|<span data-ttu-id="f6d07-114">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="f6d07-114">**Data Type**</span></span>|<span data-ttu-id="f6d07-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6d07-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f6d07-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="f6d07-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="f6d07-117">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="f6d07-117">Required</span></span>  <br/> |<span data-ttu-id="f6d07-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f6d07-118">**String**</span></span> <br/> |<span data-ttu-id="f6d07-119">El valor LCID o BCP 47 para el idioma.</span><span class="sxs-lookup"><span data-stu-id="f6d07-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="f6d07-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6d07-120">Return value</span></span>

<span data-ttu-id="f6d07-121">Integer</span><span class="sxs-lookup"><span data-stu-id="f6d07-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="f6d07-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6d07-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="f6d07-123">Devuelve un valor de '1033'.</span><span class="sxs-lookup"><span data-stu-id="f6d07-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="f6d07-124">Devuelve un valor de '3082'.</span><span class="sxs-lookup"><span data-stu-id="f6d07-124">Returns a value of '3082'.</span></span>
  

