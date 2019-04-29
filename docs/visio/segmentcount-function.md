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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424500"
---
# <a name="segmentcount-function"></a><span data-ttu-id="8c638-103">Función SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="8c638-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="8c638-104">Devuelve el número de segmentos de línea que conforma la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="8c638-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8c638-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c638-105">Syntax</span></span>

<span data-ttu-id="8c638-106">SEGMENTCOUNT (\* \* *pathRef* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8c638-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8c638-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c638-107">Parameters</span></span>

|<span data-ttu-id="8c638-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8c638-108">**Name**</span></span>|<span data-ttu-id="8c638-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8c638-109">**Required/Optional**</span></span>|<span data-ttu-id="8c638-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="8c638-110">**Data Type**</span></span>|<span data-ttu-id="8c638-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8c638-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8c638-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="8c638-112">_pathRef_</span></span> <br/> |<span data-ttu-id="8c638-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8c638-113">Required</span></span>  <br/> |<span data-ttu-id="8c638-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8c638-114">**Integer**</span></span> <br/> |<span data-ttu-id="8c638-115">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="8c638-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8c638-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c638-116">Return value</span></span>

<span data-ttu-id="8c638-117">Entero</span><span class="sxs-lookup"><span data-stu-id="8c638-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c638-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8c638-118">Remarks</span></span>

<span data-ttu-id="8c638-119">Los saltos de línea no se incluyen en el número total de segmentos devuelto.</span><span class="sxs-lookup"><span data-stu-id="8c638-119">Line jumps are not included in the total number of segments returned.</span></span>
  

