---
title: Celda LangID (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Indica el idioma del valor de los datos de formas.
ms.openlocfilehash: c5a0cca5f71bc5520337ad2bdcf354a2b4affe92
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420328"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="4b34c-103">Celda LangID (Sección de datos de formas)</span><span class="sxs-lookup"><span data-stu-id="4b34c-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="4b34c-104">Indica el idioma del valor de los datos de formas.</span><span class="sxs-lookup"><span data-stu-id="4b34c-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4b34c-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b34c-105">Remarks</span></span>

<span data-ttu-id="4b34c-106">Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office System, vea la celda [DocLangID](doclangid-cell-document-properties-section.md) (Sección de propiedades del documento).</span><span class="sxs-lookup"><span data-stu-id="4b34c-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="4b34c-107">Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="4b34c-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4b34c-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="4b34c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="4b34c-109">Polyprop.  *nombre* . LangID donde prop.  *Name* es el nombre de la fila</span><span class="sxs-lookup"><span data-stu-id="4b34c-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="4b34c-110">Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="4b34c-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4b34c-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="4b34c-111">Section index:</span></span>  <br/> |<span data-ttu-id="4b34c-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="4b34c-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="4b34c-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="4b34c-113">Row index:</span></span>  <br/> |<span data-ttu-id="4b34c-114">**visRowProp** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4b34c-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4b34c-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="4b34c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="4b34c-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="4b34c-116">**visCustPropsLangID**</span></span> <br/> |
   

