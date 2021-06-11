---
title: Celda UIVisibility (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Determina si el nombre de la página está visible en la interfaz de usuario.
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437332"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="bb561-103">Celda UIVisibility (Sección de propiedades de página)</span><span class="sxs-lookup"><span data-stu-id="bb561-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="bb561-104">Determina si el nombre de la página está visible en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bb561-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="bb561-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bb561-105">**Value**</span></span>|<span data-ttu-id="bb561-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb561-106">**Description**</span></span>|<span data-ttu-id="bb561-107">**Constante de automatización**</span><span class="sxs-lookup"><span data-stu-id="bb561-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb561-108">0</span><span class="sxs-lookup"><span data-stu-id="bb561-108">0</span></span>  <br/> |<span data-ttu-id="bb561-109">Muestra el nombre de la página en la interfaz de usuario (predeterminado).</span><span class="sxs-lookup"><span data-stu-id="bb561-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="bb561-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="bb561-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="bb561-111">1</span><span class="sxs-lookup"><span data-stu-id="bb561-111">1</span></span>  <br/> |<span data-ttu-id="bb561-112">No muestra el nombre de la página en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="bb561-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="bb561-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="bb561-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb561-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb561-114">Remarks</span></span>

<span data-ttu-id="bb561-115">Al establecer la celda UIVisibility como **visUIVHidden**, se impide que la página aparezca en cualquier lugar de la interfaz donde se muestra la cadena que contiene el nombre de la página.</span><span class="sxs-lookup"><span data-stu-id="bb561-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="bb561-116">Por ejemplo, la página no se mostraría como opción en el cuadro de diálogo Página (menú Edición, submenú Ir a), en el **Explorador de dibujos** o en las fichas de la página.</span><span class="sxs-lookup"><span data-stu-id="bb561-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="bb561-117">Sin embargo, la página sigue siendo accesible si usas rutas de acceso de automatización o de interfaz de usuario que no incluyen el nombre de página, por ejemplo, el **comando** Imprimir.</span><span class="sxs-lookup"><span data-stu-id="bb561-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="bb561-118">Esta celda está concebida para usarse con páginas de documento, y no para páginas de superposición de revisiones, cuya celda UIVisibility está establecida en **visUIVHidden** de manera predeterminada y no debe cambiarse.</span><span class="sxs-lookup"><span data-stu-id="bb561-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bb561-119">Para ocultar una página del  comando Imprimir del documento, haga que sea una página de fondo ( La propiedad **Type** es **visTypeBackground** ) que ninguna página usa como fondo (las formas de las páginas de fondo se imprimen cuando se imprime una página que la usa como fondo).</span><span class="sxs-lookup"><span data-stu-id="bb561-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="bb561-120">El comando **Imprimir** del documento solo funciona con páginas indizadas y las páginas en segundo plano no se indizan.</span><span class="sxs-lookup"><span data-stu-id="bb561-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="bb561-121">Para obtener una referencia a la celda UIVisibility por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="bb561-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb561-122">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="bb561-122">Cell name:</span></span>  <br/> |<span data-ttu-id="bb561-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="bb561-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="bb561-124">Para obtener una referencia desde un programa a la celda UIVisibility por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="bb561-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb561-125">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="bb561-125">Section index:</span></span>  <br/> |<span data-ttu-id="bb561-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bb561-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bb561-127">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="bb561-127">Row index:</span></span>  <br/> |<span data-ttu-id="bb561-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="bb561-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="bb561-129">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="bb561-129">Cell index:</span></span>  <br/> |<span data-ttu-id="bb561-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="bb561-130">**visPageUIVisibility**</span></span> <br/> |
   

