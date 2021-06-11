---
title: Función Replace (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 93c8fc1d-e70c-4726-af2f-c6501d82e49b
description: Reemplaza todas las repeticiones de un valor de cadena especificado por otro valor de cadena.
ms.openlocfilehash: 678cf88fe66d65be454613ce2c615bb7cb8f66d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421035"
---
# <a name="replace-function-access-custom-web-app"></a><span data-ttu-id="a0d05-103">Función Replace (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="a0d05-103">Replace Function (Access custom web app)</span></span>

<span data-ttu-id="a0d05-104">Reemplaza todas las repeticiones de un valor de cadena especificado por otro valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="a0d05-104">Replaces all occurrences of a specified string value with another string value.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a0d05-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="a0d05-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a0d05-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0d05-107">Syntax</span></span>

 <span data-ttu-id="a0d05-108">**Replace** (*TextExpression*, *Pattern*, *Replacement*)</span><span class="sxs-lookup"><span data-stu-id="a0d05-108">**Replace** (*TextExpression*, *Pattern*, *Replacement*)</span></span> 
  
<span data-ttu-id="a0d05-109">La **función Replace** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="a0d05-109">The **Replace** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a0d05-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="a0d05-110">**Argument name**</span></span>|<span data-ttu-id="a0d05-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0d05-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a0d05-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="a0d05-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="a0d05-113">Expresión de cadena que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="a0d05-113">The string expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="a0d05-114">*Pattern*</span><span class="sxs-lookup"><span data-stu-id="a0d05-114">*Pattern*</span></span>  <br/> |<span data-ttu-id="a0d05-115">Subcadena que se va a encontrar.</span><span class="sxs-lookup"><span data-stu-id="a0d05-115">The substring to be found.</span></span>  <span data-ttu-id="a0d05-116">*Pattern*  no puede ser una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="a0d05-116">*Pattern*  cannot be an empty string ("").</span></span>  <br/> |
| <span data-ttu-id="a0d05-117">*Replacement*</span><span class="sxs-lookup"><span data-stu-id="a0d05-117">*Replacement*</span></span>  <br/> |<span data-ttu-id="a0d05-118">Cadena de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="a0d05-118">The replacement string.</span></span>  <br/> |
   

