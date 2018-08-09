---
title: NEARESTPOINTONPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Devuelve el porcentaje (como un valor entre 0 y 1) de la distancia a lo largo de la ruta de acceso del punto que se encuentra más cerca de las coordenadas especificadas.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822666"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="81c23-103">Función NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="81c23-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="81c23-104">Devuelve el porcentaje (como un valor entre 0 y 1) de la distancia a lo largo de la ruta de acceso del punto que se encuentra más cerca de las coordenadas especificadas.</span><span class="sxs-lookup"><span data-stu-id="81c23-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="81c23-105">Información de versión</span><span class="sxs-lookup"><span data-stu-id="81c23-105">Version Information</span></span>

<span data-ttu-id="81c23-106">Versión añadida: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="81c23-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="81c23-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81c23-107">Syntax</span></span>

<span data-ttu-id="81c23-108">NEARESTPOINTONPATH (** *sección* **, ** *x* **, ** *y* **)</span><span class="sxs-lookup"><span data-stu-id="81c23-108">NEARESTPOINTONPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="81c23-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81c23-109">Parameters</span></span>

|<span data-ttu-id="81c23-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="81c23-110">**Name**</span></span>|<span data-ttu-id="81c23-111">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="81c23-111">**Required/Optional**</span></span>|<span data-ttu-id="81c23-112">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="81c23-112">**Data Type**</span></span>|<span data-ttu-id="81c23-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81c23-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="81c23-114">_section_</span><span class="sxs-lookup"><span data-stu-id="81c23-114">_section_</span></span> <br/> |<span data-ttu-id="81c23-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="81c23-115">Required</span></span>  <br/> |<span data-ttu-id="81c23-116">**String**</span><span class="sxs-lookup"><span data-stu-id="81c23-116">**String**</span></span> <br/> |<span data-ttu-id="81c23-117">Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="81c23-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="81c23-118">_x_</span><span class="sxs-lookup"><span data-stu-id="81c23-118">_x_</span></span> <br/> |<span data-ttu-id="81c23-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="81c23-119">Required</span></span>  <br/> |<span data-ttu-id="81c23-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="81c23-120">**Double**</span></span> <br/> |<span data-ttu-id="81c23-121">La _x_-coordenadas del punto especificado.</span><span class="sxs-lookup"><span data-stu-id="81c23-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="81c23-122">_y_</span><span class="sxs-lookup"><span data-stu-id="81c23-122">_y_</span></span> <br/> |<span data-ttu-id="81c23-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="81c23-123">Required</span></span>  <br/> |<span data-ttu-id="81c23-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="81c23-124">**Double**</span></span> <br/> |<span data-ttu-id="81c23-125">La _y_-coordenadas del punto especificado.</span><span class="sxs-lookup"><span data-stu-id="81c23-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="81c23-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81c23-126">Return value</span></span>

 <span data-ttu-id="81c23-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="81c23-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81c23-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81c23-128">Remarks</span></span>

<span data-ttu-id="81c23-129">Si la _sección_ no existe, Microsoft Visio devuelve #REF!.</span><span class="sxs-lookup"><span data-stu-id="81c23-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

