---
title: GETREF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Hace referencia a una celda y no recalcula la fórmula cuando cambia de la celda que se hace referencia.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822224"
---
# <a name="getref-function"></a><span data-ttu-id="5bcf2-103">GETREF (función)</span><span class="sxs-lookup"><span data-stu-id="5bcf2-103">GETREF Function</span></span>

<span data-ttu-id="5bcf2-104">Hace referencia a una celda y no recalcula la fórmula cuando cambia de la celda que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="5bcf2-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5bcf2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bcf2-105">Syntax</span></span>

<span data-ttu-id="5bcf2-106">GETREF (** *nombreDeCelda* **)</span><span class="sxs-lookup"><span data-stu-id="5bcf2-106">GETREF(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5bcf2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bcf2-107">Parameters</span></span>

|<span data-ttu-id="5bcf2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5bcf2-108">**Name**</span></span>|<span data-ttu-id="5bcf2-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="5bcf2-109">**Required/Optional**</span></span>|<span data-ttu-id="5bcf2-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="5bcf2-110">**Data Type**</span></span>|<span data-ttu-id="5bcf2-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bcf2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5bcf2-112">_nombreDeCelda_</span><span class="sxs-lookup"><span data-stu-id="5bcf2-112">_cellname_</span></span> <br/> |<span data-ttu-id="5bcf2-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="5bcf2-113">Required</span></span>  <br/> |<span data-ttu-id="5bcf2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5bcf2-114">**String**</span></span> <br/> |<span data-ttu-id="5bcf2-115">El nombre de la celda para obtener una referencia a.</span><span class="sxs-lookup"><span data-stu-id="5bcf2-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="5bcf2-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5bcf2-116">Example</span></span>

<span data-ttu-id="5bcf2-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="5bcf2-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="5bcf2-118">Establece el valor 5,1 en la fórmula de la celda PinX.</span><span class="sxs-lookup"><span data-stu-id="5bcf2-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

