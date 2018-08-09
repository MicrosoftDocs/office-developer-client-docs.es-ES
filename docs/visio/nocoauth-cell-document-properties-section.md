---
title: Celda NoCoauth (sección Propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede editarse por varios autores simultáneamente en una sesión de co-autoría.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822679"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="c4fb0-103">Celda NoCoauth (sección Propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="c4fb0-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="c4fb0-104">Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede editarse por varios autores simultáneamente en una sesión de co-autoría.</span><span class="sxs-lookup"><span data-stu-id="c4fb0-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="c4fb0-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c4fb0-105">**Value**</span></span>|<span data-ttu-id="c4fb0-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4fb0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4fb0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4fb0-107">TRUE</span></span>  <br/> |<span data-ttu-id="c4fb0-108">El documento no se puede ser coautor y está bloqueado para su edición cuando se abre.</span><span class="sxs-lookup"><span data-stu-id="c4fb0-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="c4fb0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4fb0-109">FALSE</span></span>  <br/> |<span data-ttu-id="c4fb0-110">Puede ser coautor del documento.</span><span class="sxs-lookup"><span data-stu-id="c4fb0-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4fb0-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4fb0-111">Remarks</span></span>

<span data-ttu-id="c4fb0-112">Para obtener una referencia a la celda **NoCoauth** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="c4fb0-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4fb0-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="c4fb0-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c4fb0-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="c4fb0-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="c4fb0-115">Para obtener una referencia a la celda **NoCoauth** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c4fb0-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c4fb0-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="c4fb0-116">Section index:</span></span>  <br/> |<span data-ttu-id="c4fb0-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4fb0-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c4fb0-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="c4fb0-118">Row index:</span></span>  <br/> |<span data-ttu-id="c4fb0-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="c4fb0-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="c4fb0-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="c4fb0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c4fb0-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="c4fb0-121">**visDocNoCoauth**</span></span> <br/> |
   

