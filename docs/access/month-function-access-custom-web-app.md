---
title: Función Month (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Devuelve un valor de tipo integer que representa el mes de la fecha especificada.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815467"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="914dd-103">Función Month (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="914dd-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="914dd-104">Devuelve un valor de tipo integer que representa el mes de la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="914dd-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="914dd-p101">[!NOTA] La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="914dd-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="914dd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="914dd-107">Syntax</span></span>

 <span data-ttu-id="914dd-108">**Mes** (*Fecha*)</span><span class="sxs-lookup"><span data-stu-id="914dd-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="914dd-109">La función **Month** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="914dd-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="914dd-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="914dd-110">**Argument name**</span></span>|<span data-ttu-id="914dd-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="914dd-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="914dd-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="914dd-112">*Date*</span></span>  <br/> |<span data-ttu-id="914dd-113">Una expresión que se puede resolver en un valor Fecha/Hora.</span><span class="sxs-lookup"><span data-stu-id="914dd-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="914dd-114">Notas</span><span class="sxs-lookup"><span data-stu-id="914dd-114">Remarks</span></span>

 <span data-ttu-id="914dd-115">**Mes** devuelve el mismo valor que **DatePart** (mes, fecha).</span><span class="sxs-lookup"><span data-stu-id="914dd-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="914dd-116">Si *fecha* contiene sólo una parte del tiempo, el valor devuelto es 1, el mes de base.</span><span class="sxs-lookup"><span data-stu-id="914dd-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

