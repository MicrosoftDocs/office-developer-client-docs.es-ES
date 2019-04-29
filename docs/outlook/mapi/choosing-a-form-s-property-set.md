---
title: Elegir el conjunto de propiedades de un formulario
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407196"
---
# <a name="choosing-a-forms-property-set"></a>Elegir el conjunto de propiedades de un formulario

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando implemente el servidor de formularios, necesitará tener una propiedad para cada información que necesite su clase de mensaje. Estas propiedades pueden ser propiedades MAPI predefinidas o pueden ser propiedades personalizadas definidas por el usuario. Para obtener más información sobre cómo trabajar con propiedades, consulte [Introducción a la propiedad MAPI](mapi-property-overview.md).
  
El archivo de configuración del formulario contendrá una lista de propiedades que el servidor de formularios expone para que lo usen las aplicaciones cliente, pero no es necesario que sea la lista completa de propiedades usadas por el servidor de formularios. Las aplicaciones cliente suelen usar las propiedades expuestas para permitir a los usuarios ordenar los mensajes de una carpeta o personalizar sus interfaces de alguna manera.
  
MAPI tiene un gran conjunto de propiedades predefinidas que son suficientes para la mayoría de las aplicaciones. Sin embargo, habrá veces en las que una clase de mensaje personalizada necesite una propiedad que MAPI no defina. Puede usar propiedades personalizadas para ampliar el conjunto de propiedades MAPI predefinido para cualquier información especial que el servidor de formularios necesite admitir.
  
Puede usar cualquiera de las formas siguientes para definir propiedades personalizadas:
  
- Elija un nombre para la propiedad y use el método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener una etiqueta de propiedad. La interfaz [IMAPIProp](imapipropiunknown.md) a través de la cual se llama a este método procede del puntero [IMessage](imessageimapiprop.md) que se pasa al servidor de formularios cuando se crea el mensaje. Tenga en cuenta que el nombre de la propiedad debe ser una cadena de caracteres anchos. 
    
- Definir una etiqueta de propiedad personalizada personalmente. Las etiquetas de propiedades personalizadas deben estar en el intervalo de 0x6800 a 0x7BFF. Las propiedades de este intervalo son específicas de la clase de mensaje.
    
Para obtener más información acerca de la definición de propiedades personalizadas, consulte [Defining New MAPI Properties](defining-new-mapi-properties.md).
  
> [!NOTE]
> Los servidores de formularios que tienen un texto de mensaje suelen usar la propiedad **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para almacenarla. Si el servidor de formularios usa **PR_RTF_COMPRESSED**, también debe asegurarse de que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contiene una versión de solo texto del texto del mensaje, en caso de que el mensaje resultante sea leído por un cliente que no admite texto enriquecido Formato (RTF) texto del mensaje. 
  
## <a name="see-also"></a>Ver también

- [Desarrollar servidores de formulario MAPI](developing-mapi-form-servers.md)

