---
title: Función Year (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Devuelve un valor numérico que representa el año de la fecha especificada en el calendario gregoriano.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433125"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="16a25-103">Función Year (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="16a25-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="16a25-104">Devuelve un valor numérico que representa el año de la fecha especificada en el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="16a25-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="16a25-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="16a25-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="16a25-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16a25-107">Syntax</span></span>

 <span data-ttu-id="16a25-108">**Año** (*Fecha*)</span><span class="sxs-lookup"><span data-stu-id="16a25-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="16a25-109">La función **Year** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="16a25-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="16a25-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="16a25-110">**Argument name**</span></span>|<span data-ttu-id="16a25-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16a25-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="16a25-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="16a25-112">*Date*</span></span>  <br/> |<span data-ttu-id="16a25-p102">Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  </span><span class="sxs-lookup"><span data-stu-id="16a25-p102">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="16a25-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16a25-115">Remarks</span></span>

<span data-ttu-id="16a25-116">Los valores devueltos por las funciones **Year**, **Month**y **Day** serán valores gregorianos independientemente del formato de presentación del valor de fecha proporcionado.</span><span class="sxs-lookup"><span data-stu-id="16a25-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="16a25-117">Por ejemplo, si el formato de presentación de la fecha suministrada utiliza el calendario Hijri, los valores devueltos para las funciones **Year**, **Month**y **Day** serán valores asociados con la fecha Gregoriana equivalente.</span><span class="sxs-lookup"><span data-stu-id="16a25-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

