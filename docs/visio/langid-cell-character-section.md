---
title: Celda LangID (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Indica el idioma del texto.
ms.openlocfilehash: e503abb2365635fa25a4dbec54b7fe3da4043fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822405"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="60546-103">Celda LangID (sección Caracteres)</span><span class="sxs-lookup"><span data-stu-id="60546-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="60546-104">Indica el idioma del texto.</span><span class="sxs-lookup"><span data-stu-id="60546-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60546-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60546-105">Remarks</span></span>

<span data-ttu-id="60546-106">Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office, vea el tema sobre la celda [DocLangID](doclangid-cell-document-properties-section.md) (sección sobre propiedades del documento).</span><span class="sxs-lookup"><span data-stu-id="60546-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="60546-107">Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="60546-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60546-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="60546-108">Cell name:</span></span>  <br/> | <span data-ttu-id="60546-109">Char.LangID [ *i* ] donde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="60546-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="60546-110">Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="60546-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60546-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="60546-111">Section index:</span></span>  <br/> |<span data-ttu-id="60546-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="60546-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="60546-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="60546-113">Row index:</span></span>  <br/> |<span data-ttu-id="60546-114">**visRowCharacter** +  *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="60546-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="60546-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="60546-115">Cell index:</span></span>  <br/> |<span data-ttu-id="60546-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="60546-116">**visCharacterLangID**</span></span> <br/> |
   

