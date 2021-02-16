---
title: Celda NoCoauth (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Establece si varios autores pueden editar simultáneamente un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive en una sesión de coautoría.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420517"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="8f051-103">Celda NoCoauth (Sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="8f051-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="8f051-104">Establece si varios autores pueden editar simultáneamente un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive en una sesión de coautoría.</span><span class="sxs-lookup"><span data-stu-id="8f051-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="8f051-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8f051-105">**Value**</span></span>|<span data-ttu-id="8f051-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f051-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8f051-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="8f051-107">TRUE</span></span>  <br/> |<span data-ttu-id="8f051-108">El documento no se puede coautor y se bloquea para su edición al abrirse.</span><span class="sxs-lookup"><span data-stu-id="8f051-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="8f051-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="8f051-109">FALSE</span></span>  <br/> |<span data-ttu-id="8f051-110">El documento se puede coautor.</span><span class="sxs-lookup"><span data-stu-id="8f051-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f051-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f051-111">Remarks</span></span>

<span data-ttu-id="8f051-112">Para obtener una referencia a la celda **NoCoauth** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell,** o desde un programa mediante la propiedad **CellsU,** utilice:</span><span class="sxs-lookup"><span data-stu-id="8f051-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8f051-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="8f051-113">Cell name:</span></span>  <br/> | <span data-ttu-id="8f051-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="8f051-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="8f051-115">Para obtener una referencia desde un programa a la celda **NoCoauth** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8f051-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8f051-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="8f051-116">Section index:</span></span>  <br/> |<span data-ttu-id="8f051-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8f051-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8f051-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="8f051-118">Row index:</span></span>  <br/> |<span data-ttu-id="8f051-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="8f051-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="8f051-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="8f051-120">Cell index:</span></span>  <br/> |<span data-ttu-id="8f051-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="8f051-121">**visDocNoCoauth**</span></span> <br/> |
   

