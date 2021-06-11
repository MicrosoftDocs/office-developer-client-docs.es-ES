---
title: Acción de macro SetProperty (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Puede usar la acción SetProperty para establecer una propiedad para un control en una vista.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438032"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="7bdc3-103">Acción de macro SetProperty (aplicación web personalizada de Access)</span><span class="sxs-lookup"><span data-stu-id="7bdc3-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="7bdc3-104">Puede usar la acción **SetProperty** para establecer una propiedad para un control en una vista.</span><span class="sxs-lookup"><span data-stu-id="7bdc3-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="7bdc3-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="7bdc3-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="7bdc3-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="7bdc3-107">Setting</span></span>

<span data-ttu-id="7bdc3-108">La **acción SetProperty** tiene los argumentos enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7bdc3-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="7bdc3-109">**Argumento de la acción**</span><span class="sxs-lookup"><span data-stu-id="7bdc3-109">**Action argument**</span></span>|<span data-ttu-id="7bdc3-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7bdc3-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7bdc3-111">_Control Name_</span><span class="sxs-lookup"><span data-stu-id="7bdc3-111">_Control Name_</span></span> <br/> |<span data-ttu-id="7bdc3-112">Escriba el nombre del campo o control para el cual desee definir el valor de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="7bdc3-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="7bdc3-113">Deje este argumento en blanco para establecer la propiedad de la vista.</span><span class="sxs-lookup"><span data-stu-id="7bdc3-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="7bdc3-114">_Property_</span><span class="sxs-lookup"><span data-stu-id="7bdc3-114">_Property_</span></span> <br/> |<span data-ttu-id="7bdc3-p103">Seleccione la propiedad que desee definir. Vea la sección **Comentarios** de este artículo para ver una lista de las propiedades que se pueden definir mediante esta acción.  </span><span class="sxs-lookup"><span data-stu-id="7bdc3-p103">Select the property that you want to set. See the **Remarks** section in this article for a list of the properties that can be set by using this action.  </span></span><br/> |
| <span data-ttu-id="7bdc3-117">_Value_</span><span class="sxs-lookup"><span data-stu-id="7bdc3-117">_Value_</span></span> <br/> |<span data-ttu-id="7bdc3-p104">Escriba el valor en el que desee establecer la propiedad. Para las propiedades cuyos valores son Sí o No, use **-1** para Sí y **0** para No.  </span><span class="sxs-lookup"><span data-stu-id="7bdc3-p104">Type the value that the property is to be set to. For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bdc3-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7bdc3-120">Remarks</span></span>

<span data-ttu-id="7bdc3-121">Puede usar la acción **SetProperty** para establecer las siguientes propiedades de un control:</span><span class="sxs-lookup"><span data-stu-id="7bdc3-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="7bdc3-122">Caption</span><span class="sxs-lookup"><span data-stu-id="7bdc3-122">Caption</span></span>
    
- <span data-ttu-id="7bdc3-123">Habilitado</span><span class="sxs-lookup"><span data-stu-id="7bdc3-123">Enabled</span></span>
    
- <span data-ttu-id="7bdc3-124">ForeColor</span><span class="sxs-lookup"><span data-stu-id="7bdc3-124">ForeColor</span></span>
    
- <span data-ttu-id="7bdc3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7bdc3-125">Value</span></span>
    
- <span data-ttu-id="7bdc3-126">Visible</span><span class="sxs-lookup"><span data-stu-id="7bdc3-126">Visible</span></span>
    
<span data-ttu-id="7bdc3-127">Si especifica un valor no válido para el argumento \*\* *Valor* \*\*, no se genera ningún error, pero puede que Access cambie el valor de la propiedad según su interpretación del argumento.</span><span class="sxs-lookup"><span data-stu-id="7bdc3-127">If you enter an invalid value for the \*\* *Value* \*\* argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

