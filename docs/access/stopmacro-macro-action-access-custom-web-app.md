---
title: DetenerMacro (acción de macro) (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Puede usar la acción DetenerMacro para detener la macro que se está ejecutando actualmente.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429498"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="04158-103">DetenerMacro (acción de macro) (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="04158-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="04158-104">Puede usar la acción **DetenerMacro** para detener la macro que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="04158-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="04158-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="04158-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="04158-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="04158-107">Setting</span></span>

<span data-ttu-id="04158-108">La acción **DetenerMacro** no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="04158-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="04158-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04158-109">Remarks</span></span>

<span data-ttu-id="04158-110">Normalmente, esta acción se usa cuando una condición hace necesario detener la macro.</span><span class="sxs-lookup"><span data-stu-id="04158-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="04158-111">Por ejemplo, puede crear una macro de interfaz de usuario que abra una vista que muestre los totales de los pedidos diarios para la fecha introducida en la vista actual.</span><span class="sxs-lookup"><span data-stu-id="04158-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="04158-112">Puede usar una expresión condicional para asegurarse de que el control de fecha de orden en el cuadro de diálogo contiene una fecha válida.</span><span class="sxs-lookup"><span data-stu-id="04158-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="04158-113">Si no lo hace, la acción **MessageBox** puede mostrar un mensaje de error y la acción **DetenerMacro** puede detener la macro de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="04158-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

