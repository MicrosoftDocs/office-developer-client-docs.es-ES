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
description: Representa una cadena que pasa información que se utiliza en una dirección URL, como las coordenadas de un mapa de imagen. Por ejemplo, en la celda ExtraInfo, x=41 &amp; y=7 especifica las coordenadas de un mapa de imágenes.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409576"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="d5f38-104">Celda ExtraInfo (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="d5f38-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="d5f38-105">Representa una cadena que pasa información que se utiliza en una dirección URL, como las coordenadas de un mapa de imagen.</span><span class="sxs-lookup"><span data-stu-id="d5f38-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="d5f38-106">Por ejemplo, en la celda ExtraInfo, "x=41 &amp; y=7" especifica las coordenadas de un mapa de imágenes.</span><span class="sxs-lookup"><span data-stu-id="d5f38-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5f38-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5f38-107">Remarks</span></span>

<span data-ttu-id="d5f38-108">Las celdas de eventos se evalúan sólo cuando se produce el evento, no al escribir la fórmula.</span><span class="sxs-lookup"><span data-stu-id="d5f38-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="d5f38-109">Para obtener una referencia a la celda ExtraInfo por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="d5f38-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d5f38-110">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="d5f38-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d5f38-111">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="d5f38-111">Hyperlink.</span></span>  <span data-ttu-id="d5f38-112">*nombre*  . ExtraInfo donde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="d5f38-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="d5f38-113">*nombre*  es el nombre de fila</span><span class="sxs-lookup"><span data-stu-id="d5f38-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d5f38-114">Para obtener una referencia desde un programa a la celda ExtraInfo por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5f38-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d5f38-115">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="d5f38-115">Section index:</span></span>  <br/> |<span data-ttu-id="d5f38-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="d5f38-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="d5f38-117">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="d5f38-117">Row index:</span></span>  <br/> |<span data-ttu-id="d5f38-118">**visRow1stHyperlink**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d5f38-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d5f38-119">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="d5f38-119">Cell index:</span></span>  <br/> |<span data-ttu-id="d5f38-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="d5f38-120">**visHLinkExtraInfo**</span></span> <br/> |
   

