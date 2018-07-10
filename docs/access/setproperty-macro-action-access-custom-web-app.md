---
title: Acción de Macro DefinirPropiedad (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Puede usar la acción DefinirPropiedad para establecer una propiedad para un control en una vista.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815483"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="0de0e-103">Acción de Macro DefinirPropiedad (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="0de0e-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="0de0e-104">Puede usar la acción **DefinirPropiedad** para establecer una propiedad para un control en una vista.</span><span class="sxs-lookup"><span data-stu-id="0de0e-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="0de0e-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/es-es/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="0de0e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/es-es/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="0de0e-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="0de0e-107">Setting</span></span>

<span data-ttu-id="0de0e-108">La acción **DefinirPropiedad** tiene los argumentos enumerados en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0de0e-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="0de0e-109">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="0de0e-109">**Action argument**</span></span>|<span data-ttu-id="0de0e-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0de0e-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0de0e-111">_Control Name_</span><span class="sxs-lookup"><span data-stu-id="0de0e-111">_Control Name_</span></span> <br/> |<span data-ttu-id="0de0e-112">Escriba el nombre del campo o control para el cual desee definir el valor de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="0de0e-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="0de0e-113">Deje este argumento en blanco para establecer la propiedad para la vista.</span><span class="sxs-lookup"><span data-stu-id="0de0e-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="0de0e-114">_Property_</span><span class="sxs-lookup"><span data-stu-id="0de0e-114">_Property_</span></span> <br/> |<span data-ttu-id="0de0e-p103">Seleccione la propiedad que desee definir. Vea la sección **Comentarios** de este artículo para ver una lista de las propiedades que se pueden definir mediante esta acción.  </span><span class="sxs-lookup"><span data-stu-id="0de0e-p103">Select the property that you want to set. See the **Remarks** section in this article for a list of the properties that can be set by using this action.  </span></span><br/> |
| <span data-ttu-id="0de0e-117">_Value_</span><span class="sxs-lookup"><span data-stu-id="0de0e-117">_Value_</span></span> <br/> |<span data-ttu-id="0de0e-p104">Escriba el valor en el que desee establecer la propiedad. Para las propiedades cuyos valores son Sí o No, use **-1** para Sí y **0** para No.  </span><span class="sxs-lookup"><span data-stu-id="0de0e-p104">Type the value that the property is to be set to. For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="0de0e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0de0e-120">Remarks</span></span>

<span data-ttu-id="0de0e-121">Puede usar la acción **DefinirPropiedad** para definir las siguientes propiedades de un control:</span><span class="sxs-lookup"><span data-stu-id="0de0e-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="0de0e-122">Caption</span><span class="sxs-lookup"><span data-stu-id="0de0e-122">Caption</span></span>
    
- <span data-ttu-id="0de0e-123">Habilitado</span><span class="sxs-lookup"><span data-stu-id="0de0e-123">Enabled</span></span>
    
- <span data-ttu-id="0de0e-124">ForeColor</span><span class="sxs-lookup"><span data-stu-id="0de0e-124">ForeColor</span></span>
    
- <span data-ttu-id="0de0e-125">Value</span><span class="sxs-lookup"><span data-stu-id="0de0e-125">Value</span></span>
    
- <span data-ttu-id="0de0e-126">Visible</span><span class="sxs-lookup"><span data-stu-id="0de0e-126">Visible</span></span>
    
<span data-ttu-id="0de0e-127">Si especifica un valor no válido para el argumento ** *Valor* **, no se genera ningún error, pero puede que Access cambie el valor de la propiedad según su interpretación del argumento.</span><span class="sxs-lookup"><span data-stu-id="0de0e-127">If you enter an invalid value for the ** *Value* ** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

