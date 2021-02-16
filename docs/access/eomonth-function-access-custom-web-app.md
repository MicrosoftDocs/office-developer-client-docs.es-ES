---
title: Función EOMonth (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Devuelve el último día del mes anterior o el número de meses especificado.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437458"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="9d46c-103">Función EOMonth (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="9d46c-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="9d46c-104">Devuelve el último día del mes anterior o el número de meses especificado.</span><span class="sxs-lookup"><span data-stu-id="9d46c-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9d46c-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="9d46c-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9d46c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d46c-107">Syntax</span></span>

 <span data-ttu-id="9d46c-108">**EOMonth** (*Date*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="9d46c-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="9d46c-109">El **EOMonth** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9d46c-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="9d46c-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="9d46c-110">**Argument name**</span></span>|<span data-ttu-id="9d46c-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d46c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9d46c-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="9d46c-112">*Date*</span></span>  <br/> |<span data-ttu-id="9d46c-113">La fecha de inicio en formato fecha/hora, o en una representación de texto aceptada de una fecha.</span><span class="sxs-lookup"><span data-stu-id="9d46c-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="9d46c-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="9d46c-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="9d46c-115">Un número que representa el número de meses antes o después de la  *fecha*  .</span><span class="sxs-lookup"><span data-stu-id="9d46c-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d46c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d46c-116">Remarks</span></span>

<span data-ttu-id="9d46c-117">Si  *Date*  no es una fecha válida, **EOMonth** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="9d46c-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="9d46c-118">Si  *Date*  más  *NumberOfMonth produce*  una fecha no válida, **EOMonth** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="9d46c-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

