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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396669"
---
# <a name="pidtagmessageclass-canonical-property"></a>Propiedad canónica PidTagMessageClass

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una cadena de texto que identifica la clase de mensaje definido por el remitente, como IPM. Tenga en cuenta. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Identificador:  <br/> |0x001A  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>Comentarios

La clase de mensaje especifica el tipo del mensaje. Determina el conjunto de propiedades definidas para el mensaje, el tipo de información del mensaje se transmite y cómo controlar el mensaje. 
  
Estas propiedades contienen las cadenas que se concatena con períodos. Cada cadena representa un nivel de creación de subclases. Por ejemplo, IPM. Nota es una subclase de IPM y una superclase de IPM. Note.Private. 
  
Estas propiedades deben constar de los caracteres ASCII 32 a 127 y no deben terminar con un punto (ASCII 46). Las operaciones de ordenación y comparación deben tratar como una cadena entre mayúsculas y minúsculas. La longitud máxima permitida es de 255 caracteres, pero con el fin de permitir la sala MAPI anexar calificadores se recomienda que la longitud original mantenerse por debajo de 128 caracteres. 
  
Cada mensaje es necesario para proporcionar estas propiedades. Normalmente, la aplicación cliente de creación de un nuevo mensaje establece tan pronto como [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) devuelve correctamente. Pero si no se ha establecido la propiedad cuando el cliente llama a [IMAPIProp::SaveChanges](imapiprop-savechanges.md), el almacén de mensajes debe establecer para IPM. 
  
Los valores definidos por MAPI son: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM y IPC están diseñados para ser solo superclase, y un mensaje debe tener al menos un calificador de subclase anexado antes de que se almacenan o enviado. Para obtener más información sobre el uso de la clase de mensaje, vea [Las clases de mensajes](mapi-message-classes.md). Para las listas de propiedades opcionales y obligatorios para las clases de mensajes, vea los temas secundarios de [Acerca de propiedades del mensaje](message-properties-overview.md).
  
Una clase de mensaje personalizada puede definir propiedades en un intervalo reservado para su uso con sólo esa clase de mensaje. Para obtener más información, vea [Acerca de identificadores de propiedad](mapi-property-identifier-overview.md). 
  
Control de clases de mensaje que recibe un mensaje entrante de la carpeta se almacena en. Para obtener más información, vea el método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Para obtener más información sobre el uso de las clases de mensajes con servidores de formulario y formularios, vea [Elegir una clase de mensaje](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para que representa los mensajes de fax y correo de voz.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

