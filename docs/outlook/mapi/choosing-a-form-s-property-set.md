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
  
Al implementar el servidor de formularios, debe tener una propiedad para cada información que necesite la clase de mensaje. Estas propiedades pueden ser propiedades MAPI predefinidas o pueden ser propiedades personalizadas que defina. Para obtener más información acerca de cómo trabajar con propiedades, vea [Información general sobre la propiedad MAPI](mapi-property-overview.md).
  
El archivo de configuración del formulario contendrá una lista de propiedades que el servidor de formularios expone para que las aplicaciones cliente las usen, pero no tiene que ser la lista completa de propiedades usadas por el servidor de formularios. Las aplicaciones cliente suelen usar las propiedades expuestas para permitir a los usuarios ordenar mensajes en una carpeta o personalizar sus interfaces de alguna manera.
  
MAPI tiene un gran conjunto de propiedades predefinidas que son suficientes para la mayoría de las aplicaciones. Sin embargo, habrá ocasiones en las que una clase de mensaje personalizada necesite una propiedad que MAPI no define. Puede usar propiedades personalizadas para ampliar el conjunto predefinido mapi de propiedades para cualquier información especial que el servidor de formulario necesite admitir.
  
Puede usar cualquiera de las siguientes maneras de definir propiedades personalizadas:
  
- Elija un nombre para la propiedad y use el [método IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener una etiqueta de propiedad para ella. La [interfaz IMAPIProp a](imapipropiunknown.md) través de la cual se llama a este método proviene del puntero [IMessage](imessageimapiprop.md) que se pasa al servidor de formularios cuando se crea el mensaje. Tenga en cuenta que el nombre de la propiedad debe ser una cadena de caracteres anchos. 
    
- Defina usted mismo una etiqueta de propiedad personalizada. Las etiquetas de propiedad personalizadas deben estar en el intervalo 0x6800 a 0x7BFF. Las propiedades de este intervalo son específicas de la clase de mensaje.
    
Para obtener más información acerca de la definición de propiedades personalizadas, vea [Definir nuevas propiedades MAPI](defining-new-mapi-properties.md).
  
> [!NOTE]
> Los servidores de formulario que tienen un texto de mensaje a menudo **usan la PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para almacenarlo. Si el servidor de formulario usa **PR_RTF_COMPRESSED,** también debe asegurarse de que la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contiene una versión de solo texto del texto del mensaje, en caso de que el mensaje resultante sea leído por un cliente que no admite texto de mensaje de formato de texto enriquecido (RTF). 
  
## <a name="see-also"></a>Consulte también

- [Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md)

