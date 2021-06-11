---
title: Acción De macro SetReturnVar (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: La acción SetReturnVar crea una variable de devolución y la establece en un valor específico.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409597"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="ab6be-103">Acción De macro SetReturnVar (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="ab6be-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="ab6be-104">La **acción SetReturnVar** crea una variable de devolución y la establece en un valor específico.</span><span class="sxs-lookup"><span data-stu-id="ab6be-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ab6be-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="ab6be-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab6be-107">La **acción SetReturnVar** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="ab6be-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ab6be-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="ab6be-108">Setting</span></span>

<span data-ttu-id="ab6be-109">La **acción SetReturnVar** tiene los argumentos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ab6be-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="ab6be-110">**Nombre de argumento**</span><span class="sxs-lookup"><span data-stu-id="ab6be-110">**Argument name**</span></span>|<span data-ttu-id="ab6be-111">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ab6be-111">**Required**</span></span>|<span data-ttu-id="ab6be-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab6be-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ab6be-113">_Name_</span><span class="sxs-lookup"><span data-stu-id="ab6be-113">_Name_</span></span> <br/> |<span data-ttu-id="ab6be-114">Sí</span><span class="sxs-lookup"><span data-stu-id="ab6be-114">Yes</span></span>  <br/> |<span data-ttu-id="ab6be-115">Una cadena que especifica el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="ab6be-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="ab6be-116">_Expression_</span><span class="sxs-lookup"><span data-stu-id="ab6be-116">_Expression_</span></span> <br/> |<span data-ttu-id="ab6be-117">Sí</span><span class="sxs-lookup"><span data-stu-id="ab6be-117">Yes</span></span>  <br/> |<span data-ttu-id="ab6be-118">Una expresión que se utilizará para establecer el valor de esta variable temporal.</span><span class="sxs-lookup"><span data-stu-id="ab6be-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="ab6be-119">No anteponga el signo igual (=) a la expresión.</span><span class="sxs-lookup"><span data-stu-id="ab6be-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="ab6be-120">Puede hacer clic en el botón **Generar** para utilizar el **Generador de expresiones** para establecer este argumento.</span><span class="sxs-lookup"><span data-stu-id="ab6be-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab6be-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab6be-121">Remarks</span></span>

<span data-ttu-id="ab6be-122">La **acción SetReturnVar** se usa para crear **un objeto ReturnVar**, que es una variable que pueden usar las macros que llaman a una macro de datos mediante la acción **RunDataMacro.**</span><span class="sxs-lookup"><span data-stu-id="ab6be-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="ab6be-123">Después de que la acción **SetReturnVar** cree un **ReturnVar,** la macro de llamada puede usarla en una expresión.</span><span class="sxs-lookup"><span data-stu-id="ab6be-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="ab6be-124">Por ejemplo, si creó un **ReturnVar** denominado **UpdateSuccess**, podría usar la variable mediante la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="ab6be-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="ab6be-125">La **acción SetReturnVar** solo se puede usar en macros de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="ab6be-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="ab6be-126">No está disponible en macros de datos adjuntas a un evento de macro de datos.</span><span class="sxs-lookup"><span data-stu-id="ab6be-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

