---
title: Acción de macro RunMacro (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Puede usar la acción EjecutarMacro para ejecutar una macro de interfaz de usuario (UI).
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438445"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="0b498-103">Acción de macro RunMacro (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="0b498-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="0b498-104">Puede usar la acción **EjecutarMacro** para ejecutar una macro de interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="0b498-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="0b498-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="0b498-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="0b498-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="0b498-107">Setting</span></span>

<span data-ttu-id="0b498-108">La acción **EjecutarMacro** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="0b498-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="0b498-109">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="0b498-109">**Action argument**</span></span>|<span data-ttu-id="0b498-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b498-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b498-111">**Nombre de macro**</span><span class="sxs-lookup"><span data-stu-id="0b498-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="0b498-112">Nombre de la macro de interfaz de usuario que se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="0b498-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b498-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b498-113">Remarks</span></span>

<span data-ttu-id="0b498-114">Cuando ejecutas una macro de interfaz de usuario que contiene la acción **RunMacro** y llega a la acción **RunMacro,** Access ejecuta la llamada macro de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0b498-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="0b498-115">Cuando la macro de interfaz de usuario llamada ha finalizado, Access vuelve a la macro de interfaz de usuario original y ejecuta la siguiente acción.</span><span class="sxs-lookup"><span data-stu-id="0b498-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

