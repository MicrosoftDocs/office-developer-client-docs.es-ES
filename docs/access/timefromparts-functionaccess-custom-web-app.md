---
title: Función TimeFromParts (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Devuelve un valor de hora basado en elementos especificados.
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304252"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="24593-103">Función TimeFromParts (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="24593-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="24593-104">Devuelve un valor de hora basado en elementos especificados.</span><span class="sxs-lookup"><span data-stu-id="24593-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="24593-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="24593-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="24593-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24593-107">Syntax</span></span>

 <span data-ttu-id="24593-108">**TimeFromParts** (*Hora*, *minuto*, *segundo*)</span><span class="sxs-lookup"><span data-stu-id="24593-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="24593-109">La función **TimeFromParts** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="24593-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="24593-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="24593-110">**Argument name**</span></span>|<span data-ttu-id="24593-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="24593-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="24593-112">*Hour*</span><span class="sxs-lookup"><span data-stu-id="24593-112">*Hour*</span></span>  <br/> |<span data-ttu-id="24593-113">Expresión de tipo inTeger que especifica las horas.</span><span class="sxs-lookup"><span data-stu-id="24593-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="24593-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="24593-114">*Minute*</span></span>  <br/> |<span data-ttu-id="24593-115">Expresión de número entero que especifica los minutos.</span><span class="sxs-lookup"><span data-stu-id="24593-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="24593-116">*Second*</span><span class="sxs-lookup"><span data-stu-id="24593-116">*Second*</span></span>  <br/> |<span data-ttu-id="24593-117">Expresión de número entero que especifica los segundos.</span><span class="sxs-lookup"><span data-stu-id="24593-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24593-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="24593-118">See also</span></span>

 <span data-ttu-id="24593-119">**TimeFromParts** devuelve un valor de tiempo completamente inicializado.</span><span class="sxs-lookup"><span data-stu-id="24593-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="24593-120">Si los argumentos no son válidos, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="24593-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="24593-121">Si alguno de los parámetros es null, se devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="24593-121">If any of the parameters are null, null is returned.</span></span> 
  

