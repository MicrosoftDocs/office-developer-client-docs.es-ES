---
title: Acción de Macro EjecutarMacroDeDatos (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Puede usar la acción EjecutarMacroDeDatos para ejecutar una macro de datos independientes.
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815480"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="9a95f-103">Acción de Macro EjecutarMacroDeDatos (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="9a95f-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="9a95f-104">Puede usar la acción **EjecutarMacroDeDatos** para ejecutar una macro de datos independientes.</span><span class="sxs-lookup"><span data-stu-id="9a95f-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9a95f-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="9a95f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="9a95f-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="9a95f-107">Setting</span></span>

<span data-ttu-id="9a95f-108">La acción **EjecutarMacroDeDatos** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="9a95f-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="9a95f-109">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="9a95f-109">**Action argument**</span></span>|<span data-ttu-id="9a95f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a95f-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9a95f-111">_Nombre de macro_</span><span class="sxs-lookup"><span data-stu-id="9a95f-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="9a95f-112">Nombre de la macro de datos que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="9a95f-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a95f-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a95f-113">Remarks</span></span>

<span data-ttu-id="9a95f-114">Cuando selecciona la macro de datos que desea ejecutar en el Diseñador de macros, Access determina si la macro de datos requiere parámetros.</span><span class="sxs-lookup"><span data-stu-id="9a95f-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="9a95f-115">Si la macro de datos requiere parámetros, se mostrarán cuadros de texto que se puede escribir en los argumentos.</span><span class="sxs-lookup"><span data-stu-id="9a95f-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="9a95f-p103">Cuando se ejecuta una macro que contiene la acción **EjecutarMacroDeDatos** y se llega a la acción **EjecutarMacroDeDatos**, Access ejecuta la macro de datos a la que se ha llamado. Cuando esta macro de datos termina, Access vuelve a la macro original y ejecuta la acción siguiente.</span><span class="sxs-lookup"><span data-stu-id="9a95f-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  
