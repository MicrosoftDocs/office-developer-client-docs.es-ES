---
title: Celda RotateGradientWithShape (Sección de propiedades de degradado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Determina si un degradado de relleno gira con una forma en rotación 2D, como un valor booleano.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412222"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="f742e-103">Celda RotateGradientWithShape (Sección de propiedades de degradado)</span><span class="sxs-lookup"><span data-stu-id="f742e-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="f742e-104">Determina si un degradado de relleno gira con una forma en rotación 2D, como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="f742e-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="f742e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f742e-105">**Value**</span></span>|<span data-ttu-id="f742e-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f742e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f742e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f742e-107">TRUE</span></span>  <br/> |<span data-ttu-id="f742e-108">El degradado gira con la forma cuando la forma gira alrededor del eje de rotación.</span><span class="sxs-lookup"><span data-stu-id="f742e-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="f742e-109">La "parte superior" del degradado es paralela al controlador de rotación.</span><span class="sxs-lookup"><span data-stu-id="f742e-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="f742e-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="f742e-110">FALSE</span></span>  <br/> |<span data-ttu-id="f742e-111">El degradado no gira con la forma cuando la forma gira alrededor del eje de rotación.</span><span class="sxs-lookup"><span data-stu-id="f742e-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="f742e-112">La "parte superior" del degradado es paralela al lienzo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="f742e-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f742e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f742e-113">Remarks</span></span>

<span data-ttu-id="f742e-114">Para obtener una referencia a la celda **RotateGradientWithShape** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="f742e-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f742e-115">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="f742e-115">Cell name:</span></span>  <br/> | <span data-ttu-id="f742e-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="f742e-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="f742e-117">Para obtener una referencia desde un programa a **la celda RotateGradientWithShape** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="f742e-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f742e-118">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="f742e-118">Section index:</span></span>  <br/> |<span data-ttu-id="f742e-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f742e-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f742e-120">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="f742e-120">Row index:</span></span>  <br/> |<span data-ttu-id="f742e-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="f742e-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="f742e-122">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="f742e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f742e-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="f742e-123">**visRotateGradientWithShape**</span></span> <br/> |
   

