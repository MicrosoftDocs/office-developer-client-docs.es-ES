---
title: Función DateWithTimeFromParts (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Devuelve una hora, fecha y hora en función de un año especificado, el mes, día.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815292"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="8a5ad-103">Función DateWithTimeFromParts (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="8a5ad-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="8a5ad-104">Devuelve una hora, fecha y hora en función de un año especificado, el mes, día.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8a5ad-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="8a5ad-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8a5ad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a5ad-107">Syntax</span></span>

<span data-ttu-id="8a5ad-108">**DateWithTimeFromParts** (*Año*, *mes*, *día*, *hora*, *minuto*, *segundo*)</span><span class="sxs-lookup"><span data-stu-id="8a5ad-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="8a5ad-109">La función **DateWithTimeFromParts** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8a5ad-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="8a5ad-110">**Argument name**</span></span>|<span data-ttu-id="8a5ad-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a5ad-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8a5ad-112">*year*</span><span class="sxs-lookup"><span data-stu-id="8a5ad-112">*Year*</span></span>  <br/> |<span data-ttu-id="8a5ad-113">Expresión de tipo entero que especifica un año.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="8a5ad-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="8a5ad-114">*Month*</span></span>  <br/> |<span data-ttu-id="8a5ad-115">Expresión de tipo entero que especifica un mes.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="8a5ad-116">*Día*</span><span class="sxs-lookup"><span data-stu-id="8a5ad-116">*Day*</span></span>  <br/> |<span data-ttu-id="8a5ad-117">Expresión de tipo entero que especifica un día.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="8a5ad-118">*Hora*</span><span class="sxs-lookup"><span data-stu-id="8a5ad-118">*Hour*</span></span>  <br/> |<span data-ttu-id="8a5ad-119">Expresión de tipo Integer que especifica horas.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="8a5ad-120">*Minuto*</span><span class="sxs-lookup"><span data-stu-id="8a5ad-120">*Minute*</span></span>  <br/> |<span data-ttu-id="8a5ad-121">Expresión de tipo Integer que especifica los minutos.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="8a5ad-122">*Segundo*</span><span class="sxs-lookup"><span data-stu-id="8a5ad-122">*Second*</span></span>  <br/> |<span data-ttu-id="8a5ad-123">Expresión de tipo Integer que especifica los segundos.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a5ad-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a5ad-124">Remarks</span></span>

<span data-ttu-id="8a5ad-125">**DateWithTimeFromParts** devuelve un valor de fecha y hora totalmente inicializado.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="8a5ad-126">Si los argumentos no son válidos, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="8a5ad-127">Si es necesario argumentos son Null, se devuelve Null.</span><span class="sxs-lookup"><span data-stu-id="8a5ad-127">If required arguments are Null, then Null is returned.</span></span> 
  

