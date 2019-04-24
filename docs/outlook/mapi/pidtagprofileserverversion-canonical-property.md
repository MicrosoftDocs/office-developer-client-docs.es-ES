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
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286569"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Propiedad canónica PidTagProfileServerVersion

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica información sobre la versión de Microsoft Exchange Server a la que se conectan las cuentas de un perfil de Microsoft Outlook.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Identificador:  <br/> |0x661B  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuración del perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Un perfil puede especificar una o más cuentas que se conectan a un servidor de Exchange, pero deben estar conectadas al mismo servidor de Exchange.
  
Las versiones de Outlook anteriores a Microsoft Office Outlook 2007 pueden escribir en esta propiedad para almacenar información acerca de la versión de Exchange Server a la que está conectado el perfil activo. Sin embargo, el formato de la información de versión varía para las diferentes versiones de Exchange Server. Por ejemplo, Outlook almacena en **PR_PROFILE_SERVER_VERSION** el valor decimal 6944 para representar solo el número de compilación principal en el identificador de la versión de **6.5.6944.3** para Microsoft Exchange Server 2003. Para una conexión de Exchange 2007, Outlook almacena el número de versión principal y el número de compilación principal en una representación hexadecimal concatenada de estos números en la propiedad. Un identificador de versión de Exchange 2007 de **8.0.685.24** tiene un número de versión 8 principal y un número de compilación superior 685 en decimal. Al convertir ambos números a hexadecimal, se obtiene 0x8 y 0x2AD. Concatenación de estos dos números, Outlook almacena el valor 0x82AD en **PR_PROFILE_SERVER_VERSION** en representación hexadecimal. 
  
Outlook 2007 no lee ni escribe en esta propiedad. Admite **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
Es probable que solo exista un **PR_PROFILE_SERVER_VERSION** o **PR_PROFILE_SERVER_FULL_VERSION** en un perfil, pero no hay ninguna garantía que siempre exista en un perfil. Outlook no escribe en ninguna de las dos propiedades hasta que se haya conectado correctamente al servidor de Exchange. 
  
En el modelo de objetos de Outlook, puede usar la propiedad **ExchangeMailboxServerVersion** del objeto **namespace** para buscar la versión de Exchange Server en la que se hospeda el buzón activo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjuntos de propiedades.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

