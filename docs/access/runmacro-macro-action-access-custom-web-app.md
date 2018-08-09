---
title: Acción de Macro EjecutarMacro (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Puede utilizar la acción EjecutarMacro para ejecutar una macro (UI) de la interfaz de usuario.
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815485"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="d2ba4-103">Acción de Macro EjecutarMacro (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="d2ba4-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="d2ba4-104">Puede utilizar la acción **EjecutarMacro** para ejecutar una macro (UI) de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d2ba4-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d2ba4-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="d2ba4-107">Setting</span></span>

<span data-ttu-id="d2ba4-108">La acción **EjecutarMacro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="d2ba4-109">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="d2ba4-109">**Action argument**</span></span>|<span data-ttu-id="d2ba4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2ba4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2ba4-111">**Nombre de macro**</span><span class="sxs-lookup"><span data-stu-id="d2ba4-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="d2ba4-112">El nombre de la macro de la interfaz de usuario para que se ejecute.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2ba4-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2ba4-113">Remarks</span></span>

<span data-ttu-id="d2ba4-114">Cuando se ejecuta una macro de la interfaz de usuario que contiene la acción **EjecutarMacro** y se llega a la acción **RunMacro (EjecutarMacro)** , Access ejecuta la macro llamada de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="d2ba4-115">Cuando haya terminado la macro llamada de la interfaz de usuario, Access vuelve a la macro de la interfaz de usuario original y ejecuta la siguiente acción.</span><span class="sxs-lookup"><span data-stu-id="d2ba4-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

