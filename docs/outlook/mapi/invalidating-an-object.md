---
title: Invalidar un objeto
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2346ec8541e1a8b7f5ea198722833447f9f5a289
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566477"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="22f9e-103">Invalidar un objeto</span><span class="sxs-lookup"><span data-stu-id="22f9e-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="22f9e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22f9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22f9e-105">Como parte del proceso de cierre de su proveedor, es posible que desee invalidar un objeto.</span><span class="sxs-lookup"><span data-stu-id="22f9e-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="22f9e-106">Invalidar un objeto implica reemplazar su tabla vtable con una tabla virtual que contiene las implementaciones para los tres métodos de **IUnknown** : **QueryInterface**, **AddRef**y **Release**.</span><span class="sxs-lookup"><span data-stu-id="22f9e-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="22f9e-107">Invalidar un objeto mediante una llamada a [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), un método que se incluye en el objeto de soporte técnico de cada uno de los tres tipos comunes de proveedor.</span><span class="sxs-lookup"><span data-stu-id="22f9e-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="22f9e-108">Normalmente, los proveedores de realizan esta llamada en la implementación del método de **cierre de sesión** del objeto su inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="22f9e-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="22f9e-109">Invalidar un objeto ofrece MAPI la responsabilidad final para liberar la memoria asociada con un objeto.</span><span class="sxs-lookup"><span data-stu-id="22f9e-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="22f9e-110">Puede liberar todos los recursos conectados a un objeto y, a continuación, llame a **MakeInvalid** para invalidar todos los métodos en sus interfaces heredadas.</span><span class="sxs-lookup"><span data-stu-id="22f9e-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="22f9e-111">Las llamadas a cualquiera de estos métodos devolverá MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="22f9e-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="22f9e-112">Uso de **MakeInvalid** es una opción que elija muchos proveedores de servicios para omitir.</span><span class="sxs-lookup"><span data-stu-id="22f9e-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22f9e-113">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="22f9e-113">See also</span></span>



[<span data-ttu-id="22f9e-114">Apagar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="22f9e-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

