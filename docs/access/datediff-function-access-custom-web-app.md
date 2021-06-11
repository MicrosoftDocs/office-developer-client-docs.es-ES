---
title: Función DateDiff (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Devuelve el recuento de los límites de partes de fecha especificados cruzados entre la fecha de inicio y la fecha de finalización especificadas.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415617"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="2f30a-103">Función DateDiff (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="2f30a-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="2f30a-104">Devuelve el recuento de los límites de partes de fecha especificados cruzados entre la fecha de inicio y la fecha de finalización especificadas.</span><span class="sxs-lookup"><span data-stu-id="2f30a-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2f30a-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="2f30a-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2f30a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f30a-107">Syntax</span></span>

<span data-ttu-id="2f30a-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="2f30a-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="2f30a-109">La **función DateDiff** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="2f30a-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="2f30a-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="2f30a-110">**Argument name**</span></span>|<span data-ttu-id="2f30a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2f30a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2f30a-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="2f30a-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="2f30a-113">Es la parte de  *StartDate*  y  *EndDate*  que especifica el tipo de límite cruzado.</span><span class="sxs-lookup"><span data-stu-id="2f30a-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="2f30a-114">Consulte la sección Comentarios para obtener una lista de configuraciones válidas.</span><span class="sxs-lookup"><span data-stu-id="2f30a-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="2f30a-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="2f30a-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="2f30a-p103">Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  </span><span class="sxs-lookup"><span data-stu-id="2f30a-p103">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
| <span data-ttu-id="2f30a-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="2f30a-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="2f30a-p104">Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  </span><span class="sxs-lookup"><span data-stu-id="2f30a-p104">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f30a-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f30a-121">Remarks</span></span>

<span data-ttu-id="2f30a-122">La siguiente tabla muestra todos los argumentos  *ParcFecha*  válidos.</span><span class="sxs-lookup"><span data-stu-id="2f30a-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="2f30a-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="2f30a-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="2f30a-124">**year**</span><span class="sxs-lookup"><span data-stu-id="2f30a-124">**year**</span></span> <br/> |
|<span data-ttu-id="2f30a-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="2f30a-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="2f30a-126">**month**</span><span class="sxs-lookup"><span data-stu-id="2f30a-126">**month**</span></span> <br/> |
|<span data-ttu-id="2f30a-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="2f30a-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="2f30a-128">**day**</span><span class="sxs-lookup"><span data-stu-id="2f30a-128">**day**</span></span> <br/> |
|<span data-ttu-id="2f30a-129">**week**</span><span class="sxs-lookup"><span data-stu-id="2f30a-129">**week**</span></span> <br/> |
|<span data-ttu-id="2f30a-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="2f30a-130">**hour**</span></span> <br/> |
|<span data-ttu-id="2f30a-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="2f30a-131">**minute**</span></span> <br/> |
|<span data-ttu-id="2f30a-132">**second**</span><span class="sxs-lookup"><span data-stu-id="2f30a-132">**second**</span></span> <br/> |
|<span data-ttu-id="2f30a-133">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="2f30a-133">**millisecond**</span></span> <br/> |
   

