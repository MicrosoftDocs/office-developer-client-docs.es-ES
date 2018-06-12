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
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822448"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="54e70-103">Celda LangID (Sección de varios)</span><span class="sxs-lookup"><span data-stu-id="54e70-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="54e70-104">Indica el idioma de las fórmulas de celda.</span><span class="sxs-lookup"><span data-stu-id="54e70-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54e70-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="54e70-105">Remarks</span></span>

<span data-ttu-id="54e70-106">Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office, vea el tema de [DocLangID](doclangid-cell-document-properties-section.md) (sección Document Properties) de la celda.</span><span class="sxs-lookup"><span data-stu-id="54e70-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="54e70-107">Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="54e70-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54e70-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="54e70-108">Cell name:</span></span>  <br/> | <span data-ttu-id="54e70-109">LangID</span><span class="sxs-lookup"><span data-stu-id="54e70-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="54e70-110">Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="54e70-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54e70-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="54e70-111">Section index:</span></span>  <br/> |<span data-ttu-id="54e70-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54e70-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="54e70-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="54e70-113">Row index:</span></span>  <br/> |<span data-ttu-id="54e70-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="54e70-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="54e70-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="54e70-115">Cell index:</span></span>  <br/> |<span data-ttu-id="54e70-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="54e70-116">**visObjLangID**</span></span> <br/> |
   

