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
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823459"
---
# <a name="type-cell-text-fields-section"></a><span data-ttu-id="07052-103">Celda Type (Sección de campos de texto)</span><span class="sxs-lookup"><span data-stu-id="07052-103">Type Cell (Text Fields Section)</span></span>

<span data-ttu-id="07052-104">Especifica un tipo de datos para el valor del campo de texto.</span><span class="sxs-lookup"><span data-stu-id="07052-104">Specifies a data type for the text field value.</span></span>
  
|<span data-ttu-id="07052-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="07052-105">**Value**</span></span>|<span data-ttu-id="07052-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07052-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07052-107">0</span><span class="sxs-lookup"><span data-stu-id="07052-107">0</span></span>  <br/> |<span data-ttu-id="07052-108">Cadena.</span><span class="sxs-lookup"><span data-stu-id="07052-108">String.</span></span>  <br/> |
|<span data-ttu-id="07052-109">2</span><span class="sxs-lookup"><span data-stu-id="07052-109">2</span></span>  <br/> |<span data-ttu-id="07052-p101">Número. Incluye los valores de fecha, hora, duración y moneda, así como escalares, dimensiones y ángulos. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="07052-p101">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="07052-113">5</span><span class="sxs-lookup"><span data-stu-id="07052-113">5</span></span>  <br/> |<span data-ttu-id="07052-p102">Valor de fecha u hora. Muestra días, meses y años; o segundos, minutos y horas; o un valor combinado de fecha y hora. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="07052-p102">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="07052-117">6</span><span class="sxs-lookup"><span data-stu-id="07052-117">6</span></span>  <br/> |<span data-ttu-id="07052-p103">Valor de duración. Muestra el tiempo transcurrido. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="07052-p103">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |
|<span data-ttu-id="07052-121">7</span><span class="sxs-lookup"><span data-stu-id="07052-121">7</span></span>  <br/> |<span data-ttu-id="07052-p104">Valor de moneda. Utiliza la configuración regional actual del sistema. Especifique una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="07052-p104">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07052-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07052-125">Remarks</span></span>

<span data-ttu-id="07052-126">También puede establecer el valor de esta celda mediante el cuadro de diálogo **campo** (con una forma seleccionada, en la ficha **Insertar** , en el grupo **texto** , haga clic en **campo** ).</span><span class="sxs-lookup"><span data-stu-id="07052-126">You can also set the value of this cell using the **Field** dialog box (with a shape selected, on the **Insert** tab, in the **Text** group, click **Field** ).</span></span> 
  
<span data-ttu-id="07052-127">Para obtener una referencia a la celda Type por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="07052-127">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07052-128">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="07052-128">Cell name:</span></span>  <br/> |<span data-ttu-id="07052-129">Fields.Type [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="07052-129">Fields.Type[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="07052-130">Para obtener una referencia a la celda Type por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="07052-130">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07052-131">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="07052-131">Section index:</span></span>  <br/> |<span data-ttu-id="07052-132">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="07052-132">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="07052-133">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="07052-133">Row index:</span></span>  <br/> |<span data-ttu-id="07052-134">**visRowField** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="07052-134">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="07052-135">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="07052-135">Cell index:</span></span>  <br/> |<span data-ttu-id="07052-136">**visFieldType**</span><span class="sxs-lookup"><span data-stu-id="07052-136">**visFieldType**</span></span> <br/> |
   

