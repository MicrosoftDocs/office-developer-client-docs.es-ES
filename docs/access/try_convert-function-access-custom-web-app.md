---
title: Función Try_Convert (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convierte un valor en un tipo de datos especificado o devuelve Null si la conversión no es válida.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815526"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="f2b40-103">Función Try_Convert (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="f2b40-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="f2b40-104">Convierte un valor en un tipo de datos especificado o devuelve Null si la conversión no es válida.</span><span class="sxs-lookup"><span data-stu-id="f2b40-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f2b40-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="f2b40-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f2b40-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2b40-107">Syntax</span></span>

 <span data-ttu-id="f2b40-108">**Try_Convert** (*Tipo de datos*, *expresión*)</span><span class="sxs-lookup"><span data-stu-id="f2b40-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="f2b40-109">La función **Try_Convert** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f2b40-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="f2b40-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="f2b40-110">**Argument name**</span></span>|<span data-ttu-id="f2b40-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f2b40-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f2b40-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="f2b40-112">*DataType*</span></span>  <br/> |<span data-ttu-id="f2b40-113">El tipo de datos en el que se va a convertir *expresión* .</span><span class="sxs-lookup"><span data-stu-id="f2b40-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="f2b40-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="f2b40-114">*Expression*</span></span>  <br/> |<span data-ttu-id="f2b40-115">El valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="f2b40-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2b40-116">Notas</span><span class="sxs-lookup"><span data-stu-id="f2b40-116">Remarks</span></span>

 <span data-ttu-id="f2b40-117">**Try_Convert** toma el valor que se pasa a ella e intenta convertir en el *tipo de datos* de especificado.</span><span class="sxs-lookup"><span data-stu-id="f2b40-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="f2b40-118">Si la conversión se realiza correctamente, **Try_Convert** devuelve el valor como el *tipo de datos* de especificado; Si se produce un error, se devuelve null.</span><span class="sxs-lookup"><span data-stu-id="f2b40-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="f2b40-119">Sin embargo si solicita una conversión explícitamente no está permitido, a continuación, **Try_Convert** se produce un error con un error.</span><span class="sxs-lookup"><span data-stu-id="f2b40-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

