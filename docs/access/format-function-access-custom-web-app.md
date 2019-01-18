---
title: Función Format (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Devuelve un valor con formato según un patrón especificado.
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710394"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="38579-103">Función Format (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="38579-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="38579-104">Devuelve un valor con formato según un patrón especificado.</span><span class="sxs-lookup"><span data-stu-id="38579-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="38579-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="38579-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="38579-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38579-107">Syntax</span></span>

 <span data-ttu-id="38579-108">**Format** (*Expresión*, *Formato*)</span><span class="sxs-lookup"><span data-stu-id="38579-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="38579-109">La función **Format** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="38579-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="38579-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="38579-110">**Argument name**</span></span>|<span data-ttu-id="38579-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38579-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="38579-112">*Expresión*</span><span class="sxs-lookup"><span data-stu-id="38579-112">*Expression*</span></span>  <br/> |<span data-ttu-id="38579-113">Expresión de un tipo de datos admitido para dar formato.</span><span class="sxs-lookup"><span data-stu-id="38579-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="38579-114">*Formato*</span><span class="sxs-lookup"><span data-stu-id="38579-114">*Format*</span></span>  <br/> | <span data-ttu-id="38579-p102">Un patrón de formato. El argumento de formato debe contener una cadena de formato válida, como una cadena de formato estándar (por ejemplo, "C" o "D"), o como un patrón de caracteres personalizados para fechas y valores numéricos (por ejemplo, "MMMM dd, aaaa (dddd)"). Para más información, consulte Comenatrios.</span><span class="sxs-lookup"><span data-stu-id="38579-p102">A format pattern. The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)"). For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38579-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38579-118">Remarks</span></span>

<span data-ttu-id="38579-119">Para el parámetro  *Formato*  , puede pasar las cadenas que coincidan con cualquiera de los siguientes patrones:</span><span class="sxs-lookup"><span data-stu-id="38579-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="38579-120">Cadenas de formato numérico estándar</span><span class="sxs-lookup"><span data-stu-id="38579-120">Standard Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="38579-121">Cadenas de formato numérico personalizado</span><span class="sxs-lookup"><span data-stu-id="38579-121">Custom Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="38579-122">Cadenas de formato de fecha y hora estándar</span><span class="sxs-lookup"><span data-stu-id="38579-122">Standard Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="38579-123">Cadenas de formato de fecha y hora personalizado</span><span class="sxs-lookup"><span data-stu-id="38579-123">Custom Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="38579-124">No puede usar la función **Formato** en las siguientes áreas de las aplicaciones web de Access 2013:</span><span class="sxs-lookup"><span data-stu-id="38579-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="38579-125">Columnas calculadas en el nivel de tabla</span><span class="sxs-lookup"><span data-stu-id="38579-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="38579-126">Macros de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="38579-126">UI macros</span></span>
    
- <span data-ttu-id="38579-127">Expresiones de vistas (por ejemplo, en formularios)</span><span class="sxs-lookup"><span data-stu-id="38579-127">Expressions in views (for example, in forms)</span></span>
    

