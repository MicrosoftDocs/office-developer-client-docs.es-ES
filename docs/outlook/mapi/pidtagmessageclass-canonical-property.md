---
title: Propiedad canónica PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359270"
---
# <a name="pidtagmessageclass-canonical-property"></a>Propiedad canónica PidTagMessageClass

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena de texto que identifica la clase de mensaje definida por el remitente, como IPM. Note. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Identificador:  <br/> |0x001A  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Común  <br/> |
   
## <a name="remarks"></a>Comentarios

La clase de mensaje especifica el tipo de mensaje. Determina el conjunto de propiedades definidas para el mensaje, el tipo de información que transmite el mensaje y cómo controlar el mensaje. 
  
Estas propiedades contienen cadenas concatenadas con puntos. Cada cadena representa un nivel de subclases. Por ejemplo, IPM. Note es una subclase de IPM y una superclase de IPM. Note. Private. 
  
Estas propiedades deben constar de los caracteres ASCII 32 a 127 y no deben terminar con un punto (ASCII 46). Las operaciones de ordenación y comparación deben tratarla como una cadena que no distingue mayúsculas de minúsculas. La longitud máxima posible es de 255 caracteres, pero para permitir que la sala MAPI pueda anexar calificadores se recomienda que la longitud original se mantenga en 128 caracteres. 
  
Cada mensaje es necesario para proporcionar estas propiedades. Normalmente, la aplicación cliente que crea un nuevo mensaje lo establece en cuanto [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) vuelve correctamente. Sin embargo, si no se ha establecido la propiedad cuando el cliente llama a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md), el almacén de mensajes debe establecerlo en IPM. 
  
Los valores definidos por MAPI son los siguientes: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM y IPC están pensados para ser de sólo superclases y un mensaje debe tener al menos un calificador de subclases anexado antes de almacenarlo o enviarlo. Para obtener más información sobre el uso de la clase de mensaje, vea [clases de mensajes](mapi-message-classes.md). Para obtener listas de propiedades obligatorias y opcionales para las clases de mensajes, vea los temas secundarios [sobre las propiedades](message-properties-overview.md)de los mensajes.
  
Una clase de mensaje personalizada puede definir propiedades en un intervalo reservado para su uso con esa clase de mensaje únicamente. Para obtener más información, vea [acerca de](mapi-property-identifier-overview.md)los identificadoRes de propiedad. 
  
Las clases de mensaje controlan la carpeta de recepción en la que se almacena un mensaje entrante. Para obtener más información, vea el método [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Para obtener más información sobre el uso de las clases de mensajes con formularios y servidores de formularios, vea [elegir una clase de mensaje](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para representar los mensajes de correo de voz y de fax.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

