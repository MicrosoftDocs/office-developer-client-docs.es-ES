---
title: Acción de SetReturnVar Macro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: La acción SetReturnVar crea una variable de retorno y establece en un valor específico.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815512"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="c67e3-103">Acción de SetReturnVar Macro (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="c67e3-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="c67e3-104">La acción **SetReturnVar** crea una variable de retorno y establece en un valor específico.</span><span class="sxs-lookup"><span data-stu-id="c67e3-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c67e3-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="c67e3-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c67e3-107">La acción **SetReturnVar** sólo está disponible en Macros de datos.</span><span class="sxs-lookup"><span data-stu-id="c67e3-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="c67e3-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="c67e3-108">Setting</span></span>

<span data-ttu-id="c67e3-109">La acción **SetReturnVar** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c67e3-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="c67e3-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="c67e3-110">**Argument name**</span></span>|<span data-ttu-id="c67e3-111">**Necesario**</span><span class="sxs-lookup"><span data-stu-id="c67e3-111">**Required**</span></span>|<span data-ttu-id="c67e3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c67e3-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c67e3-113">_Name_</span><span class="sxs-lookup"><span data-stu-id="c67e3-113">_Name_</span></span> <br/> |<span data-ttu-id="c67e3-114">Sí</span><span class="sxs-lookup"><span data-stu-id="c67e3-114">Yes</span></span>  <br/> |<span data-ttu-id="c67e3-115">Una cadena que especifica el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="c67e3-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="c67e3-116">_Expresión_</span><span class="sxs-lookup"><span data-stu-id="c67e3-116">_Expression_</span></span> <br/> |<span data-ttu-id="c67e3-117">Sí</span><span class="sxs-lookup"><span data-stu-id="c67e3-117">Yes</span></span>  <br/> |<span data-ttu-id="c67e3-118">Una expresión que se usará para establecer el valor de esta variable temporal.</span><span class="sxs-lookup"><span data-stu-id="c67e3-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="c67e3-119">Delante de la expresión con el signo igual (=).</span><span class="sxs-lookup"><span data-stu-id="c67e3-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="c67e3-120">Puede hacer clic en el botón **Generar** para usar el **Generador de expresiones** para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="c67e3-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c67e3-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c67e3-121">Remarks</span></span>

<span data-ttu-id="c67e3-122">La acción **SetReturnVar** se usa para crear un **ReturnVar**, que es la variable que se puede utilizar las macros que llaman a una macro de datos mediante el uso de la acción **EjecutarMacroDeDatos** .</span><span class="sxs-lookup"><span data-stu-id="c67e3-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="c67e3-123">Una vez creado un **ReturnVar** por la acción **SetReturnVar** , la macro llamada puede usar en una expresión.</span><span class="sxs-lookup"><span data-stu-id="c67e3-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="c67e3-124">Por ejemplo, si ha creado un **ReturnVar** denominado **UpdateSuccess**, podría usar la variable utilizando la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="c67e3-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="c67e3-125">La acción **SetReturnVar** se puede usar en macros de datos con nombre.</span><span class="sxs-lookup"><span data-stu-id="c67e3-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="c67e3-126">No está disponible en macros de datos que están asociadas a un evento de macro de datos.</span><span class="sxs-lookup"><span data-stu-id="c67e3-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

