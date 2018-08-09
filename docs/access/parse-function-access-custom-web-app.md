---
title: Parse (función) (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analiza un valor de texto y devuelve su valor en un tipo dado utilizando la referencia cultural de la aplicación.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815470"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="f959f-103">Parse (función) (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="f959f-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="f959f-104">Analiza un valor de texto y devuelve su valor en un tipo dado utilizando la referencia cultural de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f959f-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f959f-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="f959f-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f959f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f959f-107">Syntax</span></span>

 <span data-ttu-id="f959f-108">**Analizar** (*TextExpression*, *tipo de datos*)</span><span class="sxs-lookup"><span data-stu-id="f959f-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="f959f-109">La función **analizar** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f959f-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="f959f-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="f959f-110">**Argument name**</span></span>|<span data-ttu-id="f959f-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f959f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f959f-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="f959f-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="f959f-113">Una expresión de texto que representa el valor con formato para analizar en el tipo de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="f959f-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="f959f-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="f959f-114">*DataType*</span></span>  <br/> |<span data-ttu-id="f959f-115">Valor literal que representa el tipo de datos solicitado para el resultado.</span><span class="sxs-lookup"><span data-stu-id="f959f-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f959f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f959f-116">Remarks</span></span>

<span data-ttu-id="f959f-117">Use **analizar** sólo para convertir una cadena de fecha y hora y tipos de número.</span><span class="sxs-lookup"><span data-stu-id="f959f-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="f959f-118">Para las conversiones de tipo general, use la función **convertir** .</span><span class="sxs-lookup"><span data-stu-id="f959f-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="f959f-119">Tenga en cuenta que hay un cierto nivel de performance una sobrecarga en el valor de cadena de análisis.</span><span class="sxs-lookup"><span data-stu-id="f959f-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

