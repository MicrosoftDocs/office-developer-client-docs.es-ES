---
title: Función Update (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Devuelve si se intentó realizar una operación de inserción o actualización en el campo especificado.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307829"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="c6b6f-103">Función Update (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="c6b6f-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="c6b6f-104">Devuelve si se intentó realizar una operación de inserción o actualización en el campo especificado.</span><span class="sxs-lookup"><span data-stu-id="c6b6f-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c6b6f-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="c6b6f-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c6b6f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6b6f-107">Syntax</span></span>

 <span data-ttu-id="c6b6f-108">**Actualización** de (*Columna*)</span><span class="sxs-lookup"><span data-stu-id="c6b6f-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="c6b6f-109">La función **Update** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c6b6f-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="c6b6f-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="c6b6f-110">**Argument name**</span></span>|<span data-ttu-id="c6b6f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6b6f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c6b6f-112">*Column*</span><span class="sxs-lookup"><span data-stu-id="c6b6f-112">*Column*</span></span>  <br/> |<span data-ttu-id="c6b6f-113">Nombre del campo en el que se busca una operación de inserción o actualización.</span><span class="sxs-lookup"><span data-stu-id="c6b6f-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6b6f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6b6f-114">Remarks</span></span>

<span data-ttu-id="c6b6f-115">La función **Update** devuelve true independientemente de si un intento de inserción o actualización se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6b6f-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

