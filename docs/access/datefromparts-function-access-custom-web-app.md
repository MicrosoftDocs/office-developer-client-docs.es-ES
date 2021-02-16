---
title: Función DateFromParts (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Devuelve un valor de fecha para el año, el mes y el día especificados.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423226"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="ce6f5-103">Función DateFromParts (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="ce6f5-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="ce6f5-104">Devuelve un valor de fecha para el año, el mes y el día especificados.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ce6f5-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="ce6f5-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ce6f5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce6f5-107">Syntax</span></span>

<span data-ttu-id="ce6f5-108">**DateFromParts** (*Year*, *Month*, *Day*)</span><span class="sxs-lookup"><span data-stu-id="ce6f5-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="ce6f5-109">La **función DateFromParts** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ce6f5-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="ce6f5-110">**Argument name**</span></span>|<span data-ttu-id="ce6f5-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ce6f5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ce6f5-112">*Year*</span><span class="sxs-lookup"><span data-stu-id="ce6f5-112">*Year*</span></span>  <br/> |<span data-ttu-id="ce6f5-113">Expresión entera que especifica un año.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="ce6f5-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="ce6f5-114">*Month*</span></span>  <br/> |<span data-ttu-id="ce6f5-115">Expresión entera que especifica un mes, de 1 a 12.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="ce6f5-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="ce6f5-116">*Day*</span></span>  <br/> |<span data-ttu-id="ce6f5-117">Expresión de entero que especifica un día.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce6f5-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce6f5-118">Remarks</span></span>

<span data-ttu-id="ce6f5-119">**DateFromParts** devuelve un valor de fecha con la parte de fecha establecida en el año, mes y día especificados, y la parte de hora establecida en el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="ce6f5-120">Si los argumentos no son válidos, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="ce6f5-121">Si los argumentos necesarios son nulos, se devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ce6f5-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce6f5-122">Example</span></span>

<span data-ttu-id="ce6f5-123">La expresión siguiente usa la **función DateFromParts** para calcular el primer día del mes actual.</span><span class="sxs-lookup"><span data-stu-id="ce6f5-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



