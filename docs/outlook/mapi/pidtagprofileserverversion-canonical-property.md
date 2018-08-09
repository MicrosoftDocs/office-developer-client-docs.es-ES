---
title: Propiedad canónica PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 571ac25d6bc738f8289e3019c342820682d08c28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819947"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Propiedad canónica PidTagProfileServerVersion

  
  
**Hace referencia a**: Outlook 
  
Especifica información acerca de la versión de Microsoft Exchange Server a la que están conectadas cuentas en un perfil de Microsoft Outlook.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Identificador:  <br/> |0x661B  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuración de perfiles de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Un perfil puede especificar una o más cuentas que se conectan a un servidor de Exchange, pero deben estar conectados al mismo servidor de Exchange.
  
Versiones de Outlook anteriores a Microsoft Office Outlook 2007 pueden escribir en esta propiedad para almacenar información acerca de la versión de Exchange Server al que está conectado el perfil activo. Sin embargo, el formato de la información de versión varía en función de las diferentes versiones de Exchange Server. Por ejemplo, almacenes de Outlook en **PR_PROFILE_SERVER_VERSION** el valor decimal 6944 para representar a sólo los principales número de compilación en el identificador de versión de **6.5.6944.3** para Microsoft Exchange Server 2003. Para una conexión de Exchange 2007, Outlook almacena el número de versión principal y el mayor número de compilación en una representación hexadecimal concatenada de estos números en la propiedad. Un identificador de versión de Exchange 2007 de **8.0.685.24** tiene un número de versión principal 8 y un número de versión de compilación principal 685 en decimal. Conversión de ambos números en hexadecimal, obtendrá 0 x 8 y 0x2AD. Concatenación de estos dos números, Outlook almacena el valor 0x82AD en **PR_PROFILE_SERVER_VERSION** en representación hexadecimal. 
  
Outlook 2007 no leer o escribir en esta propiedad. Admite **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
Solo uno de **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** es probable que existan en un perfil, pero no hay ninguna garantía de que siempre existe alguna en un perfil. Outlook no se escribe en cualquiera de las propiedades hasta que se haya conectado correctamente al servidor de Exchange. 
  
En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **NameSpace** para buscar la versión de Exchange Server en el que se hospeda el buzón activo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

