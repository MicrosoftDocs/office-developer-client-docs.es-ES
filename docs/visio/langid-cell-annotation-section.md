---
title: Celda LangID (Sección de anotación)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Indica el idioma del comentario.
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360553"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="74eca-103">Celda LangID (sección de anotación)</span><span class="sxs-lookup"><span data-stu-id="74eca-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="74eca-104">Indica el idioma del comentario.</span><span class="sxs-lookup"><span data-stu-id="74eca-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="74eca-105">Esta celda se utiliza para realizar un seguimiento de los comentarios sólo cuando se abre un archivo. VSD en Microsoft Visio 2013 o cuando se guarda un archivo. vsdx en el formato de archivo. VSD.</span><span class="sxs-lookup"><span data-stu-id="74eca-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="74eca-106">No se usa para el seguimiento de comentarios en documentos. vsdx en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="74eca-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="74eca-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74eca-107">Remarks</span></span>

<span data-ttu-id="74eca-p102">Este valor es el identificador de configuración regional del idioma que se encuentra activo en la barra de idioma en el momento de la creación del comentario. Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office, vea el tema sobre la celda [DocLangID](doclangid-cell-document-properties-section.md) (sección sobre propiedades del documento).</span><span class="sxs-lookup"><span data-stu-id="74eca-p102">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered. For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="74eca-110">Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="74eca-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74eca-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="74eca-111">Cell name:</span></span>  <br/> | <span data-ttu-id="74eca-112">Annotation. LangID [ *i* ] donde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="74eca-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="74eca-113">Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="74eca-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74eca-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="74eca-114">Section index:</span></span>  <br/> |<span data-ttu-id="74eca-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="74eca-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="74eca-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="74eca-116">Row index:</span></span>  <br/> |<span data-ttu-id="74eca-117">**visRowAnnotation** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="74eca-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="74eca-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="74eca-118">Cell index:</span></span>  <br/> |<span data-ttu-id="74eca-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="74eca-119">**visAnnotationLangID**</span></span> <br/> |
   

