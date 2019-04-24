---
title: Función Parse (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analiza un valor de texto y devuelve su valor en un tipo determinado utilizando la referencia cultural de la aplicación.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308060"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="f7c5a-103">Función Parse (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="f7c5a-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="f7c5a-104">Analiza un valor de texto y devuelve su valor en un tipo determinado utilizando la referencia cultural de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f7c5a-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="f7c5a-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f7c5a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7c5a-107">Syntax</span></span>

 <span data-ttu-id="f7c5a-108">**Análisis** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="f7c5a-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="f7c5a-109">La \*\*\*\* función Parse contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="f7c5a-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-110">**Argument name**</span></span>|<span data-ttu-id="f7c5a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7c5a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f7c5a-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="f7c5a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="f7c5a-113">Una expresión de texto que representa el valor con formato que se va a analizar en el tipo de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="f7c5a-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="f7c5a-114">*DataType*</span></span>  <br/> |<span data-ttu-id="f7c5a-115">Valor literal que representa el tipo de datos solicitado para el resultado.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7c5a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7c5a-116">Remarks</span></span>

<span data-ttu-id="f7c5a-117">Use **Parse** Only para convertir de cadena en tipos de número, fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="f7c5a-118">Para las conversiones de tipo generales, use la función **Convert** .</span><span class="sxs-lookup"><span data-stu-id="f7c5a-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="f7c5a-119">Tenga en cuenta que hay una cierta sobrecarga en el rendimiento al analizar el valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="f7c5a-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

