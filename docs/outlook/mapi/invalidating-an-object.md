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
# <a name="invalidating-an-object"></a>Invalidar un objeto

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como parte del proceso de cierre del proveedor, es posible que desee invalidar un objeto. Invalidar un objeto implica reemplazar su tabla virtual por una tabla virtual que contiene implementaciones para los tres métodos **IUnknown:** **AddRef**, **Release** y **QueryInterface**. Invalide un objeto llamando a [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), un método que se incluye en el objeto de soporte técnico de cada uno de los tres tipos de proveedor comunes. Normalmente, los proveedores hacen esta llamada en la implementación del método **Logoff** del objeto de inicio de sesión. 
  
La invalidación de un objeto proporciona a MAPI la responsabilidad última de liberar la memoria asociada a un objeto. Puede liberar todos los recursos conectados a un objeto y, a continuación, llamar a **MakeInvalid** para invalidar todos los métodos de sus interfaces heredadas. Las llamadas a cualquiera de estos métodos devolverán MAPI_E_INVALID_OBJECT. Usar **MakeInvalid** es una opción que muchos proveedores de servicios eligen omitir. 
  
## <a name="see-also"></a>Vea también



[Apagar un proveedor de servicios](shutting-down-a-service-provider.md)

