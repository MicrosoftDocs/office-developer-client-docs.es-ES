---
title: Función DateDiff (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Devuelve el recuento de los límites de parte de fecha especificados entre la fecha de inicio y la fecha de finalización especificadas.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280729"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="0e64d-103">Función DateDiff (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="0e64d-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="0e64d-104">Devuelve el recuento de los límites de parte de fecha especificados entre la fecha de inicio y la fecha de finalización especificadas.</span><span class="sxs-lookup"><span data-stu-id="0e64d-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0e64d-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="0e64d-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0e64d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e64d-107">Syntax</span></span>

<span data-ttu-id="0e64d-108">**DifFecha** (*DatePart*, *startDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="0e64d-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="0e64d-109">La función **DateDiff** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0e64d-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="0e64d-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="0e64d-110">**Argument name**</span></span>|<span data-ttu-id="0e64d-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e64d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0e64d-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="0e64d-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="0e64d-113">Es la parte de *startDate* y *EndDate* que especifica el tipo de límite cruzado.</span><span class="sxs-lookup"><span data-stu-id="0e64d-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="0e64d-114">Consulte la sección Comentarios para obtener una lista de configuraciones válidas.</span><span class="sxs-lookup"><span data-stu-id="0e64d-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="0e64d-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="0e64d-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="0e64d-116">Una expresión que se puede resolver en un valor Fecha/Hora.</span><span class="sxs-lookup"><span data-stu-id="0e64d-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="0e64d-117">La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.</span><span class="sxs-lookup"><span data-stu-id="0e64d-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="0e64d-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="0e64d-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="0e64d-p104">Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  </span><span class="sxs-lookup"><span data-stu-id="0e64d-p104">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e64d-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e64d-121">Remarks</span></span>

<span data-ttu-id="0e64d-122">La siguiente tabla muestra todos los argumentos  *ParcFecha*  válidos.</span><span class="sxs-lookup"><span data-stu-id="0e64d-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="0e64d-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="0e64d-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="0e64d-124">**year**</span><span class="sxs-lookup"><span data-stu-id="0e64d-124">**year**</span></span> <br/> |
|<span data-ttu-id="0e64d-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="0e64d-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="0e64d-126">**month**</span><span class="sxs-lookup"><span data-stu-id="0e64d-126">**month**</span></span> <br/> |
|<span data-ttu-id="0e64d-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="0e64d-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="0e64d-128">**day**</span><span class="sxs-lookup"><span data-stu-id="0e64d-128">**day**</span></span> <br/> |
|<span data-ttu-id="0e64d-129">**week**</span><span class="sxs-lookup"><span data-stu-id="0e64d-129">**week**</span></span> <br/> |
|<span data-ttu-id="0e64d-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="0e64d-130">**hour**</span></span> <br/> |
|<span data-ttu-id="0e64d-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="0e64d-131">**minute**</span></span> <br/> |
|<span data-ttu-id="0e64d-132">**second**</span><span class="sxs-lookup"><span data-stu-id="0e64d-132">**second**</span></span> <br/> |
|<span data-ttu-id="0e64d-133">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="0e64d-133">**millisecond**</span></span> <br/> |
   

