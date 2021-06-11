---
title: Try_Parse (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analiza un valor de texto al tipo de datos especificado en la referencia cultural de la aplicación o devuelve Null si la conversión no es válida.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427531"
---
# <a name="try_parse-function-access-custom-web-app"></a><span data-ttu-id="96a27-103">Try_Parse (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="96a27-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="96a27-104">Analiza un valor de texto al tipo de datos especificado en la referencia cultural de la aplicación o devuelve Null si la conversión no es válida.</span><span class="sxs-lookup"><span data-stu-id="96a27-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="96a27-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="96a27-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="96a27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96a27-107">Syntax</span></span>

 <span data-ttu-id="96a27-108">**Try_Parse** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="96a27-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="96a27-109">La **Try_Parse** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="96a27-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="96a27-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="96a27-110">**Argument name**</span></span>|<span data-ttu-id="96a27-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96a27-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="96a27-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="96a27-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="96a27-113">Expresión de texto que representa el valor con formato para analizar en el tipo de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="96a27-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="96a27-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="96a27-114">*DataType*</span></span>  <br/> |<span data-ttu-id="96a27-115">Tipo de datos en el que se va a analizar  *TextExpression*  .</span><span class="sxs-lookup"><span data-stu-id="96a27-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96a27-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96a27-116">Remarks</span></span>

<span data-ttu-id="96a27-117">Use **Try_Parse** solo para convertir de cadena a fecha/hora y tipos de números.</span><span class="sxs-lookup"><span data-stu-id="96a27-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="96a27-118">Para las conversiones de tipos generales, siga usando **Convert**.</span><span class="sxs-lookup"><span data-stu-id="96a27-118">For general type conversions, continue to use **Convert**.</span></span> 
  

