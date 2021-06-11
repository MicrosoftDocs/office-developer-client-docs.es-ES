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
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407679"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="78d0a-103">Invalidar un objeto</span><span class="sxs-lookup"><span data-stu-id="78d0a-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="78d0a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78d0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78d0a-105">Como parte del proceso de cierre del proveedor, es posible que desee invalidar un objeto.</span><span class="sxs-lookup"><span data-stu-id="78d0a-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="78d0a-106">Invalidar un objeto implica reemplazar su tabla virtual por una tabla virtual que contiene implementaciones para los tres métodos **IUnknown:** **AddRef**, **Release** y **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="78d0a-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="78d0a-107">Invalide un objeto llamando a [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), un método que se incluye en el objeto de soporte técnico de cada uno de los tres tipos de proveedor comunes.</span><span class="sxs-lookup"><span data-stu-id="78d0a-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="78d0a-108">Normalmente, los proveedores hacen esta llamada en la implementación del método **Logoff** del objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="78d0a-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="78d0a-109">La invalidación de un objeto proporciona a MAPI la responsabilidad última de liberar la memoria asociada a un objeto.</span><span class="sxs-lookup"><span data-stu-id="78d0a-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="78d0a-110">Puede liberar todos los recursos conectados a un objeto y, a continuación, llamar a **MakeInvalid** para invalidar todos los métodos de sus interfaces heredadas.</span><span class="sxs-lookup"><span data-stu-id="78d0a-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="78d0a-111">Las llamadas a cualquiera de estos métodos devolverán MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="78d0a-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="78d0a-112">Usar **MakeInvalid** es una opción que muchos proveedores de servicios eligen omitir.</span><span class="sxs-lookup"><span data-stu-id="78d0a-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78d0a-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="78d0a-113">See also</span></span>



[<span data-ttu-id="78d0a-114">Apagar un proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="78d0a-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

