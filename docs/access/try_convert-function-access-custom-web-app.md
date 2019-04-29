---
title: Función Try_Convert (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convierte un valor en un tipo de datos especificado o devuelve NULL si la conversión no es válida.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410899"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="edda0-103">Función Try_Convert (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="edda0-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="edda0-104">Convierte un valor en un tipo de datos especificado o devuelve NULL si la conversión no es válida.</span><span class="sxs-lookup"><span data-stu-id="edda0-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="edda0-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="edda0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="edda0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edda0-107">Syntax</span></span>

 <span data-ttu-id="edda0-108">**Try_Convert** (*DataType*, *expresión*)</span><span class="sxs-lookup"><span data-stu-id="edda0-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="edda0-109">La función **Try_Convert** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="edda0-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="edda0-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="edda0-110">**Argument name**</span></span>|<span data-ttu-id="edda0-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="edda0-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="edda0-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="edda0-112">*DataType*</span></span>  <br/> |<span data-ttu-id="edda0-113">Tipo de datos en el que se va a convertir la *expresión* .</span><span class="sxs-lookup"><span data-stu-id="edda0-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="edda0-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="edda0-114">*Expression*</span></span>  <br/> |<span data-ttu-id="edda0-115">Valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="edda0-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edda0-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edda0-116">Remarks</span></span>

 <span data-ttu-id="edda0-117">**Try_Convert** toma el valor que se ha pasado e intenta convertirlo en el *tipo de texto* especificado.</span><span class="sxs-lookup"><span data-stu-id="edda0-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="edda0-118">Si la conversión se realiza correctamente, **Try_Convert** devuelve el valor como el *tipo de tipodedatos* especificado; Si se produce un error, se devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="edda0-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="edda0-119">Sin embargo, si solicita una conversión que no está permitida explícitamente, **Try_Convert** produce un error.</span><span class="sxs-lookup"><span data-stu-id="edda0-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

