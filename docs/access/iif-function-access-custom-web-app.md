---
title: Función IIf (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Comprueba si se cumple una condición y devuelve un valor si es verdadero de otra si es falso.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301865"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="9d703-103">Función IIf (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="9d703-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="9d703-104">Comprueba si se cumple una condición y devuelve un valor si es verdadero de otra si es falso.</span><span class="sxs-lookup"><span data-stu-id="9d703-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9d703-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="9d703-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9d703-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d703-107">Syntax</span></span>

<span data-ttu-id="9d703-108">**IIf** (*Condición*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="9d703-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="9d703-109">La función **IIf** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="9d703-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="9d703-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="9d703-110">**Argument name**</span></span>|<span data-ttu-id="9d703-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d703-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9d703-112">*Condition*</span><span class="sxs-lookup"><span data-stu-id="9d703-112">*Condition*</span></span>  <br/> |<span data-ttu-id="9d703-113">Expresión que se desea evaluar.</span><span class="sxs-lookup"><span data-stu-id="9d703-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="9d703-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="9d703-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="9d703-115">Valor o expresión devuelta si *Condition* es true.</span><span class="sxs-lookup"><span data-stu-id="9d703-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="9d703-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="9d703-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="9d703-117">Valor o expresión devuelta si *condición* es false.</span><span class="sxs-lookup"><span data-stu-id="9d703-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="9d703-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d703-118">Example</span></span>

<span data-ttu-id="9d703-119">La siguiente expresión puede usarse para mostrar el nombre completo de una persona en la tabla que contiene los campos Nombre, Segundo nombre y Apellidos.</span><span class="sxs-lookup"><span data-stu-id="9d703-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="9d703-120">Si el campo Segundo nombre está en blanco, los campos Nombre y Apellidos se combinan para mostrar el nombre completo,</span><span class="sxs-lookup"><span data-stu-id="9d703-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


