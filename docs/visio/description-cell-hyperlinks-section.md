---
title: Celda Description (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Representa una cadena de texto descriptivo para un hipervínculo.
ms.openlocfilehash: 567a90b3162c109582c3149c156a994392980577
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821990"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="20403-103">Celda Description (sección Hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="20403-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="20403-104">Representa una cadena de texto descriptivo para un hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="20403-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="20403-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20403-105">Remarks</span></span>

<span data-ttu-id="20403-106">Use esta celda para guardar comentarios acerca del hipervínculo; por ejemplo "Vínculo a nuestro sitio web de precios".</span><span class="sxs-lookup"><span data-stu-id="20403-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing Web site."</span></span>
  
<span data-ttu-id="20403-107">También puede usar el cuadro de diálogo **Hipervínculos** para establecer el valor de esta celda (haga clic en **Hipervínculo** en la ficha **Insertar**).</span><span class="sxs-lookup"><span data-stu-id="20403-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="20403-108">Para obtener una referencia a la celda Description por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="20403-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20403-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="20403-109">Cell name:</span></span>  <br/> | <span data-ttu-id="20403-110">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="20403-110">Hyperlink.</span></span>  <span data-ttu-id="20403-111">*Nombre* . Descripción donde hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="20403-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="20403-112">*Nombre* es el nombre de la fila de hipervínculo</span><span class="sxs-lookup"><span data-stu-id="20403-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="20403-113">Para obtener una referencia a la celda Description por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="20403-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20403-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="20403-114">Section index:</span></span>  <br/> |<span data-ttu-id="20403-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="20403-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="20403-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="20403-116">Row index:</span></span>  <br/> |<span data-ttu-id="20403-117">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="20403-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="20403-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="20403-118">Cell index:</span></span>  <br/> |<span data-ttu-id="20403-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="20403-119">**visHLinkDescription**</span></span> <br/> |
   

