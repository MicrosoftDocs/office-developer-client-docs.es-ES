---
title: Asignar nombres a carpetas usando cadenas de caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326253"
---
# <a name="naming-folders-by-using-character-strings"></a>Asignar nombres a carpetas usando cadenas de caracteres

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si obtiene acceso a una o más carpetas con frecuencia durante una sesión, considere la posibilidad de asignar nombres a las carpetas con el método [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) . Aunque **IMsgStore:: SetReceiveFolder** se usa principalmente para establecer carpetas especiales para recibir mensajes entrantes para clases de mensajes particulares, también se puede usar para asociar cualquier carpeta con un nombre. El nombre puede ser el mismo que el de la clase de mensaje o puede ser cualquier cadena de caracteres, personalizada para el uso de su cliente. La Asociación de un nombre con una carpeta disminuye el tiempo que se tarda en buscar y abrir la carpeta. 
  

