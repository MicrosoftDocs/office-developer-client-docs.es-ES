---
title: SEGMENTCOUNT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Devuelve el número de segmentos de línea que conforma la ruta de acceso.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326043"
---
# <a name="segmentcount-function"></a><span data-ttu-id="5d53d-103">Función SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="5d53d-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="5d53d-104">Devuelve el número de segmentos de línea que conforma la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="5d53d-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5d53d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d53d-105">Syntax</span></span>

<span data-ttu-id="5d53d-106">SEGMENTCOUNT (\* \* *pathRef* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5d53d-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5d53d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d53d-107">Parameters</span></span>

|<span data-ttu-id="5d53d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5d53d-108">**Name**</span></span>|<span data-ttu-id="5d53d-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="5d53d-109">**Required/Optional**</span></span>|<span data-ttu-id="5d53d-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5d53d-110">**Data Type**</span></span>|<span data-ttu-id="5d53d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d53d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5d53d-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="5d53d-112">_pathRef_</span></span> <br/> |<span data-ttu-id="5d53d-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5d53d-113">Required</span></span>  <br/> |<span data-ttu-id="5d53d-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="5d53d-114">**Integer**</span></span> <br/> |<span data-ttu-id="5d53d-115">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="5d53d-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5d53d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d53d-116">Return value</span></span>

<span data-ttu-id="5d53d-117">Entero</span><span class="sxs-lookup"><span data-stu-id="5d53d-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d53d-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d53d-118">Remarks</span></span>

<span data-ttu-id="5d53d-119">Los saltos de línea no se incluyen en el número total de segmentos devuelto.</span><span class="sxs-lookup"><span data-stu-id="5d53d-119">Line jumps are not included in the total number of segments returned.</span></span>
  

