---
title: Acción de Macro SetVariable (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a4ffbd02-eed7-43ed-9da2-f0d1ff5d8014
description: Puede usar la acción SetVariable para crear una variable temporal y establézcalo en un valor específico. A continuación, se puede usar la variable como una condición o un argumento en las acciones posteriores, o puede usar la variable en otra macro (UI) de la interfaz de usuario.
ms.openlocfilehash: 28daa4e8de247fbe4ca0d7a3fa8a908f6d7d885d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815487"
---
# <a name="setvariable-macro-action-access-custom-web-app"></a><span data-ttu-id="7b3ec-104">Acción de Macro SetVariable (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="7b3ec-104">SetVariable Macro Action (Access custom web app)</span></span>

<span data-ttu-id="7b3ec-105">Puede usar la acción **SetVariable** para crear una variable temporal y establézcalo en un valor específico.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-105">You can use the **SetVariable** action to create a temporary variable and set it to a specific value.</span></span> <span data-ttu-id="7b3ec-106">A continuación, se puede usar la variable como una condición o un argumento en las acciones posteriores, o puede usar la variable en otra macro (UI) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-106">The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7b3ec-p103">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="7b3ec-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="7b3ec-109">Setting</span></span>

<span data-ttu-id="7b3ec-110">La acción **SetVariable** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-110">The **SetVariable** action has the following arguments.</span></span> 
  
|<span data-ttu-id="7b3ec-111">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-111">**Action argument**</span></span>|<span data-ttu-id="7b3ec-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b3ec-113">**Variable**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-113">**Variable**</span></span> <br/> |<span data-ttu-id="7b3ec-114">Especifique el nombre de la variable temporal.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-114">Enter the name of the temporary variable.</span></span>  <br/> |
|<span data-ttu-id="7b3ec-115">**Valor =**</span><span class="sxs-lookup"><span data-stu-id="7b3ec-115">**Value =**</span></span> <br/> |<span data-ttu-id="7b3ec-116">Escriba una expresión que se usará para establecer el valor de esta variable temporal.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-116">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="7b3ec-117">Delante de la expresión con la igual (**=** ) inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-117">Do not precede the expression with the equal (**=** ) sign.</span></span> <span data-ttu-id="7b3ec-118">Puede hacer clic en el botón **Generar** ![fórmula](media/buildbut_ZA06047218.gif "fórmula") para usar el generador de expresiones para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="7b3ec-118">You can click the **Build** button ![Formula](media/buildbut_ZA06047218.gif "Formula") to use the Expression Builder to set this argument.</span></span>  <br/> |
   

