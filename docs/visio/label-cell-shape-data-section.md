---
title: Celda Label (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Especifica la etiqueta que se muestra a los usuarios en la ventana Datos de formas. Una etiqueta está compuesta de caracteres alfanuméricos, incluido el carácter de subrayado (_).
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420181"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="c45d9-104">Celda Label (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="c45d9-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="c45d9-p102">Especifica la etiqueta que se muestra a los usuarios en la ventana **Datos de formas**. Una etiqueta está compuesta de caracteres alfanuméricos, incluido el carácter de subrayado (_).</span><span class="sxs-lookup"><span data-stu-id="c45d9-p102">Specifies the label that appears to users in the **Shape Data** window. A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c45d9-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c45d9-107">Remarks</span></span>

<span data-ttu-id="c45d9-108">La aplicación encierra automáticamente la cadena Label entre comillas en la celda, aunque las comillas no se muestran en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="c45d9-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="c45d9-109">Si no encuentra ningún texto de etiqueta, Visio muestra el nombre de fila (Prop.Row) en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="c45d9-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="c45d9-110">Para obtener una referencia a la celda Label por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c45d9-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c45d9-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c45d9-111">Cell name:</span></span>  <br/> |<span data-ttu-id="c45d9-112">Prop. *Name*  . Etiqueta donde Prop.  *Name*  es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="c45d9-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="c45d9-113">Para obtener una referencia desde un programa a la celda Label por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c45d9-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c45d9-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c45d9-114">Section index:</span></span>  <br/> |<span data-ttu-id="c45d9-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="c45d9-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="c45d9-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c45d9-116">Row index:</span></span>  <br/> |<span data-ttu-id="c45d9-117">**visRowProp**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c45d9-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c45d9-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c45d9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c45d9-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="c45d9-119">**visCustPropsLabel**</span></span> <br/> |
   

