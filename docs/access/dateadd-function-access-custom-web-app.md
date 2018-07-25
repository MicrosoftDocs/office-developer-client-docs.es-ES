---
title: Función DateAdd (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Devuelve una fecha especificada con el intervalo especificado de número (entero positivo o negativo) que se agrega a una parte de fecha especificada de la fecha.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815348"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="d0b7f-103">Función DateAdd (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="d0b7f-103">DateAdd Function (Access custom web app)</span></span>

<span data-ttu-id="d0b7f-104">Devuelve una fecha especificada con el intervalo especificado de número (entero positivo o negativo) que se agrega a una parte de fecha especificada de la fecha.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d0b7f-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="d0b7f-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d0b7f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0b7f-107">Syntax</span></span>

<span data-ttu-id="d0b7f-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="d0b7f-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="d0b7f-109">La función **DateAdd** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d0b7f-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-110">**Argument name**</span></span>|<span data-ttu-id="d0b7f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d0b7f-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="d0b7f-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="d0b7f-p102">La parte de la  *Fecha*  a la que se agrega un entero. Consulte la sección Comentarios para obtener una lista de configuraciones válidas.  </span><span class="sxs-lookup"><span data-stu-id="d0b7f-p102">The part of  *Date*  to which an integer number is added. Refer to the Remarks section for the list of valid settings.  </span></span><br/> |
| <span data-ttu-id="d0b7f-115">*Número*</span><span class="sxs-lookup"><span data-stu-id="d0b7f-115">*Number*</span></span>  <br/> |<span data-ttu-id="d0b7f-p103">Es una expresión que se puede resolver en un entero que se agrega a  *ParcFecha*  de  *Fecha*  . Si especifica un valor con una fracción decimal, la fracción se trunca.  </span><span class="sxs-lookup"><span data-stu-id="d0b7f-p103">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  . If you specify a value with a decimal fraction, the fraction is truncated.  </span></span><br/> |
| <span data-ttu-id="d0b7f-118">*Fecha*</span><span class="sxs-lookup"><span data-stu-id="d0b7f-118">*Date*</span></span>  <br/> |<span data-ttu-id="d0b7f-p104">Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  </span><span class="sxs-lookup"><span data-stu-id="d0b7f-p104">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0b7f-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0b7f-121">Remarks</span></span>

<span data-ttu-id="d0b7f-122">La siguiente tabla muestra todos los argumentos  *ParcFecha*  válidos.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="d0b7f-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="d0b7f-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="d0b7f-124">**year**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-124">**year**</span></span> <br/> |
|<span data-ttu-id="d0b7f-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="d0b7f-126">**month**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-126">**month**</span></span> <br/> |
|<span data-ttu-id="d0b7f-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="d0b7f-128">**day**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-128">**day**</span></span> <br/> |
|<span data-ttu-id="d0b7f-129">**week**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-129">**week**</span></span> <br/> |
|<span data-ttu-id="d0b7f-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-130">**hour**</span></span> <br/> |
|<span data-ttu-id="d0b7f-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-131">**minute**</span></span> <br/> |
|<span data-ttu-id="d0b7f-132">**second**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-132">**second**</span></span> <br/> |
|<span data-ttu-id="d0b7f-133">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="d0b7f-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="d0b7f-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0b7f-134">Example</span></span>

<span data-ttu-id="d0b7f-135">La siguiente expresión calcula el último día del mes actual.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="d0b7f-136">La siguiente expresión calcula el último día del mes anterior.</span><span class="sxs-lookup"><span data-stu-id="d0b7f-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


