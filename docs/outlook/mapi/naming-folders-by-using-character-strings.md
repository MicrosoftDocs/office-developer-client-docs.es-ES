---
title: Asignar nombres a carpetas mediante cadenas de caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428315"
---
# <a name="naming-folders-by-using-character-strings"></a>Asignar nombres a carpetas mediante cadenas de caracteres

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si tiene acceso a una o varias carpetas con frecuencia durante una sesión, considere la posibilidad de asignar nombres a las carpetas con el método [IMsgStore::SetReceiveFolder.](imsgstore-setreceivefolder.md) Aunque **IMsgStore::SetReceiveFolder** se usa principalmente para establecer carpetas especiales para recibir mensajes entrantes para determinadas clases de mensaje, también se puede usar para asociar cualquier carpeta con un nombre. El nombre puede ser el mismo que la clase de mensaje o puede ser cualquier cadena de caracteres, personalizada para el uso del cliente. La asociación de un nombre con una carpeta reduce el tiempo que se tarda en buscar y abrir la carpeta. 
  

