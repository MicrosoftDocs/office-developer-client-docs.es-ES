---
title: THEMEGUARD (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Protege las celdas de formato de una forma para garantizar que usan los aspectos apropiados del tema actual.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404949"
---
# <a name="themeguard-function"></a><span data-ttu-id="e114f-103">Función THEMEGUARD</span><span class="sxs-lookup"><span data-stu-id="e114f-103">THEMEGUARD Function</span></span>

<span data-ttu-id="e114f-104">Protege las celdas de formato de una forma para garantizar que usan los aspectos apropiados del tema actual.</span><span class="sxs-lookup"><span data-stu-id="e114f-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e114f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e114f-105">Syntax</span></span>

<span data-ttu-id="e114f-106">THEMEGUARD ()</span><span class="sxs-lookup"><span data-stu-id="e114f-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e114f-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e114f-107">Remarks</span></span>

<span data-ttu-id="e114f-108">Si se aplica la función THEMEGUARD a una celda, no se protege el formato manual de la misma forma que si se aplicase la función GUARD.</span><span class="sxs-lookup"><span data-stu-id="e114f-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="e114f-109">Si aplica formato a la forma en la interfaz de usuario o mediante programación, por medio de la automatización, se reemplaza la fórmula THEMEGUARD, a menos que incluya la función SETATREFEXPR en la fórmula para almacenar el valor de formato manual.</span><span class="sxs-lookup"><span data-stu-id="e114f-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e114f-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e114f-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="e114f-111">Especifica que la forma toma el color de énfasis 2 del tema actual, en vez del color de relleno principal del tema.</span><span class="sxs-lookup"><span data-stu-id="e114f-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

