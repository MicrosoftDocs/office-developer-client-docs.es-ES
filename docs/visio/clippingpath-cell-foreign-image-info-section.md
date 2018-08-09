---
title: Celda ClippingPath (sección Información de imagen externa)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ec70417-5b23-45af-95a0-1b26f6791699
description: Contiene una referencia a la geometría de la ruta de acceso que está rodeada de una imagen.
ms.openlocfilehash: 9f1c159e303c1d7bc3467c36756a422a3f325c7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821762"
---
# <a name="clippingpath-cell-foreign-image-info-section"></a><span data-ttu-id="cbaf4-103">Celda ClippingPath (sección Información de imagen externa)</span><span class="sxs-lookup"><span data-stu-id="cbaf4-103">ClippingPath Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="cbaf4-104">Contiene una referencia a la geometría de la ruta de acceso que está rodeada de una imagen.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-104">Contains a reference to the geometry of the path that an image is bounded by.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cbaf4-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cbaf4-105">Remarks</span></span>

<span data-ttu-id="cbaf4-106">Si la celda **ClippingPath** apunta a una ruta de acceso válida, la imagen se recorta para que se represente la imagen dentro de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-106">If the **ClippingPath** cell points to a valid path, the image is clipped so that the image is rendered inside of the path.</span></span> <span data-ttu-id="cbaf4-107">Si la celda **ClippingPath** está vacía o contiene una entrada no válida, la imagen se representará con un clip rectangular, usando los valores de escala y desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-107">If the **ClippingPath** cell is empty or contains an invalid entry, then the image will be rendered with a rectangular clip, using the scale and offset values.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cbaf4-108">Sólo rutas de acceso definidas por una sección de [geometría](geometry-section.md) de ShapeSheet de la imagen son las entradas válidas de la celda **ClippingPath** .</span><span class="sxs-lookup"><span data-stu-id="cbaf4-108">Only paths defined by a [Geometry](geometry-section.md) section in the image's ShapeSheet are valid entries for the **ClippingPath** cell.</span></span> <span data-ttu-id="cbaf4-109">Referencias entre hojas no se puede usar para definir una ruta de acceso de recorte de imagen.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-109">Cross-sheet references cannot be used to define an image clipping path.</span></span> 
  
<span data-ttu-id="cbaf4-110">Para obtener una referencia a la celda **ClippingPath** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="cbaf4-110">To get a reference to the **ClippingPath** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cbaf4-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="cbaf4-111">Cell name:</span></span>  <br/> | <span data-ttu-id="cbaf4-112">ClippingPath</span><span class="sxs-lookup"><span data-stu-id="cbaf4-112">ClippingPath</span></span>  <br/> |
   
<span data-ttu-id="cbaf4-113">Para obtener una referencia a la celda **ClippingPath** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbaf4-113">To get a reference to the **ClippingPath** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cbaf4-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="cbaf4-114">Section index:</span></span>  <br/> |<span data-ttu-id="cbaf4-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cbaf4-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cbaf4-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="cbaf4-116">Row index:</span></span>  <br/> |<span data-ttu-id="cbaf4-117">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="cbaf4-117">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="cbaf4-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="cbaf4-118">Cell index:</span></span>  <br/> |<span data-ttu-id="cbaf4-119">**visFrgnImgClippingPath**</span><span class="sxs-lookup"><span data-stu-id="cbaf4-119">**visFrgnImgClippingPath**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="cbaf4-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbaf4-120">Example</span></span>

<span data-ttu-id="cbaf4-121">Puede cambiar la forma de límite de una imagen a un óvalo haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbaf4-121">You can change the bounding shape of an image to an oval by doing the following:</span></span>
  
- <span data-ttu-id="cbaf4-122">Inserte la imagen en el lienzo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-122">Insert the picture onto the drawing canvas.</span></span>
    
- <span data-ttu-id="cbaf4-123">Haga clic en la imagen y, a continuación, seleccione **Mostrar ShapeSheet**.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-123">Right-click the picture and then select **Show ShapeSheet**.</span></span>
    
- <span data-ttu-id="cbaf4-124">El botón secundario en cualquier lugar de la hoja ShapeSheet y seleccione **Insertar sección**.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-124">Right-click anywhere in the ShapeSheet and select **Insert Section**.</span></span>
    
- <span data-ttu-id="cbaf4-125">En el cuadro de diálogo **Insertar sección** , seleccione la **geometría** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-125">In the **Insert Section** dialog box, select **Geometry** and then click **OK**.</span></span>
    
- <span data-ttu-id="cbaf4-126">En la sección de geometría nueva (por ejemplo, "Geometry2"), Eliminar fila todos menos uno.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-126">In the new Geometry section (e.g. "Geometry2"), delete all but one row.</span></span>
    
- <span data-ttu-id="cbaf4-127">Haga clic en la fila restante y, a continuación, haga clic en **Cambiar tipo de fila**.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-127">Right-click the remaining row and then click **Change Row Type**.</span></span>
    
- <span data-ttu-id="cbaf4-128">En el cuadro de diálogo **Cambiar tipo de fila** , seleccione **elipse** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-128">In the **Change Row Type** dialog box, select **Ellipse** and then click **OK**.</span></span>
    
- <span data-ttu-id="cbaf4-129">En la sección **Foreign Image** , establezca la fórmula de la celda **ClippingPath** a `="Geometry2.Path"` y, a continuación, acepte la fórmula.</span><span class="sxs-lookup"><span data-stu-id="cbaf4-129">In the **Foreign Image** section, set the formula for the **ClippingPath** cell to  `="Geometry2.Path"` and then accept the formula.</span></span> 
    

