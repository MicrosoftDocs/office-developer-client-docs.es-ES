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
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822409"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="87b5e-103">Celda LangID (sección Anotación)</span><span class="sxs-lookup"><span data-stu-id="87b5e-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="87b5e-104">Indica el idioma del comentario.</span><span class="sxs-lookup"><span data-stu-id="87b5e-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="87b5e-105">Esta celda se utiliza para realizar un seguimiento de los comentarios sólo cuando se abre un archivo .vsd en Microsoft Visio 2013 o al guardar un archivo .vsdx en el formato de archivo .vsd.</span><span class="sxs-lookup"><span data-stu-id="87b5e-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="87b5e-106">No se usa para realizar un seguimiento de los comentarios de documentos .vsdx en Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="87b5e-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="87b5e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87b5e-107">Remarks</span></span>

<span data-ttu-id="87b5e-p102">Este valor es el identificador de configuración regional del idioma que se encuentra activo en la barra de idioma en el momento de la creación del comentario. Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office, vea el tema sobre la celda [DocLangID](doclangid-cell-document-properties-section.md) (sección sobre propiedades del documento).</span><span class="sxs-lookup"><span data-stu-id="87b5e-p102">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered. For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="87b5e-110">Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="87b5e-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87b5e-111">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="87b5e-111">Cell name:</span></span>  <br/> | <span data-ttu-id="87b5e-112">Annotation.LangID [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="87b5e-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="87b5e-113">Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="87b5e-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87b5e-114">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="87b5e-114">Section index:</span></span>  <br/> |<span data-ttu-id="87b5e-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="87b5e-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="87b5e-116">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="87b5e-116">Row index:</span></span>  <br/> |<span data-ttu-id="87b5e-117">**visRowAnnotation** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="87b5e-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="87b5e-118">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="87b5e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="87b5e-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="87b5e-119">**visAnnotationLangID**</span></span> <br/> |
   

