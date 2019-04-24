---
title: Función Choose (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Devuelve el elemento en el índice especificado de una lista de valores.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282288"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="99932-103">Función Choose (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="99932-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="99932-104">Devuelve el elemento en el índice especificado de una lista de valores.</span><span class="sxs-lookup"><span data-stu-id="99932-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="99932-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="99932-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="99932-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99932-107">Syntax</span></span>

<span data-ttu-id="99932-108">**Elige** (*IndexNumber*, *Value*, [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="99932-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="99932-109">La función **Choose** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="99932-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="99932-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="99932-110">**Argument name**</span></span>|<span data-ttu-id="99932-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99932-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="99932-112">*IndexNumber*</span><span class="sxs-lookup"><span data-stu-id="99932-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="99932-113">Expresión de tipo Integer que representa un índice de base 1 en la lista de los elementos que le siguen.</span><span class="sxs-lookup"><span data-stu-id="99932-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="99932-114">*Value*</span><span class="sxs-lookup"><span data-stu-id="99932-114">*Value*</span></span>  <br/> |<span data-ttu-id="99932-115">Lista de valores de cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="99932-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99932-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99932-116">Remarks</span></span>

<span data-ttu-id="99932-117">Si el *IndexNumber* proporcionado no es un entero, el valor se convierte implícitamente en un entero.</span><span class="sxs-lookup"><span data-stu-id="99932-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="99932-118">Si el valor de índice supera los límites de la matriz de valores, **Choose** devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="99932-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

