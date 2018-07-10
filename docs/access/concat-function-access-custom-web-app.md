---
title: Función concat (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Devuelve una cadena que es el resultado de combinar dos o más valores de cadena.
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815302"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="af6e1-103">Función concat (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="af6e1-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="af6e1-104">Devuelve una cadena que es el resultado de combinar dos o más valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="af6e1-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="af6e1-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/es-es/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="af6e1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/es-es/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="af6e1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="af6e1-107">Syntax</span></span>

<span data-ttu-id="af6e1-108">**Concat** (*Valor1*, *valor2*... [*ValorN*])</span><span class="sxs-lookup"><span data-stu-id="af6e1-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="af6e1-109">La función **Concat** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="af6e1-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="af6e1-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="af6e1-110">**Argument Name**</span></span>|<span data-ttu-id="af6e1-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="af6e1-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af6e1-112">Value</span><span class="sxs-lookup"><span data-stu-id="af6e1-112">Value</span></span>  <br/> |<span data-ttu-id="af6e1-113">Un valor de cadena que se concatena a los otros valores.</span><span class="sxs-lookup"><span data-stu-id="af6e1-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af6e1-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="af6e1-114">Remarks</span></span>

<span data-ttu-id="af6e1-p102">**Concat** toma un número variable de argumentos de cadena y los concatena en una sola cadena. Se necesitan, como mínimo, dos argumentos de cadena; si no, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="af6e1-p102">**Concat** takes a variable number of string arguments and concatenates them into a single string. A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="af6e1-117">Todos los argumentos se convierten implícitamente en tipos de datos de cadena y luego se concatenan.</span><span class="sxs-lookup"><span data-stu-id="af6e1-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="af6e1-118">Example</span><span class="sxs-lookup"><span data-stu-id="af6e1-118">Example</span></span>

<span data-ttu-id="af6e1-119">La siguiente expresión puede usarse para mostrar el nombre completo de una persona cuando la tabla contiene los campos Nombre, Inicial intermedia y Apellidos.</span><span class="sxs-lookup"><span data-stu-id="af6e1-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="af6e1-120">Si el campo MiddleInitial está en blanco, se combinan los campos FirstName y LastName (apellidos) para mostrar el nombre completo.</span><span class="sxs-lookup"><span data-stu-id="af6e1-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


