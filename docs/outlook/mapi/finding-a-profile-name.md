---
title: Buscar un nombre de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a32c73f8a907b371c4d0f1c07050d44fd45801ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576291"
---
# <a name="finding-a-profile-name"></a>Buscar un nombre de perfil

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
A veces, los clientes necesitan buscar el nombre del perfil se utiliza actualmente para la sesión, el nombre del perfil predeterminado o el nombre de un perfil alternativo instalado en el equipo.
  
Hay varias formas de recuperar el nombre de un perfil durante el transcurso de una sesión. Si necesita buscar el nombre de un perfil que no es necesariamente la que se utiliza para la sesión, use el primer procedimiento. Si necesita buscar el nombre del perfil predeterminado, use el segundo procedimiento. Si necesita encontrar el nombre del perfil actual de la sesión, use el último procedimiento. 
  
 **Para buscar el nombre de cualquier perfil**
  
1. Llame a [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** . 
    
2. Llame a [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfil. 
    
3. Llamar al método [IMAPITable:: QueryRows](imapitable-queryrows.md) de la tabla de perfil para recuperar todas las filas en la tabla y examinar cada uno de ellos para determinar si representa el perfil de destino. 
    
 **Para buscar el nombre del perfil predeterminado**
  
1. Llame a [MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Llame a [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfil. 
    
3. Crear una restricción de propiedad con una estructura de [SPropertyRestriction](spropertyrestriction.md) para que coincida con **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) con el valor TRUE.
    
4. Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para localizar la fila en la tabla de perfil que representa el perfil predeterminado. La columna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contiene el nombre del perfil predeterminado.
    
 **Para buscar el nombre del perfil actual**
  
Para buscar el nombre del perfil actual, siga uno de los siguientes pasos:
  
- Suponiendo que tiene la estructura [MAPIUID](mapiuid.md) que representa una de las secciones del perfil actual, páselo en el parámetro _lpUID_ a [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Recuperar la propiedad de **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) de la sección de perfil mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) . 
    
- Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acceder a la tabla de estado y busque la fila que tiene su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) que se establece en MAPI_SUBSYSTEM. La columna **PR_DISPLAY_NAME** para esta fila es el nombre del perfil. No use la tabla de estado durante el inicio debido a que se bloquea una aplicación hasta que la cola MAPI ha terminado de inicializar todos los proveedores de transporte. Esto puede afectar negativamente al rendimiento de su. 
    

