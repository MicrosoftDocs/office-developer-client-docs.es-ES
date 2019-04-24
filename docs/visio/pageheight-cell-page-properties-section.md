---
title: Celda PageHeight (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Contiene el alto de la página impresa en las unidades de dibujo.
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334352"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="09708-103">Celda PageHeight (sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="09708-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="09708-104">Contiene el alto de la página impresa en las unidades de dibujo.</span><span class="sxs-lookup"><span data-stu-id="09708-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09708-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09708-105">Remarks</span></span>

<span data-ttu-id="09708-106">También puede establecer el alto de la página en la ficha **Tamaño de página** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**) o manualmente cambiando el tamaño de la página con el mouse.</span><span class="sxs-lookup"><span data-stu-id="09708-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="09708-107">Para obtener una referencia a la celda PageHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="09708-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09708-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="09708-108">Cell name:</span></span>  <br/> |<span data-ttu-id="09708-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="09708-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="09708-110">Para obtener una referencia desde un programa a la celda PageHeight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="09708-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09708-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="09708-111">Section index:</span></span>  <br/> |<span data-ttu-id="09708-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="09708-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="09708-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="09708-113">Row index:</span></span>  <br/> |<span data-ttu-id="09708-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="09708-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="09708-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="09708-115">Cell index:</span></span>  <br/> |<span data-ttu-id="09708-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="09708-116">**visPageHeight**</span></span> <br/> |
   

