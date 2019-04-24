---
title: Celda ExtraInfo (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Representa una cadena que pasa información que se utiliza en una dirección URL, como las coordenadas de un mapa de imagen. Por ejemplo, en la celda extraInfo, x = 41&amp;y = 7specifies las coordenadas de un mapa de imagen.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357823"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="58018-104">Celda ExtraInfo (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="58018-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="58018-105">Representa una cadena que pasa información que se utiliza en una dirección URL, como las coordenadas de un mapa de imagen.</span><span class="sxs-lookup"><span data-stu-id="58018-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="58018-106">Por ejemplo, en la celda extraInfo, "x = 41&amp;y = 7" especifica las coordenadas de un mapa de imagen.</span><span class="sxs-lookup"><span data-stu-id="58018-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58018-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58018-107">Remarks</span></span>

<span data-ttu-id="58018-108">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="58018-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="58018-109">Para obtener una referencia a la celda ExtraInfo por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="58018-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58018-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="58018-110">Cell name:</span></span>  <br/> | <span data-ttu-id="58018-111">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="58018-111">Hyperlink.</span></span>  <span data-ttu-id="58018-112">*nombre* . ExtraInfo donde HYPERLINK.</span><span class="sxs-lookup"><span data-stu-id="58018-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="58018-113">*Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="58018-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="58018-114">Para obtener una referencia desde un programa a la celda ExtraInfo por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="58018-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58018-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="58018-115">Section index:</span></span>  <br/> |<span data-ttu-id="58018-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="58018-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="58018-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="58018-117">Row index:</span></span>  <br/> |<span data-ttu-id="58018-118">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="58018-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="58018-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="58018-119">Cell index:</span></span>  <br/> |<span data-ttu-id="58018-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="58018-120">**visHLinkExtraInfo**</span></span> <br/> |
   

