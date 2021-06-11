---
title: Función Stuff (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición de inicio y, a continuación, inserta la segunda cadena en la primera cadena en la posición de inicio.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427678"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="5d584-104">Función Stuff (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="5d584-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="5d584-105">Inserta una cadena de texto en otra cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="5d584-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="5d584-106">Elimina una longitud especificada de caracteres en la primera cadena en la posición de inicio y, a continuación, inserta la segunda cadena en la primera cadena en la posición de inicio.</span><span class="sxs-lookup"><span data-stu-id="5d584-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5d584-p103">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="5d584-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5d584-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d584-109">Syntax</span></span>

 <span data-ttu-id="5d584-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="5d584-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="5d584-111">La **función Stuff** contiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="5d584-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="5d584-112">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="5d584-112">**Argument name**</span></span>|<span data-ttu-id="5d584-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5d584-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5d584-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="5d584-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="5d584-115">Expresión de texto que especifica el texto en el que se insertará el texto especificado por *ThisTextExpression.*</span><span class="sxs-lookup"><span data-stu-id="5d584-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="5d584-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="5d584-116">*Start*</span></span>  <br/> |<span data-ttu-id="5d584-117">Valor entero que especifica la ubicación para iniciar la eliminación y la inserción.</span><span class="sxs-lookup"><span data-stu-id="5d584-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="5d584-118">Si start o length es negativo, se devuelve una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="5d584-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="5d584-119">Si start es más largo que el primer  *Objeto IntoTextExpression*  , se devuelve una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="5d584-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="5d584-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="5d584-120">*Length*</span></span>  <br/> |<span data-ttu-id="5d584-121">Entero que especifica el número de caracteres que se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="5d584-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="5d584-122">Si la longitud es mayor que la primera  *IntoTextExpression*  , la eliminación se produce hasta el último carácter del último  *IntoTextExpression*  .</span><span class="sxs-lookup"><span data-stu-id="5d584-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="5d584-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="5d584-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="5d584-124">Un sombrero de expresión de texto especifica el texto que se insertará en  *IntoTextExpression*  .</span><span class="sxs-lookup"><span data-stu-id="5d584-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="5d584-125">Esta expresión reemplazará los caracteres de longitud de  *IntoTextExpression a*  partir de  *Start*  .</span><span class="sxs-lookup"><span data-stu-id="5d584-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d584-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d584-126">Remarks</span></span>

<span data-ttu-id="5d584-127">Si los  *argumentos Start*  o  *Length*  son negativos, o si la posición inicial es mayor que la longitud de la primera cadena, se devuelve una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="5d584-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="5d584-128">Si la posición de inicio es 0, se devuelve un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="5d584-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="5d584-129">Si la longitud que se va a eliminar es mayor que la primera cadena, se elimina al primer carácter de la primera cadena.</span><span class="sxs-lookup"><span data-stu-id="5d584-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

