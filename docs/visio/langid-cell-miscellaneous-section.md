---
title: Celda LangID (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Indica el idioma de las fórmulas de celda.
ms.openlocfilehash: e1e5b92f01e97bc63003a4b195c159a50f61e77b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346504"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="c667a-103">Celda LangID (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="c667a-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c667a-104">Indica el idioma de las fórmulas de celda.</span><span class="sxs-lookup"><span data-stu-id="c667a-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c667a-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c667a-105">Remarks</span></span>

<span data-ttu-id="c667a-106">Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office, vea el tema sobre la celda [DocLangID](doclangid-cell-document-properties-section.md) (sección sobre propiedades del documento).</span><span class="sxs-lookup"><span data-stu-id="c667a-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="c667a-107">Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="c667a-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c667a-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c667a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c667a-109">Idioma</span><span class="sxs-lookup"><span data-stu-id="c667a-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="c667a-110">Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c667a-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c667a-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c667a-111">Section index:</span></span>  <br/> |<span data-ttu-id="c667a-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c667a-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c667a-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c667a-113">Row index:</span></span>  <br/> |<span data-ttu-id="c667a-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c667a-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c667a-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c667a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c667a-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="c667a-116">**visObjLangID**</span></span> <br/> |
   

