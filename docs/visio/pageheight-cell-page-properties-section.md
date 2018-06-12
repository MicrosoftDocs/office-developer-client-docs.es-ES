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
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822709"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="2161c-103">Celda PageHeight (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="2161c-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="2161c-104">Contiene el alto de la página impresa en las unidades de dibujo.</span><span class="sxs-lookup"><span data-stu-id="2161c-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2161c-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2161c-105">Remarks</span></span>

<span data-ttu-id="2161c-106">También puede establecer el alto de página en la ficha **Tamaño de página** del cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ), o por cambiar manualmente el tamaño de la página con el mouse.</span><span class="sxs-lookup"><span data-stu-id="2161c-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="2161c-107">Para obtener una referencia a la celda PageHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="2161c-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2161c-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="2161c-108">Cell name:</span></span>  <br/> |<span data-ttu-id="2161c-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="2161c-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="2161c-110">Para obtener una referencia a la celda PageHeight por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2161c-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2161c-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="2161c-111">Section index:</span></span>  <br/> |<span data-ttu-id="2161c-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2161c-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2161c-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="2161c-113">Row index:</span></span>  <br/> |<span data-ttu-id="2161c-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="2161c-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="2161c-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="2161c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="2161c-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="2161c-116">**visPageHeight**</span></span> <br/> |
   

