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
# <a name="invalidating-an-object"></a>Invalidar un objeto

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como parte del proceso de cierre de su proveedor, es posible que desee invalidar un objeto. Invalidar un objeto implica reemplazar su tabla vtable con una tabla virtual que contiene las implementaciones para los tres métodos de **IUnknown** : **QueryInterface**, **AddRef**y **Release**. Invalidar un objeto mediante una llamada a [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), un método que se incluye en el objeto de soporte técnico de cada uno de los tres tipos comunes de proveedor. Normalmente, los proveedores de realizan esta llamada en la implementación del método de **cierre de sesión** del objeto su inicio de sesión. 
  
Invalidar un objeto ofrece MAPI la responsabilidad final para liberar la memoria asociada con un objeto. Puede liberar todos los recursos conectados a un objeto y, a continuación, llame a **MakeInvalid** para invalidar todos los métodos en sus interfaces heredadas. Las llamadas a cualquiera de estos métodos devolverá MAPI_E_INVALID_OBJECT. Uso de **MakeInvalid** es una opción que elija muchos proveedores de servicios para omitir. 
  
## <a name="see-also"></a>Recursos adicionales



[Apagar un proveedor de servicios](shutting-down-a-service-provider.md)

