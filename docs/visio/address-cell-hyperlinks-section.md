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
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438039"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="58a26-103">Celda Address (Sección de hipervínculos)</span><span class="sxs-lookup"><span data-stu-id="58a26-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="58a26-104">Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.</span><span class="sxs-lookup"><span data-stu-id="58a26-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="58a26-105">Puede especificar Dirección como ruta de acceso relativa en función de la ruta de acceso  base definida para  el documento en el cuadro **base** Hipervínculo de la ficha Resumen del cuadro de diálogo Propiedades (haga clic en la pestaña Archivo, haga clic en **Información,** haga clic en \*\* Propiedades \*\*y, a continuación, haga clic en Propiedades **avanzadas).** </span><span class="sxs-lookup"><span data-stu-id="58a26-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click \*\* Properties \*\*, and then click **Advanced Properties**).</span></span> <span data-ttu-id="58a26-106">Si el documento no tiene ruta de acceso base, la aplicación explorará basándose en la ruta de acceso del documento.</span><span class="sxs-lookup"><span data-stu-id="58a26-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="58a26-107">Si éste no se ha guardado, el hipervínculo estará sin definir.</span><span class="sxs-lookup"><span data-stu-id="58a26-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58a26-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58a26-108">Remarks</span></span>

<span data-ttu-id="58a26-109">También puede establecer el valor de la celda Address en el cuadro de diálogo **Hipervínculos** (haga clic en **Hipervínculos** en la pestaña **Insertar**).</span><span class="sxs-lookup"><span data-stu-id="58a26-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="58a26-110">Para obtener una referencia a la celda Address por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="58a26-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58a26-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="58a26-111">Cell name:</span></span>  <br/> |<span data-ttu-id="58a26-112">Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="58a26-112">Hyperlink.</span></span> <span data-ttu-id="58a26-113">*nombre*  . Dirección donde Hipervínculo.</span><span class="sxs-lookup"><span data-stu-id="58a26-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="58a26-114">*es*  el nombre de la fila de hipervínculo</span><span class="sxs-lookup"><span data-stu-id="58a26-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="58a26-115">Para obtener una referencia a la celda Address por su nombre desde otra fórmula, o desde un programa, mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="58a26-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58a26-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="58a26-116">Section index:</span></span>  <br/> |<span data-ttu-id="58a26-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="58a26-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="58a26-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="58a26-118">Row index:</span></span>  <br/> |<span data-ttu-id="58a26-119">**visRow1stHyperlink**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="58a26-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="58a26-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="58a26-120">Cell index:</span></span>  <br/> |<span data-ttu-id="58a26-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="58a26-121">**visHLinkAddress**</span></span> <br/> |
   

