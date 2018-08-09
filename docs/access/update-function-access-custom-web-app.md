---
title: Función de actualización (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Devuelve si se intentó una operación INSERT o UPDATE en el campo especificado.
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815521"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="d912e-103">Función de actualización (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="d912e-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="d912e-104">Devuelve si se intentó una operación INSERT o UPDATE en el campo especificado.</span><span class="sxs-lookup"><span data-stu-id="d912e-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d912e-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="d912e-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d912e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d912e-107">Syntax</span></span>

 <span data-ttu-id="d912e-108">**Actualización** (*Columna*)</span><span class="sxs-lookup"><span data-stu-id="d912e-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="d912e-109">La función de **actualización** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d912e-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d912e-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="d912e-110">**Argument name**</span></span>|<span data-ttu-id="d912e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d912e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d912e-112">*Column*</span><span class="sxs-lookup"><span data-stu-id="d912e-112">*Column*</span></span>  <br/> |<span data-ttu-id="d912e-113">El nombre del campo para comprobar si una operación INSERT o UPDATE.</span><span class="sxs-lookup"><span data-stu-id="d912e-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d912e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d912e-114">Remarks</span></span>

<span data-ttu-id="d912e-115">La función de **actualización** devuelve el valor TRUE, independientemente de si un intento de INSERCIÓN o actualización es correcto.</span><span class="sxs-lookup"><span data-stu-id="d912e-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

