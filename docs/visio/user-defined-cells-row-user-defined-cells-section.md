---
title: Fila User-defined Cells (Sección de celdas definidas por el usuario)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Contiene el valor y la descripción de cada celda definida por el usuario en la solución. Una forma contiene una fila User-defined Cells por cada pareja de celdas Value/Prompt definida por el usuario.
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337187"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a><span data-ttu-id="26a69-104">Fila User-defined Cells (Sección de celdas definidas por el usuario)</span><span class="sxs-lookup"><span data-stu-id="26a69-104">User-defined Cells Row (User-defined Cells Section)</span></span>

<span data-ttu-id="26a69-p102">Contiene el valor y la descripción de cada celda definida por el usuario en la solución. Una forma contiene una fila User-defined Cells por cada pareja de celdas Value/Prompt definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="26a69-p102">Contains the value and descriptive prompt for any user-defined cells in your solution. A shape contains one User-defined Cells row for each user-defined Value/Prompt cell pair.</span></span>
  
<span data-ttu-id="26a69-107">Las filas User-defined Cells se denominan User.</span><span class="sxs-lookup"><span data-stu-id="26a69-107">User-defined Cells rows are named User.</span></span> <span data-ttu-id="26a69-108">*nombre* y contienen las celdas siguientes.</span><span class="sxs-lookup"><span data-stu-id="26a69-108">*name*  and contain the following cells.</span></span> <span data-ttu-id="26a69-109">Para obtener más detalles, vea los temas de Ayuda acerca de la celda específica.</span><span class="sxs-lookup"><span data-stu-id="26a69-109">For more details, see the specific cell topics.</span></span> 
  
|<span data-ttu-id="26a69-110">**Cell**</span><span class="sxs-lookup"><span data-stu-id="26a69-110">**Cell**</span></span>|<span data-ttu-id="26a69-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26a69-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26a69-112">Valor</span><span class="sxs-lookup"><span data-stu-id="26a69-112">Value</span></span>](value-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="26a69-113">Especifica un valor para la correspondiente celda definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="26a69-113">Specifies a value for the corresponding user-defined cell.</span></span>  <br/> |
|[<span data-ttu-id="26a69-114">Prompt</span><span class="sxs-lookup"><span data-stu-id="26a69-114">Prompt</span></span>](prompt-cell-user-defined-cells-section.md) <br/> |<span data-ttu-id="26a69-115">Especifica un mensaje o comentario descriptivo para la celda definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="26a69-115">Specifies a descriptive prompt or comment for the user-defined cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26a69-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26a69-116">Remarks</span></span>

<span data-ttu-id="26a69-p104">Las celdas definidas por el usuario se pueden utilizar para escribir fórmulas y constantes a las que hacen referencia otras celdas y herramientas complementarias. Los valores de las celdas definidas por el usuario son portátiles; es decir, si una fórmula que hace referencia a una celda definida por el usuario de una forma se copia en otra forma que no tiene la misma celda definida por el usuario, la celda se agrega a la forma.</span><span class="sxs-lookup"><span data-stu-id="26a69-p104">User-defined cells can be used for entering formulas or constants that are referred to by other cells or add-ons. Values in user-defined cells are portable, that is, if a shape that refers to a user-defined cell in one shape is copied to another shape that does not have the same user-defined cell, the cell is added to the shape.</span></span>
  
 <span data-ttu-id="26a69-119">Puede agregar tantas filas User.</span><span class="sxs-lookup"><span data-stu-id="26a69-119">You can add as many User.</span></span>  <span data-ttu-id="26a69-120">Asigne un *nombre* a las filas que necesite, asigne nombres descriptivos a las filas y establezca los valores de las celdas.</span><span class="sxs-lookup"><span data-stu-id="26a69-120">*name*  rows as you need, assign meaningful names to the rows, and set cell values.</span></span> <span data-ttu-id="26a69-121">Para agregar una fila a una sección existente de celdas definidas por el usuario, haga clic con el botón secundario en una fila y, después, haga clic en **Insertar fila** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="26a69-121">To add a row to an existing User-defined Cells section, right-click a row and click **Insert Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="26a69-122">Puede hacer referencia a estas celdas por su nombre de fila, que aparece en la ventana ShapeSheet como texto en color rojo.</span><span class="sxs-lookup"><span data-stu-id="26a69-122">You can reference these cells by their row name, which appears in a ShapeSheet window in red text.</span></span> <span data-ttu-id="26a69-123">Para asignar un nombre descriptivo a una fila User.</span><span class="sxs-lookup"><span data-stu-id="26a69-123">To assign meaningful names to User.</span></span> <span data-ttu-id="26a69-124">*nombre* filas, haga clic en la fila y, a continuación, escriba un nombre como *desplazamiento* , por ejemplo, para crear el nombre de fila User. offset.</span><span class="sxs-lookup"><span data-stu-id="26a69-124">*name*  rows, click the row, and then type a name such as  *Offset*  , for example, to create the row name User.Offset.</span></span> <span data-ttu-id="26a69-125">Después, podrá hacer referencia a la celda Prompt usando User.Desplazamiento.Prompt.</span><span class="sxs-lookup"><span data-stu-id="26a69-125">You can then reference the Prompt cell using User.Offset.Prompt.</span></span> 
  
<span data-ttu-id="26a69-126">El nombre de fila que escriba debe ser único en la sección.</span><span class="sxs-lookup"><span data-stu-id="26a69-126">The row name you enter must be unique within the section.</span></span>
  

