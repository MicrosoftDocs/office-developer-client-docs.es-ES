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
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818416"
---
# <a name="naming-folders-by-using-character-strings"></a>Asignar nombres a carpetas usando cadenas de caracteres

  
  
**Hace referencia a**: Outlook 
  
Si tiene acceso a una o varias carpetas con frecuencia durante una sesión, considere la posibilidad de asignar nombres a las carpetas con el método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Aunque **IMsgStore::SetReceiveFolder** se usa principalmente para establecer carpetas especiales para recibir los mensajes entrantes para las clases de mensaje en particular, también se puede usar para asociar cualquier carpeta con un nombre. El nombre puede ser la misma que la clase de mensaje o puede ser cualquier cadena de caracteres, personalizado para el uso de su cliente. Asociar un nombre a una carpeta, reduce el tiempo necesario para buscar y abrir la carpeta. 
  

