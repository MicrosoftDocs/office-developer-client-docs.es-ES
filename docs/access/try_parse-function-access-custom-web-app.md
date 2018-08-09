---
title: Función Try_Parse (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analiza un valor de texto para el tipo de datos especificado en la referencia cultural de la aplicación o devuelve Null si la conversión no es válida.
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815510"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="7299e-103">Función Try_Parse (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="7299e-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="7299e-104">Analiza un valor de texto para el tipo de datos especificado en la referencia cultural de la aplicación o devuelve Null si la conversión no es válida.</span><span class="sxs-lookup"><span data-stu-id="7299e-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7299e-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="7299e-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7299e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7299e-107">Syntax</span></span>

 <span data-ttu-id="7299e-108">**Try_Parse** (*TextExpression*, *tipo de datos*)</span><span class="sxs-lookup"><span data-stu-id="7299e-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="7299e-109">La función **Try_Parse** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="7299e-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="7299e-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="7299e-110">**Argument name**</span></span>|<span data-ttu-id="7299e-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7299e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7299e-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="7299e-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="7299e-113">Una expresión de texto que representa el valor con formato para analizar en el tipo de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="7299e-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="7299e-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="7299e-114">*DataType*</span></span>  <br/> |<span data-ttu-id="7299e-115">El tipo de datos en el que se va a analizar *TextExpression* .</span><span class="sxs-lookup"><span data-stu-id="7299e-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7299e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7299e-116">Remarks</span></span>

<span data-ttu-id="7299e-117">Use **Try_Parse** sólo para convertir una cadena de fecha y hora y tipos de número.</span><span class="sxs-lookup"><span data-stu-id="7299e-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="7299e-118">Para las conversiones de tipo general, seguir usando **convertir**.</span><span class="sxs-lookup"><span data-stu-id="7299e-118">For general type conversions, continue to use **Convert**.</span></span> 
  

