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
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822388"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="bf322-104">Celda Label (sección Datos de formas)</span><span class="sxs-lookup"><span data-stu-id="bf322-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="bf322-p102">Especifica la etiqueta que se muestra a los usuarios en la ventana **Datos de formas**. Una etiqueta está compuesta de caracteres alfanuméricos, incluido el carácter de subrayado (_).</span><span class="sxs-lookup"><span data-stu-id="bf322-p102">Specifies the label that appears to users in the **Shape Data** window. A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bf322-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf322-107">Remarks</span></span>

<span data-ttu-id="bf322-108">La aplicación encierra automáticamente la cadena Label entre comillas en la celda, aunque las comillas no se muestran en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="bf322-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="bf322-109">Si no encuentra ningún texto de etiqueta, Visio muestra el nombre de fila (Prop.Row) en la ventana **Datos de formas**.</span><span class="sxs-lookup"><span data-stu-id="bf322-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="bf322-110">Para obtener una referencia a la celda Label por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="bf322-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf322-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bf322-111">Cell name:</span></span>  <br/> |<span data-ttu-id="bf322-112">De propiedades. *Nombre* . Etiqueta de propiedades donde.  *Nombre* es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="bf322-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="bf322-113">Para obtener una referencia desde un programa a la celda Label por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bf322-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf322-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bf322-114">Section index:</span></span>  <br/> |<span data-ttu-id="bf322-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="bf322-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="bf322-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bf322-116">Row index:</span></span>  <br/> |<span data-ttu-id="bf322-117">**visRowProp** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bf322-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="bf322-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bf322-118">Cell index:</span></span>  <br/> |<span data-ttu-id="bf322-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="bf322-119">**visCustPropsLabel**</span></span> <br/> |
   

