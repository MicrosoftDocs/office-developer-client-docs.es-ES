---
title: Celda Ask (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Determina si se le pide al usuario que especifique los datos de formas cuando crea una instancia o cuando duplica o copia la forma.
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821524"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="51f7f-103">Celda Ask (sección Datos de formas)</span><span class="sxs-lookup"><span data-stu-id="51f7f-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="51f7f-104">Determina si se le pide al usuario que especifique los datos de formas cuando crea una instancia o cuando duplica o copia la forma.</span><span class="sxs-lookup"><span data-stu-id="51f7f-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="51f7f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="51f7f-105">**Value**</span></span>|<span data-ttu-id="51f7f-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="51f7f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51f7f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="51f7f-107">TRUE</span></span>  <br/> |<span data-ttu-id="51f7f-108">
          Se pide al usuario que especifique los datos de formas en el cuadro de diálogo **Definir datos de formas**.
</span><span class="sxs-lookup"><span data-stu-id="51f7f-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="51f7f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="51f7f-109">FALSE</span></span>  <br/> |<span data-ttu-id="51f7f-110">
          No se le pide al usuario que especifique datos.
</span><span class="sxs-lookup"><span data-stu-id="51f7f-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51f7f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51f7f-111">Remarks</span></span>

<span data-ttu-id="51f7f-112">El valor de esta celda corresponde a la casilla **Preguntar al colocar** del cuadro de diálogo **Definir datos de formas** (haga clic con el botón secundario en la forma, seleccione **Datos** y, a continuación, en **Definir datos de formas**).</span><span class="sxs-lookup"><span data-stu-id="51f7f-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="51f7f-113">Para obtener una referencia a la celda Ask por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="51f7f-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51f7f-114">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="51f7f-114">Cell name:</span></span>  <br/> |<span data-ttu-id="51f7f-115">De propiedades. *nombre* . Comprobar donde de propiedades.  *nombre* es el nombre de la fila de propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="51f7f-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="51f7f-116">Para obtener una referencia a la celda Ask por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="51f7f-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51f7f-117">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="51f7f-117">Section index:</span></span>  <br/> |<span data-ttu-id="51f7f-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="51f7f-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="51f7f-119">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="51f7f-119">Row index:</span></span>  <br/> |<span data-ttu-id="51f7f-120">**visRowProp** +  *i* donde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="51f7f-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="51f7f-121">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="51f7f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="51f7f-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="51f7f-122">**visCustPropsAsk**</span></span> <br/> |
   

