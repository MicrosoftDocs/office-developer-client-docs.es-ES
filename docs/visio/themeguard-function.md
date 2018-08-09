---
title: THEMEGUARD (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protege las celdas de formato de una forma para asegurarse de que usan los aspectos apropiados del tema actual.
ms.openlocfilehash: 10a7772995b9cc22e53ff577b2f663d7c97d0816
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823396"
---
# <a name="themeguard-function"></a><span data-ttu-id="c05dd-103">Función THEMEGUARD</span><span class="sxs-lookup"><span data-stu-id="c05dd-103">THEMEGUARD Function</span></span>

<span data-ttu-id="c05dd-104">Protege las celdas de formato de una forma para asegurarse de que usan los aspectos apropiados del tema actual.</span><span class="sxs-lookup"><span data-stu-id="c05dd-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c05dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c05dd-105">Syntax</span></span>

<span data-ttu-id="c05dd-106">THEMEGUARD()</span><span class="sxs-lookup"><span data-stu-id="c05dd-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c05dd-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c05dd-107">Remarks</span></span>

<span data-ttu-id="c05dd-108">Aplica la función THEMEGUARD a una celda no se protege el formato manual de la misma manera que hace función aplicar la protección.</span><span class="sxs-lookup"><span data-stu-id="c05dd-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="c05dd-109">Si se aplica formato a la forma en la interfaz de usuario o mediante programación, mediante la automatización, se reemplaza la fórmula THEMEGUARD, a menos que incluya la función SETATREFEXPR en la fórmula para almacenar el valor de formato manual.</span><span class="sxs-lookup"><span data-stu-id="c05dd-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c05dd-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c05dd-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="c05dd-111">Especifica que la forma toma el color de énfasis 2 del tema actual, en vez del color de relleno principal del tema.</span><span class="sxs-lookup"><span data-stu-id="c05dd-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

