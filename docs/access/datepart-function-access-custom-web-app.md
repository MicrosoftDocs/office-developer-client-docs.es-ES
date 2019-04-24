---
title: Función DatePart (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Devuelve un valor numérico que representa la parte de fecha especificada de la fecha especificada.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280776"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="8dc29-103">Función DatePart (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="8dc29-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="8dc29-104">Devuelve un valor numérico que representa la parte de fecha especificada de la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="8dc29-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8dc29-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="8dc29-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8dc29-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8dc29-107">Syntax</span></span>

<span data-ttu-id="8dc29-108">**DatePart** (*DatePart*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="8dc29-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="8dc29-109">La función **DatePart** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8dc29-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8dc29-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="8dc29-110">**Argument name**</span></span>|<span data-ttu-id="8dc29-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8dc29-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8dc29-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="8dc29-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="8dc29-p102">La parte de  *Fecha*  (un valor de fecha u hora) para la que se devolverá un entero. Consulte la sección Comentarios para obtener la lista de las abreviaturas válidas.  </span><span class="sxs-lookup"><span data-stu-id="8dc29-p102">The part of  *Date*  (a date or time value) for which an integer will be returned. Refer to the Remarks section for the list of valid abbreviations.  </span></span><br/> |
| <span data-ttu-id="8dc29-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="8dc29-115">*Date*</span></span>  <br/> |<span data-ttu-id="8dc29-p103">Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  </span><span class="sxs-lookup"><span data-stu-id="8dc29-p103">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="8dc29-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8dc29-118">Remarks</span></span>

<span data-ttu-id="8dc29-119">La siguiente tabla muestra todos los argumentos  *ParcFecha*  válidos.</span><span class="sxs-lookup"><span data-stu-id="8dc29-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="8dc29-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="8dc29-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="8dc29-121">**year**</span><span class="sxs-lookup"><span data-stu-id="8dc29-121">**year**</span></span> <br/> |
|<span data-ttu-id="8dc29-122">**quarter**</span><span class="sxs-lookup"><span data-stu-id="8dc29-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="8dc29-123">**month**</span><span class="sxs-lookup"><span data-stu-id="8dc29-123">**month**</span></span> <br/> |
|<span data-ttu-id="8dc29-124">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="8dc29-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="8dc29-125">**day**</span><span class="sxs-lookup"><span data-stu-id="8dc29-125">**day**</span></span> <br/> |
|<span data-ttu-id="8dc29-126">**week**</span><span class="sxs-lookup"><span data-stu-id="8dc29-126">**week**</span></span> <br/> |
|<span data-ttu-id="8dc29-127">**weekday**</span><span class="sxs-lookup"><span data-stu-id="8dc29-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="8dc29-128">**hour**</span><span class="sxs-lookup"><span data-stu-id="8dc29-128">**hour**</span></span> <br/> |
|<span data-ttu-id="8dc29-129">**minute**</span><span class="sxs-lookup"><span data-stu-id="8dc29-129">**minute**</span></span> <br/> |
|<span data-ttu-id="8dc29-130">**second**</span><span class="sxs-lookup"><span data-stu-id="8dc29-130">**second**</span></span> <br/> |
|<span data-ttu-id="8dc29-131">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="8dc29-131">**millisecond**</span></span> <br/> |
   

