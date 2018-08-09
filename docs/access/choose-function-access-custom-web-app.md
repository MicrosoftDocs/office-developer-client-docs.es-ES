---
title: Elija función (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Devuelve el elemento en el índice especificado de una lista de valores.
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815328"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="76e40-103">Elija función (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="76e40-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="76e40-104">Devuelve el elemento en el índice especificado de una lista de valores.</span><span class="sxs-lookup"><span data-stu-id="76e40-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="76e40-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="76e40-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="76e40-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76e40-107">Syntax</span></span>

<span data-ttu-id="76e40-108">**Elija** (*NúmeroDeÍndice*, *valor*, [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="76e40-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="76e40-109">La función **Choose** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="76e40-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="76e40-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="76e40-110">**Argument name**</span></span>|<span data-ttu-id="76e40-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="76e40-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="76e40-112">*NúmeroDeÍndice*</span><span class="sxs-lookup"><span data-stu-id="76e40-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="76e40-113">Una expresión de número entero que representa un índice basado en 1 en la lista de los elementos a continuación del mismo.</span><span class="sxs-lookup"><span data-stu-id="76e40-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="76e40-114">*Valor*</span><span class="sxs-lookup"><span data-stu-id="76e40-114">*Value*</span></span>  <br/> |<span data-ttu-id="76e40-115">Lista de valores de cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="76e40-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76e40-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76e40-116">Remarks</span></span>

<span data-ttu-id="76e40-117">Si la proporcionada *númeroDeÍndice* no es un entero, el valor se convierte implícitamente a un valor entero.</span><span class="sxs-lookup"><span data-stu-id="76e40-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="76e40-118">Si el valor de índice supera los límites de la matriz de valores, **Choose** devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="76e40-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

