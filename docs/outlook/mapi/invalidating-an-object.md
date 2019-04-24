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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317202"
---
# <a name="invalidating-an-object"></a>Invalidar un objeto

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como parte del proceso de cierre de su proveedor, es posible que desee invalidar un objeto. Invalidar un objeto implica reemplazar su vtable por una vtable que contiene implementaciones para los tres métodos **IUnknown** : **AddRef**, **Release**y **QueryInterface**. Invalide un objeto llamando a [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md), un método que se incluye en el objeto support de cada uno de los tres tipos de proveedor comunes. Normalmente, los proveedores realizan esta llamada en la implementación del método **Logoff** del objeto de inicio de sesión. 
  
Invalidar un objeto da a MAPI la máxima responsabilidad para liberar la memoria asociada a un objeto. Puede liberar todos los recursos conectados a un objeto y, a continuación, llamar a **MakeInvalid** para invalidar todos los métodos en sus interfaces heredadas. Las llamadas a cualquiera de estos métodos devolverán MAPI_E_INVALID_OBJECT. El uso de **MakeInvalid** es una opción que muchos proveedores de servicios eligen omitir. 
  
## <a name="see-also"></a>Vea también



[Cerrar un proveedor de servicios](shutting-down-a-service-provider.md)

