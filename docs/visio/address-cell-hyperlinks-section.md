---
title: Celda Address (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821534"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="4e0bc-103">Celda Address (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="4e0bc-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="4e0bc-104">Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.</span><span class="sxs-lookup"><span data-stu-id="4e0bc-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="4e0bc-105">Puede especificar la dirección como una ruta de acceso relativa basada en la ruta de acceso base definida para el documento en el cuadro **base de hipervínculo** en la ficha **Resumen** del cuadro de diálogo **Propiedades** (haga clic en la pestaña **archivo** , haga clic en **información**, haga clic en ** Propiedades ** y, a continuación, haga clic en **Propiedades avanzadas**).</span><span class="sxs-lookup"><span data-stu-id="4e0bc-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click ** Properties **, and then click **Advanced Properties**).</span></span> <span data-ttu-id="4e0bc-106">Si el documento no tiene ninguna ruta de acceso base, la aplicación se desplaza en función de la ruta de acceso del documento.</span><span class="sxs-lookup"><span data-stu-id="4e0bc-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="4e0bc-107">Si no se ha guardado el documento, el hipervínculo no está definido.</span><span class="sxs-lookup"><span data-stu-id="4e0bc-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e0bc-108">Notas</span><span class="sxs-lookup"><span data-stu-id="4e0bc-108">Remarks</span></span>

<span data-ttu-id="4e0bc-109">También puede establecer el valor de la celda dirección en el cuadro de diálogo **hipervínculos** (haga clic en **hipervínculo** en la ficha **Insertar** ).</span><span class="sxs-lookup"><span data-stu-id="4e0bc-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="4e0bc-110">Para obtener una referencia a la celda Address por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e0bc-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e0bc-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4e0bc-111">Cell name:</span></span>  <br/> |<span data-ttu-id="4e0bc-112">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="4e0bc-112">Hyperlink.</span></span> <span data-ttu-id="4e0bc-113">*nombre* . Direcciones where hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="4e0bc-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="4e0bc-114">*nombre* es el nombre de la fila de hipervínculo</span><span class="sxs-lookup"><span data-stu-id="4e0bc-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="4e0bc-115">Para obtener una referencia a la celda Address por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="4e0bc-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e0bc-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4e0bc-116">Section index:</span></span>  <br/> |<span data-ttu-id="4e0bc-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="4e0bc-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="4e0bc-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4e0bc-118">Row index:</span></span>  <br/> |<span data-ttu-id="4e0bc-119">**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4e0bc-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4e0bc-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4e0bc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4e0bc-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="4e0bc-121">**visHLinkAddress**</span></span> <br/> |
   

