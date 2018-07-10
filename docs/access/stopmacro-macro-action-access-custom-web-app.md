---
title: Acción de Macro DetenerMacro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Puede utilizar la acción DetenerMacro para detener la macro que se está ejecutando.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815491"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="7de47-103">Acción de Macro DetenerMacro (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="7de47-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="7de47-104">Puede utilizar la acción **DetenerMacro** para detener la macro que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="7de47-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7de47-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/es-es/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="7de47-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/es-es/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="7de47-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="7de47-107">Setting</span></span>

<span data-ttu-id="7de47-108">La acción **DetenerMacro** no tiene ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="7de47-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7de47-109">Notas</span><span class="sxs-lookup"><span data-stu-id="7de47-109">Remarks</span></span>

<span data-ttu-id="7de47-110">Esta acción se suele utilizar cuando una condición haga necesario detener la macro.</span><span class="sxs-lookup"><span data-stu-id="7de47-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="7de47-111">Por ejemplo, podría crear una macro de usuario (UI) de la interfaz que se abre una vista que muestra los totales de pedidos diarios para la fecha especificada en la vista actual.</span><span class="sxs-lookup"><span data-stu-id="7de47-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="7de47-112">Podría utilizar una expresión condicional para asegurarse de que el control de fecha de pedido en el cuadro de diálogo contiene una fecha válida.</span><span class="sxs-lookup"><span data-stu-id="7de47-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="7de47-113">Si no es así, la acción de **cuadro de mensaje** puede mostrar un mensaje de error y la acción **DetenerMacro** puede detener la macro de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7de47-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

