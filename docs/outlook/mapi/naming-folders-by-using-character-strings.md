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
ms.openlocfilehash: 93d959bf41b5d18610d77c6b5573895b0e3880d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594589"
---
# <a name="naming-folders-by-using-character-strings"></a>Asignar nombres a carpetas usando cadenas de caracteres

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si tiene acceso a una o varias carpetas con frecuencia durante una sesión, considere la posibilidad de asignar nombres a las carpetas con el método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Aunque **IMsgStore::SetReceiveFolder** se usa principalmente para establecer carpetas especiales para recibir los mensajes entrantes para las clases de mensaje en particular, también se puede usar para asociar cualquier carpeta con un nombre. El nombre puede ser la misma que la clase de mensaje o puede ser cualquier cadena de caracteres, personalizado para el uso de su cliente. Asociar un nombre a una carpeta, reduce el tiempo necesario para buscar y abrir la carpeta. 
  

