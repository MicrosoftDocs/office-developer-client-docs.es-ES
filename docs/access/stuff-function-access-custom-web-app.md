---
title: Función cosas (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición inicial y, a continuación, inserta la segunda cadena en la primera cadena en la posición inicial.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311028"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="203d3-104">Función cosas (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="203d3-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="203d3-105">Inserta una cadena de texto en otra cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="203d3-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="203d3-106">Elimina una longitud especificada de caracteres en la primera cadena en la posición inicial y, a continuación, inserta la segunda cadena en la primera cadena en la posición inicial.</span><span class="sxs-lookup"><span data-stu-id="203d3-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="203d3-p103">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="203d3-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="203d3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="203d3-109">Syntax</span></span>

 <span data-ttu-id="203d3-110">**Cosas** (*IntoTextExpression*, *Start*, *length*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="203d3-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="203d3-111">La función **cosas** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="203d3-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="203d3-112">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="203d3-112">**Argument name**</span></span>|<span data-ttu-id="203d3-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="203d3-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="203d3-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="203d3-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="203d3-115">Una expresión de texto que especifica el texto en el que se insertará el texto especificado por *ThisTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="203d3-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="203d3-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="203d3-116">*Start*</span></span>  <br/> |<span data-ttu-id="203d3-117">Valor entero que especifica la ubicación en la que se iniciará la eliminación y la inserción.</span><span class="sxs-lookup"><span data-stu-id="203d3-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="203d3-118">Si Start o length es negativo, se devuelve una cadena null.</span><span class="sxs-lookup"><span data-stu-id="203d3-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="203d3-119">Si Start es superior a la primera *IntoTextExpression* , se devuelve una cadena null.</span><span class="sxs-lookup"><span data-stu-id="203d3-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="203d3-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="203d3-120">*Length*</span></span>  <br/> |<span data-ttu-id="203d3-121">Un entero que especifica el número de caracteres que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="203d3-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="203d3-122">Si length es superior a la primera *IntoTextExpression* , la eliminación se produce hasta el último carácter del último *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="203d3-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="203d3-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="203d3-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="203d3-124">Una expresión de texto Hat especifica el texto que se va a insertar en *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="203d3-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="203d3-125">Esta expresión reemplazará los caracteres de longitud de *IntoTextExpression* comenzando en *Start* .</span><span class="sxs-lookup"><span data-stu-id="203d3-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="203d3-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="203d3-126">Remarks</span></span>

<span data-ttu-id="203d3-127">Si los argumentos *Start* o *length* son negativos, o si la posición inicial es mayor que la longitud de la primera cadena, se devuelve una cadena null.</span><span class="sxs-lookup"><span data-stu-id="203d3-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="203d3-128">Si la posición inicial es 0, se devuelve un valor null.</span><span class="sxs-lookup"><span data-stu-id="203d3-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="203d3-129">Si la longitud que se va a eliminar es superior a la primera cadena, se elimina al primer carácter de la primera cadena.</span><span class="sxs-lookup"><span data-stu-id="203d3-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

