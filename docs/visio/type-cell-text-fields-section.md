---
title: Celda Type (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Especifica un tipo de datos para el valor del campo de texto.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407987"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="4e52d-103">Celda Type (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="4e52d-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="4e52d-104">Especifica un tipo de datos para el valor del campo de texto.</span><span class="sxs-lookup"><span data-stu-id="4e52d-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="4e52d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4e52d-105">**Value**</span></span>|<span data-ttu-id="4e52d-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e52d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e52d-107">0</span><span class="sxs-lookup"><span data-stu-id="4e52d-107">0</span></span>  <br/> |<span data-ttu-id="4e52d-108">Cadena.</span><span class="sxs-lookup"><span data-stu-id="4e52d-108">String.</span></span>  <br/> |
|<span data-ttu-id="4e52d-109">2</span><span class="sxs-lookup"><span data-stu-id="4e52d-109">2</span></span>  <br/> |<span data-ttu-id="4e52d-p101">Número. Incluye los valores de fecha, hora, duración y moneda, así como escalares, dimensiones y ángulos. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="4e52d-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="4e52d-113">5 </span><span class="sxs-lookup"><span data-stu-id="4e52d-113">5</span></span>  <br/> |<span data-ttu-id="4e52d-p102">Valor de fecha u hora. Muestra días, meses y años; o segundos, minutos y horas; o un valor combinado de fecha y hora. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="4e52d-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="4e52d-117">6 </span><span class="sxs-lookup"><span data-stu-id="4e52d-117">6</span></span>  <br/> |<span data-ttu-id="4e52d-p103">Valor de duración. Muestra el tiempo transcurrido. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="4e52d-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="4e52d-121">7 </span><span class="sxs-lookup"><span data-stu-id="4e52d-121">7</span></span>  <br/> |<span data-ttu-id="4e52d-p104">Valor de moneda. Utiliza la configuración regional actual del sistema. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="4e52d-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e52d-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e52d-125">Remarks</span></span>

<span data-ttu-id="4e52d-126">También puede establecer el valor de  esta celda mediante el cuadro  de diálogo Campo  (con una forma seleccionada, en la ficha Insertar, en el grupo Texto, haga clic en **Campo** ).</span><span class="sxs-lookup"><span data-stu-id="4e52d-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="4e52d-127">Para obtener una referencia a la celda Type por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="4e52d-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e52d-128">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4e52d-128">Cell name:</span></span>  <br/> |<span data-ttu-id="4e52d-129">Fields.Type[ *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4e52d-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4e52d-130">Para obtener una referencia desde un programa a la celda Type por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e52d-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e52d-131">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4e52d-131">Section index:</span></span>  <br/> |<span data-ttu-id="4e52d-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="4e52d-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="4e52d-133">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4e52d-133">Row index:</span></span>  <br/> |<span data-ttu-id="4e52d-134">**visRowField**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4e52d-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4e52d-135">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4e52d-135">Cell index:</span></span>  <br/> |<span data-ttu-id="4e52d-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="4e52d-136">**visFieldType**</span></span> <br/> |
   

