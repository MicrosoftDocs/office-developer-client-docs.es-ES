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
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419285"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="179d8-103">Celda LangID (Sección de caracteres)</span><span class="sxs-lookup"><span data-stu-id="179d8-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="179d8-104">Indica el idioma del texto.</span><span class="sxs-lookup"><span data-stu-id="179d8-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="179d8-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="179d8-105">Remarks</span></span>

<span data-ttu-id="179d8-106">Para obtener una lista de los idiomas admitidos por las aplicaciones de Microsoft Office, vea el tema sobre la celda [DocLangID](doclangid-cell-document-properties-section.md) (sección sobre propiedades del documento).</span><span class="sxs-lookup"><span data-stu-id="179d8-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="179d8-107">Para obtener una referencia a la celda LangID por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:</span><span class="sxs-lookup"><span data-stu-id="179d8-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="179d8-108">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="179d8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="179d8-109">Char.LangID[  *i*  ] donde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="179d8-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="179d8-110">Para obtener una referencia a la celda LangID por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="179d8-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="179d8-111">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="179d8-111">Section index:</span></span>  <br/> |<span data-ttu-id="179d8-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="179d8-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="179d8-113">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="179d8-113">Row index:</span></span>  <br/> |<span data-ttu-id="179d8-114">**visRowCharacter**  +   *i* donde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="179d8-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="179d8-115">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="179d8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="179d8-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="179d8-116">**visCharacterLangID**</span></span> <br/> |
   

