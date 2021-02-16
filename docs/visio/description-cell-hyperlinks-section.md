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
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360245"
---
# <a name="description-cell-hyperlinks-section"></a><span data-ttu-id="4d82c-103">Celda Description (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="4d82c-103">Description Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="4d82c-104">Representa una cadena de texto descriptivo para un hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="4d82c-104">Represents a descriptive text string for a hyperlink.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4d82c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d82c-105">Remarks</span></span>

<span data-ttu-id="4d82c-106">Use esta celda para almacenar comentarios sobre el hipervínculo; por ejemplo, "Vínculo a nuestro sitio web de precios".</span><span class="sxs-lookup"><span data-stu-id="4d82c-106">Use this cell to store comments about the hyperlink; for example, "Link to our pricing website."</span></span>
  
<span data-ttu-id="4d82c-107">También puede usar el cuadro de diálogo **Hipervínculos** para establecer el valor de esta celda (haga clic en **Hipervínculo** en la ficha **Insertar**).</span><span class="sxs-lookup"><span data-stu-id="4d82c-107">You can also set the value of this cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="4d82c-108">Para obtener una referencia a la celda Description por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4d82c-108">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d82c-109">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4d82c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="4d82c-110">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="4d82c-110">Hyperlink.</span></span>  <span data-ttu-id="4d82c-111">*Nombre*  . Descripción donde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="4d82c-111">*Name*  .Description where Hyperlink.</span></span>  <span data-ttu-id="4d82c-112">*El*  nombre es el nombre de la fila de hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="4d82c-112">*Name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="4d82c-113">Para obtener una referencia a la celda Description por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4d82c-113">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d82c-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4d82c-114">Section index:</span></span>  <br/> |<span data-ttu-id="4d82c-115">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="4d82c-115">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="4d82c-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4d82c-116">Row index:</span></span>  <br/> |<span data-ttu-id="4d82c-117">**visRow1stHyperlink**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4d82c-117">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4d82c-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4d82c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="4d82c-119">**visHLinkDescription**</span><span class="sxs-lookup"><span data-stu-id="4d82c-119">**visHLinkDescription**</span></span> <br/> |
   

