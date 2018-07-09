---
title: Función de material (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Inserta una cadena de texto en otra cadena de texto. Elimina una longitud especificada de caracteres en la primera cadena en la posición de inicio y, a continuación, inserta la segunda cadena en la primera cadena en la posición de inicio.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815494"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="df0e9-104">Función de material (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="df0e9-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="df0e9-105">Inserta una cadena de texto en otra cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="df0e9-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="df0e9-106">Elimina una longitud especificada de caracteres en la primera cadena en la posición de inicio y, a continuación, inserta la segunda cadena en la primera cadena en la posición de inicio.</span><span class="sxs-lookup"><span data-stu-id="df0e9-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="df0e9-p103">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="df0e9-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="df0e9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="df0e9-109">Syntax</span></span>

 <span data-ttu-id="df0e9-110">**Cosas** (*IntoTextExpression*, *Inicio*, *longitud*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="df0e9-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="df0e9-111">La función **cosas** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="df0e9-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="df0e9-112">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="df0e9-112">**Argument name**</span></span>|<span data-ttu-id="df0e9-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df0e9-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="df0e9-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="df0e9-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="df0e9-115">Una expresión de texto que especifica el texto en el que se va a insertar el texto especificado por el *ThisTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="df0e9-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="df0e9-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="df0e9-116">*Start*</span></span>  <br/> |<span data-ttu-id="df0e9-117">Un valor entero que especifica la ubicación para iniciar la inserción y eliminación.</span><span class="sxs-lookup"><span data-stu-id="df0e9-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="df0e9-118">Si start o length es negativo, se devuelve una cadena null.</span><span class="sxs-lookup"><span data-stu-id="df0e9-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="df0e9-119">Si start es mayor que el primer *IntoTextExpression* , se devuelve una cadena null.</span><span class="sxs-lookup"><span data-stu-id="df0e9-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="df0e9-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="df0e9-120">*Length*</span></span>  <br/> |<span data-ttu-id="df0e9-121">Un entero que especifica el número de caracteres que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="df0e9-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="df0e9-122">Si length es mayor que el primer *IntoTextExpression* , se produce la eliminación hasta el último carácter de la última *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="df0e9-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="df0e9-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="df0e9-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="df0e9-124">Un acento circunflejo expresión de texto especifica el texto para insertar en *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="df0e9-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="df0e9-125">Esta expresión reemplazará los caracteres de longitud de *Inicio* a partir de *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="df0e9-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df0e9-126">Notas</span><span class="sxs-lookup"><span data-stu-id="df0e9-126">Remarks</span></span>

<span data-ttu-id="df0e9-127">Si los argumentos *Iniciar* o *Length* son negativos, o si la posición inicial es mayor que la longitud de la primera cadena, se devuelve una cadena nula.</span><span class="sxs-lookup"><span data-stu-id="df0e9-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="df0e9-128">Si la posición inicial es 0, se devuelve un valor nulo.</span><span class="sxs-lookup"><span data-stu-id="df0e9-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="df0e9-129">Si la longitud para eliminar es mayor que la primera cadena, se elimina hasta el primer carácter de la primera cadena.</span><span class="sxs-lookup"><span data-stu-id="df0e9-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

