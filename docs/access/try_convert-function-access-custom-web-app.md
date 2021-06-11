---
title: Try_Convert (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convierte un valor en un tipo de datos especificado o devuelve Null si la conversión no es válida.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410899"
---
# <a name="try_convert-function-access-custom-web-app"></a><span data-ttu-id="dedb2-103">Try_Convert (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="dedb2-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="dedb2-104">Convierte un valor en un tipo de datos especificado o devuelve Null si la conversión no es válida.</span><span class="sxs-lookup"><span data-stu-id="dedb2-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="dedb2-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="dedb2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dedb2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dedb2-107">Syntax</span></span>

 <span data-ttu-id="dedb2-108">**Try_Convert** (*DataType*, *Expression*)</span><span class="sxs-lookup"><span data-stu-id="dedb2-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="dedb2-109">La **Try_Convert** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="dedb2-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="dedb2-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="dedb2-110">**Argument name**</span></span>|<span data-ttu-id="dedb2-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dedb2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dedb2-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="dedb2-112">*DataType*</span></span>  <br/> |<span data-ttu-id="dedb2-113">Tipo de datos en el que se va a convertir  *Expression*  .</span><span class="sxs-lookup"><span data-stu-id="dedb2-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="dedb2-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="dedb2-114">*Expression*</span></span>  <br/> |<span data-ttu-id="dedb2-115">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="dedb2-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dedb2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dedb2-116">Remarks</span></span>

 <span data-ttu-id="dedb2-117">**Try_Convert** toma el valor que se le ha pasado e intenta convertirlo en el *DataType especificado.*</span><span class="sxs-lookup"><span data-stu-id="dedb2-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="dedb2-118">Si la conversión se realiza **correctamente, Try_Convert** devuelve el valor como  *datatype especificado*  ; si se produce un error, se devuelve null.</span><span class="sxs-lookup"><span data-stu-id="dedb2-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="dedb2-119">Sin embargo, si solicita una conversión que no está permitida explícitamente, **Try_Convert** error.</span><span class="sxs-lookup"><span data-stu-id="dedb2-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

