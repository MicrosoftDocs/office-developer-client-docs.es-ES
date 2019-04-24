---
title: THEMERESTORE (función)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Almacena el valor de formato local de una forma cuando se aplica un tema, de modo que se pueda restaurar el formato local si el usuario quita el tema posteriormente.
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332217"
---
# <a name="themerestore-function"></a><span data-ttu-id="9ba90-103">Función THEMERESTORE</span><span class="sxs-lookup"><span data-stu-id="9ba90-103">THEMERESTORE Function</span></span>

<span data-ttu-id="9ba90-104">Almacena el valor de formato local de una forma cuando se aplica un tema, de modo que se pueda restaurar el formato local si el usuario quita el tema posteriormente.</span><span class="sxs-lookup"><span data-stu-id="9ba90-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9ba90-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ba90-105">Syntax</span></span>

<span data-ttu-id="9ba90-106">THEMERESTORE ()</span><span class="sxs-lookup"><span data-stu-id="9ba90-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="9ba90-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ba90-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="9ba90-108">Restaura el formato de color de relleno local aplicado anteriormente a una forma si se elimina el tema actual.</span><span class="sxs-lookup"><span data-stu-id="9ba90-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

