---
title: Función Concat (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Devuelve una cadena que es el resultado de combinar dos o más valores de cadena.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282295"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="f3976-103">Función Concat (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="f3976-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="f3976-104">Devuelve una cadena que es el resultado de combinar dos o más valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="f3976-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f3976-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="f3976-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f3976-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3976-107">Syntax</span></span>

<span data-ttu-id="f3976-108">**Concat**(*Valor1*, *Valor2*, …[*ValorN*])</span><span class="sxs-lookup"><span data-stu-id="f3976-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="f3976-109">La función **Concat** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f3976-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="f3976-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="f3976-110">**Argument Name**</span></span>|<span data-ttu-id="f3976-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3976-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3976-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f3976-112">Value</span></span>  <br/> |<span data-ttu-id="f3976-113">Un valor de cadena que se concatena a los otros valores.</span><span class="sxs-lookup"><span data-stu-id="f3976-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3976-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3976-114">Remarks</span></span>

<span data-ttu-id="f3976-p102">**Concat** toma un número variable de argumentos de cadena y los concatena en una sola cadena. Se necesitan, como mínimo, dos argumentos de cadena; si no, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f3976-p102">**Concat** takes a variable number of string arguments and concatenates them into a single string. A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="f3976-117">Todos los argumentos se convierten implícitamente en tipos de datos de cadena y luego se concatenan.</span><span class="sxs-lookup"><span data-stu-id="f3976-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="f3976-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3976-118">Example</span></span>

<span data-ttu-id="f3976-119">La siguiente expresión puede usarse para mostrar el nombre completo de una persona en la tabla que contiene los campos Nombre, Segundo nombre y Apellidos.</span><span class="sxs-lookup"><span data-stu-id="f3976-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="f3976-120">Si el campo Segundo nombre está en blanco, los campos Nombre y Apellidos se combinan para mostrar el nombre completo,</span><span class="sxs-lookup"><span data-stu-id="f3976-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


