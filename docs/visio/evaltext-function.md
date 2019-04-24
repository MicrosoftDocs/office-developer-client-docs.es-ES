---
title: EVALTEXT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Evalúa el texto en nombredeforma como si fuera una fórmula y devuelve el resultado.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329053"
---
# <a name="evaltext-function"></a><span data-ttu-id="643ac-103">Función EVALTEXT</span><span class="sxs-lookup"><span data-stu-id="643ac-103">EVALTEXT Function</span></span>

<span data-ttu-id="643ac-104">Evalúa el texto en _nombredeforma_ como si fuera una fórmula y devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="643ac-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="643ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="643ac-105">Syntax</span></span>

<span data-ttu-id="643ac-106">EVALTEXT (\* \* *nombredeforma! el texto* \* \*)</span><span class="sxs-lookup"><span data-stu-id="643ac-106">EVALTEXT(\*\* *shapename!theText* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="643ac-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="643ac-107">Parameters</span></span>

|<span data-ttu-id="643ac-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="643ac-108">**Name**</span></span>|<span data-ttu-id="643ac-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="643ac-109">**Required/Optional**</span></span>|<span data-ttu-id="643ac-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="643ac-110">**Data Type**</span></span>|<span data-ttu-id="643ac-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="643ac-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="643ac-112">_nombredeforma! TheText_</span><span class="sxs-lookup"><span data-stu-id="643ac-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="643ac-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="643ac-113">Required</span></span>  <br/> |<span data-ttu-id="643ac-114">**String**</span><span class="sxs-lookup"><span data-stu-id="643ac-114">**String**</span></span> <br/> |<span data-ttu-id="643ac-115">Una celda que se desencadena cuando cambia la composición texto de la forma asociada.</span><span class="sxs-lookup"><span data-stu-id="643ac-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="643ac-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="643ac-116">Return value</span></span>

<span data-ttu-id="643ac-117">String</span><span class="sxs-lookup"><span data-stu-id="643ac-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="643ac-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="643ac-118">Remarks</span></span>

 <span data-ttu-id="643ac-119">_nombreDeForma_ se puede usar para hacer referencia al texto de una forma que no es la actual.</span><span class="sxs-lookup"><span data-stu-id="643ac-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="643ac-120">Si no hay ningún texto, el resultado es cero.</span><span class="sxs-lookup"><span data-stu-id="643ac-120">If there is no text, the result is zero.</span></span> <span data-ttu-id="643ac-121">Si el texto no se puede evaluar, la función devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="643ac-121">If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="643ac-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="643ac-122">Example</span></span>

<span data-ttu-id="643ac-123">EVALTEXT (line. 2! TheText)</span><span class="sxs-lookup"><span data-stu-id="643ac-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="643ac-p102">Evalúa el texto que contiene la forma Línea.2. Por ejemplo, si Línea.2 contiene "4 cm + 0,5 cm", devuelve el valor 4,5 cm.</span><span class="sxs-lookup"><span data-stu-id="643ac-p102">Evaluates the text contained in the shape Line.2. For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

