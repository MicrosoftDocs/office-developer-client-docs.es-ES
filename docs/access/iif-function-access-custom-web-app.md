---
title: Función IIf (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Comprueba si se cumple una condición y devuelve un valor si TRUE de otro en if es FALSE.
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815310"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="b872b-103">Función IIf (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="b872b-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="b872b-104">Comprueba si se cumple una condición y devuelve un valor si TRUE de otro en if es FALSE.</span><span class="sxs-lookup"><span data-stu-id="b872b-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b872b-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="b872b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b872b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b872b-107">Syntax</span></span>

<span data-ttu-id="b872b-108">**IIf** (*Condición*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="b872b-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="b872b-109">La función **IIf** contiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b872b-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="b872b-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="b872b-110">**Argument name**</span></span>|<span data-ttu-id="b872b-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b872b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b872b-112">*Condición*</span><span class="sxs-lookup"><span data-stu-id="b872b-112">*Condition*</span></span>  <br/> |<span data-ttu-id="b872b-113">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="b872b-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="b872b-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="b872b-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="b872b-115">Valor o expresión devuelta si *condición* es True.</span><span class="sxs-lookup"><span data-stu-id="b872b-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="b872b-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="b872b-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="b872b-117">Valor o expresión devuelta si la *condición* es False.</span><span class="sxs-lookup"><span data-stu-id="b872b-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="b872b-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b872b-118">Example</span></span>

<span data-ttu-id="b872b-119">La siguiente expresión puede usarse para mostrar el nombre completo de una persona en la tabla que contiene los campos Nombre, Segundo nombre y Apellidos.</span><span class="sxs-lookup"><span data-stu-id="b872b-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="b872b-120">Si el campo Segundo nombre está en blanco, los campos Nombre y Apellidos se combinan para mostrar el nombre completo,</span><span class="sxs-lookup"><span data-stu-id="b872b-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


