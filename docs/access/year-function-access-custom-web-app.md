---
title: Función Year (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Devuelve un valor numérico que representa el año de la fecha especificada en el calendario gregoriano.
ms.openlocfilehash: f9d72343637734257a2ed9589e5539b845933826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815518"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="e8fca-103">Función Year (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="e8fca-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="e8fca-104">Devuelve un valor numérico que representa el año de la fecha especificada en el calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="e8fca-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e8fca-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="e8fca-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e8fca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8fca-107">Syntax</span></span>

 <span data-ttu-id="e8fca-108">**Año** (*Fecha*)</span><span class="sxs-lookup"><span data-stu-id="e8fca-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="e8fca-109">La función **Year** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="e8fca-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e8fca-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="e8fca-110">**Argument name**</span></span>|<span data-ttu-id="e8fca-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8fca-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e8fca-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="e8fca-112">*Date*</span></span>  <br/> |<span data-ttu-id="e8fca-p102">Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  </span><span class="sxs-lookup"><span data-stu-id="e8fca-p102">An expression that can be resolved to a Date/Time value. The  *Date*  argument expression, column expression, user-defined variable or string literal.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8fca-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8fca-115">Remarks</span></span>

<span data-ttu-id="e8fca-116">Los valores devueltos por las funciones **Year**, **Month**y **Day** serán valores de gregoriano independientemente del formato de presentación para el valor de fecha suministrado.</span><span class="sxs-lookup"><span data-stu-id="e8fca-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="e8fca-117">Por ejemplo, si el formato de presentación de la fecha proporcionada usa el calendario Hijri, los valores devueltos para el **año**, **mes**y **día** funciones va a ser valores asociados con la fecha del calendario gregoriano equivalente.</span><span class="sxs-lookup"><span data-stu-id="e8fca-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

