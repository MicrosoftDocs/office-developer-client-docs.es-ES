---
title: Función DateWithTimeFromParts (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Devuelve una fecha y hora basándose en un año, mes, día y hora especificados.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422092"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="5ea31-103">Función DateWithTimeFromParts (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="5ea31-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="5ea31-104">Devuelve una fecha y hora basándose en un año, mes, día y hora especificados.</span><span class="sxs-lookup"><span data-stu-id="5ea31-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5ea31-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="5ea31-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5ea31-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ea31-107">Syntax</span></span>

<span data-ttu-id="5ea31-108">**DateWithTimeFromParts** (*Año*, *mes*, *día*, *hora*, *minuto*, *segundo*)</span><span class="sxs-lookup"><span data-stu-id="5ea31-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="5ea31-109">La función **DateWithTimeFromParts** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="5ea31-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="5ea31-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="5ea31-110">**Argument name**</span></span>|<span data-ttu-id="5ea31-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5ea31-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5ea31-112">*Year*</span><span class="sxs-lookup"><span data-stu-id="5ea31-112">*Year*</span></span>  <br/> |<span data-ttu-id="5ea31-113">Expresión de tipo inTeger que especifica un año.</span><span class="sxs-lookup"><span data-stu-id="5ea31-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="5ea31-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="5ea31-114">*Month*</span></span>  <br/> |<span data-ttu-id="5ea31-115">Expresión de tipo inTeger que especifica un mes.</span><span class="sxs-lookup"><span data-stu-id="5ea31-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="5ea31-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="5ea31-116">*Day*</span></span>  <br/> |<span data-ttu-id="5ea31-117">Expresión de tipo inTeger que especifica un día.</span><span class="sxs-lookup"><span data-stu-id="5ea31-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="5ea31-118">*Hour*</span><span class="sxs-lookup"><span data-stu-id="5ea31-118">*Hour*</span></span>  <br/> |<span data-ttu-id="5ea31-119">Expresión de tipo inTeger que especifica las horas.</span><span class="sxs-lookup"><span data-stu-id="5ea31-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="5ea31-120">*Minute*</span><span class="sxs-lookup"><span data-stu-id="5ea31-120">*Minute*</span></span>  <br/> |<span data-ttu-id="5ea31-121">Expresión de número entero que especifica los minutos.</span><span class="sxs-lookup"><span data-stu-id="5ea31-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="5ea31-122">*Second*</span><span class="sxs-lookup"><span data-stu-id="5ea31-122">*Second*</span></span>  <br/> |<span data-ttu-id="5ea31-123">Expresión de número entero que especifica los segundos.</span><span class="sxs-lookup"><span data-stu-id="5ea31-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ea31-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5ea31-124">Remarks</span></span>

<span data-ttu-id="5ea31-125">**DateWithTimeFromParts** devuelve un valor de fecha y hora completamente inicializado.</span><span class="sxs-lookup"><span data-stu-id="5ea31-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="5ea31-126">Si los argumentos no son válidos, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="5ea31-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="5ea31-127">Si los argumentos required son NULL, se devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="5ea31-127">If required arguments are Null, then Null is returned.</span></span> 
  

