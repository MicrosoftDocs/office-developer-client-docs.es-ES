---
title: TRIM (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Quita todo el espacio del texto, excepto los espacios individuales que hay entre palabras.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280846"
---
# <a name="trim-function"></a><span data-ttu-id="de825-103">Función TRIM</span><span class="sxs-lookup"><span data-stu-id="de825-103">TRIM Function</span></span>

<span data-ttu-id="de825-104">Quita todo el espacio del texto, excepto los espacios individuales que hay entre palabras.</span><span class="sxs-lookup"><span data-stu-id="de825-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="de825-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de825-105">Syntax</span></span>

<span data-ttu-id="de825-106">TRIM (\* \* *Text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="de825-106">TRIM (\*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="de825-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de825-107">Parameters</span></span>

|<span data-ttu-id="de825-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="de825-108">**Name**</span></span>|<span data-ttu-id="de825-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="de825-109">**Required/Optional**</span></span>|<span data-ttu-id="de825-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="de825-110">**Data Type**</span></span>|<span data-ttu-id="de825-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de825-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="de825-112">_text_</span><span class="sxs-lookup"><span data-stu-id="de825-112">_text_</span></span> <br/> |<span data-ttu-id="de825-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="de825-113">Required</span></span>  <br/> |<span data-ttu-id="de825-114">**String**</span><span class="sxs-lookup"><span data-stu-id="de825-114">**String**</span></span> <br/> |<span data-ttu-id="de825-115">El texto cuyos espacios se desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="de825-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="de825-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de825-116">Return value</span></span>

<span data-ttu-id="de825-117">String</span><span class="sxs-lookup"><span data-stu-id="de825-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de825-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de825-118">Remarks</span></span>

<span data-ttu-id="de825-119">La función TRIM puede ser útil para tratar el texto proveniente de otra aplicación que presente un espaciado irregular.</span><span class="sxs-lookup"><span data-stu-id="de825-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="de825-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de825-120">Example</span></span>

<span data-ttu-id="de825-121">TRIM ("1 de enero de 2003")</span><span class="sxs-lookup"><span data-stu-id="de825-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="de825-122">Devuelve "1 de enero, 2003".</span><span class="sxs-lookup"><span data-stu-id="de825-122">Returns "January 1, 2003".</span></span> 
  

