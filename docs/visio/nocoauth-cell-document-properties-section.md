---
title: Celda NoCoauth (sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede ser editado por varios autores de forma simultánea en una sesión de coautoría.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319442"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="85981-103">Celda NoCoauth (sección de propiedades del documento)</span><span class="sxs-lookup"><span data-stu-id="85981-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="85981-104">Establece si un documento almacenado en un servidor de Microsoft SharePoint 2013 o Microsoft OneDrive puede ser editado por varios autores de forma simultánea en una sesión de coautoría.</span><span class="sxs-lookup"><span data-stu-id="85981-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="85981-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="85981-105">**Value**</span></span>|<span data-ttu-id="85981-106">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85981-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85981-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="85981-107">TRUE</span></span>  <br/> |<span data-ttu-id="85981-108">El documento no puede ser coautor y está bloqueado para edición al abrirlo.</span><span class="sxs-lookup"><span data-stu-id="85981-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="85981-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="85981-109">FALSE</span></span>  <br/> |<span data-ttu-id="85981-110">El documento puede ser coautor.</span><span class="sxs-lookup"><span data-stu-id="85981-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85981-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85981-111">Remarks</span></span>

<span data-ttu-id="85981-112">Para obtener una referencia a la celda **NoCoauth** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice:</span><span class="sxs-lookup"><span data-stu-id="85981-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85981-113">Nombre de celda:</span><span class="sxs-lookup"><span data-stu-id="85981-113">Cell name:</span></span>  <br/> | <span data-ttu-id="85981-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="85981-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="85981-115">Para obtener una referencia desde un programa a la celda **NoCoauth** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:</span><span class="sxs-lookup"><span data-stu-id="85981-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85981-116">Índice de sección:</span><span class="sxs-lookup"><span data-stu-id="85981-116">Section index:</span></span>  <br/> |<span data-ttu-id="85981-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="85981-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="85981-118">Índice de fila:</span><span class="sxs-lookup"><span data-stu-id="85981-118">Row index:</span></span>  <br/> |<span data-ttu-id="85981-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="85981-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="85981-120">Índice de celda:</span><span class="sxs-lookup"><span data-stu-id="85981-120">Cell index:</span></span>  <br/> |<span data-ttu-id="85981-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="85981-121">**visDocNoCoauth**</span></span> <br/> |
   

