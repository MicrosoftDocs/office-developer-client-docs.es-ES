---
title: Try_Parse (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analiza un valor de texto para el tipo de datos especificado en la referencia cultural de la aplicación o devuelve Null si la conversión no es válida.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427531"
---
# <a name="try_parse-function-access-custom-web-app"></a><span data-ttu-id="37b5a-103">Try_Parse (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="37b5a-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="37b5a-104">Analiza un valor de texto para el tipo de datos especificado en la referencia cultural de la aplicación o devuelve Null si la conversión no es válida.</span><span class="sxs-lookup"><span data-stu-id="37b5a-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="37b5a-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="37b5a-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="37b5a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37b5a-107">Syntax</span></span>

 <span data-ttu-id="37b5a-108">**Try_Parse** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="37b5a-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="37b5a-109">La **Try_Parse** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="37b5a-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="37b5a-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="37b5a-110">**Argument name**</span></span>|<span data-ttu-id="37b5a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="37b5a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="37b5a-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="37b5a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="37b5a-113">Expresión de texto que representa el valor con formato que se debe analizar en el tipo de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="37b5a-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="37b5a-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="37b5a-114">*DataType*</span></span>  <br/> |<span data-ttu-id="37b5a-115">Tipo de datos en el que se va a analizar  *TextExpression*  .</span><span class="sxs-lookup"><span data-stu-id="37b5a-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37b5a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37b5a-116">Remarks</span></span>

<span data-ttu-id="37b5a-117">Use **Try_Parse** solo para convertir de tipos de cadena a fecha/hora y números.</span><span class="sxs-lookup"><span data-stu-id="37b5a-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="37b5a-118">Para las conversiones de tipos generales, siga usando **Convert**.</span><span class="sxs-lookup"><span data-stu-id="37b5a-118">For general type conversions, continue to use **Convert**.</span></span> 
  

