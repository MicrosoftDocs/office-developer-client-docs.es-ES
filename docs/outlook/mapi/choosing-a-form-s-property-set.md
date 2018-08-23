---
title: Selección de conjunto de propiedades de un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0ff8d9f1ae25c55d66847b8c0e5e66c406dfdfba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586154"
---
# <a name="choosing-a-forms-property-set"></a>Selección de conjunto de propiedades de un formulario

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Al implementar el servidor de formulario, debe tener una propiedad para cada parte de la información que necesita su clase de mensaje. Estas propiedades pueden ser propiedades MAPI predefinidas, o pueden ser propiedades personalizadas que se definen. Para obtener más información sobre cómo trabajar con propiedades, vea [Información general sobre la propiedad de MAPI](mapi-property-overview.md).
  
El archivo de configuración de formulario contendrá una lista de propiedades que expone el servidor de formulario para que aplicaciones de cliente para usar, pero esto no tiene que ser toda la lista de propiedades que se usan por el servidor en el formulario. Normalmente, las aplicaciones cliente usan las propiedades expuestas para habilitar a los usuarios ordenar los mensajes en una carpeta o personalizar sus interfaces de alguna manera.
  
MAPI tiene un amplio conjunto de propiedades predefinidas que ser suficiente para la mayoría de las aplicaciones. Sin embargo, habrá veces cuando una clase de mensaje personalizada necesita una propiedad que no definen MAPI. Puede usar las propiedades personalizadas para ampliar el conjunto MAPI predefinido de propiedades para cualquier información especial que el servidor de formulario que se necesita para admitir.
  
Puede usar cualquiera de las maneras siguientes para definir propiedades personalizadas:
  
- Elija un nombre para la propiedad y utilizar el método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener una etiqueta de propiedad. La interfaz de [IMAPIProp](imapipropiunknown.md) a través del cual se invoca este método viene desde el puntero de [IMessage](imessageimapiprop.md) que se pasa al servidor de formulario cuando se crea el mensaje. Tenga en cuenta que el nombre de la propiedad debe ser una cadena de caracteres anchos. 
    
- Definir una etiqueta de propiedad personalizada. Etiquetas de propiedad personalizada deben estar en el intervalo 0x6800 a través de 0x7BFF. Las propiedades de este intervalo son la clase de mensaje específico.
    
Para obtener más información sobre cómo definir propiedades personalizadas, vea [Definir nuevas propiedades de MAPI](defining-new-mapi-properties.md).
  
> [!NOTE]
> Los servidores que tienen un mensaje de texto suelen usar la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para almacenarlo de formulario. Si su servidor de formulario utiliza **PR_RTF_COMPRESSED**, debe también asegurarse de que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contiene una versión de sólo texto del texto del mensaje, en caso de que se lea el mensaje resultante por un cliente que no admite texto Rich Texto del mensaje con formato (RTF). 
  
## <a name="see-also"></a>Recursos adicionales

- [Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

