---
title: Convención de nomenclatura de valores devueltos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423618"
---
# <a name="return-value-naming-convention"></a>Convención de nomenclatura de valores devueltos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
The MAPICODE. El archivo de encabezado H contiene muchos de los valores que un cliente o proveedor de servicios puede devolver de una implementación de método de interfaz o que se pueden ver devueltos desde una llamada.
  
Los códigos para representar las condiciones de advertencia y error siguen una convención de nomenclatura diferente que comienza con el prefijo MAPI, un carácter de subrayado y una W o E para indicar el tipo de código. El resto del código es una cadena de caracteres corta para describir la condición. Cada palabra de la cadena está separada por un carácter de subrayado. Por ejemplo, el valor de error MAPI_E_TOO_COMPLEX indica que la implementación no pudo controlar lo que se solicitaba en la llamada. El valor de MAPI_W_PARTIAL_COMPLETION indica que la llamada se ha hecho correctamente, pero que hubo problemas. Solo una parte de la operación se completó correctamente.
  

